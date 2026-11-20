# Abilitazione dei cambiamenti

**L'abilitazione dei cambiamenti esiste per far avvenire in sicurezza e rapidamente le modifiche utili, e le prove della ricerca sulla consegna del software sono che il rischio è controllato meglio da modifiche piccole, revisione tra pari e controlli automatici che dall'invio di ogni modifica a un comitato.**

## Perché è importante

Il cambiamento è il punto in cui la consegna continua e la gestione dei servizi si scontrano più spesso. I team di delivery vogliono rilasciare spesso, perché modifiche piccole e frequenti sono più facili da capire e annullare. Operations e governance vogliono evitare interruzioni e tenere i record, perché modifiche passate hanno rotto dei servizi. Hanno ragione entrambe. Il disaccordo riguarda di solito come controllare il rischio: con l'approvazione prima della modifica o con la qualità della modifica e la rapidità del ripristino.

La pratica si chiama abilitazione dei cambiamenti in ITIL 4. Il nuovo nome è una dichiarazione di scopo. L'obiettivo è permettere alle modifiche utili di avvenire, non impedire le modifiche. Le versioni più vecchie di ITIL chiamavano la pratica gestione dei cambiamenti e le davano un ruolo forte nelle approvazioni e nelle pianificazioni, che molti team vivevano come un cancello.

Questo argomento usa le migliori prove disponibili: le indicazioni del programma di ricerca DORA sull'approvazione dei cambiamenti e le sue metriche di consegna del software, lette dalle pagine del programma stesso. Le pagine DORA riferiscono che l'approvazione esterna pesante è associata a prestazioni di consegna peggiori. Non danno nemmeno dimensioni dell'effetto o dettagli statistici e rimandano a un rapporto del 2019 per la ricerca di base, quindi considera le indicazioni forti ma non definitive e mettile alla prova nel tuo contesto. Il vocabolario ITIL qui viene da descrizioni ampiamente pubblicate che questa guida non ha potuto verificare rispetto al testo del proprietario del framework (vedi Argomento 2.2 — ITIL).

## Concetti fondamentali

### Che cosa fa l'abilitazione dei cambiamenti

Un **cambiamento** è l'aggiunta, la modifica o la rimozione di qualsiasi cosa che possa influenzare un servizio. L'abilitazione dei cambiamenti è la pratica che assicura che i cambiamenti siano valutati, autorizzati e programmati in modo da gestire il rischio e far procedere i cambiamenti utili. La pratica conserva anche un record di che cosa è cambiato, vitale per la risposta agli incidenti perché molti incidenti iniziano con una modifica recente (vedi Argomento 3.2 — Gestione degli incidenti).

### Tipi di cambiamento

ITIL 4 è ampiamente descritto come riconoscitore di tre tipi di cambiamento, ciascuno con un percorso diverso:

| Tipo | Che cos'è | Percorso tipico |
|---|---|---|
| **Cambiamento standard** | Una modifica a basso rischio e ben compresa che segue una procedura documentata | Preautorizzata; registrata, senza approvazione caso per caso |
| **Cambiamento normale** | Una modifica che richiede valutazione e autorizzazione | Valutata per rischio e impatto, poi autorizzata dalla persona o dal gruppo appropriato |
| **Cambiamento di emergenza** | Una modifica da fare con urgenza, per esempio per ripristinare il servizio | Autorizzazione accelerata, con revisione più completa dopo |

I nomi e le definizioni esatte vanno verificati rispetto alle pubblicazioni del proprietario. Il principio è stabile: adegua il livello di controllo al rischio.

### Autorità sul cambiamento

Ogni tipo di cambiamento ha bisogno di qualcuno con l'autorità di approvarlo. Nella pratica più vecchia questo era spesso un comitato consultivo sui cambiamenti (CAB). La pagina DORA non abolisce il CAB; suggerisce un ruolo "strategico", di coordinamento tra i team, di sostegno al miglioramento dei processi e di decisioni su compromessi di business come tempo di arrivo sul mercato contro rischio. Per le modifiche di routine, dice, l'approvazione è implementata al meglio tramite revisione tra pari durante lo sviluppo, sostenuta dall'automazione.

### Che cosa riferisce DORA sull'approvazione

