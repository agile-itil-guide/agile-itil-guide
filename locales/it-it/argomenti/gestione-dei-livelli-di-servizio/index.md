# Gestione dei livelli di servizio

**La gestione dei livelli di servizio trasforma ciò di cui gli utenti hanno bisogno in obiettivi che un team può misurare e difendere, e la forma più utile per i team agili è un piccolo numero di obiettivi centrati sull'utente con un budget esplicito per il fallimento.**

## Perché è importante

Ogni servizio ha un livello di qualità, che qualcuno l'abbia misurato o no. Se non è dichiarato, gli utenti ne presumono uno e il team un altro, e il divario si scopre durante un'interruzione. La gestione dei livelli di servizio è la pratica di dichiarare il livello, misurarlo e agire sui risultati. Dà a un team qualcosa con cui orientarsi e ai clienti qualcosa su cui contare.

I team agili spesso resistono ai livelli di servizio perché li associano a contratti e penali. Eppure un team agile che rilascia ogni settimana sta prendendo una decisione, lo sappia o no, su quanto rischio assumere sulla disponibilità. Un obiettivo chiaro rende esplicita quella decisione. Il libro *Site Reliability Engineering* di Google, nel capitolo sugli obiettivi di livello di servizio, descrive come farlo in un modo adatto ai team che si muovono in fretta: scegliere pochi indicatori che contano per gli utenti, fissare obiettivi e usare lo spazio tra perfetto e accettabile, l'error budget, per decidere quando rilasciare.

Questo argomento combina quel capitolo con l'[articolo di Wikipedia sugli accordi sul livello di servizio](https://en.wikipedia.org/wiki/Service-level_agreement) per le definizioni degli accordi e con il vocabolario ITIL di uso comune che questa guida non ha potuto confermare rispetto al testo del proprietario del framework. Il capitolo SRE riflette la pratica di un'organizzazione e sostiene un approccio specifico; leggilo come un'opzione ben spiegata, non come una regola universale.

## Concetti fondamentali

### Indicatore, obiettivo, accordo

Il capitolo SRE distingue tre termini spesso confusi:

| Termine | Significato | Esempio |
|---|---|---|
| **Service level indicator (SLI)** | Una misura quantitativa definita con cura di qualche aspetto del livello di servizio | La frazione di richieste ben formate che hanno successo |
| **Service level objective (SLO)** | Un valore o intervallo obiettivo per un SLI | Almeno il 99,9% delle richieste ha successo nell'arco di un mese |
| **Service level agreement (SLA)** | Un contratto esplicito o implicito con gli utenti che include conseguenze per il rispetto o il mancato rispetto degli obiettivi, più spesso finanziarie | Un rimborso se la disponibilità scende sotto un livello dichiarato |

Il test del capitolo per distinguere uno SLA da uno SLO è se esiste una conseguenza esplicita. Se no, è uno SLO. I numeri d'esempio nella tabella sono illustrazioni, non raccomandazioni.

L'articolo di Wikipedia descrive uno SLA come un accordo, tipicamente un contratto vincolante, tra un fornitore e un cliente che definisce aspetti del servizio come qualità, disponibilità e responsabilità. Elenca i contenuti tipici: una descrizione del servizio, livelli di prestazione, monitoraggio e reporting, come si segnalano i problemi, tempi di risposta e risoluzione e conseguenze per l'inadempimento. Nomina metriche comuni come tempo medio tra i guasti, tempo medio di riparazione, uptime, risoluzione alla prima chiamata e tempo di evasione. Nota che le grandi organizzazioni usano spesso SLA interni tra unità. Descrive i tipi per ambito: basati sul cliente, basati sul servizio e multilivello.

### Scegliere gli indicatori

Il capitolo SRE consiglia di scegliere pochi indicatori che riflettano ciò a cui gli utenti tengono, non ogni metrica che puoi monitorare. I sistemi rivolti agli utenti di solito si concentrano su disponibilità, latenza e throughput. I sistemi di archiviazione aggiungono la durabilità, e tutti i sistemi dovrebbero monitorare la correttezza. Suggerisce che la misurazione lato client può cogliere problemi che le metriche lato server perdono. Una conseguenza pratica per i team di servizio: parti dall'esperienza dell'utente, come "posso prenotare un appuntamento e ci vogliono pochi secondi", poi trova un indicatore che la approssimi.

