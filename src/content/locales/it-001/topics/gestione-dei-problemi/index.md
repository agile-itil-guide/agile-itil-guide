# Gestione dei problemi

**La gestione dei problemi trova e rimuove le cause degli incidenti ricorrenti, e la sua forma agile è un flusso costante di piccole correzioni basate sulle prove nel backlog anziché occasionali grandi indagini.**

## Perché è importante

Un team che gestisce bene gli incidenti ma non ne rimuove mai le cause è su un tapis roulant. Ogni interruzione viene riparata, lo stesso guasto ritorna e gli ingegneri di turno si stancano. La gestione dei problemi è la pratica che scende dal tapis roulant: chiede perché l'incidente è avvenuto, se si ripeterà e che cosa lo fermerebbe.

I team agili sono ben posizionati per farlo. Hanno un backlog in cui una correzione può competere con una funzionalità, lavorano in cicli brevi che rendono economiche le piccole correzioni e tengono retrospettive in cui si possono notare gli schemi. Ciò che spesso manca loro è l'abitudine di collegare gli incidenti tra loro e la disciplina di cercare le cause nel modo giusto. La gestione dei problemi fornisce entrambe.

L'[articolo di Wikipedia sull'analisi delle cause radice](https://en.wikipedia.org/wiki/Root_cause_analysis) è la fonte principale letta per questo argomento, perché la Wikipedia inglese non ha un articolo intitolato "Problem management" all'indirizzo verificato. Quell'articolo descrive l'analisi delle cause radice (RCA) come un metodo di risoluzione dei problemi usato nelle operazioni IT e in altri campi e porta etichette di manutenzione per citazioni mancanti. Il vocabolario ITIL usato qui, come errore noto e workaround, viene da descrizioni ampiamente pubblicate della pratica, che questa guida non ha potuto confermare rispetto al testo del proprietario del framework. Leggi le pubblicazioni correnti del proprietario quando servono definizioni esatte (vedi Argomento 2.2 — ITIL).

## Concetti fondamentali

### Incidente, problema, errore noto

Tre termini sono usati insieme, e le distinzioni contano:

| Termine | Significato, come ampiamente usato nell'ITSM | Esempio |
|---|---|---|
| **Incidente** | Un'interruzione non pianificata di un servizio o una riduzione della sua qualità | La pagina di prenotazione è ferma per venti minuti |
| **Problema** | La causa di fondo, o presunta tale, di uno o più incidenti | Una perdita di memoria nel servizio di prenotazione |
| **Errore noto** | Un problema la cui causa è stata individuata, di solito con un workaround registrato | Una perdita di memoria è compresa; riavviare il servizio ogni notte previene le interruzioni finché non è corretta |

Un **workaround** è un modo di ridurre o evitare l'impatto di un incidente o problema senza rimuoverne la causa. La gestione dei problemi riguarda la rimozione della causa, e la gestione degli incidenti il ripristino del servizio (vedi Argomento 3.2 — Gestione degli incidenti).

### Reattivo e proattivo

L'articolo sull'analisi delle cause radice distingue in termini generali approcci reattivi e proattivi. Il lavoro reattivo tratta rapidamente i sintomi. Il lavoro proattivo punta a prevenire i problemi e mette l'accuratezza diagnostica prima della velocità. Nella pratica ITSM esistono entrambi: la gestione reattiva dei problemi indaga sui problemi dopo gli incidenti, e quella proattiva cerca schemi e debolezze prima che causino incidenti.

### Che cos'è una causa radice

L'articolo definisce una causa radice con un test pratico: un fattore è la causa radice di un problema se rimuoverlo impedisce al problema di ripetersi. Distingue una causa radice da altri fattori causali. È una regola utile. Se rimuovi un fattore e il problema può ancora ritornare, hai trovato un contributore, non la radice.

L'articolo avverte anche dei limiti. Dice che dati di monitoraggio mancanti, volumi di eventi molto alti, cause radice multiple e investigatori che si fermano a una radice superficiale complicano l'analisi. Nell'IT, osserva, l'RCA spesso manca di alberi dei guasti o specifiche di progetto, quindi "non c'è una causa radice" è diventato un modo di dire comune. Per i sistemi complessi, aspettati diverse cause concorrenti e non un singolo colpevole.

### Principi dell'analisi delle cause radice

L'articolo elenca passaggi generali:

1. Descrivere chiaramente il problema.
2. Costruire una cronologia dal funzionamento normale al guasto.
3. Separare la causa radice dagli altri fattori causali.
4. Tracciare un grafo causale che colleghi la causa radice al problema.

Aggiunge che gli investigatori dovrebbero guardare alle difese che hanno fallito o mancavano (barrier analysis), evitare distorsioni nelle linee d'indagine, decidere le azioni correttive e verificare se tali azioni sono state efficaci.

### Metodi

L'articolo dice che, secondo ISO/IEC 31010, l'RCA può usare i cinque perché, la failure mode and effects analysis (FMEA), l'analisi ad albero dei guasti, i diagrammi di Ishikawa (a lisca di pesce) e l'analisi di Pareto. Attribuisce a Kaoru Ishikawa il diagramma causale che porta il suo nome. Definisce anche i metodi a lisca di pesce e dei cinque perché "not rigorous enough", un parere che non sostiene con una fonte. Una lettura pratica: i metodi semplici sono buoni punti di partenza per la discussione di team, e i guasti complessi o ad alto rischio possono richiederne di più rigorosi.

| Metodo | Che cosa fa | Quando aiuta |
|---|---|---|
| **Cinque perché** | Chiede ripetutamente "perché" per passare da un sintomo verso una causa | Discussione rapida a livello di team di catene di cause semplici |
| **Diagramma di Ishikawa (a lisca di pesce)** | Raggruppa le possibili cause per categoria | Brainstorming di molte possibili cause |
| **Analisi di Pareto** | Ordina le cause per frequenza o impatto | Scegliere quale problema ricorrente affrontare per primo |
| **Analisi ad albero dei guasti** | Mappa le combinazioni di guasti che portano a un esito | Guasti critici per la sicurezza o complessi |
| **FMEA** | Guarda avanti a come le parti potrebbero guastarsi e quale sarebbe l'effetto | Revisione proattiva del progetto |

### Azioni correttive efficaci

L'articolo dice che le azioni correttive che aggiungono solo burocrazia o formazione sono meno efficaci. Nella pratica ciò suggerisce di favorire azioni che cambiano il sistema: automatizzare un controllo, rimuovere una modalità di guasto, aggiungere una salvaguardia, migliorare il monitoraggio. Un'azione come "ricordare agli ingegneri di stare attenti" è debole.

### Il principio dell'assenza di colpe

L'indagine sui problemi condivide il principio dell'assenza di colpe descritto per i post-mortem nel libro SRE di Google: individuare le cause concorrenti senza incolpare gli individui, perché le persone si possono formare e i sistemi correggere (vedi Argomento 3.2 — Gestione degli incidenti). Un'indagine che trova "errore umano" e si ferma di solito si è fermata troppo presto. Chiedi che cosa ha reso possibile l'errore e che cosa lo renderebbe più difficile.

### Gestione dei problemi in un flusso agile

Un approccio agile pratico è così:

- Incidenti e post-mortem creano problemi candidati.
- Una breve revisione regolare raggruppa gli incidenti ripetuti e ordina i problemi per impatto e frequenza.
- I problemi selezionati entrano nel backlog come elementi ordinari, con un responsabile, un'ipotesi e un limite di tempo per l'indagine.
- I workaround sono registrati come errori noti così che il service desk e gli ingegneri di turno possano usarli (vedi Argomento 3.9 — Gestione della conoscenza).
- Le correzioni sono piccole e testate, rilasciate nel modo normale e verificate dopo per vedere se gli incidenti si sono fermati.

## Buone pratiche

1. **Collega gli incidenti ai problemi.** Registra quali incidenti sembrano avere la stessa causa. Senza collegamenti non vedi lo schema, e senza lo schema non puoi sostenere una correzione.
2. **Rivedi gli incidenti per schemi a scadenza fissa.** Una volta al mese, raggruppa gli incidenti recenti per servizio e causa probabile e scegli i primi. Usa il pensiero di Pareto: poche cause di solito spiegano gran parte del dolore.
3. **Tratta i problemi come elementi del backlog.** Dai a ogni problema selezionato un responsabile, un'enunciazione e un limite di tempo per l'indagine e lascia che competa con altro lavoro. Una coda separata di "problemi" che nessuno programma è un cimitero.
4. **Parti da un'enunciazione chiara del problema.** Scrivi che cosa accade, dove, quanto spesso e quale è l'impatto, usando fatti. Enunciazioni vaghe portano a correzioni vaghe.
5. **Costruisci una cronologia.** Raccogli log, modifiche ed eventi dal funzionamento normale al guasto. L'articolo elenca la cronologia come passaggio centrale, e molte sorprese vengono da modifiche che nessuno aveva collegato.
6. **Cerca la causa che, se rimossa, impedisce la ricorrenza.** Usa il test dell'articolo. Quando il team propone una causa, chiedi se rimuoverla impedirebbe al problema di tornare.
7. **Aspettati più di una causa.** Cerca fattori concorrenti in progettazione, monitoraggio, processo e conoscenza delle persone. Non fermarti alla prima plausibile.
8. **Scegli i metodi adatti al problema.** Usa i cinque perché o una lisca di pesce per una rapida discussione di team e strumenti più rigorosi per guasti gravi o complessi.
9. **Preferisci azioni che cambiano il sistema.** Favorisci automazione, salvaguardie e un monitoraggio migliore rispetto a promemoria e formazione. Registra l'effetto atteso per poterlo verificare.
10. **Registra i workaround come errori noti.** Scrivi che aspetto ha il sintomo, il workaround e chi possiede la correzione. Condividi il record con il service desk e il personale di turno.
11. **Verifica che la correzione abbia funzionato.** Dopo una correzione, osserva la ricorrenza per un periodo concordato e riferisci il risultato. Una correzione mai verificata è una speranza.
12. **Condividi ciò che trovi.** Pubblica brevi riassunti di problemi e correzioni così che altri team possano riconoscere schemi simili.

## Domande da discutere con il team

**Quale incidente continua a tornare, e che cosa pensiamo lo causi?**

Chiedi alle persone di nominare l'incidente di cui sono più stanche. Confronta le risposte. Poi chiedi che cosa ciascuno crede sia la causa e come lo sa. Le convinzioni spesso differiscono, il che mostra quanto poche siano le prove condivise. Chi facilita può chiedere quali dati lo deciderebbero. Scegline uno da indagare con un limite di tempo.

**Come sappiamo se due incidenti hanno la stessa causa?**

Guarda come gli incidenti sono registrati e chiedi se qualcuno potrebbe trovare rapidamente gli incidenti correlati. Le risposte tipiche sono testo libero, memoria o fortuna. Chiedi quale piccola modifica ai record aiuterebbe, come un campo per servizio e causa probabile. Concordane una.

**Che cosa facciamo quando troviamo "errore umano" in una revisione?**

Chiedi un esempio recente. La domanda è se la revisione si è fermata lì. Discuti che cosa nel sistema ha reso possibile l'errore: istruzioni poco chiare, uno strumento confuso, pressione dei tempi. Confronta con l'idea che non si possono correggere le persone ma si possono correggere i sistemi. Concorda una domanda da porre ogni volta, come "Che cosa ha reso facile farlo?".

**Quali azioni delle revisioni passate hanno davvero cambiato il sistema, e quali hanno solo aggiunto un promemoria?**

Elenca le azioni delle ultime cinque revisioni e segna ciascuna come cambiamento del sistema o promemoria. L'articolo dice che promemoria e burocrazia sono meno efficaci. Chiedi perché i promemoria siano così comuni: sono rapidi, economici e danno la sensazione di agire. Scegli un promemoria da sostituire con una correzione più forte.

**Dove abbiamo workaround che nessuno ha messo per iscritto?**

Chiedi agli ingegneri di turno e agli analisti del desk quali trucchi usano. Ogni workaround non scritto è un rischio. Registrali come errori noti con sintomo, workaround e responsabile. Chi facilita può chiedere chi beneficia di ciascun record. Fai un breve elenco questa settimana.

**Come sapremo che una correzione ha funzionato?**

Scegli una correzione recente e chiedi quali prove l'hanno mostrato. Se la risposta è "non ci sono più reclami", chiedi quanto hai aspettato e che cosa hai misurato. Discuti un semplice controllo: osservare lo specifico sintomo per un periodo fisso. Concorda di registrare il controllo con ogni correzione.

## Nella pratica: un esempio di ITIL agile

Un'azienda logistica di medie dimensioni gestisce un servizio di pianificazione dei percorsi usato dai suoi autisti e dai suoi dispatcher. Il team di piattaforma di nove persone ha gestito lo stesso incidente circa ogni due settimane: i calcoli dei percorsi vanno in timeout per dieci-quindici minuti al mattino e poi si riprendono. Ogni volta, l'ingegnere di turno riavvia un processo worker e l'incidente viene chiuso. I dispatcher si lamentano che non ci si può fidare della pianificazione del mattino.

La responsabile del team avvia una revisione mensile degli incidenti, raggruppandoli per servizio e causa probabile. I timeout del mattino sono in cima all'elenco. Scrive un'enunciazione del problema dai record degli incidenti: i timeout avvengono nei giorni feriali tra le 7:00 e le 7:30, durano dieci-quindici minuti e colpiscono tutti i dispatcher. Il team costruisce una cronologia che include un'importazione dati programmata alle 7:00 e una modifica recente che ha aumentato le dimensioni dell'importazione. Una discussione con i cinque perché suggerisce che l'importazione saturi il database. Provano la correzione ovvia, aggiungere capacità, ma gli incidenti continuano a un tasso inferiore, quindi concludono che la capacità era un contributore e non la radice.

Un secondo sguardo scopre che l'importazione blocca una tabella che anche i calcoli dei percorsi leggono. Il team sposta l'importazione su una replica separata e aggiunge un allarme sulle attese dei lock. Registrano il riavvio come errore noto con sintomo e workaround finché la correzione non è attiva e concordano di osservare il sintomo per sei settimane. Gli incidenti si fermano. Restano alcune questioni: un'altra importazione da un partner gira ancora nell'ora di punta, e il team non ha ancora convinto il partner a cambiare orario. Mettono il calendario del partner all'ordine del giorno della prossima pianificazione e mantengono l'allarme sui lock.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery hanno la conoscenza per correggere le cause. Porta i problemi principali nel tuo backlog e trattali come lavoro che guadagna fiducia. Aggiungi monitoraggio e test che avrebbero rivelato la causa e scrivi l'errore noto in un linguaggio che il desk possa usare.

### Team di servizio e di operations

I team operativi vedono gli incidenti e tengono i record. Collega gli incidenti, conduci la revisione mensile e registra i workaround come errori noti. Porta le prove ai team di delivery in una forma che sostenga il caso, con frequenza, impatto e cronologia.

### Leadership e governance

I leader decidono se la correzione dei problemi ottiene tempo. Chiedi i principali problemi ricorrenti e che cosa si sta facendo. Resisti a contare gli incidenti chiusi come misura del successo, perché premia la riparazione. Sostieni le correzioni che richiedono sforzo ma eliminano il dolore.

### Clienti e utenti

Clienti e utenti traggono vantaggio quando i guasti ripetuti si fermano. Segnala i problemi ricorrenti con date ed effetti, perché gli schemi aiutano il team. Chiedi ai fornitori che cosa hanno fatto sulle cause delle interruzioni ripetute e aspettati una risposta che vada oltre "l'abbiamo riavviato".

## Modalità di fallimento comuni

- **Riparazione senza rimozione.** Gli incidenti sono chiusi e ritornano. Collega invece le ripetizioni a un problema e correggi la causa.
- **Una coda di problemi che nessuno programma.** I problemi aspettano per sempre. Metti invece i problemi selezionati nel backlog con responsabili e limiti di tempo.
- **Fermarsi all'errore umano.** La revisione finisce con qualcuno da incolpare. Chiedi invece che cosa ha reso possibile l'errore e correggi il sistema.
- **Azioni deboli.** Promemoria e formazione sostituiscono i cambiamenti di sistema. Preferisci invece automazione, salvaguardie e un monitoraggio migliore.
- **Cercare un'unica causa radice.** Il team insiste su un singolo colpevole. Accetta invece diverse cause concorrenti e affronta le più efficaci.
- **Nessuna verifica che la correzione abbia funzionato.** Il problema è chiuso al rilascio. Definisci invece un modo di vedere se il sintomo ritorna.
- **Workaround non scritti.** La conoscenza vive con gli individui. Registra invece gli errori noti e condividili.
- **Culto del metodo.** I team discutono sulle tecniche. Scegli invece i metodi adatti al problema e spendi lo sforzo sulle prove.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Collegamento e prioritizzazione | Gli incidenti non sono collegati | Alcuni team notano le ripetizioni | Gli incidenti sono collegati ai problemi e rivisti per schemi a scadenza fissa | I problemi sono ordinati per impatto e frequenza misurati | Le priorità dei problemi sono condivise tra team e fornitori |
| Indagine | L'indagine è informale | Alcuni team usano metodi semplici | Si usa un approccio scritto con cronologie e prove | Qualità e tempi dell'indagine sono rivisti | Le indagini attraversano team e fornitori con dati condivisi |
| Azione correttiva | Le correzioni sono estemporanee o promemoria | Alcune correzioni cambiano il sistema | Le azioni sono scelte per effetto, con responsabili e date | Gli effetti sono verificati e la ricorrenza è misurata | Le correzioni si diffondono a sistemi simili in tutta l'organizzazione |
| Errori noti e conoscenza | I workaround non sono scritti | Alcuni sono registrati da singole persone | Gli errori noti sono registrati e condivisi con desk e personale di turno | Uso e accuratezza degli errori noti sono monitorati | Gli errori noti sono condivisi con utenti, fornitori e partner |

## Checklist

- [ ] Gli incidenti che sembrano condividere una causa sono collegati.
- [ ] Una revisione regolare raggruppa gli incidenti e sceglie i principali problemi ricorrenti.
- [ ] I problemi selezionati sono nel backlog con responsabili e limiti di tempo.
- [ ] Ogni problema ha un'enunciazione scritta con fatti.
- [ ] Per ogni indagine viene costruita una cronologia.
- [ ] Le revisioni chiedono che cosa nel sistema ha permesso qualsiasi errore umano.
- [ ] Le azioni favoriscono i cambiamenti di sistema rispetto ai promemoria, con l'effetto atteso registrato.
- [ ] I workaround sono registrati come errori noti e condivisi con il desk e il personale di turno.
- [ ] Ogni correzione ha un controllo della ricorrenza per un periodo concordato.
- [ ] I riassunti di problemi e correzioni sono condivisi con altri team.

## Prompt per l'IA

**Scopo: trovare incidenti ripetuti e problemi candidati nei tuoi record.**

```text
Below are descriptions of [number] incidents from the last [period], with dates and the service affected: [paste anonymized descriptions, one per line].

Group the incidents that look as if they might share a cause, based only on what is written. For each group, list the incidents, give a one-sentence description of the common symptom, and say how confident you are and why (low, medium, high). List incidents that do not fit any group. Do not guess at technical causes beyond the text. Suggest three questions for the team to ask to test each group. List what you are unsure of.
```

**Scopo: scrivere un'enunciazione chiara del problema dalle prove.**

```text
Help me write a problem statement.

What we observe, with dates and counts: [paste facts].
What is affected and who is affected: [describe].
What we know about when it started and what changed around then: [paste, or write "unknown"].
What we have already tried: [paste].

Write a problem statement of three to five sentences that describes what happens, where, how often, and the impact, without naming a cause. Then list the facts we still need and where to find them. Mark anything that is an assumption. Do not suggest causes as facts. List what you are unsure of.
```

**Scopo: preparare una sessione dei cinque perché e registrare la catena di ragionamento.**

```text
Help me prepare a five whys discussion for this problem: [paste the problem statement].

Facts we have: [list evidence such as logs, timelines, and changes].

Prepare: a first "why" question grounded in the evidence, a template where each answer records the evidence for it, and a reminder to branch when there is more than one possible answer. Warn me against stopping at human error. After the session I will paste the notes: do not invent answers yourself. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: valutare se le azioni correttive proposte cambiano il sistema.**

```text
Here are the actions proposed after our review: [paste a list].

For each, say whether it changes the system (for example automates a check, removes a failure mode, adds a safeguard, improves monitoring) or relies on people remembering or on training, and give one sentence of reasoning from the text only. For each reminder-type action, suggest a stronger alternative as a question for the team. Suggest how we could check whether each action worked, without inventing numbers. List what you are unsure of.
```

## Competenze per l'IA

- [root-cause-analysis](../../../../skills/root-cause-analysis/SKILL.md): da usare per guidare un'indagine da un'enunciazione chiara del problema a una causa verificata.
- [fishbone-diagram](../../../../skills/fishbone-diagram/SKILL.md): da usare per fare brainstorming con un team sulle possibili cause per categoria.
- [cause-and-effect-diagram](../../../../skills/cause-and-effect-diagram/SKILL.md): da usare per disporre come cause ed effetti si collegano in un guasto complicato.
- [postmortem](../../../../skills/postmortem/SKILL.md): da usare per condurre la revisione che individua i problemi candidati.
- [six-sigma](../../../../skills/six-sigma/SKILL.md): da usare quando servono metodi basati sui dati per analizzare variazione o difetti ricorrenti.

## Fonti principali

- **Root cause analysis** (Wikipedia): una panoramica generale del metodo, dei principi e dei limiti, con ISO/IEC 31010 elencato per i metodi.
- **Postmortem Culture: Learning from Failure** (*Site Reliability Engineering*, Google, sre.google): l'approccio senza colpe all'apprendimento dai guasti.
- **Managing Incidents** (*Site Reliability Engineering*, Google, sre.google): come la gestione degli incidenti alimenta l'analisi successiva.
- **Ishikawa diagram** e **Five whys** (Wikipedia): contesto su due metodi semplici comuni.

## Riferimenti

1. Root cause analysis — Wikipedia — https://en.wikipedia.org/wiki/Root_cause_analysis
2. Postmortem Culture: Learning from Failure — Google SRE book, sre.google — https://sre.google/sre-book/postmortem-culture/
3. Managing Incidents — Google SRE book, sre.google — https://sre.google/sre-book/managing-incidents/
4. Five whys — Wikipedia — https://en.wikipedia.org/wiki/Five_whys
5. Ishikawa diagram — Wikipedia — https://en.wikipedia.org/wiki/Ishikawa_diagram
6. Failure mode and effects analysis — Wikipedia — https://en.wikipedia.org/wiki/Failure_mode_and_effects_analysis
7. Fault tree analysis — Wikipedia — https://en.wikipedia.org/wiki/Fault_tree_analysis
8. Pareto analysis — Wikipedia — https://en.wikipedia.org/wiki/Pareto_analysis
9. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
10. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