La pagina DORA sulla semplificazione dell'approvazione dei cambiamenti dice:

- L'approvazione esterna pesante, come un CAB o la firma di un dirigente senior, è associata a prestazioni di consegna del software peggiori.
- La pagina non riporta prove che una revisione esterna più formale riduca i tassi di fallimento dei cambiamenti.
- Sostiene che l'approvazione pesante rallenta la consegna, portando a rilasci più grandi e meno frequenti con rischio maggiore, e dice che i suoi dati hanno sostenuto questa ipotesi.

La pagina nomina insidie: affidarsi a un CAB centrale per intercettare gli errori, applicare lo stesso processo di approvazione a tutte le modifiche indipendentemente dal rischio, non migliorare il processo rispetto alle metriche e aggiungere processo e approvazioni in risposta all'instabilità in produzione, il che dice tenda a peggiorare le cose. "No evidence was found" significa che non sono state trovate prove del beneficio; non dimostra che la revisione esterna non abbia effetto. La pagina non dà criteri per che cosa conti come modifica ad alto rischio, né indicazioni per normative specifiche, né un piano di transizione per i settori regolamentati.

### L'alternativa: il controllo nella pipeline

DORA suggerisce di soddisfare la separazione dei compiti attraverso una revisione tra pari registrata nella piattaforma di sviluppo e di usare test continui, integrazione continua e monitoraggio per rilevare, prevenire e correggere presto le modifiche difettose. Suggerisce anche di trattare la piattaforma come un prodotto che dà agli sviluppatori feedback rapido su sicurezza, prestazioni, stabilità e difetti, di segnalare le modifiche ad alto rischio per un'ulteriore attenzione e di rendere il normale processo di cambiamento abbastanza rapido da gestire le emergenze. Il controllo sta nelle prove che la pipeline produce: chi ha rivisto, quali test sono passati, che cosa è stato installato e come può essere annullato.

### Misurare il cambiamento

La pagina DORA sulle metriche di prestazione della consegna del software elenca cinque misure:

| Misura | Che cos'è | Gruppo |
|---|---|---|
| Change lead time | Tempo da quando una modifica è registrata nel controllo di versione al deployment in produzione | Throughput |
| Deployment frequency | Quanto spesso avvengono i deployment | Throughput |
| Failed deployment recovery time | Quanto tempo ci vuole per riprendersi da un deployment che fallisce e richiede un intervento immediato | Throughput |
| Change fail rate | La quota di deployment che richiedono un intervento immediato, come un rollback o un hotfix | Instabilità |
| Deployment rework rate | La quota di deployment non pianificati e derivanti da un incidente in produzione | Instabilità |

La pagina dice che velocità e stabilità non sono un compromesso: le misure sono correlate per la maggior parte dei team, e i migliori ottengono buoni risultati su tutte e cinque. Mette in guardia dal fissare le misure come obiettivi (legge di Goodhart), dall'affidarsi a una sola metrica, dal confrontare applicazioni molto diverse e dal competere con altri team. Suggerisce che i team migliorino rispetto alle proprie prestazioni passate. La pagina non dà soglie di riferimento né formule, quindi definisci ogni misura per il tuo contesto prima di usarla (vedi Argomento 5.6 — Metriche e misurazione).

### Record e visione della configurazione

Un record di cambiamento dovrebbe dire che cosa è cambiato, perché, chi ha approvato e quando è stato fatto, e idealmente collegarsi ai servizi interessati. Gli strumenti di controllo di versione, build e deployment possono produrne gran parte automaticamente. Collegare i cambiamenti alla configurazione dei servizi sostiene l'analisi dell'impatto e la risposta agli incidenti (vedi Argomento 4.4 — Gestione della configurazione).

### Cambiamento e rilascio

L'abilitazione dei cambiamenti decide se una modifica può procedere. La gestione di rilasci e deployment la porta in produzione (vedi Argomento 3.5 — Gestione di rilasci e deployment). Nella consegna continua i due si fondono nella pratica, con le approvazioni incorporate nella pipeline.

## Buone pratiche

