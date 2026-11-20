# Gestione di rilasci e deployment

**La gestione di rilasci e deployment porta le modifiche in produzione in sicurezza, e l'obiettivo in un contesto agile è rendere il rilascio così routinario, automatizzato e reversibile da smettere di essere un evento.**

## Perché è importante

Molte organizzazioni trattano ancora un rilascio come una grande occasione tesa. Si fissa una data, si prenota una finestra, le persone restano fino a tardi e il successo si misura da se qualcosa si è rotto. Questo schema produce proprio il rischio che teme: quante più modifiche sono accorpate in un rilascio, tanto più è difficile capire che cosa è andato storto e tanto più doloroso è un rollback.

Il programma di ricerca DORA descrive l'alternativa. La sua pagina sulla consegna continua definisce la pratica come "the ability to release changes of all kinds on demand quickly, safely, and sustainably" e riferisce che farla bene migliora le prestazioni di consegna e la disponibilità ed è associato a minore burnout e maggiore soddisfazione lavorativa. La pagina avverte anche che installare più spesso senza cambiare processi e architettura tende ad aumentare i tassi di fallimento e a logorare i team. La lezione non è "rilascia più in fretta" ma "costruisci la capacità di rilasciare in sicurezza, poi rilascia spesso".

Il libro *Site Reliability Engineering* di Google, nel capitolo sulla release engineering, fa un'osservazione simile dalla pratica: rilasci frequenti significano meno modifiche tra una versione e l'altra, quindi test e risoluzione dei problemi diventano più facili. Questo argomento attinge a quelle due fonti, agli altri argomenti della guida sui cambiamenti e al vocabolario ITIL di uso comune che questa guida non ha potuto confermare rispetto al testo del proprietario del framework. Considera le fonti forti, specifiche e limitate ai contesti che descrivono.

## Concetti fondamentali

### Rilascio e deployment

I due termini sono spesso confusi. Una distinzione comune, ampiamente usata nella gestione dei servizi, è:

- Un **rilascio** è una versione di un servizio o di un componente resa disponibile per l'uso. È una decisione su che cosa gli utenti riceveranno.
- Un **deployment** è l'atto di spostare una versione in un ambiente, come la produzione.

