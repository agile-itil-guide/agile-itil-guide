# Previsioni di consegna e metriche di pianificazione

**Le previsioni di consegna e le metriche di pianificazione permettono a un team di dire, con intervalli onesti, quando è probabile che il lavoro finisca e quanto può assumersene, osservando il flusso continuo del lavoro concluso e la capacità del team, e funzionano per i team di servizio quando il lavoro pianificato e quello guidato dalle interruzioni vengono contati insieme.**

## Perché è importante

I team agili puntano alla consegna continua di software, e chiunque dipenda da quella consegna pone le stesse domande: quando sarà finito, quanto può assumersi il team e che cosa succede quando arriva qualcosa di urgente? Un team che non sa rispondere a queste domande con prove ripiega su promesse che non può mantenere, e chi dipende da lui impara a diffidare di ogni data.

Un team che gestisce servizi lo avverte più acutamente della maggior parte degli altri. Il lavoro di miglioramento pianificato, le richieste di servizio e gli incidenti condividono le stesse persone. Un piano che ignora la parte non pianificata fallirà la prima settimana in cui arriva un incidente. Una previsione che nasce dalla storia del team stesso e ne dichiara l'intervallo sopravvive meglio al contatto con la realtà di una data che nasce dalla speranza.

Questo argomento descrive come prevedere a partire dal flusso del lavoro concluso, come pianificare in base alla capacità del team e quali metriche di pianificazione aiutano o ingannano. Scrum, gli sprint e la velocity sono un modo di pianificare; una breve sezione verso la fine li tratta per i team che li usano. Le misure qui presentate si basano sulle misure di flusso dell'Argomento 1.5 — Kanban e sulle indicazioni più ampie sulla misurazione dell'Argomento 5.6 — Metriche e misurazione.

## Concetti fondamentali

### Prevedere dal flusso, non dalle promesse

Una previsione è un'affermazione sul futuro basata su prove del passato, e comporta incertezza. La Kanban Guide definisce un'aspettativa di livello di servizio come una previsione di quanto tempo dovrebbe impiegare un elemento di lavoro a percorrere il flusso di lavoro, basata sui cycle time passati, e dice che non è un accordo. Quella definizione è un buon modello per ogni previsione di consegna: usa storia reale, di' che cosa copre ed evita di promettere più di quanto hai misurato (vedi Argomento 1.5 — Kanban).

Sono comuni due tipi di previsione:

- **Quanto tempo richiederà un singolo elemento?** Guarda quanto hanno impiegato elementi simili già conclusi e indica un intervallo o un'affermazione come "la maggior parte degli elementi di questo tipo si conclude entro un dato numero di giorni".
- **Quanto avremo finito entro una data, o quando si concluderà un insieme di elementi?** Guarda quanti elementi il team conclude di solito in un periodo e applica quell'intervallo al lavoro che resta.

### Le misure di flusso dietro una previsione

La Kanban Guide definisce quattro misure, ed esse sono la materia prima della previsione di consegna:

| Misura | Che cosa ti dice | Come alimenta una previsione |
|---|---|---|
| **Cycle time** | Quanto tempo ha impiegato un elemento concluso dall'inizio alla fine | La dispersione dei cycle time recenti dà un intervallo per quanto richiederà un nuovo elemento |
| **Throughput** | Quanti elementi sono stati conclusi in un periodo | L'intervallo del throughput recente dà un intervallo per quanto si concluderà in un periodo futuro |
| **Lavoro in corso (WIP)** | Quanti elementi sono iniziati ma non conclusi | Troppo WIP allunga i cycle time e rende ogni previsione meno affidabile |
| **Età dell'elemento di lavoro** | Da quanto tempo un elemento non concluso è in corso | Mostra gli elementi già più vecchi della maggior parte di quelli conclusi, quando c'è ancora tempo per agire |

La guida nota che i team possono rinominare queste misure e dovrebbero aggiungerne altre dove utile, e che le misure contano solo quando informano il modo di lavorare del team. Usa percentili e intervalli, non solo medie, perché le code lunghe si nascondono nelle medie (vedi Argomento 5.6 — Metriche e misurazione).

### Un semplice metodo di previsione

Un team può prevedere senza strumenti speciali:

1. Raccogli il throughput di ciascuna delle ultime otto-dodici settimane, o periodi simili, da elementi realmente conclusi.
2. Prendi il più basso, uno tipico e il più alto di questi valori.
3. Dividi il numero di elementi rimanenti per ciascun valore per ottenere un intervallo di periodi per concludere.
4. Indica l'intervallo, i dati da cui deriva e che cosa lo cambierebbe, come nuovo lavoro, un cambiamento nel team o una dipendenza.

È una regola empirica, non uno standard. Presuppone che il lavoro futuro assomigli a quello passato e che gli elementi abbiano dimensioni all'incirca simili. Quando ciò è falso, dillo e considera l'intervallo più ampio. Confronta ogni previsione con ciò che è accaduto e adatta il metodo, come consiglia l'Argomento 3.11 — Disponibilità, capacità e prestazioni per le previsioni di domanda.

### Capacità del team

La capacità è quanto lavoro un team può assorbire in un periodo. Per un team di delivery non è il numero di persone moltiplicato per i giorni del periodo. Ferie, compiti di supporto, riunioni e lavoro non pianificato riducono tutti ciò che è disponibile per gli elementi pianificati. Una buona dichiarazione di capacità elenca persone e giorni disponibili, poi sottrae una quota riservata al lavoro non pianificato, in base a ciò che hanno mostrato gli ultimi periodi.

La competenza capacity-planning e l'Argomento 3.11 — Disponibilità, capacità e prestazioni descrivono la capacità per servizi e infrastruttura. La stessa logica vale per un team: pianifica con intervalli, verifica rispetto a ciò che è accaduto e rivedi il piano quando i fatti cambiano.

### Lavoro pianificato e non pianificato insieme

I team di servizio ricevono incidenti, richieste urgenti e modifiche che nessuno aveva programmato. Se non vengono contati, la previsione per il lavoro pianificato sarà troppo ottimistica. Dai al lavoro non pianificato i suoi tipi di elemento, conta quanti ne arrivano e quanto tempo richiedono, e tieni i dati accanto al lavoro pianificato. Questo dà anche al Product Owner o al responsabile del servizio prove su quali incidenti ricorrenti consumano capacità, il che sostiene le decisioni di correggere le cause (vedi Argomento 3.3 — Gestione dei problemi).

### Flusso di consegna continua e cadenza dei rilasci

I team che consegnano in modo continuo rilasciano piccole modifiche quando sono pronte, invece di aspettare la fine di un periodo di pianificazione. Questo accorcia il tempo tra la conclusione e la consegna e rende le previsioni più semplici da verificare: ogni elemento concluso è un punto dati. Le modifiche seguono comunque l'approccio di abilitazione dei cambiamenti dell'organizzazione, e le modifiche standard preautorizzate aiutano in questo (vedi Argomento 3.4 — Abilitazione dei cambiamenti e Argomento 3.5 — Gestione di rilasci e deployment).

### Se usi Scrum, sprint e velocity

Alcuni team pianificano in cicli di lunghezza fissa. La Scrum Guide 2020, di Ken Schwaber e Jeff Sutherland, definisce Scrum come un framework leggero per soluzioni adattive a problemi complessi. I suoi eventi avvengono all'interno dello Sprint, un timebox di un mese o meno. Questa sezione copre il minimo necessario a un team che li usa; leggi la guida stessa prima di cambiare il modo di lavorare di un team.

- **Sprint e Sprint Goal:** lo Sprint è il timebox e lo Sprint Goal è l'unico obiettivo per esso. Un obiettivo che una persona esterna al team può capire guida le scelte meglio di un elenco di ticket.
- **Product Backlog, Product Owner e Scrum Master:** il Product Backlog è un elenco ordinato di ciò di cui il prodotto ha bisogno. Il Product Owner è l'unica persona responsabile del suo ordine, e lo Scrum Master è responsabile di stabilire Scrum e di aiutare il team ad applicarlo.
- **Incremento e Definition of Done:** un Incremento è un passo utilizzabile e verificato verso il Product Goal, e la Definition of Done è lo standard di qualità che il lavoro deve soddisfare per contare. Un team di servizio può includervi monitoraggio, un runbook e un rollback collaudato.
- **Eventi:** Sprint Planning, Daily Scrum, Sprint Review e Sprint Retrospective. La retrospettiva è il momento in cui il team esamina come ha lavorato e pianifica i miglioramenti (vedi Argomento 6.1 — Conversazioni di team).
- **Velocity:** un valore basato sulle stime che alcuni team usano per pianificare quanto lavoro assumersi. Usalo solo per la pianificazione del team stesso. Se diventa un obiettivo, i team gonfiano le stime, quindi preferisci le misure di flusso, che contano gli elementi conclusi, e le misure di risultato.