### Le medie nascondono il dolore

Il capitolo sostiene di non affidarsi alle medie: "Most metrics are better thought of as distributions rather than averages". I percentili alti, come il 99° o il 99,9°, mostrano i plausibili casi peggiori, mentre la mediana mostra il caso tipico. Le medie possono nascondere una lunga coda di richieste lente. Se la tua misura è una media, alcuni utenti potrebbero vivere un momento molto brutto senza che il numero si muova.

### Scegliere gli obiettivi

Le indicazioni del capitolo sugli obiettivi sono dirette e utili:

- **Parti dagli utenti.** "Start by thinking about (or finding out!) what your users care about, not what you can measure."
- **Non ancorarti alle prestazioni attuali.** Scegliere un obiettivo in base a ciò che ottieni ora può cristallizzare uno sforzo eroico.
- **Mantieni semplice.** Le aggregazioni complicate oscurano i cambiamenti e sono più difficili da ragionare.
- **Evita gli assoluti.** Promesse di disponibilità "sempre" non sono realistiche.
- **Abbi il minor numero possibile di SLO.** Ciascuno dovrebbe valere la pena di essere difeso in una discussione sulle priorità.
- **La perfezione può aspettare.** È meglio partire da un obiettivo largo che si stringe che da uno che poi deve essere allentato.

### Error budget

Il capitolo dice che richiedere il 100% di conformità non è realistico e rallenta l'innovazione. I team ammettono invece un **error budget**: il tasso con cui uno SLO può essere mancato, monitorato giornalmente, settimanalmente o mensilmente. Il budget informa le decisioni sui rilasci. Quando resta molto budget, un team può prendere più rischio con il cambiamento; quando è quasi esaurito, il team rallenta il cambiamento e investe nell'affidabilità. Questo dà ai team agili e alle operations un modo condiviso e numerico di discutere di velocità contro stabilità, al posto della discussione per autorità.

### Fissare le aspettative

Il capitolo nota che pubblicare uno SLO fissa le aspettative degli utenti. I team possono mantenere un margine di sicurezza con un obiettivo interno più stretto. Mette in guardia anche dall'eccedere, perché gli utenti vengono a dipendere da qualunque prestazione osservino. Se un servizio è molto migliore del suo obiettivo dichiarato, gli utenti ci costruiranno sopra, e l'obiettivo non protegge più il team.

### Il ciclo di controllo

Il capitolo descrive SLI e SLO come la base di un ciclo di controllo: monitorare gli SLI, confrontarli con gli SLO, decidere se serve un'azione, stabilire quale azione raggiungerà l'obiettivo e intraprenderla. Senza uno SLO, un team non può dire se o quando agire (vedi Argomento 3.10 — Monitoraggio e gestione degli eventi).

### Accordi interni ed esterni

Uno SLA è tra un fornitore e un cliente. All'interno di un fornitore, i team dipendono l'uno dall'altro e dai fornitori. L'articolo di Wikipedia menziona che gli SLA possono essere sostenuti da accordi a livello operativo (OLA) ma non li spiega. Nel vocabolario ITIL, un OLA è un accordo tra team interni che sostiene uno SLA, e un contratto di supporto (underpinning contract) è l'equivalente con un fornitore esterno. Le fonti lette qui non confermano queste definizioni, quindi verificale sulle pubblicazioni ITIL. Il punto pratico è che una promessa a un cliente vale quanto le promesse che ci stanno dietro (vedi Argomento 3.14 — Gestione dei fornitori).

### Aspettative di livello di servizio in Kanban

