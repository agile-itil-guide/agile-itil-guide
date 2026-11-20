# Gestione del flusso di valore

**La gestione del flusso di valore guarda all'intero percorso dalla richiesta al valore, misura dove il lavoro aspetta e migliora il flusso tra i team, perché i ritardi maggiori in un'organizzazione di servizio di solito stanno tra i team, non dentro di essi.**

## Perché è importante

La maggior parte dei team misura il proprio lavoro: ticket chiusi, story concluse, modifiche rilasciate. Questi numeri possono sembrare buoni mentre il cliente aspetta settimane. La ragione è che la maggior parte del tempo trascorso in una richiesta tipica è speso ad aspettare, in code, per approvazioni, tra team. Un team che rende più veloce il proprio passaggio può non cambiare nulla per la persona che ha chiesto.

Il pensiero lean ha un metodo per vederlo: la mappa del flusso di valore, che disegna ogni passaggio dall'inizio di un processo al cliente e registra tempo e volume a ogni fase. ITIL 4 ha una propria idea di flusso di valore, un insieme di attività che creano e consegnano un servizio, che combina le attività della catena del valore in ordini diversi (vedi Argomento 2.6 — La catena del valore del servizio). I due si integrano. L'idea ITIL dice che cos'è un flusso, e il metodo lean mostra come misurarne e migliorarne uno.

La gestione del flusso di valore va oltre un workshop di mappatura una tantum. Significa gestire continuamente il flusso di lavoro, con misure condivise, un responsabile nominato e revisioni regolari che includono ogni team del flusso. L'elenco di capacità di DORA include la visibilità del lavoro nel flusso di valore e i limiti al lavoro in corso, e le sue indicazioni sui limiti descrivono il rendere visibile tutto il lavoro, compreso quello fuori dal team. Questo argomento attinge all'articolo di Wikipedia sulla mappatura del flusso di valore, a DORA e alla Kanban Guide e dice dove le fonti tacciono.

## Concetti fondamentali

### Che cos'è un flusso di valore

Un **flusso di valore** è la sequenza di passaggi attraverso cui una richiesta diventa valore consegnato. L'[articolo di Wikipedia sulla mappatura del flusso di valore](https://en.wikipedia.org/wiki/Value-stream_mapping) descrive il metodo come una tecnica di gestione lean che analizza lo stato attuale e progetta uno stato futuro per gli eventi che portano un prodotto o servizio dall'inizio di un processo al cliente. Nella visione ITIL, un flusso di valore è uno specifico insieme di attività che creano e consegnano ai clienti un particolare servizio o prodotto (vedi Argomento 2.6 — La catena del valore del servizio).

Esempi in un'organizzazione di servizio: gestire un incidente dalla segnalazione al ripristino, consegnare una modifica dall'idea alla produzione, inserire un nuovo cliente o evadere una richiesta di accesso.

### Mappatura del flusso di valore

L'articolo dice che la mappa visiva risultante mostra ogni passaggio critico e quantifica tempo e volume a ogni fase. Descrive due mappe: una **mappa dello stato attuale**, costruita osservando e tracciando il flusso reale di materiali e informazioni, e una **mappa dello stato futuro**, che mostra il processo ideale dopo i miglioramenti. Lo stato attuale va costruito per primo. L'articolo cita come fonte *Learning to See* di Mike Rother e John Shook (Lean Enterprise Institute, 1999). Elenca sviluppo del software, sviluppo di prodotto, gestione dei progetti e processi amministrativi e d'ufficio come aree di uso e menziona due approcci orientati al software di Ali e colleghi: l'analisi degli artefatti di sviluppo e l'analisi del flusso di informazioni.

L'articolo non definisce lead time, tempo di processo né percentuale completa e accurata, non elenca simboli e non discute critiche. La pagina DORA sulla consegna continua, tuttavia, rimanda alla mappatura del flusso di valore come modo di far emergere i colli di bottiglia confrontando il tempo trascorso con il tempo a valore aggiunto e misurando la percentuale completa e accurata (%C/A). I termini seguenti sono l'uso comune:

| Termine | Significato, nell'uso comune |
|---|---|
| **Lead time** | Tempo totale trascorso dall'inizio di una richiesta alla consegna |
| **Tempo di processo** (o tempo di lavoro effettivo) | Tempo in cui qualcuno sta effettivamente lavorando sulla richiesta |
| **Tempo di attesa** | Tempo in cui la richiesta resta inattiva tra i passaggi |
| **Percentuale completa e accurata (%C/A)** | Quota di lavoro che arriva a un passaggio e non richiede correzioni o informazioni mancanti |
| **Efficienza di flusso** | Tempo di processo diviso per il lead time, in percentuale |

L'efficienza di flusso è un semplice rapporto calcolato per l'illustrazione di questa guida, e le fonti lette non la definiscono.

### Misure di flusso

La Kanban Guide nomina quattro misure di flusso (vedi Argomento 1.5 — Kanban): **lavoro in corso** (elementi iniziati ma non conclusi), **throughput** (elementi conclusi per periodo), **età dell'elemento di lavoro** (tempo da quando un elemento non concluso è iniziato) e **cycle time** (tempo dall'inizio alla fine per un elemento concluso). Funzionano al livello del workflow di un team. La gestione del flusso di valore applica le stesse idee tra i team: misura il tempo trascorso dalla richiesta alla ricezione da parte del cliente, non dal punto in cui un singolo team la prende in carico.

Le misure di consegna del software di DORA, come il change lead time, si applicano a una fetta del flusso, dal commit alla produzione (vedi Argomento 3.4 — Abilitazione dei cambiamenti). La parte precedente, dall'idea al commit, fa anch'essa parte del flusso di valore e ha spesso le attese più lunghe.

### Limiti al lavoro in corso

La pagina DORA sui limiti al lavoro in corso (WIP) li descrive come tetti al numero di elementi che possono essere in ogni fase di un workflow. Dice che la ricerca DORA collega i limiti WIP a migliori prestazioni di consegna del software solo in combinazione con altre capacità, come visualizzazioni e cicli di feedback dal monitoraggio, e non dà dimensioni dell'effetto. I suoi consigli di implementazione includono rendere visibile tutto il lavoro, compreso quello fuori dal team, fissare ogni limite in base alla capacità del team, mantenere fermi i limiti e non alzarli quando le persone sono inattive, tirare il lavoro solo quando si libera uno slot, monitorare il lead time e la sua variabilità, ridurre i passaggi di consegne e abbassare gradualmente i limiti per far emergere il vincolo successivo. Le insidie che nomina includono ignorare il lavoro a monte e a valle, il che porta a ottimizzazione locale, e fissare limiti troppo alti.

### Vedere l'intero flusso

L'insidia dell'"ottimizzazione locale" è quella centrale. Un flusso con cinque team ha cinque code. Se un team raddoppia la propria velocità, il lead time del flusso può cambiare appena, perché gli altri aspettano ancora. La gestione del flusso di valore cerca il **vincolo**, il passaggio che limita l'insieme, e lo migliora per primo (vedi Argomento 1.7 — Sviluppo software lean sull'ottimizzare l'intero).

### Responsabilità e governance

Un flusso attraversa i team, quindi ha bisogno di qualcuno responsabile dell'insieme. Un responsabile del flusso di valore (o un piccolo gruppo) detiene la mappa, le misure e l'elenco dei miglioramenti e convoca i team. Senza un responsabile, nessuno risponde del flusso e i miglioramenti restano entro i confini dei team. Questo si collega alla responsabilità di prodotto e di servizio (vedi Argomento 5.5 — Responsabilità di prodotto e di servizio).

### Strumenti

