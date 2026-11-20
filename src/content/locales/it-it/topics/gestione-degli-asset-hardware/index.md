# Gestione degli asset hardware

**La gestione degli asset hardware segue le attrezzature fisiche dall'acquisto alla dismissione, e i suoi rischi silenziosi sono il dispositivo che nessuno conosce, il dispositivo tenuto troppo a lungo e il dispositivo che se ne va con ancora dati dentro.**

## Perché è importante

L'hardware conta ancora in un mondo cloud-first. Le persone lavorano su portatili, telefoni e tablet. Le reti girano su switch e access point. Molte organizzazioni tengono in sede server, archiviazione e attrezzature specializzate. Quando un portatile viene perso, un server esce dalla garanzia o un lotto di dispositivi va sostituito, le domande sono le stesse: che cosa abbiamo, dov'è, chi lo ha, quanto vale e che cosa contiene?

Una gestione scadente dell'hardware si manifesta in modi familiari. Il personale aspetta le attrezzature perché nessuno sa che cosa c'è in magazzino. I vecchi dispositivi restano in servizio perché nessuno ha i dati per giustificare la sostituzione, poi si guastano in un momento scomodo. I dispositivi sono buttati via con i dati ancora dentro. Le richieste di garanzia vengono perse. Per un team agile l'effetto è un inserimento rallentato, rilasci falliti su hardware di test non mantenuto ed esposizioni di sicurezza che nessuna pipeline può vedere.