La guida dice che Scrum è un framework, non un metodo completo. Non copre la risposta agli incidenti, i livelli di servizio o il processo di cambiamento, e usarne solo parti non rende il risultato Scrum. Se lo adatti, dai alla variazione un nome onesto. Un misto di eventi Scrum e flusso Kanban è talvolta chiamato [Scrumban](https://en.wikipedia.org/wiki/Scrumban).

## Buone pratiche

1. **Prevedi dalla tua storia.** Usa i cycle time e il throughput degli elementi conclusi di recente e indica il periodo coperto dai dati. Non prendere in prestito numeri da un altro team.
2. **Dai un intervallo, non una data singola.** Mostra un caso basso, uno tipico e uno alto e di' che cosa sposterebbe il risultato. Una data senza intervallo promette una certezza che non hai.
3. **Conta il lavoro non pianificato.** Registra incidenti, richieste urgenti e interruzioni come elementi di lavoro con i propri tipi. Misura quanti ne arrivano e quanto tempo richiedono.
4. **Fissa la capacità dai dati.** Elenca persone e giorni disponibili, sottrai ferie e compiti di supporto e riserva una quota al lavoro non pianificato in base ai periodi recenti. Rivedi la quota con regolarità.
5. **Limita il lavoro in corso.** Troppo lavoro avviato allunga i cycle time e indebolisce ogni previsione. Fissa un limite e rivedilo quando i dati cambiano (vedi Argomento 1.5 — Kanban).
6. **Osserva ogni giorno l'età degli elementi di lavoro.** L'età mostra i guai negli elementi non conclusi quando c'è ancora tempo per agire. Rivedi per primi gli elementi più vecchi.
7. **Usa percentili e distribuzioni.** Di' che la maggior parte degli elementi di un tipo si conclude entro un certo numero di giorni e mostra la coda lenta. Le medie la nascondono.
8. **Confronta le previsioni con i consuntivi.** Dopo ogni periodo, registra che cosa era previsto e che cosa è accaduto. Adatta il metodo, non solo il numero.
9. **Tieni le stime per pianificare, non per giudicare.** Se il team stima gli elementi, usa i valori per la propria pianificazione e non classificare persone o team in base a essi (vedi Argomento 5.6 — Metriche e misurazione).
10. **Rendi le previsioni visibili a chi ne dipende.** Condividi l'intervallo e le ipotesi con clienti e stakeholder e aggiornali quando i fatti cambiano.
11. **Porta il lavoro di miglioramento nello stesso flusso.** Metti correzioni dei problemi, lavoro di monitoraggio e automazione accanto alle funzionalità, così che i compromessi siano visibili (vedi Argomento 3.15 — Miglioramento continuo).
12. **Se usi sprint e velocity, mantienili piccoli e onesti.** Concorda quali parti di Scrum segui, dai un nome alla variazione e prova un approccio basato sul flusso se dominano le interruzioni.

## Domande da discutere con il team

**Come rispondiamo oggi a "quando sarà finito?", e su che cosa si basa la risposta?**

Chiedi le ultime tre risposte date dal team e su che cosa si basava ciascuna. Confrontale con ciò che è accaduto. I team spesso scoprono che le date venivano dalla speranza o dall'opinione della persona più anziana. Prosegui chiedendo quale storia il team potrebbe usare al suo posto.

**Quale quota del nostro tempo va in lavoro che nessuno aveva pianificato, e lo sappiamo dai dati?**

Conta elementi pianificati, richieste urgenti e incidenti nelle ultime settimane. Chi facilita può chiedere se la quota è stabile o varia con la stagione, e chi decide quando un'interruzione prevale sul lavoro pianificato. Concordate come registrarlo d'ora in poi.

**Che aspetto hanno i nostri cycle time, e che cosa diremmo se un cliente chiedesse quanto richiede una richiesta tipica?**

Traccia o elenca i cycle time degli ultimi elementi conclusi. Chiedi quanto richiede la maggior parte, quanto richiedono i più lenti e che cosa spiega quelli lenti. Discuti se un'aspettativa di livello di servizio basata su questa storia sarebbe equa e chi dovrebbe ascoltarla.

**Quali dei nostri elementi attuali sono già più vecchi della maggior parte di quelli conclusi?**

Guarda gli elementi aperti più vecchi. Chiedi perché ciascuno è fermo, chi può sbloccarlo e che cosa farà il team oggi. Concludi decidendo con quale frequenza il team rivedrà l'età.

**Quando una nostra previsione si è rivelata sbagliata per l'ultima volta, e che cosa abbiamo cambiato dopo?**

Chiedi un esempio recente, la previsione e l'esito. Cerca ciò che la previsione ha mancato: lavoro non pianificato, una dipendenza o elementi più grandi del previsto. Concorda un cambiamento al metodo e come il team lo verificherà.

**Se usiamo sprint o velocity, che cosa fanno per noi, e che cosa perderemmo se li abbandonassimo?**

Chiedi onestamente quale problema risolve ciascuno. Cerca prove, come una migliore concentrazione o obiettivi più chiari, e danni, come stime gonfiate o interruzioni ignorate. Chi facilita dovrebbe fare attenzione a qualsiasi cambiamento che elimini i cicli di feedback, che sono le parti utili. Concorda un esperimento e come confrontare i risultati.

## Nella pratica: un esempio di ITIL agile

Il reparto IT di un ospedale regionale ha un team di sette persone che mantiene l'applicazione di prenotazione dei pazienti. I responsabili degli ambulatori chiedono date, e il team le ha date. La maggior parte delle date è mancata, perché incidenti dai reparti, richieste dagli ambulatori e patching di sicurezza continuano ad arrivare, e il team passa la maggior parte dei giorni su di essi.

Il responsabile del team comincia a registrare ogni elemento, pianificato o no, con le date di inizio e fine. Dopo otto settimane i dati mostrano che circa metà del tempo del team va in lavoro non pianificato e che la maggior parte degli elementi pianificati si conclude in meno di due settimane, con una lunga coda di elementi in attesa di un altro team. Il team concorda tre cambiamenti. Indicherà ogni previsione come intervallo, usando throughput e cycle time recenti. Riserverà metà della sua capacità al lavoro non pianificato e pianificherà solo sul resto. Rivedrà ogni mattina gli elementi aperti più vecchi.

Nei due mesi successivi le previsioni sono per lo più giuste, e i responsabili degli ambulatori, che ora vedono un intervallo e le sue ipotesi, pianificano di conseguenza. Il responsabile del servizio, un dirigente delle operazioni ambulatoriali, può vedere quali incidenti ricorrenti consumano capacità e alza la priorità di una correzione per un guasto ricorrente della sincronizzazione degli appuntamenti; il guasto cessa. Restano difficoltà. Un incidente maggiore sposta ancora parte del lavoro, e i responsabili a cui piacevano le risposte rapide del vecchio assetto trovano gli intervalli meno soddisfacenti. Il team concorda di dire loro che cosa è cambiato nella previsione ogni volta che si sposta e di confrontare il proprio approccio con un metodo a cicli fissi per il lavoro di miglioramento alla prossima revisione.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery traggono il massimo vantaggio dal prevedere con i propri dati di flusso. Registra il lavoro quando inizia e finisce, limita il lavoro in corso e rilascia piccole modifiche in continuo. Condividi l'intervallo con chi aspetta e usa la Definition of Done, se ne hai una, per includere il lavoro operativo che rende un rilascio supportabile.

### Team di servizio e di operations

I team operativi possiedono il lavoro non pianificato che fa fallire le previsioni. Registra incidenti, richieste e modifiche come elementi di lavoro e condividi gli schemi ricorrenti perché influenzino l'ordine del lavoro. Usa i dati di cycle time per fissare aspettative realistiche con i clienti e sii esplicito su quanta capacità va al miglioramento pianificato.

### Leadership e governance

I leader ottengono un quadro più onesto da intervalli di previsione e misure di flusso che dai rapporti di stato. Chiedi intervalli con le loro ipotesi, l'accuratezza delle previsioni nel tempo e ciò che il team ha cambiato grazie ai dati. Evita di fissare obiettivi sui singoli numeri, il che produce giochi di prestigio, e accetta che una previsione si sposti quando si spostano i fatti.

### Clienti e utenti

Clienti e utenti traggono beneficio da aspettative più chiare e meno date mancate. Chiedi al team il tempo atteso per il tuo tipo di richiesta e aspettati che poggi sulla storia. Se la tua richiesta è urgente, aspettati che ti si chieda perché, perché anticiparla incide sul lavoro di tutti gli altri.

## Modalità di fallimento comuni

- **Promettere date per speranza.** Le date vengono dall'opinione e sono mancate. Prevedi invece dagli elementi conclusi di recente e mostra l'intervallo.
- **Ignorare il lavoro non pianificato.** Le interruzioni distruggono il piano a ogni periodo. Contale invece come elementi di lavoro e riserva capacità in base ai dati.
- **Previsioni a numero singolo.** Una sola data nasconde l'incertezza. Dai invece un caso basso, uno tipico e uno alto con le ipotesi.
- **Usare solo le medie.** La lunga coda degli elementi lenti resta nascosta. Usa invece percentili e distribuzioni.
- **Avviare troppo.** Un alto lavoro in corso allunga ogni cycle time. Limitalo invece e concludi prima di iniziare.
- **Usare velocity o throughput come obiettivo di prestazione.** I team gonfiano le stime o spezzano gli elementi per fare bella figura. Usa invece i valori per pianificare e giudica i risultati (vedi Argomento 5.6 — Metriche e misurazione).
- **Non verificare mai la previsione.** Il metodo non migliora mai. Confronta invece ogni previsione con ciò che è accaduto.
- **Applicare cicli fissi a lavoro che non si adatta.** Una coda di richieste imprevedibili forzata in periodi fissi crea frustrazione. Prova invece un approccio basato sul flusso e confronta i risultati.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Previsione | Le date vengono dall'opinione | Alcuni team usano dati passati | I team prevedono come intervalli dai propri dati di flusso | L'accuratezza delle previsioni è monitorata e il metodo migliorato | Le previsioni sono coordinate tra team e fornitori |
| Misure di flusso | Si raccolgono poche misure | Alcuni team registrano cycle time o throughput | Le quattro misure di flusso sono raccolte in modo coerente | Le misure sono riviste e usate per fissare le aspettative | I dati di flusso sono condivisi tra i team e usati per pianificare insieme |
| Capacità e lavoro non pianificato | Le interruzioni non sono contate | Alcuni team tracciano il lavoro non pianificato | La capacità per il lavoro non pianificato è fissata dai dati | La quota e le cause del lavoro non pianificato sono riviste e ridotte | I team operativi e di delivery pianificano insieme la capacità |
| Uso di stime e cicli fissi | Le stime sono usate per giudicare le persone | Alcuni team usano le stime per la propria pianificazione | I team concordano quali pratiche usano e nominano le variazioni | Gli effetti delle pratiche sono rivisti rispetto a flusso e risultati | Le pratiche sono adeguate tra i team da un apprendimento condiviso |

## Checklist

- [ ] Le previsioni vengono dalla storia degli elementi conclusi del team stesso.
- [ ] Ogni previsione è un intervallo con ipotesi dichiarate.
- [ ] Incidenti, richieste e lavoro di miglioramento sono tutti registrati come elementi di lavoro.
- [ ] La capacità per il lavoro non pianificato è fissata dai dati e rivista.
- [ ] Cycle time, throughput, lavoro in corso ed età degli elementi di lavoro sono monitorati.
- [ ] Il lavoro in corso ha un limite che il team rivede.
- [ ] Gli elementi aperti più vecchi sono rivisti regolarmente.
- [ ] Le previsioni sono confrontate con i consuntivi dopo ogni periodo.
- [ ] Stime e velocity, se usate, non sono obiettivi.
- [ ] Ogni uso di Scrum, sprint o di una variazione è scritto e nominato onestamente.

## Prompt per l'IA

**Scopo: costruire un intervallo di previsione dai tuoi dati di throughput.**

```text
Help me forecast delivery for a team of [number and type of people].

Throughput (items finished) for each of the last [number] weeks: [paste the real figures as a list].
Items remaining: [number], and a note on how similar in size they are: [paste].
Known changes that may affect the next weeks (leave, new work, dependencies): [paste, or write "none known"].

Calculate the lowest, typical, and highest weekly throughput from the figures, and divide the remaining items by each to give a range of weeks. State the assumptions. Do not extrapolate beyond the data or invent numbers. If the data are too thin, say so and ask what to add. List what you are unsure of.
```

**Scopo: analizzare i cycle time e proporre un'aspettativa di livello di servizio.**

```text
Below are the start and finish dates of the last [number] finished work items of type [type]: [paste as a table; use only real data].

Calculate the cycle time of each item. Describe the spread: what most items take, what the slowest take, and what might explain the slow ones. Suggest a service level expectation in the form "most items of this type finish within N days", and say how confident the data allow us to be. Do not state it as a promise. If the data are too few, say so and ask what to collect. List what you are unsure of.
```

**Scopo: misurare quanta capacità va al lavoro non pianificato.**

```text
Below is a list of the work items our team completed over the last [number] weeks, each marked as planned or unplanned, with the time it took: [paste as a table; use only real data].

Calculate the share of time on planned and unplanned work for each week, using only the numbers I gave. Describe the pattern, suggest what share of capacity to hold back for unplanned work, and name two assumptions behind the suggestion. Ask clarifying questions first if the data are thin, and list what you are unsure of.
```

**Scopo: rivedere gli elementi aperti più vecchi e pianificare lo sblocco.**

```text
Our open work items, with start dates and current state: [paste as a table; use only real data].
Cycle times of our last [number] finished items: [paste].

Calculate the current age of each open item and flag those older than most finished items. For each flagged item, suggest two questions to ask about what blocks it. Do not guess the cause. List what you are unsure of.
```

## Competenze per l'IA

- [kanban](../../../../skills/kanban/SKILL.md): da usare per impostare misure di flusso, limiti al lavoro in corso e un'aspettativa di livello di servizio.
- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): da usare per verificare se la capacità disponibile soddisfa la domanda prevista e che cosa fare in caso di divario.
- [demand-forecasting](../../../../skills/demand-forecasting/SKILL.md): da usare per stimare il carico futuro come intervallo da dati passati e piani di business.
- [software-engineering-metrics](../../../../skills/software-engineering-metrics/SKILL.md): da usare per scegliere una metrica, nominarne il vettore di manipolazione e il guardrail e compilare una carta delle metriche.
- [scrum](../../../../skills/scrum/SKILL.md): da usare se il team pianifica in sprint, per impostare o rivedere ruoli, eventi e artefatti.

## Fonti principali

- **The Kanban Guide** (kanbanguides.org): definisce le misure di flusso e l'aspettativa di livello di servizio come previsione basata sui cycle time passati.
- **The Scrum Guide** (Ken Schwaber e Jeff Sutherland, scrumguides.org): la definizione autorevole e breve di Scrum, per i team che usano gli sprint.
- **Kanban (development)** (Wikipedia): una panoramica delle misure di flusso e del sistema pull di Kanban.
- **Scrum (software development)** (Wikipedia): una panoramica di storia, ruoli, eventi e critiche di Scrum.

## Riferimenti

1. The Kanban Guide — John Coleman, Daniel Vacanti, and contributors, kanbanguides.org — https://kanbanguides.org/english/
2. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
3. The Scrum Guide (November 2020) — Ken Schwaber and Jeff Sutherland, scrumguides.org — https://scrumguides.org/scrum-guide.html
4. Scrum (software development) — Wikipedia — https://en.wikipedia.org/wiki/Scrum_(software_development)
5. Scrumban — Wikipedia — https://en.wikipedia.org/wiki/Scrumban
6. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
7. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