Gli strumenti software per la gestione del flusso di valore raccolgono dati da ticketing, controllo del codice sorgente e pipeline per mostrare il flusso lungo la catena di strumenti. Le fonti lette per questa guida non discutono tali strumenti. Se ne valuti qualcuno, verifica di quali dati ha bisogno, quanto è accurato e se le misure rispondono a una domanda che hai. Una mappa approssimativa disegnata a mano con i team coinvolti è un buon punto di partenza e spesso rivela più di un cruscotto.

### Limiti

L'articolo di Wikipedia non discute critiche, e la pagina DORA sul WIP non dà dimensioni dell'effetto né valori obiettivo. Le cautele pratiche, offerte come esperienza, includono mappature che non portano mai al cambiamento, misure usate per classificare i team e mappe disegnate dalla memoria dei manager invece che dall'osservazione di elementi reali.

## Buone pratiche

1. **Scegli un flusso che conta.** Scegli un flusso a cui gli utenti tengono, come una modifica che arriva in produzione o una richiesta di accesso. Un flusso ristretto e reale insegna più di uno ampio e astratto.
2. **Mappa da elementi reali.** Segui diversi elementi recenti dall'inizio alla fine e registra le date effettive, non il documento di processo. L'osservazione batte il ricordo, come suggerisce l'enfasi dell'articolo sull'osservare e tracciare il flusso reale.
3. **Registra tempo e attesa a ogni passaggio.** Per ogni passaggio, annota il tempo di lavoro e l'attesa prima di esso. Le attese sono di solito la storia.
4. **Includi tutti nel flusso.** Invita persone di ogni team che tocca l'elemento, compresi approvatori e fornitori. Fai la mappatura insieme, così che nessuno sia sorpreso dal risultato.
5. **Calcola lead time, tempo di processo ed efficienza di flusso.** Confronta il tempo trascorso con il tempo di lavoro e guarda quanto è attesa. Usa i numeri per avviare conversazioni.
6. **Guarda l'accuratezza.** Chiedi con quale frequenza il lavoro arriva a un passaggio incompleto o sbagliato, richiedendo rilavorazione. Un passaggio con bassa percentuale completa e accurata causa ritardo a valle.
7. **Trova il vincolo.** Individua il passaggio che limita l'intero flusso e miglioralo per primo. Migliorare altri passaggi dà poco beneficio.
8. **Disegna lo stato futuro.** Progetta con i team un flusso migliore, non uno ideale, e scegli la prima o le prime due modifiche. Concorda responsabili e date.
9. **Limita il lavoro in corso.** Fissa un tetto a ciò che ogni fase contiene, fissa i limiti in base alla capacità, mantienili quando le persone sono inattive e abbassali gradualmente, come descrivono le indicazioni DORA.
10. **Rendi visibile il lavoro.** Mostra il flusso su una lavagna o mappa condivisa che includa il lavoro fuori da qualsiasi singolo team. Aggiornala man mano che gli elementi si muovono.
11. **Nomina un responsabile del flusso.** Scegli una persona responsabile delle prestazioni del flusso che possa convocare i team e portare i miglioramenti ai leader.
12. **Rivedi regolarmente.** Tieni una breve revisione mensile di lead time, attese ed elenco dei miglioramenti. Ridisegna la mappa dopo cambiamenti significativi.

## Domande da discutere con il team

**Se seguissimo una richiesta dal primo contatto alla ricezione da parte del cliente, quanto ci metterebbe, e quanto di quel tempo è tempo di lavoro?**

Scegli un elemento recente e raccogli le date. Chiedi alle persone di indovinare la risposta prima di guardare. La stima è di solito ottimistica. Calcola la quota di tempo di lavoro. Chi facilita può chiedere dove è avvenuta l'attesa più lunga e chi la possedeva. Sceglila come primo obiettivo.

**Con chi nel flusso non abbiamo mai parlato?**

Elenca i team, gli approvatori e i fornitori che un elemento tocca. Segna quelli che il team non ha mai incontrato. Chiedi che cosa si guadagnerebbe invitandoli a una sessione di mappatura. Risposte tipiche: capire perché aspettano o di che cosa hanno bisogno per lavorare più in fretta. Inviti uno.

