# La catena del valore del servizio

**La catena del valore del servizio è un insieme di sei attività che i team combinano in ordini diversi per creare flussi di valore, e descrive come la consegna continua e l'esercizio del servizio si inseriscano in un unico flusso anziché in due separati.**

## Perché è importante

Molte organizzazioni trattano costruire e gestire come due fasi: prima un progetto costruisce il servizio, poi un gruppo operativo lo prende in carico. Il passaggio di consegne è il punto in cui si perde conoscenza, la responsabilità si sfuma e i clienti avvertono il divario. La catena del valore del servizio di ITIL 4 è stata progettata per sostituire quell'immagine con una in cui le stesse attività possono avvenire in qualsiasi ordine e tutte le volte che serve, a seconda della situazione.

È vicino a come i team agili già lavorano. In una settimana, un team può pianificare una funzionalità, costruirne una parte, rilasciarla, rispondere a una domanda di un cliente su di essa e correggere un problema trovato in produzione. Ciascuna di queste è un'attività diversa della catena. Vederle come parti di un unico flusso aiuta un team a chiedersi dove il lavoro aspetta, chi svolge ciascuna attività e quali attività vengono trascurate.

Questo argomento descrive le sei attività, come si combinano in flussi di valore e come un team agile può usare l'idea. I riassunti vengono da un fornitore di formazione e da un fornitore di software, perché le pagine pubbliche del proprietario del framework lette per questa guida nominano la catena del valore del servizio solo di passaggio. La pagina del fornitore elenca le attività senza descriverle, quindi considera le descrizioni seguenti come letture diffuse e controlla le pubblicazioni ITIL 4 per la formulazione del proprietario (vedi Argomento 2.2 — ITIL).

## Concetti fondamentali

### Dove si colloca la catena

Nel sistema di valore del servizio, la catena è il modello operativo al centro (vedi Argomento 2.3 — Il sistema di valore del servizio ITIL). La pagina di un fornitore la descrive come la parte del sistema che riguarda la pipeline di consegna o il ciclo di vita di un prodotto o servizio, che prende la domanda come input e produce valore come output. Nota anche che nella pratica il ciclo di vita è raramente lineare.

### Le sei attività

La tabella dà ciascuna attività, lo scopo che la pagina di un fornitore di formazione le attribuisce e che aspetto ha l'attività in un team agile. La colonna di destra è una lettura di questa guida.

| Attività | Scopo, come lo riassume un fornitore di formazione | Che aspetto può avere in un team agile |
|---|---|---|
| **Pianificare** | Definisce politiche, obiettivi e linee guida per la direzione dell'organizzazione, così che tutti condividano una comprensione di visione, stato attuale e direzione di miglioramento | Obiettivi di prodotto, roadmap, pianificazione trimestrale e scelte di portfolio |
| **Migliorare** | Migliora continuamente servizi, pratiche e processi in tutte le attività | Retrospettive, revisioni post-incidente ed elementi di miglioramento nel backlog |
| **Coinvolgere** | Interagisce con gli stakeholder per capire i bisogni, fornire informazioni, raccogliere feedback e requisiti e gestire le relazioni | Ricerca sugli utenti, sprint review, service desk e conversazioni con i clienti |
| **Progettare e fare transizione** | Assicura che servizi nuovi o modificati soddisfino le aspettative degli stakeholder, dalla progettazione all'ambiente live | Progettare una modifica, testarla e prepararla per il rilascio e il supporto |
| **Ottenere/costruire** | Acquisisce o crea i componenti necessari per i servizi, come risorse fisiche, infrastruttura, conoscenza o software | Sviluppare software, acquistare uno strumento, preparare l'infrastruttura, formare il personale |
| **Erogare e supportare** | Eroga i servizi come concordato e fornisce supporto continuo per risolvere problemi e soddisfare richieste | Gestire il servizio, trattare incidenti e richieste, installare i rilasci |

### Le attività non sono fasi

La pagina del fornitore di formazione dice che le attività "are not linear but are interlinked and can be combined in various ways to form multiple value streams". Un **flusso di valore**, nelle sue parole, è uno specifico insieme di attività che creano e consegnano ai clienti un particolare servizio o prodotto. È l'idea centrale. La catena è un menù di attività, e un flusso di valore è un percorso al suo interno scelto per uno scopo particolare.

### Flussi di valore a titolo illustrativo

Le pagine lette per questa guida non danno flussi di valore di esempio, quindi i seguenti sono illustrazioni di questa guida su come le attività potrebbero combinarsi. Non provengono da pubblicazioni ITIL, e un flusso reale sarà diverso.

