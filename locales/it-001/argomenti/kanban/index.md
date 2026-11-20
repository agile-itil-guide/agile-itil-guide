# Kanban

**Kanban gestisce il lavoro come un flusso: rende visibile il workflow, limita quanto è in corso e usa misure di flusso per migliorare, il che si adatta ai team di servizio il cui lavoro arriva in modo continuo e non può essere pianificato in cicli fissi.**

## Perché è importante

Un service desk, un team operativo e un team di piattaforma condividono un tratto: il lavoro arriva quando arriva. Incidenti, richieste e piccole modifiche arrivano in un flusso, e il team non può pianificarne un mese in anticipo. I framework costruiti attorno a cicli fissi, come Scrum, si adattano a questo lavoro solo con aggiustamenti (vedi Argomento 1.4 — Previsioni di consegna e metriche di pianificazione). Kanban è stato progettato per il flusso, quindi si adatta in modo più naturale.

Kanban parla anche il linguaggio della gestione dei servizi. Chiede quanto tempo richiede il lavoro, quanto ne sta aspettando e quale passaggio è il collo di bottiglia, e queste sono le domande dietro livelli di servizio, gestione delle code e pianificazione della capacità. Un team che monitora età e cycle time del proprio lavoro può parlare di livelli di servizio con dati invece che con impressioni.

Kanban è semplice da avviare e sorprendentemente facile da fare male. Una lavagna con colonne non è Kanban se nulla limita il lavoro in corso e nessuno usa le misure. Questo argomento spiega che cosa la Kanban Guide chiede a un team, da dove viene il metodo e come applicarlo al lavoro sui servizi.

## Concetti fondamentali

### Che cos'è Kanban

