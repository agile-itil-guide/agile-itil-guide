# Il Manifesto Agile

**Il Manifesto per lo Sviluppo Agile del Software è un insieme di quattro brevi dichiarazioni di valore che dicono a un team che cosa privilegiare quando due cose buone tirano in direzioni opposte, e queste scelte contano tanto per gestire un servizio in produzione quanto per costruirlo.**

## Perché è importante

Il Manifesto Agile è la radice di quasi tutto il resto di questa guida. Scrum, Kanban, Extreme Programming e DevOps sono tutti modi di mettere in pratica i valori che esso enuncia. Se conosci solo le pratiche, copierai i rituali e perderai il ragionamento, e quando un rituale smette di funzionare non avrai nulla con cui orientarti.

Conta per la gestione dei servizi IT (ITSM) per una ragione pratica. La maggior parte dei team di oggi che gestiscono servizi li costruisce anche, e i due compiti tirano in direzioni diverse. Costruire premia il cambiamento e la velocità. Gestire premia la stabilità e la prevedibilità. Il Manifesto non elimina questa tensione, ma offre al team un modo condiviso per parlarne: quale valore stiamo privilegiando qui, e a che prezzo?

Aiuta anche sapere che cosa il Manifesto non è. Non è un processo, una certificazione o una promessa che seguirlo faccia riuscire i progetti. L'[articolo di Wikipedia sullo sviluppo software agile](https://en.wikipedia.org/wiki/Agile_software_development) osserva che le prove dei benefici dei metodi agili sono limitate e meno che conclusive. Considera il Manifesto come un insieme di ipotesi ben argomentate da mettere alla prova nel tuo contesto, non come un testo sacro.

## Concetti fondamentali

### Da dove viene

Diciassette professionisti si riunirono nella località sciistica di Snowbird, sui monti Wasatch dello Utah, dall'11 al 13 febbraio 2001, e scrissero insieme il Manifesto. Secondo il [resoconto su agilemanifesto.org](https://agilemanifesto.org/history.html), provenivano da metodi come Extreme Programming, Scrum e Crystal, e volevano un'alternativa ai processi pesanti, guidati dalla documentazione. L'etichetta "Light" era stata proposta e Alistair Cockburn vi si oppose, e il gruppo finì per chiamarsi Agile Alliance.

I firmatari erano Kent Beck, Mike Beedle, Arie van Bennekum, Alistair Cockburn, Ward Cunningham, Martin Fowler, James Grenning, Jim Highsmith, Andrew Hunt, Ron Jeffries, Jon Kern, Brian Marick, Robert C. Martin, Steve Mellor, Ken Schwaber, Jeff Sutherland e Dave Thomas. Parecchi di loro avevano già creato i metodi che portarono con sé: Beck e Cunningham lavoravano a [Extreme Programming](https://en.wikipedia.org/wiki/Extreme_programming), Schwaber e Sutherland a [Scrum](https://en.wikipedia.org/wiki/Scrum_(software_development)).

Il Manifesto fu una reazione a un modo di lavorare in cui un team pianifica l'intero progetto in anticipo, costruisce in lunghe fasi e scopre tardi se il risultato è voluto. Questo stile è spesso chiamato [modello a cascata](https://en.wikipedia.org/wiki/Waterfall_model). Gli autori non inventarono il lavoro iterativo (l'articolo di Wikipedia fa risalire i metodi iterativi e incrementali al 1957), ma gli diedero un nome condiviso e una breve dichiarazione di valori.

### I quattro valori

Il Manifesto enuncia i suoi valori per intero come segue. L'avviso di copyright ne consente la libera copia in qualsiasi forma, ma solo nella sua interezza, quindi qui è citato per intero:

> Stiamo scoprendo modi migliori di sviluppare software sviluppandolo e aiutando gli altri a fare lo stesso. Grazie a questa attività siamo arrivati a considerare importanti:
>
> **Gli individui e le interazioni** più dei processi e degli strumenti
> **Il software funzionante** più della documentazione esaustiva
> **La collaborazione col cliente** più della negoziazione dei contratti
> **Rispondere al cambiamento** più del seguire un piano
>
> Ovvero, benché apprezziamo gli elementi a destra, consideriamo più importanti quelli a sinistra.

Tre dettagli della formulazione sfuggono facilmente e cambiano il significato:

- **"Più di" non significa "invece di".** L'ultima frase dice che gli elementi a destra hanno comunque valore. Un team che abbandona ogni documentazione o ogni pianificazione ha frainteso il Manifesto.
- **È una preferenza per quando devi scegliere.** I valori non ti dicono che cosa fare ogni giorno. Ti dicono da che parte pendere quando un processo, un documento, un contratto o un piano ostacola un risultato migliore.
- **"Sviluppandolo."** La frase iniziale dice che gli autori hanno trovato questi valori attraverso la pratica. L'affermazione è empirica, ed è per questo che sei invitato a verificarla sulla tua esperienza.

### Leggere ogni valore per il lavoro sui servizi

I valori furono scritti a proposito dello sviluppo software. Ecco che cosa ciascuno può significare per un team che gestisce anche servizi.

| Valore | Da che cosa protegge | Che cosa può significare nel lavoro sui servizi |
|---|---|---|
| Gli individui e le interazioni più dei processi e degli strumenti | Un processo che funziona sulla carta ma che nessuno riesce a seguire sotto pressione | Durante un incidente maggiore, le persone che conoscono il sistema si parlano direttamente. Il processo di gestione degli incidenti sostiene quella conversazione e non la sostituisce. |
| Il software funzionante più della documentazione esaustiva | Documenti che descrivono un sistema che non esiste più | Un runbook collaudato dall'ingegnere reperibile che lo usa vale più di un lungo manuale che nessuno ha mai aperto. |
| La collaborazione col cliente più della negoziazione dei contratti | Discutere su un accordo sul livello di servizio (SLA) mentre il bisogno reale del cliente resta insoddisfatto | Rivedi regolarmente i livelli di servizio con i clienti e cambiali quando cambiano i loro bisogni. |
| Rispondere al cambiamento più del seguire un piano | Congelare un piano quando la situazione è ormai cambiata | Un processo di cambiamento che sa approvare in pochi minuti una modifica piccola e a basso rischio permette al team di rispondere. Un processo che tratta ogni modifica allo stesso modo non può. |

### I dodici principi

Il Manifesto è accompagnato da dodici principi che ne esplicitano i valori. Sono l'oggetto dell'argomento successivo (vedi Argomento 1.2 — I principi agili). Insieme, valori e principi sono talvolta chiamati mentalità agile.

### Critiche da conoscere

I critici hanno obiettato che il Manifesto mina la disciplina ingegneristica. L'articolo di Wikipedia cita Stephen Rakitin, che in una lettera a *IEEE Computer* definì l'agile "l'ennesimo tentativo di minare la disciplina dell'ingegneria del software" e lesse "il software funzionante più della documentazione esaustiva" come un permesso di saltare la documentazione. I difensori rispondono che la documentazione dovrebbe essere "appena abbastanza buona", espressione usata da Scott Ambler, e che troppo poca documentazione danneggia la manutenzione e la condivisione della conoscenza.

Per un team di servizio la critica ha fondamento. Il personale operativo eredita ciò che i team di sviluppo lasciano, e una documentazione scarsa si traduce in risposte lente agli incidenti e passaggi di consegne lunghi. Una lettura corretta del Manifesto è che la documentazione deve guadagnarsi il suo posto, non che non ne serva alcuna.

## Buone pratiche