In Kanban, un'**aspettativa di livello di servizio** (service level expectation) è una previsione di quanto tempo dovrebbe richiedere un elemento di lavoro, basata sui cycle time passati (vedi Argomento 1.5 — Kanban). Non è un accordo, ma serve uno scopo simile per gli elementi di lavoro e può alimentare gli obiettivi per richieste e incidenti.

## Buone pratiche

1. **Parti da ciò di cui gli utenti hanno bisogno.** Chiedi a utenti e clienti che cosa conta di più e che cosa fa male quando fallisce. Scrivilo con le loro parole prima di scegliere una misura.
2. **Scegli pochi indicatori.** Per ogni servizio, scegli da due a quattro indicatori che riflettano l'esperienza dell'utente, come tasso di successo e velocità. Resisti ad aggiungerne finché non hai usato questi.
3. **Usa i percentili per la velocità.** Misura l'estremità lenta della distribuzione, non solo la media, così che gli utenti con una brutta esperienza siano visibili.
4. **Fissa prima obiettivi larghi, poi stringi.** Inizia con un obiettivo che puoi raggiungere e difendere e stringilo quando hai dati e fiducia. Segue il consiglio del capitolo che la perfezione può aspettare.
5. **Non copiare le prestazioni attuali.** Se il tuo servizio è attualmente eccellente, non fissare un obiettivo a quel livello a meno che gli utenti ne abbiano bisogno. Un obiettivo più largo dà spazio al cambiamento ed evita lo sforzo eroico.
6. **Concorda un error budget e usalo.** Definisci quanto fallimento è accettabile in un periodo e lascia che il budget residuo guidi le decisioni sui rilasci. Rivedilo in una riunione regolare con delivery e operations insieme.
7. **Scrivi l'accordo in linguaggio semplice.** Uno SLA dovrebbe dire che cosa viene fornito, come si misura, come si segnalano i problemi, che cosa succede quando gli obiettivi sono mancati e quando viene rivisto. Evita termini che solo un avvocato o un ingegnere sa leggere.
8. **Separa gli obiettivi dagli accordi.** Mantieni obiettivi interni più stretti degli accordi che firmi. Il margine ti dà spazio di reagire prima di dover qualcosa.
9. **Sappi da che cosa dipende la tua promessa.** Elenca i team e i fornitori da cui dipende il tuo livello di servizio e verifica che i loro impegni sostengano il tuo.
10. **Riferisci in una forma che i clienti possano usare.** Condividi regolarmente i risultati, con un breve commento su che cosa è successo e che cosa stai facendo. Evita cruscotti senza commento.
11. **Rivedi gli obiettivi con i clienti.** Almeno ogni anno, chiedi se i livelli corrispondono ancora a ciò di cui i clienti hanno bisogno e a ciò che puoi consegnare. Cambiali quando la risposta è no.
12. **Non usare i livelli di servizio per punire le persone.** Usali per avviare conversazioni e decisioni. Un obiettivo usato come bastone sarà manipolato (vedi Argomento 5.6 — Metriche e misurazione).

## Domande da discutere con il team

**Che aspetto ha una buona giornata per i nostri utenti, e come lo sapremmo?**

Chiedi al team di descrivere, con le parole dell'utente, che cos'è una buona esperienza del servizio. Poi chiedi che cosa misuriamo che vi corrisponda. Spesso le misure che abbiamo descrivono i nostri sistemi e non l'esperienza dell'utente. Chi facilita può chiedere se ci accorgeremmo che un gruppo di utenti ha avuto una brutta giornata. Scegli un indicatore da aggiungere o cambiare.

**Abbiamo un numero che promettiamo o a cui puntiamo, e chi l'ha concordato?**

Elenca gli obiettivi esistenti, formali o informali. Per ciascuno, chiedi chi l'ha fissato, quando e su quale base. Molti obiettivi si rivelano fissati per abitudine o da qualcuno che se n'è andato. Discuti quali vanno confermati, cambiati o abbandonati. Concorda chi possiede ciascuno.

**Quanto fallimento ci possiamo permettere, e che cosa faremmo con lo spazio?**