1. **Classifica i cambiamenti per rischio.** Definisci un breve elenco di tipi di cambiamento, con criteri ed esempi. Adegua il percorso al rischio, così che le modifiche di routine siano rapide e quelle rischiose ricevano attenzione.
2. **Preautorizza le modifiche a basso rischio.** Per le modifiche ben comprese, testate e reversibili, concorda una procedura standard e lasciale procedere senza approvazione caso per caso. Registrale automaticamente.
3. **Fai della revisione tra pari l'approvazione predefinita.** Richiedi che una seconda persona riveda le modifiche prima dell'integrazione e registra la revisione nella piattaforma di sviluppo. Questo soddisfa la separazione dei compiti per la maggior parte delle modifiche, come descrive la pagina DORA.
4. **Automatizza i controlli.** Esegui test, scansioni di sicurezza e controlli di policy a ogni modifica e fai dei risultati parte del record. Un'approvazione basata su prove è più forte di una basata su un modulo.
5. **Mantieni piccole le modifiche.** Le modifiche piccole sono più facili da rivedere, testare e annullare. Se una modifica sembra rischiosa, chiedi se può essere divisa.
6. **Rendi il rollback facile e provato.** Per ogni tipo di cambiamento, sappi come annullarlo ed esercitati. La capacità di riprendersi rapidamente riduce il bisogno di prevedere ogni guasto.
7. **Segnala le modifiche ad alto rischio.** Definisci segnali, come modifiche alla logica dei pagamenti o all'infrastruttura condivisa, che innescano una revisione aggiuntiva. Applica il percorso più pesante solo a esse.
8. **Dai all'autorità sul cambiamento un ruolo strategico.** Usa un eventuale comitato centrale per coordinare tra i team, risolvere conflitti e prendere decisioni di compromesso di business. Non usarlo come punto di controllo per ogni modifica.
9. **Gestisci le emergenze con il percorso normale.** Rendi il processo regolare abbastanza rapido e affidabile perché le modifiche di emergenza lo seguano, con revisione dopo. Vie di emergenza usate spesso segnalano che il percorso normale è troppo lento.
10. **Non aggiungere approvazioni dopo un incidente per impostazione predefinita.** La pagina DORA dice che aggiungere processo in risposta all'instabilità tende a peggiorare le cose. Chiedi prima se la correzione sono test migliori, modifiche più piccole o ripristino più rapido.
11. **Misura il processo.** Monitora lead time, tempo speso in attesa di approvazione, la quota di modifiche che passano senza approvazione manuale e change fail rate. Usa le misure per migliorare, non per classificare i team.
12. **Spiega il processo.** La pagina DORA nota che comunicare chiaramente il processo esistente e aiutare i team a orientarsi è legato a prestazioni migliori anche prima di cambiarlo. Pubblica una guida di una pagina con esempi.

## Domande da discutere con il team

**Quale proporzione delle nostre modifiche è a basso rischio e ben compresa, e come sono approvate oggi?**

Prendi un mese di modifiche e ordinale. La maggior parte dei team trova che la grande maggioranza è di routine. Chiedi quanto aspettano le modifiche di routine l'approvazione e che cosa aggiunge l'approvatore. Chi facilita può chiedere se qualcuno ricorda una modifica di routine che l'approvazione abbia impedito di fallire. Usa la risposta per individuare un primo candidato alla preautorizzazione.

**Che cosa intercetta davvero il nostro passaggio di approvazione?**

Elenca le ultime dieci modifiche rifiutate o ritardate all'approvazione e perché. Confronta con i problemi arrivati in produzione nonostante l'approvazione. Se l'approvazione intercetta poco, chiedi che cosa intercetterebbe gli stessi problemi prima, come test o revisione tra pari. Ricorda che la pagina DORA non riporta prove che una revisione esterna più formale riduca i tassi di fallimento dei cambiamenti. Concorda un cambiamento da provare.

**Come annulleremmo una modifica sbagliata, e con quale rapidità?**

Scegli una modifica recente e descrivi il rollback. Se è poco chiaro, non testato o manuale, quello è il rischio. Chiedi quanto ci vorrebbe e chi lo farebbe. Concorda di provare un rollback questo mese. Un team che sa riprendersi in pochi minuti può accettare più cambiamento.

**Quali delle nostre modifiche richiedono un'attenzione aggiuntiva, e come le riconosceremmo?**