La [Kanban Guide](https://kanbanguides.org/english/), la cui versione attuale è datata maggio 2025 e che elenca John Coleman e Daniel Vacanti tra i suoi autori, definisce Kanban come una strategia per ottimizzare il flusso di valore attraverso un processo. Descrive il flusso come il movimento di valore potenziale attraverso un sistema. L'obiettivo è un equilibrio tra tre cose: efficacia (consegnare ciò che gli stakeholder vogliono, quando lo vogliono), efficienza (usare bene le risorse) e prevedibilità (prevedere la consegna con un livello accettabile di incertezza). La guida dice che si applica al lavoro della conoscenza in qualsiasi settore.

La parola "kanban" è giapponese e significa cartello o tabellone. L'[articolo di Wikipedia su Kanban nello sviluppo](https://en.wikipedia.org/wiki/Kanban_(development)) dice che il metodo deriva dalla produzione lean e dal [sistema di produzione Toyota](https://en.wikipedia.org/wiki/Toyota_Production_System), con un sistema just-in-time avviato alla Toyota alla fine degli anni Quaranta. Il libro di David J. Anderson del 2010 fa risalire la versione per il software a un progetto del 2004 alla Microsoft e a un progetto del 2006–2007 alla Corbis.

### Le tre pratiche

La Kanban Guide indica tre pratiche. Un team che le svolge tutte e tre, e usa le misure seguenti, pratica Kanban nel senso della guida.

| Pratica | Che cosa fa il team | Una nota per i team di servizio |
|---|---|---|
| **Definire e visualizzare il workflow** | Concordare una Definition of Workflow (DoW): che cos'è un elemento di lavoro, dove inizia e finisce, gli stati intermedi, come si limita il lavoro in corso, le regole per spostare il lavoro e un'aspettativa di livello di servizio (SLE). Mostrarla su una lavagna. | La DoW di un service desk può definire elementi di incidente, richiesta e modifica, con stati e regole diversi per ciascuno |
| **Gestire attivamente gli elementi nel workflow** | Controllare il numero di elementi in corso, tenere d'occhio gli elementi che invecchiano e sbloccare quelli fermi. | Un limite agli incidenti aperti per ingegnere costringe il team a concludere o passare di mano il lavoro prima di iniziarne altro |
| **Migliorare il workflow** | Modificare la DoW nel tempo per migliorare efficacia, efficienza e prevedibilità, a intervalli fissi o quando serve. | Una revisione della DoW dopo un incidente maggiore può cambiare regole, limiti o stati |

La guida non prescrive un layout della lavagna né alcuna riunione. I team sono liberi di aggiungere pratiche, purché le pratiche fondamentali, le misure e l'obiettivo di ottimizzare il valore restino intatti.

### Limiti al lavoro in corso e pull

Controllare il lavoro in corso (WIP) crea ciò che la guida chiama sistema pull: il nuovo lavoro inizia solo quando c'è capacità per esso. L'articolo di Wikipedia porta l'esempio di una fase di "deployment" con un limite di cinque. Quando la fase è piena, nulla può entrare finché qualcosa non finisce, quindi un blocco diventa visibile e le persone possono aiutare a eliminarlo. Senza limiti una lavagna è solo un'immagine del disordine.

### Quattro misure di flusso

La guida elenca quattro misure che un team che usa Kanban monitora:

- **Lavoro in corso:** il numero di elementi iniziati ma non ancora conclusi.
- **Throughput:** il numero di elementi conclusi in un dato periodo.
- **Età dell'elemento di lavoro:** da quanto tempo un elemento non concluso è in corso.
- **Cycle time:** quanto tempo ha impiegato un elemento concluso dall'inizio alla fine.

La guida dice che i team possono rinominarle e dovrebbero aggiungere altre misure dove utile, e che le misure contano solo quando informano le tre pratiche. Un'aspettativa di livello di servizio è una previsione di quanto tempo dovrebbe richiedere un elemento, basata sui cycle time passati. Non è una promessa, e si distingue da un accordo sul livello di servizio (SLA) negoziato con un cliente. Vedi Argomento 3.7 — Gestione dei livelli di servizio.

### La più ampia letteratura su Kanban

Altri autori hanno descritto il metodo in modo più ampio. L'articolo di Wikipedia elenca il lavoro di Don Reinertsen sul flusso, *Personal Kanban* di Jim Benson e Tonianne DeMaria Barry, *Kanban From the Inside* di Mike Burrows e *Scrumban* di Corey Ladas, che propose Kanban come modo per migliorare Scrum. Alcune di queste fonti elencano pratiche oltre le tre della guida, come rendere esplicite le regole, implementare cicli di feedback e migliorare in modo collaborativo. Considerale aggiunte utili, non requisiti della guida.

L'articolo di Wikipedia porta un'etichetta che segnala che un importante collaboratore potrebbe avere uno stretto legame con l'argomento, quindi verifica le sue affermazioni sulle fonti primarie.

### Che cosa Kanban non dice

Kanban non è un piano di progetto, un insieme di ruoli o un processo di rilascio. Non dice come progettare un servizio o gestire un incidente. Ti dà un modo di vedere e gestire il flusso e conta sul fatto che tu porti il contenuto del tuo lavoro. È anche la sua forza: puoi partire dal processo che hai e migliorarlo a piccoli passi (vedi Argomento 3.15 — Miglioramento continuo).

## Buone pratiche

1. **Parti da ciò che fai ora.** Disegna il workflow reale, con gli stati che il lavoro attraversa davvero, comprese le attese. Non disegnare il processo che vorresti avere. Puoi migliorare solo ciò che vedi.
2. **Definisci che cos'è un elemento di lavoro.** Decidi se incidenti, richieste e modifiche sono un tipo di elemento o più d'uno e dai a ciascuno un inizio e una fine chiari. Definizioni miste rendono le misure prive di senso.
3. **Fissa limiti WIP e rispettali.** Inizia con un limite che sembri leggermente stretto, come uno o due elementi per persona, e aggiusta con l'esperienza. Un limite che viene violato di routine non dà informazioni, quindi discuti ogni violazione.
4. **Rendi esplicite le regole.** Scrivi sulla lavagna quando un elemento può passare allo stato successivo, chi può prenderlo e che cosa conta come bloccato. Regole visibili riducono le discussioni e rendono più facile l'inserimento.
5. **Osserva l'età dell'elemento di lavoro, non solo il cycle time.** Il cycle time è noto solo dopo che un elemento è concluso, mentre l'età mostra i problemi quando c'è ancora tempo per agire. Rivedi ogni giorno gli elementi più vecchi.
6. **Usa un'aspettativa di livello di servizio basata sulla storia.** Prendi i cycle time degli elementi conclusi di recente e indica, per esempio, che la maggior parte degli elementi di un tipo si conclude entro un dato numero di giorni. Rivedila quando i dati cambiano. Non promettere ai clienti un numero che non hai misurato.
7. **Tratta il lavoro espresso come un'eccezione esplicita.** Gli incidenti urgenti salteranno la coda. Definisci una regola, come una corsia con un proprio limite, così che le eccezioni siano visibili e non distruggano silenziosamente il flusso (vedi Argomento 3.2 — Gestione degli incidenti).
8. **Cerca il collo di bottiglia e aiutalo.** Quando uno stato è sempre pieno, chiedi se ha bisogno di più capacità, di una regola diversa o di un flusso a monte diverso. Spostare persone sul collo di bottiglia di solito vale più che spingervi altro lavoro.
9. **Tieni revisioni a un ritmo regolare.** La guida consente di migliorare a intervalli fissi o quando serve. Una breve revisione settimanale delle misure e uno sguardo mensile alla DoW funzionano per molti team.
10. **Collega la lavagna al resto dell'organizzazione.** Rendi la lavagna visibile ai clienti e ai team vicini. Concorda come gli elementi passano da una lavagna all'altra, per esempio da un service desk a un team di sviluppo.
11. **Tieni le misure per imparare.** Usa i numeri per porre domande, non per classificare le persone. Quando i dati di flusso diventano un obiettivo, i team li manipolano (vedi Argomento 5.6 — Metriche e misurazione).
12. **Combina con altri framework in modo deliberato.** Se il team usa gli eventi Scrum per la pianificazione e Kanban per il flusso, di' a che cosa serve ciascuno e verifica che la combinazione riduca la confusione (vedi Argomento 1.8 — Scalare l'agile per coordinare più team).