Introduci l'idea di error budget. Chiedi quale livello di indisponibilità gli utenti tollererebbero e che cosa il team potrebbe fare con lo spazio, come rilasci più rapidi. Lo scopo è vedere il compromesso in numeri. Non aspettarti risposte precise; chiedi una prima stima da mettere alla prova.

**Dove le nostre medie nascondono brutte esperienze?**

Guarda una misura che riporta una media. Chiedi che cosa vive l'1% più lento degli utenti. Se non lo sai, discuti come scoprirlo. Spesso un piccolo gruppo di utenti o una particolare ora del giorno ha un'esperienza molto peggiore. Pianifica di guardare un percentile per un mese.

**Da che cosa dipendiamo che non abbiamo chiesto?**

Elenca i servizi, i fornitori e i team su cui il tuo servizio fa affidamento. Per ciascuno, chiedi che cosa hanno promesso e come sapresti se hanno mancato. Molte dipendenze non hanno un livello dichiarato. Scegli la più importante e apri una conversazione.

**Quando è cambiato l'ultimo obiettivo, e che cosa l'ha innescato?**

Chiedi l'ultimo cambiamento. Se è stato molto tempo fa, chiedi che cosa è cambiato da allora nelle esigenze degli utenti o nella capacità del team. Discuti una revisione regolare. Buoni inneschi sono nuove esigenze degli utenti, incidenti che hanno mostrato un obiettivo irrealistico o un cambiamento di architettura.

## Nella pratica: un esempio di ITIL agile

Un gestore nazionale della lotteria gestisce un servizio online di acquisto dei biglietti. Lo costruisce e lo gestisce un team di dodici persone. L'azienda ha una regola informale per cui il servizio deve essere "sempre attivo", mentre il team rilascia due volte alla settimana e ha avuto quattro brevi interruzioni in un anno. Dopo un brutto fine settimana, lo sponsor esecutivo pretende "disponibilità al 100%", e il responsabile del team teme che questo metta fine ai rilasci frequenti.

Il responsabile del team e lo sponsor tengono un workshop con la responsabile del servizio clienti. Chiedono che cosa conta per i giocatori. La risposta è che i giocatori devono poter acquistare un biglietto nell'ora prima della chiusura di un'estrazione; fuori da quell'ora il servizio può essere fermo per qualche minuto senza danni. Definiscono un indicatore: la quota di tentativi di acquisto che riescono nelle due ore prima della chiusura di ogni estrazione. Fissano un obiettivo che il team ritiene di poter raggiungere, un po' sotto le sue prestazioni recenti, e concordano un error budget per ogni mese. Concordano anche che quando il budget è quasi esaurito, i rilasci che toccano gli acquisti si fermano fino al mese successivo e il team investe nell'affidabilità.

Tre mesi dopo il budget viene esaurito una volta, in un mese con un guasto del fornitore dei pagamenti, e il team sospende i rilasci rischiosi per due settimane senza conflitti. L'obiettivo dà al team e allo sponsor un modo condiviso di parlare. Restano alcune difficoltà. L'impegno del fornitore dei pagamenti è più debole dell'obiettivo del team, quindi la promessa del team dipende da un fornitore che non l'ha concordata. La misura ignora anche una pagina di checkout lenta di cui gli utenti si lamentano, perché conta solo il successo. Il team aggiunge un indicatore di velocità al 99° percentile e apre trattative con il fornitore sui suoi livelli di servizio.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery dovrebbero aiutare a scegliere gli indicatori e usare l'error budget nella pianificazione. Incorpora la misurazione nel servizio così che i numeri siano affidabili. Tratta un budget esaurito come una ragione per lavorare sull'affidabilità, non come una punizione.

### Team di servizio e di operations

I team operativi di solito gestiscono il monitoraggio e riferiscono sui livelli. Mantieni piccolo l'insieme delle misure, mostrale con commento e porta i dati nelle conversazioni di pianificazione. Tieni un elenco di ciò da cui il tuo servizio dipende e verifica che gli impegni si allineino.

### Leadership e governance