Raccogli esempi di modifiche che hanno causato incidenti gravi. Cerca le caratteristiche che condividono: infrastruttura condivisa, controlli di sicurezza, migrazioni di dati. Redigi tre segnali che segnalerebbero una modifica come ad alto rischio. Chiedi chi dovrebbe rivedere le modifiche segnalate e con quale rapidità.

**Quando abbiamo aggiunto un controllo dopo un incidente, e ha aiutato?**

Chiedi esempi. Elenca che cosa è stato aggiunto, i problemi che affrontava e se il problema si è ripetuto. La pagina DORA nomina l'aggiunta di approvazioni in risposta all'instabilità come un'insidia. Discuti se una risposta diversa, come test migliori o modifiche più piccole, avrebbe funzionato. Registra una lezione.

**Quali prove accetterebbe un auditor dalla nostra pipeline al posto di una firma?**

Chiedi a un auditor o a un collega della conformità di partecipare. Elenca le prove che la pipeline produce già: revisioni, risultati dei test, record di deployment. Chiedi che cosa manca. Molti auditor accettano la revisione tra pari registrata e le prove automatiche quando sono affidabili. Concorda una breve descrizione del controllo e un periodo di prova.

## Nella pratica: un esempio di ITIL agile

Il reparto IT di un ospedale regionale supporta un sistema di pianificazione clinica che viene aggiornato da un team interno di sette persone. Ogni modifica, da una correzione di un errore di battitura a una migrazione di database, va a un comitato consultivo settimanale sui cambiamenti. Le piccole correzioni aspettano fino a otto giorni. I clinici si lamentano e gli sviluppatori hanno cominciato ad accorpare le correzioni in rilasci più grandi per evitare la coda, il che rende ogni rilascio più rischioso.

Il responsabile IT e il presidente del comitato rivedono un anno di modifiche. La maggior parte era piccola, due avevano causato incidenti e nessuna delle due era stata intercettata dal comitato. Progettano un approccio a tre corsie. I cambiamenti standard, come modifiche di testo e di configurazione entro limiti concordati, con test automatici superati e un rollback collaudato, sono preautorizzati e registrati automaticamente. I cambiamenti normali richiedono una revisione tra pari registrata nella piattaforma di sviluppo e un controllo rispetto a un breve elenco di segnali ad alto rischio, come modifiche alla gestione dei dati dei pazienti. I cambiamenti segnalati come ad alto rischio vanno al comitato, che si riunisce due volte alla settimana. I cambiamenti di emergenza seguono il percorso normale con una revisione post-implementazione.

Dopo quattro mesi, i cambiamenti standard vanno in produzione entro un giorno e il comitato vede circa un quinto del volume di prima. Il change fail rate non sale. Restano problemi. Due sviluppatori applicano i segnali ad alto rischio in modo incoerente e una modifica segnalata è arrivata tardi al comitato, e l'audit interno chiede prove che le revisioni tra pari non siano timbri di gomma. Il team scrive esempi dei segnali, aggiunge una revisione a campione delle revisioni tra pari da parte di un ingegnere senior e concorda con l'audit di rivedere le prove alla prossima riunione trimestrale.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery portano la maggior parte del controllo: revisione, test, modifiche piccole e rollback. Incorporali nella pipeline e rendi visibili le prove. Mantieni piccole le modifiche e di' alle operations che cosa sta arrivando. Usa il processo di cambiamento come luogo in cui condividere informazioni sul rischio, non solo per ottenere il permesso.

### Team di servizio e di operations

I team operativi sanno quali modifiche hanno danneggiato i servizi. Condividi quella conoscenza come segnali per una revisione aggiuntiva e aiuta a costruire controlli che le intercettino presto. Sostieni percorsi più leggeri per le modifiche a basso rischio e tieni i record che rendono più rapida la risposta agli incidenti.

### Leadership e governance

I leader decidono quanta approvazione l'organizzazione richiede. Le indicazioni DORA suggeriscono di chiedere prove di controllo e non firme su ogni modifica. Sostieni la misurazione di lead time e change fail rate ed evita di aggiungere processo dopo gli incidenti senza esaminare le cause. Concorda con l'audit quali prove sono accettabili.

### Clienti e utenti