| Flusso di valore | Un possibile percorso attraverso le attività |
|---|---|
| **Gestire un incidente** | Coinvolgere (un utente lo segnala) → erogare e supportare (ripristinare il servizio) → migliorare (rivedere e correggere la causa) |
| **Rilasciare una funzionalità** | Pianificare (decidere l'obiettivo) → progettare e fare transizione (progettare, testare, preparare il supporto) → ottenere/costruire (sviluppare) → erogare e supportare (rilasciare) → coinvolgere (ottenere feedback) → migliorare |
| **Evadere una richiesta di accesso** | Coinvolgere (richiesta ricevuta) → erogare e supportare (verificare e concedere l'accesso) → coinvolgere (confermare con l'utente) |
| **Inserire un nuovo fornitore** | Pianificare (decidere il bisogno) → coinvolgere (selezionare e concordare i termini) → ottenere/costruire (integrare) → erogare e supportare (gestire) → migliorare (rivedere le prestazioni) |

### Pratiche e catena

Le pratiche sono le capacità a cui le attività attingono. La gestione degli incidenti, per esempio, è una pratica usata all'interno di più flussi di valore. Le fonti non concordano su ogni dettaglio dell'associazione tra pratiche e attività, quindi evita una tabella rigida. Un test migliore è se una pratica contribuisce al flusso di valore che stai esaminando (vedi Parte 3).

### Flussi di valore e flusso agile

Il pensiero agile e lean già usa i flussi di valore (vedi Argomento 1.7 — Sviluppo software lean). Una mappa del flusso di valore mostra passaggi, tempi e attese in un percorso. L'idea di ITIL aggiunge un vocabolario per classificare i passaggi e un promemoria che il percorso include supporto e miglioramento oltre alla costruzione. Per il lavoro digitale, questo si collega alla gestione del flusso di valore (vedi Argomento 5.4 — Gestione del flusso di valore).

### Limiti

Le pagine lette per questa guida non danno un metodo per progettare o selezionare i flussi di valore, e la pagina del fornitore non spiega come la catena si colleghi al miglioramento continuo oltre a definire il miglioramento cruciale. La catena è un modo di descrivere il lavoro, non un modo di decidere come svolgerlo. Il suo valore dipende dal fatto che la usi per guardare flussi reali.

## Buone pratiche

1. **Scegli un flusso di valore e disegnalo.** Scegli un flusso importante per i clienti, come rilasciare una modifica o gestire una richiesta. Elenca i passaggi in ordine ed etichetta ciascuno con la più vicina delle sei attività.
2. **Includi supporto e miglioramento nel quadro.** Non fermare il flusso al rilascio. Mostra che cosa accade dopo: gestire gli incidenti e imparare da essi.
3. **Cerca le attività mancanti.** Se un flusso non ha un passaggio di coinvolgimento, nessuno parla con gli utenti. Se non ha un passaggio di miglioramento, non si impara nulla. Aggiungili dove contano.
4. **Cronometra le attese.** Per un flusso, registra quanto il lavoro aspetta tra le attività e dove attraversa il confine di un team. L'attesa più lunga è la prima cosa da esaminare (vedi Argomento 5.4 — Gestione del flusso di valore).
5. **Combina le attività liberamente.** Permetti a flussi diversi di usare percorsi diversi. La correzione di un bug minore può passare direttamente da erogare e supportare a ottenere/costruire e tornare indietro, senza un passaggio di pianificazione.
6. **Metti progettazione e transizione nel lavoro del team.** Includi note di supporto, monitoraggio e formazione come parte della costruzione, non come passaggio di consegne alla fine (vedi Argomento 3.5 — Gestione di rilasci e deployment).
7. **Fai del "coinvolgere" un'attività continua.** Non limitare il contatto con gli utenti all'inizio e alla fine di un progetto. Includi service desk e feedback dei clienti nella pianificazione.
8. **Collega la pianificazione alle prove delle operations.** Usa i dati di incidenti e richieste nelle conversazioni di pianificazione così che gli obiettivi riflettano ciò che gli utenti vivono davvero (vedi Argomento 5.1 — Gestione agile dei servizi).
9. **Nomina un responsabile per ogni flusso.** Una persona dovrebbe poter dire come il flusso funziona e dovrebbe poter riunire i team per migliorarlo.
10. **Usa la catena come checklist delle lacune.** Quando qualcosa fallisce, chiedi quale attività era debole: piano poco chiaro, coinvolgimento scarso, transizione affrettata, costruzione debole, supporto traballante o nessun miglioramento.
11. **Mantieni semplice il diagramma.** Uno schizzo approssimativo con sei etichette basta. Se il disegno ha bisogno di una legenda, semplificalo.
12. **Rivedi i flussi dopo i cambiamenti.** Quando cambiano strutture dei team, fornitori o strumenti, verifica se i flussi funzionano ancora come disegnati.

## Domande da discutere con il team

**Quali sono i tre flussi di valore più importanti per i nostri utenti, e chi è responsabile di ciascuno?**

Chiedi alle persone di nominare i flussi che contano di più, come un utente che ottiene un nuovo account o una correzione che arriva in produzione. Confronta gli elenchi. Le differenze mostrano che il team ha immagini diverse di ciò che conta. Chi facilita può chiedere chi saprebbe rispondere per ogni flusso da un capo all'altro. Spesso nessuno, il che è un risultato.

**Per un flusso, quali delle sei attività facciamo bene e quali saltiamo?**

Disegna il flusso ed etichetta i passaggi. Poi cerca le attività mancanti. I team spesso scoprono di pianificare e costruire bene, e di coinvolgere e migliorare male. Chiedi che cosa aggiungerebbe l'attività mancante e quanto costerebbe. Scegline una da aggiungere su piccola scala.

**Dove aspetta il lavoro tra le attività, e chi è responsabile dell'attesa?**

Segna i passaggi di consegne e annota le attese tipiche. Molte attese stanno al confine tra team. Chiedi se l'attesa serve, per esempio per un controllo del rischio, o se è un accidente di come sono organizzati i team. Scegline una da accorciare.

**Come scopriamo che cosa pensano gli utenti di ciò che consegniamo, e con quale rapidità cambia i nostri piani?**

Ripercorri un recente feedback dall'utente al backlog. Conta i passaggi. Se ci sono volute settimane o non è mai arrivato, l'attività di coinvolgimento è debole. Chiedi che cosa accorcerebbe il percorso, come un canale condiviso con il service desk. Concorda un cambiamento.

**Che cosa facciamo dopo un incidente o un rilascio per migliorare il successivo?**

Guarda gli ultimi incidenti e rilasci per un miglioramento registrato. Se non c'è, l'attività di miglioramento è informale. Chiedi chi possiede le azioni di miglioramento e come sono monitorate. Concorda un posto semplice dove registrarle.

**Quali flussi attraversano i confini organizzativi, e chi parla per l'intero?**

Elenca i flussi che coinvolgono fornitori, altri reparti o clienti. Chiedi chi è responsabile del flusso end-to-end e che cosa accade ai confini. Un buon esito è nominare un coordinatore e una conversazione regolare attraverso il confine.

## Nella pratica: un esempio di ITIL agile

Un gruppo ospedaliero regionale gestisce un servizio di portale dei pazienti usato per prenotare appuntamenti e consultare i risultati degli esami. Lo costruisce e lo gestisce un team di dieci persone. Il team rilascia nuove funzionalità ogni due settimane, ma i pazienti si lamentano che le correzioni dei guasti segnalati richiedono mesi e che non ricevono risposta ai loro messaggi di feedback.

La responsabile dei servizi digitali chiede al team di disegnare il flusso di valore per un guasto segnalato, dal messaggio del paziente a una correzione in produzione. Etichettano i passaggi con le sei attività. Il messaggio arriva da un modulo di contatto (coinvolgere) e resta in una casella condivisa per giorni prima che qualcuno lo smisti. Un guasto smistato finisce nello stesso backlog delle nuove funzionalità (pianificare), dove compete male. Una correzione viene costruita (ottenere/costruire), testata e rilasciata con il successivo gruppo di funzionalità (progettare e fare transizione, erogare e supportare). Nessuno informa il paziente (coinvolgere), e nessuno registra che cosa il guasto ha insegnato al team (migliorare).

Il team cambia il flusso. La casella condivisa viene controllata ogni giorno a turno, i guasti sono etichettati e hanno una corsia separata nel backlog con l'obiettivo del rilascio successivo, il paziente riceve una risposta alla ricezione e un'altra quando la correzione è attiva, e ogni guasto più vecchio di un mese viene discusso nella revisione quindicinale. Dopo due mesi, il tempo mediano di correzione scende e i reclami dei pazienti sul silenzio calano. Restano problemi: i guasti che riguardano il sistema di prenotazione dell'ospedale, gestito da un fornitore, aspettano ancora la coda del fornitore, e i messaggi di risposta sono scritti dagli sviluppatori in un linguaggio che alcuni pazienti trovano difficile da seguire. Il team invita il fornitore alla revisione e chiede al team comunicazione di redigere modelli in linguaggio semplice.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery di solito dedicano più tempo a pianificare, progettare e fare transizione e ottenere/costruire. Guarda le altre tre: come coinvolgi gli utenti, come supporti ciò che rilasci e come migliori. Tratta le richieste di supporto e l'apprendimento dagli incidenti come input alla pianificazione.

### Team di servizio e di operations

I team operativi dedicano più tempo a erogare e supportare e a parti del coinvolgere. Usa la catena per mostrare come il tuo lavoro dipenda da attività precedenti, come progettare e fare transizione, e per chiedere ciò di cui hai bisogno. Partecipa alla pianificazione così che la conoscenza operativa raggiunga l'inizio del flusso.

### Leadership e governance

I leader possono usare la catena per chiedere dove il flusso si rompe per i servizi importanti. Sostieni la nomina dei responsabili dei flussi e dai loro l'autorità di riunire i team. Evita di trasformare le sei attività in sei reparti; il punto è collegarle.

### Clienti e utenti

Clienti e utenti partecipano soprattutto al coinvolgere, e traggono vantaggio quando il feedback arriva fino a piani e correzioni. Aspettati risposte e risultati visibili. Di' al fornitore quale flusso conta di più per te e quali ritardi ti danneggiano.

## Modalità di fallimento comuni

- **Leggere la catena come una sequenza.** I team forzano ogni lavoro attraverso tutte e sei in ordine. Scegli invece percorsi adatti al lavoro.
- **Mappare reparti, non flussi.** Ogni attività viene assegnata a un reparto e il flusso si perde. Ripercorri invece un lavoro attraverso di essi.
- **Dimenticare coinvolgere e migliorare.** Il flusso finisce al rilascio. Includi invece contatto con gli utenti e apprendimento in ogni flusso.
- **Passaggio di consegne al posto di progettare e fare transizione.** Note di supporto, monitoraggio e formazione sono lasciati alla fine. Incorporali invece nel lavoro fin dall'inizio.
- **Nessun responsabile del flusso.** Nessuno sa dire come il flusso funziona. Nomina invece un responsabile con l'autorità di convocare i team.
- **Diagrammi troppo dettagliati.** La mappa diventa un poster che nessuno legge. Mantienila invece a una pagina e aggiornala quando qualcosa cambia.
- **Trattare il vocabolario come scopo.** I team spendono tempo a etichettare e non a migliorare. Etichetta invece solo ciò che aiuta a trovare una lacuna.
- **Affidarsi a riassunti secondari.** Le descrizioni delle attività differiscono tra le fonti. Controlla invece le pubblicazioni del proprietario quando serve precisione.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Visibilità dei flussi di valore | I flussi sono noti solo in modo informale | Alcuni flussi sono disegnati dai loro team | I flussi chiave sono mappati con responsabili | I flussi sono misurati per attese e risultati | I flussi attraversano i confini organizzativi e sono migliorati insieme |
| Copertura delle attività | Dominano pianificazione e costruzione | Alcuni team aggiungono attività di coinvolgimento e miglioramento | Tutte e sei le attività compaiono nei flussi chiave | Le lacune di copertura sono monitorate e colmate | La copertura è bilanciata tra team e fornitori in base alle prove |
| Passaggi di consegne e transizione | I passaggi di consegne sono tardivi e non gestiti | Alcuni team includono il supporto nella costruzione | Supporto, monitoraggio e formazione fanno parte di ogni rilascio | I problemi di transizione sono misurati e ridotti | La transizione è condivisa tra delivery, operations e fornitori |
| Feedback e miglioramento | Il feedback arriva sotto forma di reclamo | Una parte del feedback raggiunge il backlog | Feedback ed elementi di miglioramento sono tracciati con responsabili | Gli effetti dei miglioramenti sono verificati | Feedback e apprendimento fluiscono continuamente tra team e clienti |

## Checklist

- [ ] Abbiamo disegnato almeno un flusso di valore importante per gli utenti.
- [ ] Ogni passaggio del disegno è etichettato con la più vicina attività della catena del valore.
- [ ] Il flusso include il coinvolgimento degli utenti e un passaggio che registra i miglioramenti.
- [ ] Sappiamo dove aspetta il lavoro e per quanto tempo, almeno approssimativamente.
- [ ] Il lavoro di progettazione e transizione, come monitoraggio e note di supporto, fa parte della costruzione.
- [ ] Una persona nominata è responsabile del flusso end-to-end.
- [ ] Il feedback degli utenti raggiunge il backlog e riceve una risposta.
- [ ] I dati di incidenti e richieste sono usati nella pianificazione.
- [ ] Il flusso è rivisto dopo cambiamenti significativi.
- [ ] Abbiamo controllato la pubblicazione del proprietario per la definizione esatta di ciascuna attività.

## Prompt per l'IA

**Scopo: etichettare i passaggi di un flusso reale con le sei attività.**

```text
Help me label the steps of a value stream with the six ITIL service value chain activities: plan; improve; engage; design and transition; obtain/build; deliver and support.

The stream (what it delivers and to whom): [describe].
The steps in order, with who does each and how long it waited before it, if known: [paste].

For each step, suggest the closest activity and give one sentence of reasoning using only my text. Then list which of the six activities do not appear, and what that might mean, as questions and not conclusions. Do not invent steps or durations. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: trovare dove il feedback si perde sulla strada verso il backlog.**

```text
I want to trace how user feedback reaches our backlog.

Where feedback arrives (channels): [list].
What happens to a piece of feedback after it arrives, step by step, with who does each step: [paste].
One recent example, with dates: [paste].

Describe the path in order and identify steps where the feedback could be lost or delayed, using only my text. Suggest three questions for the people involved and one small change to shorten the path. Do not invent causes. Ask clarifying questions first if information is missing, and list what you are unsure of.
```

**Scopo: pianificare un workshop sui flussi di valore con personale di delivery e di operations.**

```text
Plan a 90-minute workshop for [number] people from delivery and operations to draw one value stream: [stream name].

Preparation: they will bring [data, such as dates of recent examples].
Constraints: [for example remote, different time zones].

Give a timed agenda, instructions for drawing the stream step by step, how to label steps with the six value chain activities, a way to mark waits and handovers, and a closing step to agree one change with an owner and date. Keep it free of any particular tool. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: scrivere una breve guida alla catena del valore per i nuovi membri del team.**

```text
Write a one-page guide to the ITIL service value chain for new team members.

Use only these notes, which I verified: [paste the six activity names and the descriptions you have checked against official sources, plus any examples from our own work].

Include: what the chain is for, one example stream from our work, and three questions a new person can ask to find which activity a task belongs to. Keep the language plain. Do not add claims about ITIL beyond my notes. Mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [value-stream-map](../../../../skills/value-stream-map/SKILL.md): da usare per disegnare un flusso, cronometrarne le attese ed etichettarne i passaggi.
- [workflow-analysis](../../../../skills/workflow-analysis/SKILL.md): da usare per analizzare come il lavoro si muove tra i ruoli e trovare problemi nei passaggi di consegne.
- [agile-delivery](../../../../skills/agile-delivery/SKILL.md): da usare per pianificare come un team consegna a piccoli passi attraverso le attività di costruzione e rilascio.
- [getting-feedback](../../../../skills/getting-feedback/SKILL.md): da usare per progettare modi di raccogliere feedback dagli utenti per l'attività di coinvolgimento.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): da usare per condurre le revisioni che rendono reale l'attività di miglioramento.

## Fonti principali

- **ITIL 4 Foundation** (PeopleCert): la pagina del proprietario che nomina la catena del valore del servizio tra gli argomenti studiati.
- **ITIL service value system** (Purple Griffon): il riassunto delle sei attività e dei flussi di valore di un fornitore di formazione; secondario.
- **The ITIL 4 Service Value System** (ManageEngine): il riassunto di un fornitore che nomina le attività; secondario.
- **Value-stream mapping** (Wikipedia): contesto sulla tecnica di mappatura che la pratica lean usa per trovare gli sprechi.

## Riferimenti

1. ITIL 4 Foundation — PeopleCert — https://www.peoplecert.org/browse-certifications/it-governance-and-service-management/ITIL-1/itil-4-foundation-2565
2. ITIL service value system — Purple Griffon (training provider; secondary source) — https://purplegriffon.com/blog/itil-service-value-system
3. The ITIL 4 Service Value System — ManageEngine (software vendor; secondary source) — https://manageengine.com/products/service-desk/itsm/itil-4-service-value-system.html
4. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
5. Value-stream mapping — Wikipedia — https://en.wikipedia.org/wiki/Value-stream_mapping
6. Value chain — Wikipedia — https://en.wikipedia.org/wiki/Value_chain
7. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
8. Business process management — Wikipedia — https://en.wikipedia.org/wiki/Business_process_management
9. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