Leader e sponsor fissano le aspettative. Evita di chiedere la perfezione; chiedi di che cosa hanno bisogno gli utenti e quanto costa il compromesso. Sostieni l'uso di un error budget come regola condivisa e assicurati che si applichi anche alle tue richieste. Rivedi i livelli di servizio con i clienti a scadenze fisse.

### Clienti e utenti

Clienti e utenti traggono vantaggio quando il livello di servizio è dichiarato e rispettato. Di' che cosa conta per te, anche quando. Chiedi report in una forma che puoi capire e di' al fornitore quando il livello dichiarato non corrisponde più alle tue esigenze.

## Modalità di fallimento comuni

- **Troppe metriche.** Nessuno sa quale conta. Scegli invece poche che riflettano l'esperienza dell'utente.
- **Solo medie.** Un gruppo di utenti soffre mentre la media sembra a posto. Includi invece una misura a percentile alto.
- **Obiettivi copiati dalle prestazioni attuali.** Il team è bloccato negli sforzi eroici. Fissa invece gli obiettivi dalle esigenze degli utenti e stringi con i dati.
- **Pretendere il 100%.** I rilasci si fermano e l'innovazione rallenta. Concorda invece un error budget e una regola per usarlo.
- **Promesse che non puoi sostenere.** Il livello di servizio dipende da fornitori che non l'hanno concordato. Controlla invece le dipendenze e allinea gli impegni.
- **Accordi che nessuno legge.** I termini sono in linguaggio legale. Scrivi invece in modo semplice e rivedi con i clienti.
- **Cruscotti senza commento.** I numeri sono riportati senza significato. Aggiungi invece una breve spiegazione di che cosa è successo e che cosa cambierà.
- **Punire i mancati obiettivi.** Le persone nascondono i problemi. Usa invece i mancati obiettivi per stimolare decisioni e apprendimento.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Definire i livelli | I livelli sono presunti o informali | Alcuni servizi hanno obiettivi dichiarati | Ogni servizio ha indicatori basati sull'utente e obiettivi con responsabili | Gli obiettivi sono rivisti rispetto a esigenze degli utenti e dati | I livelli sono fissati congiuntamente con clienti e fornitori |
| Misurare | Le misure sono estemporanee | Alcuni indicatori sono misurati | Gli indicatori sono misurati in modo affidabile, compresi i percentili | La qualità della misurazione è rivista e le lacune corrette | La misurazione è condivisa e convalidata tra team e fornitori |
| Usare gli error budget | Il fallimento non è pianificato | Alcuni team discutono del fallimento accettabile | I budget guidano le decisioni di rilascio sui servizi chiave | L'uso del budget è rivisto e le regole regolate | I budget sono coordinati tra servizi dipendenti |
| Accordi e dipendenze | Le promesse sono informali | Esistono alcuni accordi | Gli accordi sono in linguaggio semplice, con dipendenze note | Accordi e impegni dei fornitori sono verificati rispetto ai risultati | Gli accordi formano una catena coerente tra team, fornitori e clienti |

## Checklist

- [ ] Per ogni servizio, abbiamo descritto con le parole degli utenti che aspetto ha il buono.
- [ ] Ogni servizio ha da due a quattro indicatori che riflettono l'esperienza dell'utente.
- [ ] Almeno una misura di velocità usa un percentile alto, non solo una media.
- [ ] Gli obiettivi sono fissati dalle esigenze degli utenti, non solo dalle prestazioni attuali.
- [ ] Esiste un error budget che guida le decisioni di rilascio per almeno un servizio.
- [ ] Gli accordi sono scritti in linguaggio semplice e rivisti con i clienti.
- [ ] Le dipendenze da altri team e fornitori sono elencate con i loro impegni.
- [ ] I risultati sono riferiti regolarmente con commento.
- [ ] Gli obiettivi sono rivisti almeno una volta l'anno.
- [ ] I dati sui livelli di servizio sono usati nella pianificazione e non come bastone.

## Prompt per l'IA

**Scopo: trasformare le esigenze degli utenti in indicatori e obiettivi candidati.**