## Domande da discutere con il team

**Se disegnassimo il nostro workflow reale, comprese le attese, che aspetto avrebbe?**

Chiedi a ciascuno di disegnare il percorso di un elemento recente, poi unisci i disegni su una parete. Le differenze tra i disegni mostrano passaggi nascosti e consegne informali. Aspettati sorprese: approvazioni che nessuno aveva menzionato, elementi in attesa di un altro team e cicli di rilavorazione. Prosegui segnando le tre attese più lunghe.

**Quanto lavoro è in corso per ciascuno di noi in questo momento, e quanto di esso sta aspettando?**

Conta gli elementi aperti per persona e segna quali sono bloccati o inattivi. Molti team scoprono che la maggior parte degli elementi aspetta e pochi vengono lavorati. Chiedi che cosa fa ciascuno quando è bloccato e se iniziare un nuovo elemento è la risposta abituale. Lo scopo è discutere perché iniziare viene premiato e concludere no.

**Qual è l'elemento più vecchio sulla nostra lavagna, e perché è ancora lì?**

Scegli i tre elementi più vecchi e ricostruisci che cosa è successo. Le risposte comuni sono un responsabile poco chiaro, una dipendenza da un altro team o un elemento che nessuno vuole annullare. Chiedi se l'elemento dovrebbe essere concluso, annullato o fatto salire di livello. Chi facilita può chiedere quale regola l'avrebbe intercettato prima.

**Che cosa promettiamo ai nostri clienti su quanto tempo richiedono le cose, e che cosa dicono i nostri numeri?**

Confronta i livelli di servizio concordati con i cycle time effettivi degli elementi conclusi. Se non hai dati, raccoglili prima per un mese. Discuti apertamente ogni divario. Chiedi se debba cambiare l'obiettivo o il modo di lavorare. Ricorda che un'aspettativa di livello di servizio basata sui dati è una previsione, mentre uno SLA è un accordo.