1. **Tratta i valori come un aiuto alle decisioni, non come un insieme di regole.** Quando il team è in disaccordo, chiedi quale valore è in tensione e da che parte il team dovrebbe pendere. Così una discussione sulle preferenze diventa una conversazione sui compromessi.
2. **Leggi la frase che segue i valori.** Ricorda spesso al team che gli elementi a destra hanno ancora valore. Scrivi quali processi, documenti, contratti e piani mantieni e perché.
3. **Metti alla prova ogni valore con un evento recente.** Scegli un incidente o un rilascio reale e chiediti come sarebbe andato il lavoro se il team avesse pesato nell'altro senso. Le prove tratte dal tuo lavoro convincono più di una citazione.
4. **Mantieni la documentazione, e mantienila viva.** Preferisci documenti brevi, usati, collaudati e con un responsabile, come runbook e descrizioni dei servizi, a documenti lunghi scritti una volta sola. Elimina ciò che nessuno legge.
5. **Rendi routine la collaborazione con il cliente.** Tieni conversazioni regolari con chi usa i tuoi servizi e porta ciò che impari nel backlog. Non aspettare la revisione del contratto.
6. **Fai piani che prevedono di cambiare.** Pianifica su orizzonti brevi con punti di revisione espliciti. Mantieni una direzione di più lungo periodo e accetta che i passi verso di essa si spostino.
7. **Dai ai processi dei responsabili e lasciali evolvere.** Ogni processo del tuo sistema di gestione dei servizi dovrebbe avere un responsabile nominato e un modo per chi lo usa di proporre modifiche. Un processo che nessuno può cambiare verrà aggirato.
8. **Usa i valori nell'assunzione e nell'inserimento.** Descrivili ai nuovi arrivati con esempi del tuo team, perché vedano come emergono nelle scelte quotidiane.
9. **Rivisita i valori dopo la crescita.** Le organizzazioni più grandi scivolano verso processi e strumenti. Tieni una conversazione periodica, magari due volte l'anno, per chiederti se l'equilibrio serve ancora i clienti.
10. **Non usare il Manifesto come un'arma.** Citare "gli individui più dei processi" per liquidare la preoccupazione di un collega su audit o sicurezza chiude una conversazione che avrebbe dovuto iniziare. Usalo per aprire la discussione, non per vincerla.

## Domande da discutere con il team

**Quale dei quattro valori il nostro team privilegia già nella pratica, e quale sostiene soltanto di privilegiare?**

Inizia elencando le decisioni recenti: un rilascio ritardato per le scartoffie, una richiesta rifiutata perché non era nel contratto, un piano mantenuto dopo che aveva smesso di avere senso. Abbina ciascuna a un valore. I team spesso trovano un divario tra ciò che dicono e ciò che fanno, e il divario è il risultato utile. Chi facilita dovrebbe evitare le colpe e chiedere quale pressione ha prodotto ogni scelta. Prosegui chiedendo quali di queste pressioni il team può cambiare.

**Dove i nostri processi e strumenti aiutano le persone a parlarsi, e dove si mettono in mezzo?**

Chiedi alle persone di indicare un processo che fa risparmiare fatica e uno che ne fa spendere. Quello costoso è spesso un buon processo applicato rigidamente, come un flusso di ticket che richiede quattro approvazioni per una modifica banale. Cerca i punti in cui le persone evitano lo strumento e usano la chat o la conversazione in corridoio, perché di solito segnala un disallineamento. Chiudi con un processo da semplificare questo mese.

**Quale documentazione ci dispiacerebbe perdere, e quale potremmo eliminare domani?**

Questa domanda mette alla prova il valore "il software funzionante più della documentazione esaustiva" senza portarlo all'estremo. Chiedi alle persone quali documenti hanno usato nell'ultimo mese. Spesso emergono runbook, diagrammi di architettura e descrizioni dei servizi rivolte ai clienti. I documenti che nessuno nomina sono candidati all'eliminazione o alla fusione. Ricorda al team che eliminare è una decisione, quindi assegna un responsabile.

**Come partecipano i nostri clienti a dare forma ai nostri servizi, e come sappiamo che basta?**

Raccogli esempi di contributi dei clienti che hanno cambiato una decisione. Se l'elenco è breve, chiedi perché. Le cause sono di solito strutturali: un account manager nel mezzo, una revisione degli SLA una volta l'anno, o un service desk che registra i reclami ma non li inoltra. Se puoi, chiedi direttamente ai clienti che cosa cambierebbero. L'indicazione per chi facilita è cercare un modo concreto per accorciare il percorso tra un cliente e il team.

**Che cosa ci vorrebbe per approvare entro un'ora una modifica piccola e a basso rischio, e dovremmo farlo?**

Questa domanda collega il quarto valore al controllo dei cambiamenti (vedi Argomento 3.4 — Abilitazione dei cambiamenti). Chiedi che cosa rallenta oggi le modifiche piccole: una riunione settimanale, un modulo di rischio manuale, un test mancante. Chiedi quali prove metterebbero il team a proprio agio, come test automatici o un rollback rapido. Non spingere verso il "sì". Lo scopo è scoprire che cosa il team ritiene necessario, che è l'inizio di un piano.