La [sezione di Wikipedia sulla gestione degli asset IT](https://en.wikipedia.org/wiki/IT_asset_management), che sta dentro il suo articolo sulla gestione dei data center, descrive la gestione degli asset hardware come comprensiva dei componenti fisici di computer e di rete dall'acquisizione alla dismissione, con pratiche di richiesta e approvazione, approvvigionamento, gestione del ciclo di vita, riassegnazione e dismissione, e dice che catturare le informazioni finanziarie lungo il ciclo di vita è un componente chiave. È breve. Questo argomento aggiunge gli articoli sui rifiuti elettronici e sulla cancellazione dei dati per la dismissione e indicazioni pratiche tratte dalla pratica comune, dicendolo quando lo fa.

## Concetti fondamentali

### Ambito

Gli asset hardware includono dispositivi per l'utente finale (portatili, desktop, telefoni, tablet), server e archiviazione, apparecchiature di rete, periferiche e tecnologia specializzata o operativa. Includono anche gli accessori che li rendono utilizzabili. Per ciascuno, l'organizzazione vuole conoscere le basi: che cos'è, chi ne è responsabile, dov'è, quanto è costato e in che stato è.

### Il ciclo di vita dell'hardware

La sezione di Wikipedia elenca richiesta e approvazione, approvvigionamento, gestione del ciclo di vita, riassegnazione e dismissione. Un'espansione pratica, ampiamente usata e offerta qui come tale:

| Fase | Domande a cui rispondere | Record tipici |
|---|---|---|
| **Richiesta e approvazione** | Che cosa serve e chi approva? | Richiesta, approvazione, codice di budget |
| **Approvvigionamento** | Che cosa abbiamo comprato, da chi, a quali condizioni? | Ordine, fattura, garanzia, fornitore |
| **Ricezione e preparazione** | È arrivato? È configurato ed etichettato? | Numero di serie, asset tag, configurazione |
| **Assegnazione e gestione** | Chi lo ha? A che cosa serve? | Responsabile o utente, posizione, servizio supportato |
| **Manutenzione** | Qual è lo stato, la garanzia e le patch? | Riparazioni, fine garanzia, stato del firmware |
| **Riassegnazione** | Qualcun altro può usarlo? | Cancellazione, record di riassegnazione |
| **Ritiro e dismissione** | I dati sono rimossi? Dove è andato? | Prove di cancellazione, record di dismissione |

### Informazioni finanziarie

La sezione di Wikipedia sottolinea di catturare le informazioni finanziarie sul ciclo di vita dell'hardware. I fatti utili includono costo d'acquisto, ammortamento, costo di garanzia e supporto e costo per mantenerlo in funzione. Alimentano decisioni di sostituzione e budget (vedi Argomento 4.5 — Gestione finanziaria IT e FinOps). Un dispositivo che costa di più da supportare che da sostituire è candidato al ritiro.

### Sostituzione e rinnovo

Le organizzazioni sostituiscono comunemente le attrezzature con un ciclo, come ogni pochi anni per i portatili. Le fonti lette per questa guida non indicano periodi raccomandati, e l'intervallo giusto dipende da attrezzature, lavoro e costo del guasto. Un approccio basato sui dati guarda ai tassi di guasto, al costo di supporto, al supporto di sicurezza e alle prestazioni e sostituisce quando le prove lo dicono. Un ciclo fisso è più facile da pianificare e uno basato sulle prove può far risparmiare denaro o evitare guasti.

### Sicurezza dei dati a fine vita

La dismissione è il punto in cui la gestione dell'hardware incontra la sicurezza delle informazioni (vedi Argomento 3.13 — Gestione della sicurezza delle informazioni). L'articolo di Wikipedia sulla cancellazione dei dati descrive la cancellazione dei dati come un metodo software che sovrascrive ogni settore di un'unità in modo che i dati memorizzati siano irrecuperabili; la normale cancellazione di file rimuove solo i puntatori, e strumenti comuni possono spesso recuperare i dati. Punti chiave dell'articolo:

- La **sovrascrittura** lascia utilizzabile l'unità. La **smagnetizzazione** e la **distruzione fisica** rendono inutilizzabile il supporto e si aggiungono ai rifiuti elettronici.
- Le **unità a stato solido e i supporti flash** possono conservare dati residui che la cancellazione perde. L'articolo cita uno studio del 2011 che ha trovato che i comandi di sanitizzazione integrati funzionano se implementati correttamente, mentre le tecniche software funzionano nella maggior parte dei casi, ma non in tutti.
- La **cifratura** offre un'altra via: distruggere le chiavi di un'unità autocifrante rende inaccessibili i suoi dati.
- **Verifica e certificati:** un buon software dovrebbe verificare che la sovrascrittura abbia raggiunto l'intero dispositivo, comprese le aree nascoste, ed emettere un certificato di convalida e un registro dei settori che non è stato possibile sovrascrivere.
- **Standard:** l'articolo ne elenca molti, tra cui la NIST Special Publication 800-88 (2006, rivista nel 2014), che cita come dicente che un singolo passaggio di sovrascrittura con un modello fisso come zeri binari tipicamente ostacola il recupero. Afferma che un singolo passaggio è generalmente sufficiente per i dischi rigidi moderni.

L'articolo è etichettato come bisognoso di citazioni e alcune affermazioni sono segnalate. Controlla gli standard richiesti dal tuo settore o paese e lo stato dell'arte corrente per le tue attrezzature; non affidarti a un riassunto di Wikipedia per una decisione di conformità.

### Rifiuti elettronici

L'articolo di Wikipedia sui rifiuti elettronici li definisce come dispositivi elettrici o elettronici scartati, compresi gli oggetti destinati a riuso, rivendita, recupero, riciclo o smaltimento. Riferisce circa 62 milioni di tonnellate generate nel mondo nel 2022, l'82 percento in più rispetto al 2010, con solo il 22,3 percento formalmente raccolto e riciclato secondo uno studio del 2024; cita anche altre cifre in conflitto e porta etichette di manutenzione per affermazioni non verificate, quindi controlla i numeri sulle fonti primarie prima di citarli. Descrive i pericoli di materiali come piombo, cadmio, mercurio e ritardanti di fiamma e della lavorazione informale, con esempi da Guiyu in Cina e Agbogbloshie in Ghana. Nota che la Convenzione di Basilea, adottata nel marzo 1989, regola il movimento transfrontaliero di rifiuti pericolosi e che i riciclatori certificati secondo schemi come R2 ed E-Stewards devono distruggere tutti i dati memorizzati sui dispositivi elettronici. Il riuso allunga la vita dei dispositivi e ritarda il riciclo.

Per un'organizzazione le lezioni sono pratiche: scegli partner di dismissione certificati che possano mostrare dove vanno i dispositivi, preferisci il riuso dove è sicuro e tieni i record. Le leggi sui rifiuti elettronici differiscono per paese e regione; chiedi alla tua funzione di conformità quali si applicano.

### Hardware e gestione dei servizi

I record hardware si collegano ai servizi: questo switch trasporta quel servizio, questo server ospita quell'applicazione. Quei collegamenti trasformano un registro degli asset in uno strumento per la risposta agli incidenti, la pianificazione dei cambiamenti e la valutazione dei rischi (vedi Argomento 4.4 — Gestione della configurazione). Senza di essi, un dispositivo guasto è un ticket; con essi, è una dichiarazione di impatto.

### Agile e hardware

I team agili trattano l'hardware come un vincolo attorno a cui progettare, non come l'evento principale. Cloud e virtualizzazione riducono il parco fisico, ma non a zero. Dispositivi di test per app mobili, agenti di build, attrezzature di laboratorio e dispositivi edge richiedono tutti di essere tracciati. Trattali come asset con responsabili e cicli di vita e non lasciarli in un armadio.

## Buone pratiche

1. **Etichetta e registra ogni dispositivo che conta.** Assegna un asset tag unico o un record di numero di serie alla ricezione e registra tipo, responsabile, posizione e stato. Fanne il primo passo dopo la consegna.
2. **Collega i dispositivi a persone e servizi.** Registra chi ha ogni dispositivo e quale servizio supporta e aggiorna a spostamenti e cambiamenti. Usa il processo per chi lascia l'organizzazione per recuperare le attrezzature e rimuovere gli accessi.
3. **Tieni i dati finanziari con l'asset.** Registra costo, garanzia, termini di supporto e ammortamento. Usali per confrontare riparazione, supporto e sostituzione.
4. **Usa il rilevamento per trovare l'ignoto.** Confronta il registro con il rilevamento di rete ed endpoint e indaga prontamente sui dispositivi sconosciuti (vedi Argomento 4.1 — Gestione degli asset IT).
5. **Monitora condizione e stato di supporto.** Monitora le date di fine garanzia, lo stato del firmware e del supporto di sicurezza e la storia dei guasti. Pianifica la sostituzione prima che i dispositivi si guastino o perdano il supporto.
6. **Sostituisci sulla base delle prove.** Guarda i dati su guasti e supporto, prestazioni e supporto di sicurezza per decidere la sostituzione, e non solo l'età. Rivedi la policy una volta l'anno.
7. **Prepara i dispositivi in modo coerente.** Usa una build standard e un'iscrizione automatica così che i nuovi dispositivi arrivino pronti, con i controlli di sicurezza in atto.
8. **Riassegna dove è sicuro.** Cancella e riassegna i dispositivi che soddisfano ancora le esigenze, con un record della cancellazione. Evita scorte di attrezzature inutilizzate.
9. **Cancella i dati correttamente e conserva le prove.** Usa un metodo adatto al tipo di dispositivo e alla sensibilità dei dati, verificalo e conserva un certificato o un registro. Per l'archiviazione flash, usa i comandi di sanitizzazione supportati dal dispositivo o la distruzione delle chiavi come appropriato (vedi le note sulla cancellazione dei dati sopra).
10. **Scegli con cura i partner di dismissione.** Preferisci riciclatori certificati, chiedi dove vanno dispositivi e materiali e tieni i record. Includi nel contratto i termini di distruzione dei dati.
11. **Pianifica i dispositivi persi e rubati.** Abbi un modo rapido per segnalare, un blocco o una cancellazione da remoto dove disponibile e una regola su quando trattare una perdita come incidente di sicurezza (vedi Argomento 3.2 — Gestione degli incidenti).
12. **Rivedi regolarmente.** Almeno due volte l'anno, verifica un campione del registro rispetto alla realtà fisica per le principali classi di dispositivi e correggi il processo dietro qualsiasi divario.

## Domande da discutere con il team

**Se contassimo ogni dispositivo che possediamo oggi, corrisponderemmo al registro?**

Scegli un piano, un team o un magazzino e fai un rapido conteggio rispetto al registro. Le differenze sono la lezione. Chiedi quali discrepanze contano di più: dispositivi con dati, dispositivi senza patch. Chi facilita può chiedere che cosa impedisce alle persone di aggiornare il registro nel momento del cambiamento. Scegli un processo da stringere.

**Che cosa facciamo con un portatile quando qualcuno se ne va?**

Ripercorri i passaggi: chi lo ritira, dove va, chi lo cancella, chi aggiorna il record. Le lacune compaiono spesso tra i team. Chiedi l'ultimo esempio e ripercorrilo. Concorda un responsabile e una checklist.

**Come decidiamo quando sostituire le attrezzature?**

Chiedi la regola attuale e la sua fonte. Spesso è un'età fissa che qualcuno ha stabilito molto tempo fa. Discuti di quali dati hai su guasti, costo di supporto e supporto di sicurezza. Confronta con il costo di sostituire presto o tardi. Concorda quali dati raccogliere.

**Come proveremmo che i dati su un dispositivo che abbiamo dismesso sono stati distrutti?**

Prendi una dismissione recente e chiedi quali prove esistono. Se la risposta è "l'ha detto il riciclatore", discuti che cosa dovrebbe contenere un certificato o un registro. Chiedi quale metodo è stato usato per l'archiviazione a stato solido. Concorda uno standard minimo e le prove.

**Quali dei nostri dispositivi sono fuori garanzia o fuori supporto di sicurezza, e che cosa dipende da essi?**

Elenca i dispositivi vicini alla fine del supporto. Chiedi che cosa supporta ciascuno. I dispositivi non supportati dietro servizi importanti sono rischi. Pianifica la sostituzione in ordine di impatto e decidi dove servono misure compensative.

**Chi gestisce un dispositivo perso o rubato, e con quale rapidità?**

Chiedi come un utente segnala una perdita e che cosa succede dopo. Verifica se il blocco o la cancellazione da remoto sono disponibili e se qualcuno li ha provati. Discuti quando una perdita diventa un incidente di sicurezza. Concorda un primo passo chiaro per gli utenti.

## Nella pratica: un esempio di ITIL agile

Un'azienda sanitaria provinciale fornisce circa 4.000 portatili e tablet a infermieri di comunità, che visitano i pazienti a domicilio. I dispositivi vengono persi o danneggiati con frequenza. I record dell'azienda mostrano 4.300 dispositivi, ma il service desk ritiene di gestirne meno. Una revisione di sicurezza scopre che alcuni portatili elencati come ritirati sono stati visti in uso e che una scorta di vecchi dispositivi in un armadio contiene ancora dati dei pazienti.

Il responsabile dei servizi per l'utente finale avvia un piccolo programma. Ogni dispositivo riceve un tag unico e un record collegato a un infermiere nominato e a un team. Uno strumento di rilevamento confronta il registro con i dispositivi che si connettono alla rete, e un elenco mensile dei dispositivi non corrispondenti va ai responsabili dei team, che hanno due settimane per spiegarli o restituirli. I dispositivi sono iscritti automaticamente con la cifratura attiva e il software standard, così che un portatile perso riveli poco. Una checklist per chi lascia l'organizzazione aggiunge la restituzione del dispositivo come passaggio che il responsabile firma. Per la dismissione, l'azienda stipula un contratto con un riciclatore certificato che cancella le unità, distrugge quelle che non si possono cancellare e fornisce un certificato per ogni lotto. L'armadio viene svuotato e il suo contenuto cancellato e registrato.

Entro sei mesi il registro e il rilevamento coincidono entro un piccolo margine e un portatile perso viene bloccato da remoto entro un'ora nella maggior parte dei casi. Restano alcuni problemi. Gli infermieri a volte condividono i dispositivi nei turni intensi, quindi il campo del responsabile è sbagliato, e i certificati del riciclatore elencano i lotti ma non i singoli dispositivi, cosa su cui l'auditor chiede. Il responsabile dei servizi per l'utente finale introduce un record di dispositivo condiviso con una firma giornaliera di uscita e chiede al riciclatore di includere i numeri di serie nei certificati. Decide anche di rivedere la policy di sostituzione usando i dati sui guasti del primo anno, invece di mantenere un'età fissa.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery detengono dispositivi di test, server di build e attrezzature di laboratorio. Registrali, dai loro responsabili e ritirali correttamente. Di' alla gestione degli asset quando hai bisogno di dispositivi, così che la fornitura corrisponda ai progetti.

### Team di servizio e di operations

Operations e service desk gestiscono la maggior parte del ciclo di vita: build, distribuzione, supporto e ritiro. Mantieni aggiornati i record a ogni passaggio, usa il rilevamento per cogliere le lacune e conserva le prove di dismissione. Condividi i dati su condizione e guasti con chi pianifica la sostituzione.

### Leadership e governance

I leader decidono budget di sostituzione e propensione al rischio. Chiedi il numero di dispositivi fuori supporto, il processo per i dispositivi persi e le prove della distruzione dei dati. Sostieni il rinnovo basato sulle prove e i piccoli controlli, come tag e checklist, che mantengono veri i record.

### Clienti e utenti

Gli utenti detengono le attrezzature giorno per giorno. Abbine cura, segnala rapidamente perdite o danni e restituisci le attrezzature quando te ne vai. Di' al desk se condividi un dispositivo o ti sposti in un'altra sede, così che i record siano giusti.

## Modalità di fallimento comuni

- **Attrezzature senza tag.** I dispositivi non si distinguono. Etichetta invece e registra alla ricezione.
- **Record obsoleti.** Spostamenti e partenze non sono catturati. Collega invece gli aggiornamenti a eventi come i processi di ingresso, spostamento e uscita.
- **Rinnovo a età fissa senza dati.** I dispositivi sono sostituiti troppo presto o troppo tardi. Rivedi invece guasti, costi e dati di supporto.
- **Dismissione debole.** I dati restano sui dispositivi dismessi. Cancella e verifica invece con un metodo adatto al supporto, conserva le prove e usa un partner certificato.
- **Ignorare l'archiviazione flash.** Si presume che la sovrascrittura funzioni. Usa invece comandi di sanitizzazione o la distruzione delle chiavi e verifica.
- **Scorte.** I dispositivi inutilizzati si accumulano. Riassegna o ritira invece a scadenza fissa.
- **Nessun legame con i servizi.** Un dispositivo guasto è solo un ticket. Registra invece il servizio che ogni dispositivo supporta.
- **Riciclo non certificato.** Le attrezzature finiscono dove nessuno sa. Scegli invece partner certificati e chiedi dove vanno i materiali.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Inventario e tracciamento | I dispositivi sono noti in modo informale | Un registro copre i dispositivi principali | Ogni dispositivo è etichettato e registrato, riconciliato con il rilevamento | Accuratezza e lacune sono misurate e corrette | L'inventario copre dispositivi posseduti, in leasing e dei partner con dati condivisi |
| Ciclo di vita e rinnovo | La sostituzione avviene al guasto | Alcuni dispositivi seguono un piano di rinnovo | Passaggi del ciclo di vita e policy di rinnovo sono definiti | Dati su guasti e costi guidano le decisioni di sostituzione | Il rinnovo è pianificato in tutta l'organizzazione con fornitori e finanza |
| Dismissione e protezione dei dati | La dismissione è estemporanea | Alcuni dispositivi sono cancellati | Un metodo standard di cancellazione e una dismissione certificata con prove | Le prove di dismissione sono verificate e le lacune colmate | La dismissione è coordinata con partner e programmi di riuso |
| Legame con servizio e finanza | I dispositivi non sono collegati a servizi o costi | Alcuni dati di costo sono tenuti | I dispositivi sono collegati a responsabili, servizi e costi | Dati su costi e supporto sono rivisti e usati nei budget | I dati sugli asset sono condivisi continuamente con finanza, sicurezza e fornitori |

## Checklist

- [ ] Ogni dispositivo che monitoriamo ha un tag unico o un record di numero di serie e un responsabile o utente nominato.
- [ ] I dispositivi sono collegati al servizio che supportano.
- [ ] Il rilevamento è confrontato con il registro almeno ogni mese per i tipi di dispositivo principali.
- [ ] Le date di fine garanzia e supporto sono registrate e riviste.
- [ ] La nostra policy di sostituzione è basata sui dati e rivista ogni anno.
- [ ] I processi per chi lascia o cambia ruolo recuperano o riassegnano i dispositivi.
- [ ] La cancellazione dei dati usa un metodo adatto al supporto, con verifica e un record.
- [ ] I partner di dismissione sono certificati e forniscono prove per dispositivo o per lotto.
- [ ] I dispositivi persi e rubati possono essere segnalati rapidamente e bloccati o cancellati da remoto dove disponibile.
- [ ] Un campione del registro è verificato rispetto alla realtà fisica due volte l'anno.

## Prompt per l'IA

**Scopo: riconciliare un conteggio fisico con il registro.**

```text
I have a physical count of devices in [location or team] and the register entries for the same scope.

Physical count (tag or serial, type, who has it): [paste].
Register (tag or serial, type, owner, status): [paste]. 

Using only these lists, identify items present physically but missing from the register, items in the register but not found, and items where the owner or status differs. For each group, suggest a question to ask. Do not guess about items that cannot be matched. List what you are unsure of.
```

**Scopo: preparare una revisione della sostituzione basata sui dati.**

```text
Help me prepare a replacement review for [device class, e.g. "field laptops"].

Data we have (age, repairs, failures, support tickets, warranty end, security support end, cost): [paste a table of real data].
Current replacement rule and its source: [paste, or write "unknown"].
Budget limits: [describe, or write "unknown"].

Using only this data, describe patterns by age group (for example failure and repair counts), identify devices near end of support, and suggest questions about whether the current rule fits. Do not invent failure rates or costs. If the data are too thin, say what to collect. List what you are unsure of.
```

**Scopo: scrivere una checklist di dismissione di dispositivi con i requisiti di prova.**

```text
Help me write a disposal checklist for [device type, e.g. "laptops and phones"].

Data sensitivity: [describe].
Storage types: [for example hard drives, SSDs, phones with encrypted storage].
Disposal partner and what they provide: [describe, or write "not yet chosen"].
Rules we must follow, with source text: [paste, or write "none known"].

Produce a checklist covering authorization, removal of accounts and licenses, data erasure or destruction method by storage type, verification, evidence kept (certificate content, serial numbers), disposal route, and register update. Mark steps that are assumptions. Do not state that any law or standard requires a method unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: pianificare la risposta a un dispositivo perso.**

```text
Draft a short response procedure for a lost or stolen [device type].

What controls exist today (encryption, remote lock, remote wipe, location): [describe, or write "unknown"].
Data the device may hold: [describe].
Who is told today: [list].

Write steps for the user, the service desk, and security: how to report, what to do in the first hour, when to treat the loss as a security incident, and how to record it. Leave any notification duty as [CHECK WITH LEGAL] unless I give the source text. Ask clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [configuration-management](../../../../skills/configuration-management/SKILL.md): da usare per collegare i dispositivi ai servizi che supportano.
- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): da usare per pianificare quante attrezzature servono e quando.
- [budget-forecasting](../../../../skills/budget-forecasting/SKILL.md): da usare per prevedere i costi di rinnovo e supporto.
- [data-governance](../../../../skills/data-governance/SKILL.md): da usare per decidere chi possiede i dati sui dispositivi e come sono protetti al ritiro.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): da usare per selezionare e rivedere fornitori hardware e partner di dismissione.