Clienti e utenti traggono vantaggio da miglioramenti piccoli e frequenti e da meno grandi interruzioni. Aspettati di essere informato delle modifiche che ti riguardano, in linguaggio semplice e in anticipo. Se hai esigenze particolari, come periodi di blocco, comunicalo presto al fornitore così che possano essere pianificate.

## Modalità di fallimento comuni

- **Un solo percorso per ogni modifica.** Le modifiche di routine fanno la coda dietro quelle rischiose. Classifica invece per rischio e dai a ogni classe il proprio percorso.
- **L'approvazione come unico controllo.** Una firma sostituisce la qualità. Incorpora invece test, revisione e rollback nella pipeline.
- **Un comitato che rivede ciò che non può valutare.** I membri approvano modifiche che non comprendono. Invia invece le modifiche a persone con la conoscenza e usa il comitato per il coordinamento.
- **Accorpare per evitare la coda.** I team combinano le modifiche, rendendo ogni rilascio più rischioso. Rendi invece la coda abbastanza corta perché le modifiche piccole siano la via facile.
- **Aggiungere controlli dopo ogni incidente.** Il processo cresce e la velocità cala. Cerca invece la causa e correggila con test, modifiche più piccole o ripristino più rapido.
- **Revisione tra pari a timbro di gomma.** Le revisioni sono formali ma superficiali. Campiona invece le revisioni, condividi esempi di buone revisioni e mantieni le modifiche abbastanza piccole da poter essere riviste.
- **Nessun rollback.** Le modifiche non possono essere annullate. Richiedi e prova invece un rollback per ogni tipo di cambiamento.
- **Manipolare le metriche.** I team dividono le modifiche o nascondono i fallimenti per fare bella figura. Usa invece più misure, rivedile insieme e concentrati sul miglioramento nel tempo.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Classificazione e percorsi | Tutte le modifiche seguono un percorso o nessuno | Alcuni team hanno una via rapida per le modifiche semplici | Tipi di cambiamento con criteri e percorsi distinti sono standard | Quota di modifiche per percorso e tempi di attesa sono misurati e regolati | I percorsi sono adeguati tra i team in base a prove condivise |
| Approvazione e prove | L'approvazione avviene per firma o non è registrata | Alcune modifiche sono riviste tra pari | Revisione tra pari e controlli automatici sono registrati per la maggior parte delle modifiche | Qualità della revisione e prove sono campionate e migliorate | Le prove fluiscono automaticamente verso audit e partner |
| Ripristino | Il rollback è estemporaneo | Alcune modifiche hanno passaggi di rollback | Il rollback è definito e provato per ogni tipo di cambiamento | Il tempo di ripristino è misurato e ridotto | Le pratiche di ripristino sono condivise e testate tra team e fornitori |
| Misurazione e miglioramento | Poche misure | Alcuni team monitorano il lead time | Lead time, frequenza, tasso di fallimento e tempo di ripristino sono monitorati per servizio | Le misure guidano miglioramenti pianificati e non sono usate come obiettivi | I team imparano dalle misure degli altri e migliorano in tutta l'organizzazione |

## Checklist

- [ ] Abbiamo definito tipi di cambiamento con criteri ed esempi.
- [ ] Le modifiche a basso rischio e ben comprese sono preautorizzate e registrate automaticamente.
- [ ] La revisione tra pari è registrata nella piattaforma di sviluppo per i cambiamenti normali.
- [ ] Test e controlli automatici girano a ogni modifica.
- [ ] Ogni tipo di cambiamento ha un rollback che è stato provato.
- [ ] Abbiamo segnali che segnalano le modifiche ad alto rischio per un'attenzione aggiuntiva.
- [ ] Qualsiasi comitato centrale ha un ruolo chiaro nel coordinamento e nei compromessi.
- [ ] Monitoriamo change lead time, deployment frequency, failed deployment recovery time e change fail rate per ogni servizio.
- [ ] I nostri auditor hanno detto quali prove accettano al posto delle firme.
- [ ] Abbiamo una guida di una pagina al processo di cambiamento con esempi.

## Prompt per l'IA

**Scopo: classificare le modifiche del mese scorso per rischio e percorso di approvazione.**