**Quando arriva lavoro urgente, che cosa succede a tutto il resto?**

Ripercorri l'ultimo incidente urgente e guarda quali elementi si sono fermati. Chiedi se il team ha una regola per il lavoro urgente e se qualcuno sa quanti elementi urgenti gestisce al mese. I team spesso scoprono che il lavoro urgente è routine, non eccezione, e che la regola deve rifletterlo. Prosegui concordando un limite per gli elementi espressi.

**Quali delle nostre misure considereremmo abbastanza affidabili da basarvi una decisione, e quali ignoreremmo?**

Chiedi alle persone di ordinare le misure disponibili in base a quanto si fidano e perché. La sfiducia deriva spesso da definizioni incoerenti degli elementi o da lacune nei dati. Non trasformarla in una discussione sulle persone; concentrati sulla qualità dei dati. Concludi scegliendo una misura da migliorare nel prossimo mese.

## Nella pratica: un esempio di ITIL agile

Il service desk IT di un'università ha otto analisti che gestiscono incidenti e richieste di studenti e personale. Il team ha uno strumento di ticketing con code ma senza limiti, e ogni analista ha tra 20 e 40 ticket aperti. I clienti si lamentano che i ticket sembrano sparire, e il responsabile del desk non sa dire quanto richieda una richiesta tipica.

Il responsabile e gli analisti costruiscono una lavagna che rispecchia lo strumento: nuovo, smistato, in corso, in attesa del cliente, in attesa di un altro team e risolto. Concordano un limite di otto elementi attivi per analista e una regola per cui i ticket in attesa di altri devono indicare la persona responsabile del passo successivo. Riservano una corsia agli incidenti urgenti, con un limite di due. Per un mese raccolgono solo dati su cycle time ed età.

Dopo il mese, i dati mostrano che la maggior parte delle richieste si risolve in pochi giorni ma che una lunga coda aspetta settimane, per lo più "in attesa di un altro team". Il team fissa un'aspettativa di livello di servizio dai dati e avvia una revisione quotidiana degli elementi più vecchi. Diversi ticket in attesa da tempo vengono chiusi o fatti salire di livello nella prima settimana. Resta un problema: il team di rete, che possiede molti dei ticket in attesa, non ha una propria lavagna e il desk non può vedere la sua coda. Il responsabile del desk organizza una conversazione settimanale con il responsabile del team di rete, e i due team iniziano a discutere di condividere una vista degli elementi che passano tra loro.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery possono usare Kanban per vedere dove il lavoro aspetta tra progettazione, sviluppo, test e rilascio. I limiti al lavoro in corso riducono il numero di modifiche a metà e i dati di flusso possono mostrare dove un processo di rilascio richiede attenzione. Tratta le richieste dalle operations come elementi nello stesso flusso, con una propria regola.

### Team di servizio e di operations

I team operativi sono la casa naturale di Kanban. Visualizza incidenti, richieste e modifiche in stati propri, fissa limiti e osserva l'invecchiamento. Usa i dati di cycle time per fissare aspettative realistiche con i clienti e usa gli stati bloccato e in attesa per avviare conversazioni con altri team.

### Leadership e governance

I leader traggono vantaggio dalle misure di flusso come quadro più onesto dei rapporti di stato. Chiedi cycle time, throughput ed età per tipo di lavoro e chiedi che cosa il team ha cambiato grazie a essi. Evita di fissare obiettivi sui singoli numeri, il che produce manipolazione. Sostieni i limiti al lavoro in corso anche quando gli stakeholder vogliono che si avvii di più.

### Clienti e utenti

I clienti traggono vantaggio da previsioni più chiare e meno richieste perse. Chiedi al team l'aspettativa di livello di servizio per il tuo tipo di richiesta e aspettati che si basi sulla storia. Se la tua richiesta è urgente, aspettati che ti si chieda perché, perché il team deve proteggere il flusso degli altri.