## Fonti principali

- **IT asset management** (Wikipedia): la definizione e una descrizione della gestione degli asset hardware, all'interno dell'articolo sulla gestione dei data center.
- **Data erasure** (Wikipedia): metodi, standard, verifica e il caso speciale dell'archiviazione a stato solido.
- **Electronic waste** (Wikipedia): scala, pericoli, riciclo e Convenzione di Basilea, con avvertenze sulle cifre in conflitto.
- **Guidelines for Media Sanitization** (NIST Special Publication 800-88): le indicazioni primarie che l'articolo di Wikipedia cita; leggi la revisione corrente prima di fissare uno standard.

## Riferimenti

1. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
2. Data erasure — Wikipedia — https://en.wikipedia.org/wiki/Data_erasure
3. Electronic waste — Wikipedia — https://en.wikipedia.org/wiki/Electronic_waste
4. Basel Convention — Wikipedia — https://en.wikipedia.org/wiki/Basel_Convention
5. Data center management — Wikipedia — https://en.wikipedia.org/wiki/Data_center_management
6. Total cost of ownership — Wikipedia — https://en.wikipedia.org/wiki/Total_cost_of_ownership
7. Mobile device management — Wikipedia — https://en.wikipedia.org/wiki/Mobile_device_management
8. Information security — Wikipedia — https://en.wikipedia.org/wiki/Information_security