```text
Below is a list of the changes we made last month: [paste one line per change with a short description, who reviewed it, how long it waited for approval, and whether it caused an incident; remove personal data].

Help me sort them into three groups: routine and low risk, needs normal assessment, and needs extra scrutiny. For each group, say what features of the changes in my list led you to the grouping, using only the text. Calculate the share in each group and the average wait for approval from my numbers only. Suggest which routine changes might be pre-authorized and what safeguards I would want first. Do not guess at risks beyond what I wrote. List what you are unsure of.
```

**Scopo: scrivere una procedura di cambiamento standard.**

```text
Help me write a procedure for a standard (pre-authorized) change: [name the change, for example "update a configuration value within agreed limits"].

How it is done today, step by step: [paste].
Checks that exist: [tests, scans, reviews].
How to undo it: [describe, or write "unknown"].
Who owns the procedure: [role].

Write a one-page procedure with: when it applies, the criteria that make a change standard, the steps, the checks that must pass, how it is recorded, how to undo it, and when to treat it as a normal change instead. Mark every statement you added as an assumption. Do not claim any rule requires something unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: prepararsi a discutere con un auditor le prove che la nostra pipeline produce.**

```text
An auditor asks how we authorize changes. Our pipeline does the following: [describe code review, tests, scans, deployment record, who can approve, and where records are kept].

The auditor's concern in their words: [paste, or write "unknown"].
Rules we know apply, with source text if you have it: [paste, or write "none known"].

Make a table of what evidence each step produces, where it is stored, who can alter it, and what gaps the auditor may notice. Suggest three lightweight ways to strengthen the weakest points. Do not state that any standard requires something unless I pasted its text. Mark assumptions, and list what you are unsure of.
```

**Scopo: progettare una sperimentazione di approvazione più leggera.**

```text
Design a three-month trial of lighter approval for [service].

Current process: [describe].
Change volume and types last quarter: [paste counts from your records].
Measures we already have: [list, for example lead time and change fail rate].
Concerns from audit or operations: [list].

Propose: which change types to include, safeguards, what to measure and how often (without inventing targets), what would make us stop or pause the trial, and how to report results. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [change-request](../../../../skills/change-request/SKILL.md): da usare per redigere record di cambiamento che portino ciò di cui operations e auditor hanno bisogno.
- [enterprise-change-management](../../../../skills/enterprise-change-management/SKILL.md): da usare quando un cambiamento è organizzativo e richiede una pianificazione per le persone oltre che per i sistemi.
- [release-notes](../../../../skills/release-notes/SKILL.md): da usare per dire a utenti e service desk che cosa fa una modifica.
- [two-way-door-decisions](../../../../skills/two-way-door-decisions/SKILL.md): da usare per distinguere le decisioni reversibili, che si possono prendere in fretta, da quelle irreversibili che richiedono più cura.
- [risk-register](../../../../skills/risk-register/SKILL.md): da usare per registrare e rivedere i rischi che il cambiamento introduce e come sono controllati.

## Fonti principali

- **Streamlining change approval** (DORA, dora.dev): le indicazioni del programma di ricerca su revisione tra pari, automazione e ruolo di un comitato sui cambiamenti.
- **DORA's software delivery performance metrics** (dora.dev): definizioni e avvertenze per change lead time, deployment frequency, tempo di ripristino, change fail rate e rework rate.
- **ITIL** (Wikipedia): contesto sulle versioni di ITIL e sul passaggio a ITIL 4.
- **Continuous delivery** (Wikipedia): contesto sulle pratiche che rendono sicuri i cambiamenti piccoli e frequenti.

## Riferimenti

1. Streamlining change approval — DORA, dora.dev — https://dora.dev/capabilities/streamlining-change-approval/
2. DORA's software delivery performance metrics — DORA, dora.dev — https://dora.dev/guides/dora-metrics-four-keys/
3. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
4. Continuous delivery — Wikipedia — https://en.wikipedia.org/wiki/Continuous_delivery
5. Change management — Wikipedia — https://en.wikipedia.org/wiki/Change_management
6. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
7. Separation of duties — Wikipedia — https://en.wikipedia.org/wiki/Separation_of_duties
8. Version control — Wikipedia — https://en.wikipedia.org/wiki/Version_control
9. Goodhart's law — Wikipedia — https://en.wikipedia.org/wiki/Goodhart%27s_law