**Se un'autorità di vigilanza, un auditor o un cliente importante leggesse il Manifesto, di che cosa si preoccuperebbe, e avrebbe ragione?**

Alcune preoccupazioni sono legittime. Gli auditor vogliono prove e i clienti vogliono impegni. Invita il team a prendere sul serio queste preoccupazioni e a chiedersi quali prove e impegni leggeri le soddisferebbero. I team che sanno mostrare come il lavoro agile produce una traccia di audit di solito ottengono più libertà, non meno. Registra le preoccupazioni per la discussione sulla governance nell'Argomento 5.7 — Governance, rischio e conformità.

## Nella pratica: un esempio di ITIL agile

Un rivenditore online di medie dimensioni ha un team di piattaforma di otto persone che costruisce e gestisce il servizio di checkout. Il team è passato da poco dai rilasci trimestrali a quelli settimanali, e ora ha un problema: il service desk si lamenta che le modifiche arrivano senza preavviso, e il team di piattaforma si lamenta che la riunione di approvazione delle modifiche impiega una settimana per approvare modifiche pronte il lunedì.

Il responsabile del team conduce una sessione di un'ora usando i quattro valori come cornice. Elencano gli eventi recenti su una parete. La correzione di un codice sconto ha atteso nove giorni per l'approvazione. Una modifica al database è stata approvata in fretta e ha causato un'interruzione. Un runbook per i fallimenti dei pagamenti si è rivelato descrivere un sistema dismesso l'anno prima. Il gruppo colloca ogni evento rispetto a un valore. La maggior parte dei casi di ritardo rientra in "i processi e gli strumenti più degli individui e delle interazioni", cioè il processo veniva eseguito per se stesso. L'interruzione rientra in "rispondere al cambiamento più del seguire un piano", perché la riunione di approvazione trattava ogni modifica allo stesso modo e non esaminava da vicino quella rischiosa.

Concordano tre cambiamenti. Primo, le modifiche che corrispondono a un breve elenco di schemi a basso rischio, con test automatici superati e un rollback collaudato, saranno preapprovate e registrate automaticamente. Secondo, le modifiche rischiose saranno riviste da un collega e da un rappresentante delle operations entro un giorno. Terzo, ogni runbook avrà un responsabile nominato e sarà verificato ogni volta che viene usato durante un incidente.

Due mesi dopo il responsabile rivede il risultato con il service desk. Le modifiche preapprovate scorrono rapide e il service desk ora vede ogni modifica in un feed condiviso. Resta un problema: due degli schemi preapprovati erano stati tracciati in modo troppo ampio, ed è seguito un incidente minore. Il team restringe gli schemi e mantiene l'approccio. Vede anche che il feed condiviso non sostituisce il parlarsi, quindi il responsabile del service desk si unisce alla pianificazione settimanale del team di piattaforma.

## Quattro prospettive

### Team di prodotto e di delivery

Per i team di delivery il Manifesto è un promemoria che il software funzionante include il funzionamento in esercizio. Una funzionalità che non può essere monitorata, supportata o annullata non è finita. Usa i valori per sostenere il lavoro operativo che rende sicuri i rilasci e invita presto il personale operativo alla pianificazione.

### Team di servizio e di operations

Il personale operativo spesso sente che il Manifesto parla per gli sviluppatori. Leggilo diversamente: i valori favoriscono persone che si parlano, artefatti collaudati e risposte rapide al cambiamento, tutte cose che si addicono a buone operations. Porta le pratiche ITIL al tavolo come esperienza accumulata su ciò che va storto e proponi versioni più leggere che ne conservino lo scopo.

### Leadership e governance

I leader creano le condizioni in cui i valori possono funzionare. Se ogni rilascio richiede cinque firme, un team non può privilegiare la risposta al cambiamento per quanti poster siano appesi al muro. Chiedi ai tuoi team dove le tue stesse regole li rallentano e sii pronto a cambiare una regola quando lo scopo può essere raggiunto in un altro modo.

### Clienti e utenti

I clienti sono nominati in due dei quattro valori. Per loro il Manifesto promette collaborazione, non solo consegna. Aspettati che ti venga chiesto di che cosa hai bisogno, di vedere spesso modifiche funzionanti e di poter cambiare idea. In cambio, un team ha bisogno da te di feedback e decisioni tempestivi.