```text
Help me move from user needs to indicators and objectives for [service].

What users do with the service and what matters to them (in their words, with any feedback or complaints): [paste].
Measurements we can already collect: [list].
Rules or contracts that set levels, with the source text: [paste, or write "none known"].

Propose two to four candidate indicators that reflect the user experience, say how each would be measured with the data I listed, and suggest how to express an objective for each, leaving numeric targets as [to be agreed with users and data]. Mark any indicator we cannot measure yet. Do not invent targets or performance figures. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: analizzare se le medie nascondono brutte esperienze.**

```text
Here are response times (or other measurements) for [service] over [period]: [paste a column of real values, or summary figures such as median, 90th, 99th percentile if you have them].

Using only my data, compute or describe the average, the median, and the high percentiles if the data allows. Explain in plain words what the gap between the average and the high percentiles suggests for users. Suggest one indicator and one question to ask. Do not invent data, and say if the data is too thin. List what you are unsure of.
```

**Scopo: redigere uno schema di accordo sul livello di servizio in linguaggio semplice.**

```text
Draft an outline for a service level agreement for [service] between [provider] and [customer].

What we provide: [describe].
Measures and targets already agreed or being proposed: [paste, or write "to be agreed"].
Support hours and contacts: [describe].
Dependencies on suppliers: [list].
Terms we must include because of contract or law, with source text: [paste, or write "none known"].

Produce an outline with plain-language sections: service description, hours, measures and how they are measured, how to report a problem, response and resolution expectations (marked [to be agreed]), what happens if targets are missed, reporting, review date. Do not invent legal terms. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: pianificare una policy sull'error budget.**

```text
Help me draft an error budget policy for [service].

Objective and period: [for example, "success rate of purchase attempts in the two hours before a draw closes, measured monthly"].
Current performance if known: [paste, or write "unknown"].
Release rhythm: [describe].
Who decides, and who is affected: [roles].

Draft a one-page policy: how the budget is calculated from the objective, how its use is tracked and shown, what happens at three stages of consumption (use [to be agreed] for thresholds), who may override and how, and how the policy is reviewed. Do not invent numbers. Ask clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [service-level-agreement](../../../../skills/service-level-agreement/SKILL.md): da usare per redigere o rivedere un accordo in linguaggio semplice.
- [software-engineering-metrics](../../../../skills/software-engineering-metrics/SKILL.md): da usare per scegliere e interpretare misure di consegna e di prestazione del servizio.
- [key-risk-indicators](../../../../skills/key-risk-indicators/SKILL.md): da usare per selezionare indicatori di allerta precoce che mostrano che un livello di servizio è a rischio.
- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): da usare per verificare che la capacità sostenga i livelli che prometti.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): da usare per allineare gli impegni dei fornitori ai livelli che offri.

## Fonti principali

- **Service Level Objectives** (*Site Reliability Engineering*, Google, sre.google): la spiegazione pubblica più chiara di indicatori, obiettivi, accordi, percentili ed error budget.
- **Service-level agreement** (Wikipedia): definizione, contenuti tipici, tipi e storia degli SLA.
- **DORA's software delivery performance metrics** (dora.dev): misure correlate di velocità e stabilità della consegna.
- **Quality of service** (Wikipedia): contesto su come la qualità del servizio è descritta e misurata.

## Riferimenti

1. Service Level Objectives — Google SRE book, sre.google — https://sre.google/sre-book/service-level-objectives/
2. Service-level agreement — Wikipedia — https://en.wikipedia.org/wiki/Service-level_agreement
3. DORA's software delivery performance metrics — DORA, dora.dev — https://dora.dev/guides/dora-metrics-four-keys/
4. Quality of service — Wikipedia — https://en.wikipedia.org/wiki/Quality_of_service
5. Percentile — Wikipedia — https://en.wikipedia.org/wiki/Percentile
6. Service-level objective — Wikipedia — https://en.wikipedia.org/wiki/Service-level_objective
7. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
8. Goodhart's law — Wikipedia — https://en.wikipedia.org/wiki/Goodhart%27s_law
9. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