## Modalità di fallimento comuni

- **Una lavagna senza limiti.** La lavagna mostra il disordine ma non lo riduce. Fissa e applica invece limiti al lavoro in corso e rivedi ogni violazione.
- **Definizioni miste degli elementi.** Incidenti, progetti e attività condividono un unico insieme di colonne, e le misure non significano nulla. Definisci invece tipi di elemento con stati e regole separati.
- **Ignorare l'invecchiamento.** Gli elementi vecchi restano inosservati finché un cliente si lamenta. Rivedi invece ogni giorno gli elementi più vecchi e decidi su ciascuno.
- **Trasformare le misure in obiettivi.** I team dividono o chiudono elementi per migliorare i numeri. Usa invece le misure per porre domande e rivedile con il team.
- **Corsie espresse nascoste.** Il lavoro urgente aggira i limiti senza lasciare traccia. Dai invece al lavoro urgente una corsia visibile, un limite e una regola.
- **Copiare il layout di una lavagna.** Un team adotta le colonne di un altro senza capire il proprio flusso. Mappa invece prima il workflow reale.
- **Trattare Kanban come uno strumento di reporting.** I manager usano la lavagna per sorvegliare le persone e non per migliorare il flusso. Usala invece come strumento del team per decidere che cosa fare dopo.
- **Non migliorare mai il workflow.** La lavagna resta uguale per anni. Tieni invece revisioni regolari della Definition of Workflow e cambiala quando i dati lo richiedono.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Visualizzare il workflow | Il lavoro vive nelle caselle di posta individuali e nelle teste | Alcuni team hanno lavagne che mostrano i loro stati | I team condividono una Definition of Workflow con tipi di elemento e regole | La lavagna è rivista e corretta rispetto a ciò che accade davvero | Le lavagne tra team mostrano elementi e passaggi tra team |
| Limitare il lavoro in corso | Nessun limite; le persone iniziano più di quanto concludono | Alcuni team fissano limiti informali | I limiti sono fissati e le violazioni discusse | I limiti sono aggiustati in base ai dati di flusso | Limiti e capacità sono bilanciati tra team e fornitori |
| Misure di flusso | Si raccolgono poche misure | Alcuni team registrano cycle time o throughput | Le quattro misure sono raccolte in modo coerente | Le misure sono riviste e usate per fissare le aspettative di livello di servizio | I dati di flusso sono condivisi tra i team e usati per pianificare insieme la capacità |
| Miglioramento | I cambiamenti seguono le crisi | I team aggiustano occasionalmente la lavagna | I team rivedono il workflow a un ritmo regolare | I cambiamenti sono collegati alle misure e i risultati verificati | I miglioramenti si diffondono tra i team senza direzione centrale |

## Checklist

- [ ] Abbiamo disegnato il nostro workflow reale, comprese attese e passaggi di consegne.
- [ ] I nostri elementi di lavoro sono definiti, con un inizio e una fine chiari per ogni tipo.
- [ ] Esistono limiti al lavoro in corso e ogni violazione è discussa.
- [ ] Le regole per spostare e bloccare gli elementi sono scritte sulla lavagna o vicino ad essa.
- [ ] Monitoriamo cycle time, throughput, lavoro in corso ed età degli elementi di lavoro.
- [ ] Rivediamo gli elementi più vecchi ogni giorno o almeno ogni settimana.
- [ ] Abbiamo un'aspettativa di livello di servizio basata sulla nostra storia.
- [ ] Il lavoro urgente ha la propria corsia visibile, il proprio limite e la propria regola.
- [ ] La Definition of Workflow è rivista a un ritmo regolare.
- [ ] I team vicini e i clienti possono vedere gli elementi che li riguardano.

## Prompt per l'IA

**Scopo: descrivere il tuo workflow reale e trovare dove il lavoro aspetta.**