Separarli è potente. Puoi installare il codice in produzione senza attivarlo per gli utenti e rilasciarlo più tardi in modo controllato. Tecniche come i feature switch si basano su questa separazione (vedi l'articolo di Wikipedia sui feature toggle).

### Consegna continua e deployment continuo

La pagina DORA definisce la **consegna continua** (continuous delivery) come la capacità di rilasciare modifiche di ogni tipo su richiesta in modo rapido, sicuro e sostenibile. La distingue dal **deployment continuo** (continuous deployment), che significa installare ogni modifica in produzione il prima possibile. DORA dice che i team "can and should start with continuous delivery" anche se non adotteranno mai il deployment continuo. La decisione di rilasciare resta una decisione di business; la consegna continua ne fa una scelta anziché un progetto.

### Che cosa raccomanda la ricerca

La pagina DORA elenca pratiche che sostengono la consegna continua:

| Pratica | Che cosa dice DORA |
|---|---|
| **Automazione dei test** | Suite di test automatici complete e affidabili, create e mantenute per lo più dagli sviluppatori |
| **Automazione del deployment** | Deployment completamente automatizzati, senza bisogno di intervento manuale |
| **Sviluppo trunk-based** | Meno di tre rami attivi, rami di brevissima durata, rari periodi di blocco del codice |
| **Team e architettura debolmente accoppiati** | I team possono testare e installare su richiesta senza orchestrarsi con altri servizi |
| **Altre pratiche** | Integrazione continua, test continui, controllo di versione per tutti gli artefatti di produzione, gestione dei dati di test, monitoraggio e osservabilità, notifiche proattive, gestione delle modifiche al database, sicurezza pervasiva |

La pagina riferisce che la consegna continua è associata a una qualità più alta (meno tempo speso in rilavorazioni o lavoro non pianificato), minore burnout e meno dolore nei deployment. Dice anche che i team d'élite che soddisfacevano gli obiettivi di affidabilità nel rapporto 2021 avevano tre volte più probabilità di avere un'architettura debolmente accoppiata rispetto a quelli con prestazioni basse. Non indica strumenti, frequenze di deployment obiettivo né una tempistica di implementazione, e nota che le trasformazioni seguono comunemente una "curva a J", con un calo di efficienza man mano che l'automazione aumenta i requisiti di test e si accumula debito tecnico.

### Lezioni dalla pratica di release engineering

Il capitolo del libro SRE sulla release engineering descrive l'approccio di una grande organizzazione:

- **Self-service.** I team gestiscono i propri processi di rilascio. I rilasci sono "truly automatic" e richiedono il coinvolgimento di un ingegnere solo se sorgono problemi.
- **Alta velocità.** Rilasci frequenti significano meno modifiche tra una versione e l'altra, il che rende più facili test e risoluzione dei problemi.
- **Build ermetiche.** Le build dipendono da versioni note di strumenti e librerie, quindi la stessa revisione dà risultati identici.
- **Policy applicate.** I controlli di accesso regolano approvazioni, creazione dei rilasci e deployment. Quasi tutte le modifiche richiedono una revisione del codice e ogni rilascio produce un rapporto delle modifiche incluse.

Il capitolo sottolinea anche la configurazione sotto controllo di versione e revisione del codice e suggerisce che sviluppatori, site reliability engineer e release engineer collaborino invece di passarsi i risultati "over the fence". Dice che le organizzazioni dovrebbero definire policy di rilascio anche quando non possono ancora automatizzarle o farle rispettare e che è più economico adottare buone pratiche presto che aggiungerle dopo. Il capitolo descrive gli strumenti di Google stessi; il tuo ambiente ne userà di diversi, quindi trai i principi e non i prodotti.

### Ambienti e promozione

Un rilascio di solito attraversa una serie di ambienti, come sviluppo, test e produzione. Ogni passaggio fornisce prove. Una pratica comune, coerente con la ricerca sopra, è costruire una volta e promuovere lo stesso artefatto, così che ciò che è stato testato sia ciò che viene installato. L'enfasi del capitolo SRE su build identiche dalla stessa revisione esprime la stessa idea.

### Rollout e rollback

Il modo in cui un rilascio raggiunge gli utenti può essere graduale. Il capitolo SRE descrive rollout calibrati sul rischio, da push automatici orari nello sviluppo a rollout di più giorni per l'infrastruttura sensibile, e menziona i canary release, in cui una piccola quota di traffico riceve per prima la nuova versione. Rollback significa tornare alla versione precedente e dovrebbe essere esercitato quanto il rollout. I team che sanno invertire rapidamente possono permettersi di installare spesso (vedi Argomento 3.4 — Abilitazione dei cambiamenti).

### Informazioni sul rilascio per il supporto

Il personale di supporto e gli utenti devono sapere che cosa cambia e che cosa fare se qualcosa va storto. Una nota di rilascio, un elenco di problemi noti e un referente nominato sono il minimo (vedi Argomento 3.1 — Service desk). Il rapporto del capitolo SRE sulle modifiche incluse in un rilascio serve da fonte.

### Misure

La pagina DORA suggerisce di misurare tempi di consegna brevi per cambiamenti regolari e di emergenza, bassi tassi di fallimento dei cambiamenti, breve tempo di ripristino del servizio e frequenze di rilascio che consegnano le priorità in tempo. Il suo obiettivo generale è che nessuno lavori fuori dall'orario d'ufficio per installare. Per definizioni e avvertenze sulle misure, vedi Argomento 3.4 — Abilitazione dei cambiamenti e Argomento 5.6 — Metriche e misurazione.

## Buone pratiche

1. **Separa il deployment dal rilascio.** Installa il codice in produzione in stato dormiente e attivalo per gli utenti quando è pronto, usando feature switch o rollout a stadi. Questo riduce il rischio di un deployment e dà il controllo al business.
2. **Automatizza il deployment.** Punta a nessun passaggio manuale. I passaggi manuali sono lenti, variano da persona a persona e causano incidenti. Automatizza a piccoli incrementi, partendo dai passaggi che vanno storto più spesso.
3. **Costruisci una volta, promuovi l'artefatto.** Produci un unico pacchetto e spostalo tra gli ambienti, così che ciò che hai testato sia ciò che esegui. Registra quale versione è dove.
4. **Rendi riproducibili le build.** Fissa le versioni di strumenti e librerie così che la stessa revisione dia lo stesso risultato. Segue il principio delle build ermetiche del capitolo SRE.
5. **Mantieni i rami di breve durata.** L'indicazione trunk-based di DORA è meno di tre rami attivi e rami che si integrano entro circa un giorno. I rami lunghi trasformano i rilasci in eventi di merge.
6. **Testa automaticamente e mantieni i test rapidi e affidabili.** Punta a un feedback in minuti. Una suite di test instabile o lenta spinge le persone ad aggirarla.
7. **Rilascia in piccoli lotti.** I rilasci più piccoli sono più facili da rivedere, testare e annullare. Se un rilascio è grande, chiedi come dividerlo.
8. **Fai il rollout a stadi.** Parti da una piccola quota di utenti o server, osserva i segnali ed espandi. Definisci in anticipo che cosa osserverai e chi può fermare il rollout.
9. **Esercita il rollback.** Sappi come tornare all'ultima versione buona ed esercitati. Un rollback mai provato è una speranza.
10. **Dai al supporto ciò di cui ha bisogno prima del rilascio.** Fornisci note di rilascio, problemi noti e un referente. Includi il personale di supporto nell'approvazione delle modifiche che riguardano gli utenti (vedi Argomento 3.1 — Service desk).
11. **Tieni la configurazione sotto controllo di versione.** Tratta le modifiche di configurazione come codice, con revisione e record. Scegli dove vive ogni tipo di impostazione e perché.
12. **Punta al deployment in orario d'ufficio.** DORA lo indica come obiettivo generale. Se i deployment richiedono nottate, il processo o l'architettura vanno migliorati.

## Domande da discutere con il team

**Quanto tempo ci vuole, e quanti passaggi comporta, portare in produzione una modifica finita?**

Ripercorri una modifica recente da "pronta" a "live". Elenca ogni passaggio, chi lo fa e quanto aspetta. Distingui i passaggi manuali da quelli automatici. I team sono spesso sorpresi da quanti passaggi sono manuali e dalle attese tra di essi. Chi facilita può chiedere quale passaggio ha causato più incidenti. Scegline uno da automatizzare.

**Che cosa dovrebbe essere vero perché possiamo rilasciare in orario d'ufficio senza preoccuparci?**

Chiedi che cosa il team teme del rilascio. Le risposte tipiche: nessun rollback testato, test deboli, impatto poco chiaro sugli utenti. Ciascuna è una cosa da costruire. Elencale e ordinale. Chiedi quale sarebbe il più piccolo passo per la prima. L'obiettivo DORA di nessuno che lavora fuori dall'orario d'ufficio per installare è un utile traguardo di cui discutere.

**Dove accorpiamo le modifiche perché rilasciare è doloroso, e quanto ci costa l'accorpamento?**

Guarda il contenuto dei rilasci recenti. Conta le modifiche in ciascuno. Chiedi che cosa è successo quando un lotto è andato male e quanto ci è voluto per trovare la causa. Discuti che cosa renderebbe i rilasci di una sola modifica la via facile. Concorda un primo passo, come rilasciare da sola una modifica a basso rischio.

**Come sappiamo che un rilascio funziona una volta in produzione?**

Chiedi quali segnali il team osserva nella prima ora: errori, prestazioni, segnalazioni degli utenti. Se la risposta è "aspettiamo i reclami", discuti il monitoraggio che mostrerebbe rapidamente un problema. Chiedi chi osserva e che cosa farebbe. Concorda una breve checklist per dopo il rilascio.

**Che cosa sa il nostro team di supporto di un rilascio prima che esca?**

Chiedi al service desk che cosa ha saputo dell'ultimo rilascio e quando. Confronta con ciò di cui aveva bisogno. Discuti un semplice passaggio di consegne, come una nota di rilascio e un referente nominato. Includi le persone che rispondono alle domande degli utenti nella pianificazione dei rilasci rischiosi.

**Che cosa ci impedisce di installare senza un periodo di blocco, e quanto ci costerebbe un periodo di blocco?**

I periodi di blocco sono comuni intorno ai picchi di attività. Chiedi quanto durano e che cosa ritardano. Discuti se modifiche piccole e ben testate potrebbero procedere durante di essi con salvaguardie aggiuntive. La pagina DORA mette in guardia dall'applicare la stessa approvazione a tutte le modifiche indipendentemente da rischio o tempistica, quindi chiedi se il blocco è troppo grossolano.

## Nella pratica: un esempio di ITIL agile

Un'università gestisce un sistema di iscrizioni online per 30.000 studenti. Il team di sviluppo di otto persone rilascia una volta a trimestre, in una finestra di fine settimana prima dell'apertura delle iscrizioni. Ogni rilascio accorpa centinaia di modifiche e richiede quindici persone, una lunga checklist manuale e un piano di chiamata. L'ultimo rilascio è fallito alle 2 di domenica mattina e il team ha speso quattordici ore a trovare quale delle modifiche l'aveva causato.

La responsabile del team propone un cambio di approccio. Primo, i deployment diventano completamente scriptati, partendo dai passaggi che sono falliti l'ultima volta. Secondo, il team aggiunge test automatici per il percorso delle iscrizioni che girano a ogni modifica e durano meno di dieci minuti. Terzo, le nuove funzionalità sono installate disattivate e abilitate con un feature switch dopo i controlli. Quarto, un passaggio di rollback viene scritto e provato in un ambiente di test. L'ufficio dell'anagrafe concorda una regola per cui nessun rilascio va in produzione nelle tre settimane di picco delle iscrizioni a meno che sia la correzione di un guasto visibile agli utenti.

Nel giro di un trimestre, il team installa ogni settimana fuori dalle settimane di picco, in orario d'ufficio, con le note di rilascio inviate all'helpdesk degli studenti il giorno prima. Alcuni rilasci sono rallentati da test instabili e un feature switch è stato lasciato attivo per errore e ha causato una breve confusione. La trasformazione incontra anche la curva a J descritta dalla pagina DORA: per due mesi, il lavoro su test e script rallenta la consegna di funzionalità. Il team va avanti, corregge i test instabili, aggiunge un passaggio di checklist per rimuovere gli switch e concorda con l'anagrafe di rivedere la regola del blocco l'anno prossimo. I picchi di iscrizione dei trimestri passano senza incidenti legati ai rilasci.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery possiedono la pipeline: test, build, script di deployment e rollback. Investi in essa come in un prodotto con utenti. Rilascia piccolo, rilascia spesso e tratta ogni rilascio come prova sulla pipeline. Coinvolgi supporto e operations quando le modifiche li riguardano.

### Team di servizio e di operations

I team operativi traggono vantaggio da rilasci più piccoli e prevedibili e possono aiutare definendo che cosa deve essere vero prima che un rilascio sia accettato: monitoraggio, runbook e rollback. Passa dal fare da cancello al rendere possibile, fornendo la piattaforma e i controlli che i team di delivery usano. Osserva i segnali dopo un rilascio.

### Leadership e governance

I leader decidono se i team possono investire nella pipeline e tollerare la curva a J. Chiedi lead time, change fail rate e tempo di ripristino. Resisti al blocco dei rilasci come risposta generale al rischio e chiedi invece prove che i rilasci rischiosi ricevano più attenzione.

### Clienti e utenti

Clienti e utenti vedono miglioramenti piccoli e frequenti e meno interruzioni in blocco. Aspettati un preavviso delle modifiche che ti riguardano e un modo di segnalare problemi. Se hai periodi di punta, dillo al fornitore così che possa pianificare rollout a stadi attorno ad essi.

## Modalità di fallimento comuni

- **Rilasci big-bang.** Centinaia di modifiche escono insieme. Rilascia invece in piccoli lotti e separa deployment e rilascio.
- **Deployment manuale.** I passaggi variano da persona a persona e falliscono di notte. Automatizza invece a incrementi, partendo dai passaggi più rischiosi.
- **Rilasciare più spesso senza salvaguardie.** I tassi di fallimento salgono e le persone si logorano, come avverte DORA. Investi invece prima in test, rollback e monitoraggio.
- **Artefatti diversi in ambienti diversi.** Ciò che è testato non è ciò che gira. Costruisci invece una volta e promuovi lo stesso artefatto.
- **Rami di lunga durata.** I merge diventano eventi. Mantieni invece i rami brevi e integra in continuazione.
- **Rollback mai provato.** Il primo rollback avviene durante un'interruzione. Esercitalo invece regolarmente.
- **Il supporto lo scopre per ultimo.** Il personale viene a sapere dei cambiamenti dagli utenti. Invia invece note di rilascio e un referente prima del rilascio.
- **Blocchi generalizzati.** Lo stesso blocco si applica a tutte le modifiche. Lascia invece passare le modifiche a basso rischio e ben testate con controlli aggiuntivi e riserva il blocco a ciò che è rischioso.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Automazione del deployment | I deployment sono manuali e variano | Alcuni deployment sono scriptati | I deployment sono automatizzati attraverso una pipeline comune | Fallimenti e durata dei deployment sono monitorati e ridotti | Pipeline e pratiche sono condivise e migliorate tra i team |
| Frequenza e dimensione dei rilasci | I rilasci sono rari e grandi | Alcuni team rilasciano in lotti più piccoli | I team rilasciano in piccoli lotti con un ritmo noto | Frequenza, lead time e dimensione sono misurati e regolati | I ritmi di rilascio sono coordinati tra servizi e fornitori |
| Sicurezza (test, rollout, rollback) | I test sono manuali; il rollback non è provato | Esistono alcuni test automatici e passaggi di rollback | Test automatici, rollout a stadi e rollback provato sono standard | Change fail rate e tempo di ripristino sono monitorati e migliorati | Le pratiche di sicurezza sono condivise e testate tra i team |
| Prontezza del supporto | Il supporto apprende dei rilasci dagli utenti | Alcuni rilasci hanno note | Note di rilascio e referenti sono standard | Il feedback del supporto sui rilasci è raccolto e usato | Supporto, delivery e utenti pianificano insieme i rilasci |

## Checklist

- [ ] Sappiamo dire la differenza tra installare e rilasciare e la usiamo.
- [ ] I deployment sono automatizzati senza passaggi manuali, oppure i passaggi manuali rimasti sono elencati.
- [ ] Costruiamo una volta e promuoviamo lo stesso artefatto tra gli ambienti.
- [ ] I test automatici girano a ogni modifica e danno feedback in minuti.
- [ ] I rami sono di breve durata e integrati frequentemente nel trunk.
- [ ] Esiste un rollback per ogni tipo di rilascio ed è stato provato.
- [ ] I rollout sono a stadi dove il rischio lo giustifica, con segnali definiti in anticipo.
- [ ] Note di rilascio e problemi noti raggiungono il service desk prima di un rilascio.
- [ ] La configurazione è sotto controllo di versione e rivista.
- [ ] Monitoriamo lead time, change fail rate e tempo di ripristino per ogni servizio.

## Prompt per l'IA

**Scopo: mappare i passaggi da "pronto" a "live" e trovare che cosa automatizzare.**

```text
Help me map the path of a change from ready to live.

The steps in order, with who does each, whether it is manual or automated, and how long it typically waits or takes: [paste].
The last three releases and what went wrong, if anything: [paste facts].

Produce a table of steps and mark the manual ones. Rank the manual steps by how often they caused problems in the text, and suggest, for the top three, one small way to automate or check each. Do not invent durations or failure counts. Ask clarifying questions first if information is missing, mark assumptions, and list what you are unsure of.
```

**Scopo: scrivere una nota di rilascio per il service desk e gli utenti.**

```text
Write a release note for [service].

What changed (plain words): [describe].
Who is affected and when: [describe].
What users will notice: [describe].
Known issues and workarounds: [list, or write "none known"].
How to roll back and who to contact: [describe].

Write two versions: a one-paragraph note for users and a half-page note for the service desk. Use only the facts above. Mark any statement that is an assumption and ask clarifying questions first if information is missing. List what you are unsure of.
```

**Scopo: pianificare un rollout a stadi.**

```text
Plan a staged rollout of [change].

What it changes and who uses it: [describe].
How we can limit exposure (percentage of users, regions, servers, feature switch): [describe options available].
Signals we can watch: [list monitoring and user feedback sources].
Rollback method: [describe].

Propose stages, what to check at each stage, who can pause or stop, and what would trigger a rollback, leaving numeric thresholds as [to be agreed]. Do not invent monitoring that we do not have. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: preparare le ragioni per investire nell'automazione dei rilasci.**

```text
Help me prepare a short case for investing in release automation for [service].

What a release costs us today, in facts: [people involved, hours, incidents, delays; use real numbers only].
What we want to be able to do: [describe].
Known risks of the work: [for example a temporary slowdown while tests are written].

Write a one-page case with the problem, the proposed first steps (small and incremental), what we will measure (lead time, change fail rate, recovery time, with no targets that I did not give), the risks including a temporary dip in delivery, and what we ask for. Do not invent figures. Ask clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [release-notes](../../../../skills/release-notes/SKILL.md): da usare per dire a utenti e service desk che cosa cambia un rilascio.
- [changelog](../../../../skills/changelog/SKILL.md): da usare per tenere un registro continuo delle modifiche per versione.
- [test-driven-development](../../../../skills/test-driven-development/SKILL.md): da usare per costruire i test automatici che rendono sicuro il rilascio frequente.
- [shift-left-testing](../../../../skills/shift-left-testing/SKILL.md): da usare per anticipare i test nella pipeline così che i problemi siano trovati prima.
- [agile-delivery](../../../../skills/agile-delivery/SKILL.md): da usare per pianificare rilasci piccoli e frequenti e i controlli attorno ad essi.

## Fonti principali

- **Continuous delivery** (DORA, dora.dev): la definizione del programma di ricerca, le pratiche raccomandate, i risultati e le insidie.
- **Release Engineering** (*Site Reliability Engineering*, Google, sre.google): la pratica di un'organizzazione di self-service, build riproducibili e policy di rilascio applicate.
- **Streamlining change approval** (DORA, dora.dev): indicazioni su come l'approvazione si inserisce nella consegna.
- **Continuous delivery** (Wikipedia): una panoramica della pratica e della sua storia.

## Riferimenti

1. Continuous delivery — DORA, dora.dev — https://dora.dev/capabilities/continuous-delivery/
2. Release Engineering — Google SRE book, sre.google — https://sre.google/sre-book/release-engineering/
3. Streamlining change approval — DORA, dora.dev — https://dora.dev/capabilities/streamlining-change-approval/
4. Continuous delivery — Wikipedia — https://en.wikipedia.org/wiki/Continuous_delivery
5. Software deployment — Wikipedia — https://en.wikipedia.org/wiki/Software_deployment
6. Release management — Wikipedia — https://en.wikipedia.org/wiki/Release_management
7. Feature toggle — Wikipedia — https://en.wikipedia.org/wiki/Feature_toggle
8. Continuous integration — Wikipedia — https://en.wikipedia.org/wiki/Continuous_integration
9. Version control — Wikipedia — https://en.wikipedia.org/wiki/Version_control