## Modalità di fallimento comuni

- **Usare "più di" come "invece di".** I team abbandonano del tutto documentazione, pianificazione o contratti e poi ne soffrono. Decidi invece che cosa ciascuno di essi deve ottenere e mantieni la forma più leggera che lo ottiene.
- **Trattare i valori come una licenza a saltare la disciplina.** "Siamo agili" diventa una scusa per non testare, non registrare e non fare passaggi di consegne. Collega invece ogni valore a una pratica concreta e verifica che la pratica avvenga.
- **Recitare il Manifesto senza verificarlo.** Gli slogan sostituiscono il pensiero. Rivedi invece a intervalli regolari gli eventi reali rispetto ai valori.
- **Usarlo contro i colleghi.** Citare un valore per liquidare la preoccupazione di audit, sicurezza o operations danneggia la fiducia. Chiedi invece che cosa protegge quella preoccupazione e come soddisfarla in modo leggero.
- **Adottare le pratiche senza i valori.** Compaiono riunioni quotidiane e lavagne, ma le decisioni aspettano ancora catene di approvazione. Chiedi invece quali decisioni dovrebbero avvicinarsi a chi svolge il lavoro.
- **Presumere che il Manifesto risponda a domande operative.** Fu scritto nel 2001 a proposito dello sviluppo software e dice poco sulla gestione dei servizi. Combinalo invece con le pratiche di gestione dei servizi e adatta entrambi.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Comprensione condivisa dei valori | Poche persone hanno letto il Manifesto | Alcuni team ne discutono, con letture diverse | I team condividono una breve lettura scritta dei valori per il proprio contesto | I team verificano le decisioni recenti rispetto ai valori nelle revisioni periodiche | Team, fornitori e clienti usano un vocabolario comune dei compromessi |
| Equilibrio tra processo e persone | I processi sono seguiti o ignorati a seconda della persona | Alcuni processi sono semplificati dai singoli team | Ogni processo ha un responsabile e una via per le richieste di modifica | L'attrito dei processi è misurato, per esempio il tempo di attesa per modifica | I processi sono adeguati tra i team in base a prove condivise |
| Collaborazione con il cliente | Il feedback arriva sotto forma di reclamo | Alcuni team incontrano regolarmente i clienti | Ogni servizio ha un modo definito per raccogliere il contributo dei clienti | Il contributo dei clienti è tracciato e collegato alle modifiche fatte | I clienti aiutano a definire le priorità tra i servizi |
| Documentazione e piani | I documenti sono rari o obsoleti | I team mantengono i documenti che ritengono utili | I documenti richiesti sono pochi, con responsabile e rivisti | L'uso dei documenti è osservato e quelli inutilizzati sono rimossi | La documentazione è generata o verificata come parte della delivery |

## Checklist

- [ ] Ogni membro del team ha letto una volta il Manifesto e i suoi dodici principi.
- [ ] Il team sa enunciare ogni valore con parole proprie, con un esempio del proprio lavoro.
- [ ] Abbiamo elencato quali processi, documenti, contratti e piani manteniamo, e perché.
- [ ] Ogni processo in uso ha un responsabile nominato e un modo per proporre modifiche.
- [ ] Runbook e descrizioni dei servizi hanno responsabili e una data di revisione.
- [ ] Teniamo una conversazione regolare con i clienti di almeno un servizio.
- [ ] Abbiamo riesaminato almeno un incidente o rilascio recente rispetto ai quattro valori.
- [ ] Le regole della leadership che rallentano il team sono state elencate e discusse.
- [ ] Abbiamo scritto come mostreremo agli auditor e alle autorità di vigilanza ciò che facciamo.

## Prompt per l'IA

**Scopo: trasformare i quattro valori in una breve lettura per il tuo team.**

```text
You are helping a team of [team size and type, e.g. "eight engineers who build and run a payments service"] write a plain-language reading of the four values of the Agile Manifesto for their own context.

Here are the four values as written:
- Individuals and interactions over processes and tools
- Working software over comprehensive documentation
- Customer collaboration over contract negotiation
- Responding to change over following a plan

Context about our team and work: [paste 3-5 sentences about what you build, what you run, who your customers are, and any rules you must follow, such as audit or safety rules].

For each value, write two or three sentences on what it could mean for us, and one example drawn only from the context above. Mark clearly any point where you are guessing. Ask me up to three clarifying questions first if the context is too thin. Do not invent statistics or quote sources. List what you are unsure of.
```