**Che cosa passiamo incompleto, e che cosa riceviamo incompleto?**

Chiedi esempi di lavoro tornato per rilavorazione. Annota quali passaggi di consegne causano più ritorni e che cosa manca. È l'idea di percentuale completa e accurata in termini semplici. Concorda una breve checklist per un passaggio di consegne.

**Dove sta il vincolo nel nostro flusso, e che cosa succede se acceleriamo qualcos'altro?**

Discuti quale passaggio ha la coda più lunga. Chiedi che cosa succederebbe al tempo end-to-end se un altro passaggio raddoppiasse la velocità. Il punto è vedere che migliorare un non-vincolo cambia poco. Scegli di lavorare sul vincolo.

**Su quante cose sta lavorando ogni team contemporaneamente, e che cosa succederebbe se mettessimo un tetto?**

Conta il lavoro in corso per team. Discuti che cosa significherebbe smettere di iniziare. Timori tipici: qualcosa di importante dovrà aspettare. Benefici tipici: le cose finiscono. Concorda un tetto di prova per un team e un modo di giudicare il risultato.

**Chi è responsabile di questo flusso nel suo insieme?**

Chiedi al team di nominare la persona. Se nessuno, discuti chi potrebbe esserlo e di quale autorità avrebbe bisogno. Chi facilita può notare che i miglioramenti tra team raramente avvengono senza un responsabile. Proponi un nome e portalo al leader competente.

## Nella pratica: un esempio di ITIL agile

Un'autorità nazionale di regolazione ambientale rilascia autorizzazioni a operatori industriali. I richiedenti si lamentano che un'autorizzazione tipica richiede circa quattro mesi e al gruppo servizi digitali dell'autorità, di dodici persone, viene chiesto di accelerare. Il gruppo aveva già costruito un modulo online di domanda più veloce, ma il tempo trascorso è cambiato appena.

Il responsabile del gruppo convoca persone da ogni parte del flusso: il team delle domande, due revisori tecnici, un funzionario legale, l'ufficio tariffe e il team che emette i documenti di autorizzazione. Mappano sei autorizzazioni recenti dalla data di presentazione alla data in cui l'autorizzazione è arrivata al richiedente. I risultati sono sobri. Il tempo totale è stato di circa 110 giorni e il tempo di lavoro di circa 12. L'attesa più lunga era nella coda di revisione tecnica, dove le domande aspettavano in media 40 giorni prima che qualcuno le aprisse, e circa un terzo delle domande arrivava con informazioni mancanti che dovevano essere richieste di nuovo. L'ufficio tariffe e il team dei documenti aggiungevano ciascuno una settimana di attesa per l'elaborazione a lotti.

Il gruppo concorda tre cambiamenti. Il modulo online verifica gli elementi comunemente mancanti prima dell'invio. Il team di revisione tecnica fissa un limite al lavoro in corso e una regola di aprire ogni domanda entro cinque giorni lavorativi per verificarne la completezza. L'ufficio tariffe e il team dei documenti passano da lotti settimanali a elaborazione giornaliera. Nominano il responsabile dei servizi digitali come responsabile del flusso e rivedono ogni mese il lead time. Dopo tre mesi, il lead time mediano è di circa 70 giorni e la quota di domande restituite per informazioni mancanti cala. Restano alcuni problemi. Il team di revisione dice che il limite rende più difficile gestire domande grandi e complesse, e il funzionario legale è un singolo punto di ritardo che nessuno aveva contato. Il responsabile del flusso chiede al team di revisione di separare i casi complessi in una corsia propria e lavora con l'ufficio legale su un secondo revisore.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery vedono solo una parte del flusso. Partecipa alle sessioni di mappatura, condividi i tuoi dati e guarda che cosa succede prima che il lavoro ti raggiunga e dopo il rilascio. Tratta il lead time del flusso come obiettivo condiviso, non solo il tuo passaggio.

### Team di servizio e di operations

