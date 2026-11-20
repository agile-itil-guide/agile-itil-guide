# Scalare l'agile

**Scalare l'agile significa coordinare molti team, servizi e fornitori senza perdere i brevi cicli di feedback che hanno fatto funzionare l'agile, e il rischio principale è aggiungere livelli di processo prima di sapere quale problema si sta risolvendo.**

## Perché è importante

Un singolo team agile fino a dieci persone può parlarsi ogni giorno. Un servizio reale di solito ne coinvolge di più: diversi team di delivery, un gruppo operativo, un service desk, la sicurezza, un team di rete e fornitori. Quando il lavoro di molti gruppi deve combaciare, la conversazione quotidiana di un team non basta e compaiono nuovi problemi. Le priorità entrano in conflitto, le dipendenze bloccano il lavoro e ogni team migliora la propria parte mentre il servizio nel suo insieme non migliora.

Diversi framework sostengono di risolvere il problema. Differiscono per dimensione, costo e filosofia, e suscitano opinioni forti. Alcune organizzazioni adottano un grande framework come programma e spendono anni nell'introduzione. Altre scalano rimuovendo le barriere e mantenendo un piccolo insieme di regole. La posizione onesta, sostenuta dall'[articolo di Wikipedia sullo sviluppo software agile](https://en.wikipedia.org/wiki/Agile_software_development), è che le opinioni sull'efficacia dei framework di scalatura divergono e le prove sono limitate.

Per chi si occupa di gestione dei servizi IT (ITSM), la scalatura conta perché ITIL funziona già su larga scala. Descrive un sistema di valore del servizio che collega molte pratiche e parti (vedi Argomento 2.3 — Il sistema di valore del servizio ITIL). La domanda su cui questo argomento aiuta è come combinare i due mondi: come coordinare molti team agili mantenendo le pratiche di gestione dei servizi che proteggono gli utenti, e senza costruire un secondo livello di burocrazia sopra il primo.

## Concetti fondamentali

### Perché un team è diverso da molti

L'articolo di Wikipedia sullo sviluppo software agile riferisce che la scalatura porta difficoltà quando un progetto coinvolge più di una ventina di sviluppatori o quando i team sono distribuiti su più sedi. Esistono strategie e framework per questi casi, ma l'articolo nota pareri contrastanti sul fatto che rientrino nella definizione di agile.

Tre problemi ricorrono quando si aggiungono team:

- **Allineamento:** i team hanno bisogno di una direzione comune e di priorità coerenti, altrimenti ottimizzeranno cose diverse.
- **Dipendenze:** il lavoro in un team aspetta un altro, e le attese si moltiplicano al crescere del numero di team.
- **Integrazione:** l'output di molti team deve confluire in qualcosa che funzioni come servizio, e quanto più tardi lo si testa, tanto più costose sono le sorprese.

### Quattro approcci noti

La tabella seguente riassume quattro approcci con nome. I riassunti si basano sugli articoli di Wikipedia e sulle pagine dei proprietari dei framework come lette per questa guida; verifica le versioni attuali alle fonti prima di fare affidamento sui dettagli.

| Approccio | Creatori o proprietario | Idea principale | Dimensione e forma |
|---|---|---|---|
| **Scaled Agile Framework (SAFe)** | Descritto per la prima volta nel libro di Dean Leffingwell del 2007 *Scaling Software Agility*; materiali pubblicati da Scaled Agile, Inc. | Un insieme di schemi organizzativi e di flusso di lavoro che attinge ad agile, sviluppo di prodotto lean e pensiero sistemico | Configurazioni dal livello di team e programma (Agile Release Train) fino a grandi soluzioni e portfolio |
| **Large-Scale Scrum (LeSS)** | Craig Larman e Bas Vodde | Scalare Scrum stesso: un Product Owner e un Product Backlog per un prodotto, molti feature team cross-funzionali, con il minor numero possibile di ruoli e artefatti aggiuntivi | LeSS per circa due-otto team; LeSS Huge per più, con Requirement Area di diversi team ciascuna |
| **Disciplined Agile (DA)** | Scott Ambler e Mark Lines; acquisito dal Project Management Institute (PMI) nell'agosto 2019 | Un toolkit di obiettivi di processo e opzioni che aiuta un team a scegliere il proprio modo di lavorare nel contesto | Ibrido e sensibile al contesto, con più cicli di vita e un livello per l'impresa |
| **Scrum@Scale e altri** | Nominati accanto a SAFe nell'articolo di Wikipedia | Ulteriori framework per coordinare più team Scrum | Vedi i siti dei proprietari |

### SAFe più in dettaglio

L'articolo di Wikipedia dice che SAFe fu descritto formalmente per la prima volta nel 2007, con un primo rilascio nel 2011 e la versione 6.0 nel marzo 2023. Per la versione 5.1 elenca quattro configurazioni: Essential SAFe (livello di team e programma), Large Solution SAFe, Portfolio SAFe e Full SAFe. L'articolo elenca anche dieci principi, tra cui adottare una visione economica e applicare il pensiero sistemico.

SAFe ha attirato critiche aperte, che l'articolo registra. Thoughtworks sostenne che il controllo dall'alto genera sprechi, Ken Schwaber lo criticò in un post del 2013 e Jeff Gothelf sostenne nel 2021 che SAFe non è agile. I critici lo definiscono gerarchico e rigido e dicono che possa dare a un'organizzazione l'apparenza di agilità mantenendo i vecchi processi. I sostenitori apprezzano il suo vocabolario comune e la sua struttura per le grandi organizzazioni. Leggi entrambe le parti prima di decidere.

### LeSS: scalare togliendo

Larman e Vodde descrivono LeSS come Scrum applicato a molti team che lavorano su un unico prodotto. Non aggiunge alcun livello sopra Scrum. Secondo l'introduzione del framework stesso, un Product Owner gestisce un Product Backlog e i team producono un prodotto rilasciabile in uno Sprint comune. LeSS enuncia un'idea di "more with less": meno ruoli, artefatti e regole producono team più responsabili. Per il metodo di base, vedi Argomento 1.4 — Previsioni di consegna e metriche di pianificazione.

### Disciplined Agile: scegli il tuo modo di lavorare

L'articolo di Wikipedia su Disciplined Agile Delivery descrive un toolkit ibrido che mette le persone al primo posto e copre l'intero ciclo di vita della consegna. Supporta sei cicli di vita e descrive 21 obiettivi di processo. L'approccio è aiutare i team a scegliere pratiche adatte alla loro situazione, invece di prescrivere un solo framework. L'articolo porta un avviso di manutenzione secondo cui potrebbe basarsi troppo su fonti vicine all'argomento.

### Scrum of Scrums e coordinamento semplice

Prima di adottare un framework, considera gli strumenti più semplici. Uno "scrum of scrums" riunisce rappresentanti di più team per condividere i progressi e risolvere le dipendenze. Una pianificazione trimestrale condivisa, un backlog comune per un prodotto e una riunione regolare dei responsabili di team sono altre opzioni leggere. Molte organizzazioni scalano abbastanza bene con questi.

### Scalare in un'organizzazione di servizio

In un'organizzazione IT i team possono essere organizzati in diversi modi, e la scelta incide su quanto bene l'agile scala:

| Organizzazione | Come sono organizzati i team | Effetto sulla scalatura |
|---|---|---|
| **Per componente** | Un team per livello tecnico o sistema | Le funzionalità richiedono più team, quindi le dipendenze sono molte |
| **Per funzionalità o prodotto** | Team cross-funzionali che possiedono una fetta rivolta al cliente | Meno dipendenze; servono standard condivisi per le piattaforme |
| **Per servizio** | Un team per servizio, che possiede build e run | Vicino alla gestione dei servizi; serve un modo per trattare le piattaforme condivise |
| **Piattaforma più flusso** | Team che forniscono una piattaforma e team che la usano | Servono accordi di servizio chiari tra loro |

Nessuno schema è il migliore per tutti. Passare da team per componente a team organizzati attorno a prodotti o servizi è un passo comune, ed è difficile da compiere, perché cambia chi risponde a chi.

### Che cosa dicono ricerca e critica

L'articolo sullo sviluppo software agile afferma che le prove empiriche a favore dei metodi agili in generale sono limitate e meno che conclusive. Per i framework di scalatura, le fonti consultate offrono per lo più opinioni e materiale dei fornitori. Tratta con cautela qualsiasi affermazione di miglioramento misurato, chiedi le prove che la sostengono e prova qualsiasi framework prima su una piccola parte della tua organizzazione.

## Buone pratiche

1. **Parti dal problema, non dal framework.** Dai un nome a ciò che non va: dipendenze lente, priorità in conflitto, integrazione tardiva. Scegli l'approccio più leggero che lo affronta e adottane di più solo se non basta.
2. **Prova prima il coordinamento più semplice.** Pianificazione condivisa, uno scrum of scrums e un backlog comune per ogni prodotto risolvono molti problemi a basso costo. Aggiungi struttura solo quando smettono di funzionare.
3. **Organizza i team attorno al valore.** Preferisci team che possiedono un prodotto o servizio end-to-end, con le competenze per costruirlo e gestirlo. Questo riduce passaggi e dipendenze e si accorda con il modo in cui ITIL pensa ai servizi (vedi Argomento 2.6 — La catena del valore del servizio).
4. **Mantieni un elenco ordinato per prodotto.** Avere un product backlog con un unico responsabile, come raccomanda LeSS, elimina gran parte del conflitto tra i team. Dove ciò non è possibile, rendi visibile l'ordine delle priorità tra i team.
5. **Pianifica insieme a un ritmo regolare.** Riunisci team e stakeholder chiave ogni pochi mesi per allinearsi su obiettivi, dipendenze e rischi. Mantieni l'evento breve e basato su prove ed evita di trasformarlo in una negoziazione su piani dettagliati.
6. **Integra in continuazione.** Testa insieme l'output di tutti i team il più spesso possibile, idealmente ogni giorno. L'integrazione tardiva è la ragione più comune per cui i grandi programmi sorprendono i loro sponsor (vedi Argomento 1.6 — Extreme Programming).
7. **Rendi visibili le dipendenze e riducile.** Elenca quali team aspettano quali e conta le attese. Riducile cambiando i confini dei team, condividendo competenze o costruendo piattaforme condivise con interfacce chiare.
8. **Definisci accordi di servizio tra i team.** Dove un team fornisce una piattaforma o un servizio a un altro, concorda che cosa ci si aspetta: disponibilità, risposta, orari di supporto e come chiedere modifiche (vedi Argomento 3.7 — Gestione dei livelli di servizio).
9. **Adatta e scrivi che cosa hai cambiato.** Qualunque framework adotti, registra quali parti segui, quali escludi e perché. Etichette oneste evitano la situazione in cui un ibrido è giudicato rispetto a un framework che non ha mai inteso seguire.
10. **Sperimenta prima di estendere.** Prova l'approccio con pochi team, misura i risultati che ti interessano e impara. Estendilo solo quando la sperimentazione mostra un beneficio che sai descrivere.
11. **Mantieni la governance leggera e basata sui risultati.** Chiedi prove come flusso di consegna, andamento degli incidenti e feedback degli utenti, e non rapporti di stato che ogni team scrive in un formato diverso (vedi Argomento 5.7 — Governance, rischio e conformità).
12. **Rivedi regolarmente la struttura.** Tieni una revisione una o due volte l'anno per chiederti se confini dei team, ruoli e cerimonie servono ancora il lavoro. Strutture giuste per 30 persone possono essere sbagliate per 300.

## Domande da discutere con il team

**Quale problema ci aspettiamo che la scalatura risolva, e come sapremo che è risolto?**

Chiedi alle persone di nominare il dolore: integrazione tardiva, priorità in conflitto, lunghe attese per altri team. Scrivi ciascuno con un esempio recente. Un framework scelto senza un problema dichiarato è una soluzione in cerca di un problema. Chi facilita può chiedere quale sarebbe la correzione più semplice possibile per ciascun problema e quali prove mostrerebbero che ha funzionato.

**Da quali altri team dipendiamo di più, e quanto aspettiamo?**

Mappa le dipendenze su una parete e aggiungi l'attesa tipica per ciascuna. I team che si credevano indipendenti spesso restano sorpresi. Chiedi quali dipendenze sono reali e quali derivano da confini storici tra team. Scegli una dipendenza da rimuovere, cambiando come sono organizzati i team o condividendo competenze.

**Chi decide l'ordine del lavoro tra i nostri team, e come lo scopriamo?**

Segui un recente conflitto di priorità dall'inizio alla risoluzione. Cerca escalation, riunioni e accordi informali. Chiedi se una singola persona responsabile, come in LeSS, potrebbe decidere. Considera che cosa si perderebbe o si guadagnerebbe. Un buon esito è una via chiara per decidere i conflitti, anche se non è un nuovo ruolo.

**Che cosa ci darebbe un framework come SAFe, LeSS o Disciplined Agile che non possiamo ottenere a minor costo?**

Chiedi a chi ha letto di ciascuno di spiegarlo in poche frasi e chiedi le critiche più forti. L'articolo di Wikipedia su SAFe ne elenca diverse e i siti dei proprietari dei framework elencano i benefici. Chi facilita dovrebbe mantenere la discussione pratica: che cosa faremmo lunedì se lo adottassimo e chi dovrebbe cambiare che cosa? Decidi che cosa provare, se qualcosa, e che cosa lasciare com'è.

**Come verifichiamo che il lavoro di tutti i nostri team combaci, e con quale frequenza?**

Conta i giorni tra una modifica di un team e il suo primo test con le modifiche di tutti gli altri. Intervalli più lunghi significano sorprese maggiori. Chiedi che cosa impedisce l'integrazione quotidiana, come ambienti, dati di test o responsabilità. Scegli una barriera da rimuovere.

**Quali dei nostri controlli si applicano a ogni team allo stesso modo, e quali dovrebbero dipendere dal rischio?**

Elenca i controlli standard, come revisioni, approvazioni e reporting. Chiedi quali di essi sono adattati al lavoro a basso rischio. I controlli uniformi sono facili da amministrare e lenti per tutti. I controlli che dipendono dal rischio richiedono criteri chiari. Scegli un controllo da rivedere.

## Nella pratica: un esempio di ITIL agile

Il gruppo IT di una grande banca al dettaglio ha 14 team di delivery e un gruppo operativo centrale. Ogni team ha adottato Scrum, ma i clienti della banca vedono pochi miglioramenti. I rilasci dell'app di mobile banking richiedono modifiche da cinque team, e ogni rilascio è coordinato da un ufficio di programma che traccia le dipendenze in un foglio di calcolo. Un rilascio recente è stato ritardato di tre settimane perché due team hanno scoperto all'ultimo minuto che le loro modifiche erano incompatibili.

Un architetto e il responsabile delle operations conducono uno studio su sei mesi di rilasci. Scoprono che la maggior parte dei ritardi deriva dall'integrazione tardiva e da priorità poco chiare tra i team che condividono un backlog di funzionalità mobile. Considerano di adottare un grande framework, ma decidono di partire in piccolo. Creano un unico backlog per l'app mobile con un product owner responsabile e uniscono la pianificazione dei cinque team in una sessione congiunta ogni sei settimane. Impostano una pipeline condivisa che compila e testa ogni notte insieme le modifiche di tutti i team e aggiungono il gruppo operativo alla sessione di pianificazione congiunta.

Dopo due trimestri, il numero di incompatibilità dell'ultimo minuto cala e i rilasci arrivano ogni due settimane. Alcuni problemi continuano. La product owner fatica con il volume di richieste e spende la maggior parte del tempo in arbitrati, e due team dipendono ancora da un team centrale di database con una lunga coda. La banca concorda di rendere visibile nella pianificazione congiunta la coda del team di database e di provare una via self-service per le modifiche comuni al database. Decide inoltre di rinviare qualsiasi decisione su un framework finché una seconda area di prodotto non avrà provato lo stesso approccio.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery portano la maggior parte del peso della scalatura: pianificazione condivisa, pipeline condivise e accordi con i vicini. Lavora per ridurre le dipendenze alla fonte, imparando le competenze del team vicino o costruendo interfacce che non richiedano coordinamento. Partecipa agli eventi di pianificazione con informazioni reali su progressi e rischi.

### Team di servizio e di operations

Il personale operativo dovrebbe far parte della pianificazione fin dall'inizio, perché molte dipendenze tra team sono operative: ambienti, accessi, monitoraggio e supporto. Porta dati di servizio alla sessione di pianificazione e concorda livelli di servizio con i team che dipendono da te. Sostieni piattaforme che diano ai team di delivery il self-service.

### Leadership e governance

I leader plasmano la struttura che decide quanto bene funziona la scalatura. Resisti alla tentazione di comprare un framework come sostituto del decidere che cosa l'organizzazione vuole essere. Chiedi una dichiarazione chiara del problema, una sperimentazione e prove. Mantieni leggero il reporting e accetta che i cambiamenti di struttura possano essere scomodi per i manager.

### Clienti e utenti

I clienti dovrebbero vedere un servizio coerente e non le cuciture tra i team. Aspettati un unico punto di contatto per un prodotto e una via chiara per le richieste. Di' al product owner che cosa conta di più e aspettati che la risposta includa compromessi tra richieste concorrenti.

## Modalità di fallimento comuni

- **Comprare un framework per evitare una decisione.** Un'organizzazione adotta un framework nella speranza che risolva i disaccordi sulle priorità. Decidi invece chi ha autorità sulle priorità e poi vedi quale framework, se ce n'è uno, aiuta.
- **Copiare un diagramma.** Si aggiungono ruoli e riunioni senza capirne le ragioni. Adotta invece solo gli elementi che affrontano un problema nominato.
- **Aggiungere livelli.** Coordinatori, uffici di programma e comitati si moltiplicano mentre i team perdono autonomia. Rimuovi invece le dipendenze così che ci sia meno da coordinare.
- **Integrazione tardiva.** I team integrano alla fine di un lungo ciclo. Integra e testa invece tutte le modifiche insieme ogni giorno.
- **Controlli uniformi.** Ogni team segue lo stesso processo pesante qualunque sia il rischio. Basa invece i controlli sul rischio e rendi veloci i percorsi a basso rischio.
- **Ignorare le operations.** La pianificazione include sviluppatori e product manager ma nessun addetto alle operations. Includi invece le operations nella pianificazione congiunta e condividi i dati di servizio.
- **Giudicare un ibrido rispetto al framework.** I critici dicono che non è il framework e i sostenitori dicono che lo è. Dai invece al tuo approccio un nome proprio e descrivilo.
- **Non rivedere mai la struttura.** I confini tracciati a 30 persone persistono a 300. Rivedi invece la struttura di team e ruoli almeno una volta l'anno.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Allineamento e priorità | Ogni team fissa le proprie priorità | Alcuni team condividono un backlog o si incontrano per allinearsi | I prodotti hanno un backlog ordinato e una pianificazione congiunta a un ritmo regolare | L'allineamento è verificato rispetto ai risultati e le dipendenze sono misurate | Le priorità sono aggiustate continuamente tra team, clienti e fornitori |
| Dipendenze | Le attese per altri team non sono gestite | Alcuni team elencano le proprie dipendenze | Le dipendenze sono visibili e tra i team esistono accordi | I tempi di attesa per le dipendenze sono misurati e ridotti | I confini dei team sono rimodellati dalle prove per rimuovere le dipendenze |
| Integrazione | L'integrazione avviene alla fine | Alcuni team integrano più spesso | Pipeline condivise integrano e testano di frequente le modifiche di tutti | I fallimenti di integrazione e le loro cause sono monitorati e corretti | Ambienti e test di integrazione sono condivisi e migliorati tra i team |
| Governance e struttura | I controlli sono uniformi e lenti | Esistono alcuni percorsi a basso rischio | I controlli variano in base al rischio con criteri chiari | Risultati ed efficacia dei controlli sono rivisti | Struttura e controlli sono rivisti e aggiustati abitualmente in tutta l'organizzazione |

## Checklist

- [ ] Sappiamo dire in una frase il problema che la scalatura dovrebbe risolvere.
- [ ] Abbiamo mappato le dipendenze tra i nostri team e conosciamo l'attesa tipica per ciascuna.
- [ ] Ogni prodotto ha un backlog ordinato con un responsabile.
- [ ] Team e stakeholder chiave pianificano insieme a un ritmo regolare.
- [ ] L'output di tutti i team è compilato e testato insieme almeno ogni giorno.
- [ ] I team che forniscono piattaforme o servizi ad altri hanno accordi di servizio scritti.
- [ ] Il personale operativo partecipa alla pianificazione tra team.
- [ ] I controlli variano in base al rischio e il percorso a basso rischio è rapido.
- [ ] Ogni framework che adottiamo è stato prima sperimentato su piccola scala.
- [ ] Abbiamo scritto quali parti di ogni framework seguiamo e quali no.
- [ ] La struttura di team e ruoli è rivista almeno una volta l'anno.

## Prompt per l'IA

**Scopo: mappare le dipendenze tra team da una descrizione del lavoro recente.**

```text
Help me understand the dependencies between teams in a recent delivery.

Teams involved: [list the teams and what each does].
Recent delivery: [describe a recent release or project that needed work from several teams, with approximate dates for when each team finished and what it waited for].

Using only what I wrote, produce a table of dependencies (which team waited on which, for what, and for roughly how long). Highlight the three longest waits. For each, suggest one way to reduce the dependency and one question to ask the teams. Do not invent durations. Ask me clarifying questions first if the description is thin, mark assumptions, and list what you are unsure of.
```

**Scopo: confrontare le opzioni di scalatura rispetto a un problema dichiarato.**

```text
Our problem: [describe in 3-5 sentences, with a recent example].
Number of teams and people: [numbers].
Our current coordination: [for example weekly meeting of team leads, a program office, none].

From the text I paste below, summarize what each of these approaches proposes: [paste short excerpts or summaries from the owners' public pages for the approaches you are considering, such as SAFe, LeSS, Disciplined Agile, or a simple scrum of scrums]. Use only the pasted text.

Then, for each approach, list which parts of our problem it addresses, what it would require of us, and what questions we should ask its owner. Do not state anything about an approach that is not in the pasted text. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: pianificare una sessione di pianificazione congiunta per più team.**

```text
Plan a half-day joint planning session for [number] teams working on [product or service].

Participants: [roles].
Inputs available: [for example each team's backlog, a list of dependencies, recent incident data].
Constraints: [for example people in different time zones].

Give a timed agenda that covers shared goals, dependencies, risks, and the plan for the next [period]. Include what each team brings, what the facilitator does, and a closing step that records agreed commitments and open questions. Keep it free of any particular tool. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: scrivere un accordo tra un team di piattaforma e i team che la usano.**

```text
Help me draft a one-page working agreement between a team that provides [platform or service] and the teams that use it.

What the platform team does today: [describe].
What the using teams need: [list, or write "unknown"].
Known constraints: [support hours, security rules, tools].

Draft sections for scope, how to request changes, availability and response expectations (leave numbers as [to be agreed] and do not invent them), how incidents are handled, and how the agreement is reviewed. Mark every item that is an assumption. Ask clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [scaled-agile-framework](../../../../skills/scaled-agile-framework/SKILL.md): da usare per comprendere ruoli, eventi e livelli di SAFe e giudicare quali parti servono.
- [large-scale-scrum](../../../../skills/large-scale-scrum/SKILL.md): da usare per applicare Scrum a più team che lavorano su un unico prodotto.
- [disciplined-agile](../../../../skills/disciplined-agile/SKILL.md): da usare per scegliere le pratiche per obiettivo di processo nel tuo contesto.
- [scrum-of-scrums](../../../../skills/scrum-of-scrums/SKILL.md): da usare come modo leggero per coordinare pochi team prima di adottare un framework.
- [portfolio-management](../../../../skills/portfolio-management/SKILL.md): da usare per decidere come vengono scelti e finanziati prodotti e iniziative.

## Fonti principali

- **Scaled agile framework** (Wikipedia): una panoramica di storia, configurazioni e critiche di SAFe con citazioni.
- **Introduction to LeSS** (less.works): la breve descrizione dei creatori di Large-Scale Scrum e della sua idea di "more with less".
- **Disciplined agile delivery** (Wikipedia): un riassunto del toolkit, dei suoi cicli di vita e dei suoi obiettivi.
- **Agile software development** (Wikipedia): la sezione sul lavoro su larga scala, offshore e distribuito e la discussione dei pareri contrastanti sui framework di scalatura.

## Riferimenti

1. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
2. Scaled agile framework — Wikipedia — https://en.wikipedia.org/wiki/Scaled_agile_framework
3. Disciplined agile delivery — Wikipedia — https://en.wikipedia.org/wiki/Disciplined_agile_delivery
4. LeSS framework introduction — Craig Larman and Bas Vodde, less.works — https://less.works/less/framework/introduction
5. Scrum (software development) — Wikipedia — https://en.wikipedia.org/wiki/Scrum_(software_development)
6. Project Management Institute — Wikipedia — https://en.wikipedia.org/wiki/Project_Management_Institute
7. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