**Scopo: riesaminare un evento recente rispetto ai valori.**

```text
Below is a short description of a recent event in our team (an incident, a release, or a delayed change). Help me review it against the four values of the Agile Manifesto.

Event: [paste a factual description of what happened, in order, without blaming anyone].

For each value, say whether the event shows the team leaning toward the value on the left, toward the item on the right, or neither, and explain your reasoning in two sentences. Then suggest up to three questions our team could discuss. Separate what you can see in the text from what you are assuming, and list what you are unsure of.
```

**Scopo: prepararsi a rispondere alla preoccupazione di un auditor sui modi di lavorare agili.**

```text
I need to explain to an auditor how our agile team keeps adequate records. The auditor's concern is: [paste the concern, e.g. "no evidence of who approved changes"].

Our current practice is: [describe what you do now: tools, reviews, approvals, where records are kept].

List what evidence our current practice already produces, what gaps the auditor might notice, and three lightweight ways to close each gap without adding a heavy manual process. Do not state that any law, standard, or regulation requires something unless I have pasted its text above. List your assumptions and what you are unsure of at the end.
```

**Scopo: progettare una sessione di un'ora per il team sul Manifesto.**

```text
Design a one-hour facilitated session for a team of [number] people on the Agile Manifesto. The team works on [services or products] and its biggest current frustration is [frustration].

Include: a five-minute opening, a 20-minute activity where the team matches recent real events to the four values, a 20-minute discussion of two or three of the six questions below, and a 10-minute close with one agreed action.

Questions available: [paste the questions you want to use from the "Questions to discuss" section].

Give a timed agenda, what the facilitator says, and what to watch for. Keep it practical and do not assume any tool. Ask clarifying questions if information is missing, and list what you are unsure of.
```

## Competenze per l'IA

- [agile-principles](../../../../skills/agile-principles/SKILL.md): da usare quando vuoi verificare una pratica del team o una decisione di processo rispetto ai principi del Manifesto.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): da usare per condurre una retrospettiva che riesamina gli eventi recenti rispetto ai valori e porta a un cambiamento reale.
- [agile-liftoff](../../../../skills/agile-liftoff/SKILL.md): da usare quando avvii un nuovo team o progetto e vuoi una lettura condivisa dei valori fin dal primo giorno.
- [agile-coaching](../../../../skills/agile-coaching/SKILL.md): da usare quando sei la persona che aiuta un team a passare dal copiare i rituali al comprenderne le ragioni.

## Fonti principali

- **Manifesto for Agile Software Development** (agilemanifesto.org): il testo primario. Leggilo per intero; richiede due minuti.
- **Principles behind the Agile Manifesto** (agilemanifesto.org): i dodici principi, il compagno più utile dei valori.
- **History: The Agile Manifesto** (agilemanifesto.org): il breve resoconto degli autori stessi sull'incontro di Snowbird.
- **Agile software development** (Wikipedia): una panoramica ampia con storia, metodi, pratiche e critiche, utile come mappa per ulteriori letture.

## Riferimenti

1. Manifesto for Agile Software Development — Beck et al., agilemanifesto.org — https://agilemanifesto.org/
2. Principles behind the Agile Manifesto — Beck et al., agilemanifesto.org — https://agilemanifesto.org/principles.html
3. History: The Agile Manifesto — Jim Highsmith for the Agile Alliance, agilemanifesto.org — https://agilemanifesto.org/history.html
4. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
5. Extreme programming — Wikipedia — https://en.wikipedia.org/wiki/Extreme_programming
6. Scrum (software development) — Wikipedia — https://en.wikipedia.org/wiki/Scrum_(software_development)
7. Waterfall model — Wikipedia — https://en.wikipedia.org/wiki/Waterfall_model
8. Manifesto for Agile Software Development — Wikipedia — https://en.wikipedia.org/wiki/Manifesto_for_Agile_Software_Development
9. Agile Alliance — Wikipedia — https://en.wikipedia.org/wiki/Agile_Alliance
10. Snowbird, Utah — Wikipedia — https://en.wikipedia.org/wiki/Snowbird,_Utah