```text
You are helping me map the real workflow of a team that handles [type of work, e.g. "service desk incidents and requests"].

Here are the states a typical item goes through, as best I can describe them: [paste the steps in order, including waits and handovers].
Here is what happened to three recent items, with dates for each state change: [paste three short timelines, using only real data].

Draw the workflow as a simple text diagram. Identify where each item waited longest, using only the dates I provided. Suggest three questions I should ask the team about those waits. Do not invent numbers. If the data are too thin, ask me for more first, mark your assumptions, and list what you are unsure of.
```

**Scopo: redigere una Definition of Workflow per un team.**

```text
Help me write a first Definition of Workflow for [team name and what it does].

Item types we handle: [list them, e.g. incidents, requests, changes].
States an item can be in: [list, or write "unknown"].
Current policies for starting, finishing, and blocking items: [paste, or write "none written"].
Roughly how many items each person has open at a time: [number, or "unknown"].

Produce a draft with: the item types, start and finish points, states, a proposed WIP limit approach, policies for moving items, a policy for urgent work, and how a service level expectation would be set from our own history. Mark every proposal that is a guess. Do not state any numbers I have not given you. Ask me clarifying questions first, and list what you are unsure of.
```

**Scopo: analizzare i dati di flusso del tuo sistema di ticket.**

```text
Below are the start and finish dates of [number] items our team completed recently, and the start dates of [number] items still open: [paste as a table, real data only].

Calculate the cycle time of each completed item and the current age of each open item. Describe the spread: what most items take, what the slowest take, and which open items are older than most finished items. Do not extrapolate beyond the data. Suggest two questions to ask the team about the oldest items. Tell me what extra data would make the analysis more reliable, and list what you are unsure of.
```

**Scopo: pianificare con il team una revisione della lavagna.**

```text
Plan a 30-minute weekly flow review for a team of [number] people that uses a Kanban board for [type of work].

Our measures: [list which of work in progress, throughput, cycle time, and work item age you track].
Current frustration: [describe in one or two sentences].

Include a timed agenda, five questions to ask about the measures and the oldest items, and a closing step that records at most two changes with owners. Keep it free of any particular tool. Ask clarifying questions first if information is missing, and list what you are unsure of.
```

## Competenze per l'IA

- [kanban](../../../../skills/kanban/SKILL.md): da usare per progettare o rivedere una lavagna, i limiti al lavoro in corso e le regole per un team di servizio o di operations.
- [scrumban](../../../../skills/scrumban/SKILL.md): da usare quando un team vuole gli eventi di pianificazione di Scrum insieme alla gestione del flusso di Kanban.
- [value-stream-map](../../../../skills/value-stream-map/SKILL.md): da usare per mappare come il lavoro si muove tra i team e dove aspetta prima di progettare la lavagna.
- [kaizen](../../../../skills/kaizen/SKILL.md): da usare per pianificare piccoli miglioramenti del workflow dopo una revisione del flusso.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): da usare per capire quali tipi di lavoro arrivano e in quale volume prima di fissare limiti e capacità.

## Fonti principali

- **The Kanban Guide** (John Coleman e Daniel Vacanti e altri, kanbanguides.org): la definizione concisa e autorevole delle tre pratiche e delle quattro misure.
- **Kanban (development)** (Wikipedia): una panoramica della storia e delle pratiche più ampie, con rimandi ai libri principali.
- **Kanban: Successful Evolutionary Change for Your Technology Business** (David J. Anderson, 2010): il resoconto di come Kanban è stato applicato al lavoro sul software.
- **Toyota Production System** (Wikipedia): contesto sulle origini di kanban nella produzione lean.

## Riferimenti

1. The Kanban Guide — John Coleman, Daniel Vacanti, and contributors, kanbanguides.org — https://kanbanguides.org/english/
2. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
3. Kanban — Wikipedia — https://en.wikipedia.org/wiki/Kanban
4. Toyota Production System — Wikipedia — https://en.wikipedia.org/wiki/Toyota_Production_System
5. Theory of constraints — Wikipedia — https://en.wikipedia.org/wiki/Theory_of_constraints
6. Scrumban — Wikipedia — https://en.wikipedia.org/wiki/Scrumban
7. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
8. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