I team operativi spesso detengono le code più lunghe: accessi, approvazioni, ambienti, supporto. Sii aperto su capacità e vincoli. Usa la mappa per chiedere ai team a monte input completi e per spiegare le tue priorità.

### Leadership e governance

I leader possono rimuovere i vincoli tra team che i team non possono. Nomina i responsabili dei flussi, chiedi il lead time end-to-end e rispondi ai miglioramenti che la mappa suggerisce. Evita di usare le misure del flusso per classificare i team, il che scoraggia dati onesti.

### Clienti e utenti

Clienti e utenti vivono l'intero flusso. Di' al team dove i ritardi fanno male, dai informazioni complete all'inizio e partecipa a una sessione di mappatura se invitato. La tua visione di quando la richiesta è davvero finita è la vera fine del flusso.

## Modalità di fallimento comuni

- **Ottimizzare un solo team.** Un guadagno locale non cambia nulla end-to-end. Trova invece e affronta il vincolo.
- **Mappare dalla memoria.** La mappa riflette ciò che i manager credono. Traccia invece elementi reali con date reali.
- **Voci mancanti.** Fornitori e approvatori non sono nella stanza. Includi invece ogni team del flusso.
- **Una mappa senza cambiamento.** Il poster resta appeso al muro. Concorda invece una o due modifiche con responsabili prima della fine della sessione.
- **Nessun responsabile.** Nessuno risponde del flusso. Nomina invece un responsabile del flusso con l'autorità di convocare.
- **Misure come classifiche.** I team nascondono le attese. Usa invece le misure per capire il flusso e discutile apertamente.
- **Limiti che si spostano.** I limiti WIP sono alzati ogni volta che le persone sono inattive. Mantieni invece i limiti e correggi le cause, come consiglia DORA.
- **Prima lo strumento.** Si compra un cruscotto prima di conoscere le domande. Parti invece da una mappa disegnata a mano e aggiungi strumenti se servono.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Vedere il flusso | Il flusso è giudicato a sensazione | Alcuni team mappano i propri passaggi | I flussi chiave sono mappati end-to-end da elementi reali, con tutti i team | Lead time, attese e accuratezza sono misurati e rivisti | I flussi sono mappati e misurati tra organizzazioni e fornitori |
| Migliorare il flusso | I team accelerano i propri passaggi | Si provano alcuni cambiamenti tra team | Un elenco di miglioramenti per flusso, centrato sul vincolo, con responsabili | I miglioramenti sono legati al lead time misurato e verificati | Il miglioramento del flusso è routine e condiviso tra i flussi |
| Limiti e visibilità | Il lavoro in corso è illimitato e nascosto | Alcuni team usano lavagne e limiti | Il lavoro è visibile tra i team con limiti concordati | I limiti sono regolati con i dati sul lead time | Limiti e visibilità sono coordinati tra i flussi |
| Responsabilità e governance | Nessuno possiede il flusso | Esistono coordinatori informali | Ogni flusso chiave ha un responsabile nominato e una revisione regolare | I responsabili sono accountable per risultati misurati | I responsabili collaborano tra i flussi per ottimizzare l'intero |

## Checklist

- [ ] Abbiamo scelto un flusso importante e l'abbiamo mappato da elementi reali.
- [ ] La mappa mostra tempo di lavoro e tempo di attesa a ogni passaggio.
- [ ] Persone di ogni team del flusso hanno partecipato alla mappatura.
- [ ] Conosciamo il lead time end-to-end e quanto è attesa.
- [ ] Abbiamo individuato il vincolo e scelto una o due modifiche.
- [ ] Il lavoro in corso è visibile tra i team, con limiti concordati nelle fasi chiave.
- [ ] Una persona nominata possiede il flusso.
- [ ] Una breve revisione regolare guarda lead time, attese ed elenco dei miglioramenti.
- [ ] Monitoriamo quanto spesso il lavoro arriva incompleto a un passaggio di consegne.
- [ ] Le misure del flusso non sono usate per classificare i team.

## Prompt per l'IA

**Scopo: calcolare lead time ed efficienza di flusso da elementi reali.**

```text
I have timing data for [number] recent items in the stream [name]. For each item and each step I have the date work began and ended, and the date it arrived at the step: [paste a table with real dates, step names, and the team responsible].

Using only my dates, calculate for each item the total lead time, the working time (end minus begin for each step), the waiting time (arrival at a step minus the end of the previous step), and the flow efficiency (working time divided by lead time). Show the average and range across items, and the three longest waits by team and step. Do not invent numbers. If dates are missing, say what to collect. List what you are unsure of.
```

**Scopo: pianificare un workshop di mappatura del flusso di valore.**

```text
Plan a 2-hour value stream mapping workshop for the stream [name].

Participants: [roles and teams].
Data to bring (real dates for [number] recent items): [describe what exists].
Constraints: [for example remote].

Provide a timed agenda: agree the start and end of the stream, walk through real items, mark steps with working time and waiting time, record rework and incomplete handovers, identify the constraint, draw a future state, and agree one or two changes with owners and dates. Include prompts to keep the conversation on the system. Keep it free of any particular tool. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: analizzare la qualità del passaggio di consegne tra due team.**

```text
Teams A and B hand work over in the stream [name]. Here are examples of items that came back for rework or information, with reason: [paste, one per line].

Group the reasons into categories using only the text. Count items per category from my list. For the top two categories, suggest an item for a handover checklist that team A could use, and a question for team B. Do not infer causes beyond the text. List what you are unsure of.
```

**Scopo: progettare una sperimentazione di limiti al lavoro in corso.**

```text
Design a four-week trial of work-in-process limits for [team] working in [stream or stage].

Current items in progress per person or stage: [paste real counts].
Lead time data we have: [describe].
Capacity, in people: [number].

Propose limits for each stage based on capacity, how to show work and age on a board, rules for pulling work, what to do when someone is idle (without raising limits), what to measure (leave targets as [to be agreed]), and what would make us stop. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [value-stream-map](../../../../skills/value-stream-map/SKILL.md): da usare per mappare un flusso, registrare i tempi e trovare il vincolo.
- [workflow-analysis](../../../../skills/workflow-analysis/SKILL.md): da usare per studiare come il lavoro si muove tra i ruoli e dove aspetta.
- [kanban](../../../../skills/kanban/SKILL.md): da usare per impostare visualizzazione e limiti al lavoro in corso per il flusso.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): da usare per capire che cosa entra nel flusso e in quale volume.
- [portfolio-management](../../../../skills/portfolio-management/SKILL.md): da usare per decidere quali flussi e iniziative meritano investimento.

## Fonti principali

- **Value-stream mapping** (Wikipedia): la definizione di mappe dello stato attuale e futuro e un rimando a *Learning to See*.
- **Work in process limits** (DORA, dora.dev): indicazioni su come fissare e mantenere i limiti e su come evitare l'ottimizzazione locale.
- **The Kanban Guide** (kanbanguides.org): definizioni delle quattro misure di flusso.
- **Lean software development** (Wikipedia): gli sprechi e i principi dietro il pensiero sul flusso di valore.

## Riferimenti

1. Value-stream mapping — Wikipedia — https://en.wikipedia.org/wiki/Value-stream_mapping
2. Work in process limits — DORA, dora.dev — https://dora.dev/capabilities/wip-limits/
3. Continuous delivery — DORA, dora.dev — https://dora.dev/capabilities/continuous-delivery/
4. The Kanban Guide — John Coleman, Daniel Vacanti, and contributors, kanbanguides.org — https://kanbanguides.org/english/
5. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
6. Lean manufacturing — Wikipedia — https://en.wikipedia.org/wiki/Lean_manufacturing
7. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
8. Theory of constraints — Wikipedia — https://en.wikipedia.org/wiki/Theory_of_constraints
9. Value chain — Wikipedia — https://en.wikipedia.org/wiki/Value_chain
