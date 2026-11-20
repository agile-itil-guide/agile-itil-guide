# Gestione degli asset IT

**La gestione degli asset IT tiene traccia dell'hardware, del software e delle risorse correlate che un'organizzazione possiede o paga, dall'acquisto alla dismissione, così che le decisioni su costo, rischio e supporto si basino sui fatti anziché sulle supposizioni.**

## Perché è importante

Chiedi alla maggior parte delle organizzazioni quanti portatili, server, account cloud e licenze software hanno, e la prima risposta è una stima. La seconda, dopo una ricerca, è spesso diversa. Quel divario ha dei costi. Si comprano licenze che nessuno usa, o se ne usano senza averle comprate. Vecchio hardware resta in rete senza patch. Il personale in uscita conserva l'accesso a sistemi che nessuno ha ricordato di rimuovere. Un service desk non può supportare un'attrezzatura di cui non conosce l'esistenza.

La gestione degli asset IT (ITAM) è la pratica che colma quel divario. È strettamente legata alla gestione dei servizi: i servizi girano su asset, incidenti e modifiche toccano asset e il costo di un servizio è in gran parte il costo dei suoi asset. Per i team agili, la pratica ha un risvolto particolare. Gli asset ora includono risorse cloud create da uno script in pochi secondi e distrutte minuti dopo, immagini di container, librerie open source e abbonamenti pagati con una carta. Il vecchio modello di un foglio di calcolo delle attrezzature acquistate non le cattura.

L'articolo della Wikipedia inglese intitolato "IT asset management" attualmente rimanda al suo articolo sulla gestione dei data center, in cui l'ITAM compare come sezione. Quella sezione descrive l'ITAM come pratiche di business che uniscono funzioni finanziarie, contrattuali e di inventario per sostenere la gestione del ciclo di vita e le decisioni strategiche IT, ed è breve. Questo argomento la usa per la definizione, aggiunge i dettagli dagli articoli sulla gestione degli asset software e sui database di gestione della configurazione e colloca la pratica nel contesto agile. Dove va oltre le fonti, lo dice.

## Concetti fondamentali

### Che cos'è

Secondo la sezione di Wikipedia sulla gestione degli asset dei data center, che cita Gartner, l'ITAM è un insieme di pratiche di business che uniscono funzioni finanziarie, contrattuali e di inventario per sostenere la gestione del ciclo di vita e le decisioni strategiche IT. Gli asset includono software e hardware nell'ambiente di business. La pratica è detta anche gestione dell'inventario. L'articolo nota che la pratica usa il rilevamento automatico così che l'inventario possa essere confrontato con i diritti di licenza e che una gestione completa richiede un repository di diversi tipi di informazioni, integrato con sistemi di supply chain, help desk, acquisti, risorse umane e ITSM.

### Che cosa conta come asset

Un elenco di lavoro utile per un'organizzazione di servizio:

| Tipo di asset | Esempi | Trattato in |
|---|---|---|
| **Hardware** | Portatili, server, dispositivi di rete, telefoni, archiviazione | Argomento 4.3 — Gestione degli asset hardware |
| **Software** | Applicazioni con licenza, sistemi operativi, componenti open source, abbonamenti | Argomento 4.2 — Gestione degli asset software |
| **Risorse cloud e di servizio** | Macchine virtuali, container, bucket di archiviazione, account SaaS | Argomento 4.2 — Gestione degli asset software e Argomento 4.5 — Gestione finanziaria IT e FinOps |
| **Dati e informazioni** | Dataset, record, backup | Argomento 3.13 — Gestione della sicurezza delle informazioni |
| **Contratti e diritti d'uso** | Licenze, accordi di supporto, garanzie | Argomento 4.2 — Gestione degli asset software e Argomento 3.14 — Gestione dei fornitori |
| **Persone e competenze** | Personale e capacità (di solito non nel registro degli asset, ma parte del servizio) | Argomento 2.5 — Le quattro dimensioni della gestione dei servizi |

La tabella è l'elenco di lavoro di questa guida, non una classificazione di una fonte.

### Ciclo di vita

La sezione di Wikipedia descrive la gestione degli asset hardware come comprensiva dei componenti fisici di computer e di rete dall'acquisizione alla dismissione, con pratiche elencate di richiesta e approvazione, approvvigionamento, gestione del ciclo di vita, riassegnazione e dismissione, e dice che catturare le informazioni finanziarie sul ciclo di vita dell'hardware è un componente chiave. Non dà un modello formale a fasi. Una sequenza pratica comune, ampiamente usata e offerta qui come tale, è:

1. **Pianificare e richiedere:** decidere che cosa serve e ottenere l'approvazione.
2. **Acquisire:** comprare o costruire e registrare l'acquisto.
3. **Distribuire:** mettere in servizio e collegare all'utente o al servizio.
4. **Gestire e mantenere:** applicare patch, supportare, spostare e tracciare i cambiamenti.
5. **Ritirare e dismettere:** togliere dal servizio, cancellare i dati e dismettere in sicurezza.

A ogni fase, chiedi chi è responsabile e quale record viene tenuto.

### Inventario, rilevamento e record

Un registro degli asset è utile solo se è vero. L'articolo nota che il rilevamento automatico sostiene il confronto tra inventario e diritti d'uso. Gli strumenti di rilevamento scansionano reti e account cloud per trovare ciò che esiste, e il registro registra ciò che l'organizzazione intende possedere e pagare. Le differenze tra i due sono risultati: dispositivi sconosciuti, licenze inutilizzate, abbonamenti non approvati.

### Rapporto con l'ITSM e il CMDB

La sezione di Wikipedia dice che l'ITAM si integra con l'ITSM ma non lo associa in dettaglio ai processi ITIL. Le descrizioni ITIL distinguono tipicamente la gestione degli asset, che riguarda proprietà, costo e contratti, dalla gestione della configurazione, che riguarda le relazioni tra componenti. Un **configuration management database (CMDB)**, secondo Wikipedia, è un termine ITIL per un database che memorizza informazioni su asset hardware e software, detti elementi di configurazione, e sulle relazioni tra essi (vedi Argomento 4.4 — Gestione della configurazione). I record degli asset e quelli di configurazione si sovrappongono; molte organizzazioni federano i dati così che ciascuna fonte mantenga il controllo dei propri.

### Standard

La sezione di Wikipedia nomina ISO/IEC 19770 come famiglia di standard per la gestione degli asset software senza descriverne le parti. L'articolo sulla gestione degli asset software elenca le parti: 19770-1:2017 sui requisiti del sistema di gestione degli asset IT, un framework di processo che può essere implementato in livelli graduali; 19770-2:2015 sui tag di identificazione del software; 19770-3:2016 sulla gestione dei diritti d'uso; 19770-4:2017 sulla misurazione dell'uso delle risorse; e 19770-5:2015 su panoramica e vocabolario. Controlla gli standard stessi per la formulazione esatta e le edizioni correnti.

### Benefici e limiti

La sezione di Wikipedia non elenca benefici né critiche e non nomina strumenti. I benefici pratici sono ampiamente dichiarati, come minor costo delle licenze, minor rischio di sicurezza e supporto migliore, ma questa guida non ha prove misurate per essi nelle fonti lette. Tratta con cautela le dichiarazioni di risparmio, chiedi le prove a chi le fa e misura le tue.

### ITAM in un contesto agile e cloud

Le pratiche dei decenni passati presuppongono che gli asset siano acquistati, consegnati e installati dall'IT. Oggi:

- **I team creano risorse da soli,** nelle console cloud o tramite codice. Il registro deve venirne a sapere dall'account cloud, non da un ordine d'acquisto.
- **Gli asset sono di breve durata.** Un container può durare un'ora. Monitora il servizio e l'account, non ogni istanza.
- **Gli abbonamenti sostituiscono le licenze.** Il software è pagato mensilmente con la carta di qualcuno e la proprietà è poco chiara.
- **I componenti open source** entrano attraverso il codice, fuori dal sistema degli acquisti (vedi Argomento 4.2 — Gestione degli asset software).

Questi cambiamenti spingono l'ITAM verso automazione, etichettatura e responsabilità condivisa tra l'IT e i team che usano gli asset.

## Buone pratiche

1. **Parti da ciò che conta di più.** Scegli prima gli asset con il costo o il rischio più alti: licenze costose, server esposti a Internet, dispositivi con dati sensibili. Un registro completo può venire dopo.
2. **Definisci che cos'è un asset per i tuoi scopi.** Scrivi un breve elenco dei tipi di asset che monitorerai e dei fatti di cui hai bisogno per ciascuno: responsabile, posizione o account, costo, contratto e stato. Evita campi che nessuno userà.
3. **Nomina un responsabile per ogni asset.** Una persona o un team dovrebbe rispondere di ogni asset o gruppo di asset. Gli asset senza responsabili sono dove si accumulano spreco e rischio.
4. **Usa il rilevamento per trovare ciò che esiste.** Scansiona reti, account cloud ed endpoint e confronta con il registro. Tratta le differenze come voci da indagare.
5. **Etichetta le risorse cloud.** Richiedi tag per responsabile, servizio e ambiente sulle risorse create negli account cloud e riferisci su quelle senza tag. I tag permettono al registro di seguire asset in rapido movimento.
6. **Collega gli acquisti al registro.** Assicurati che i nuovi acquisti, compresi abbonamenti e acquisti con carta, creino o aggiornino un record. Rivedi la spesa per le voci che non l'hanno fatto.
7. **Collega gli asset ai servizi.** Registra quale servizio supporta ciascun asset. Ti permette di valutare l'impatto di un incidente, una modifica o una dismissione (vedi Argomento 4.4 — Gestione della configurazione).
8. **Monitora il lato finanziario.** Registra costo, termini contrattuali, date di rinnovo e ammortamento dove rilevante. Catturare le informazioni finanziarie lungo il ciclo di vita è un componente chiave della gestione dell'hardware, come dice la sezione di Wikipedia.
9. **Gestisci la fine del ciclo di vita.** Pianifica la dismissione fin dall'inizio: cancellazione dei dati, restituzione e smaltimento. Rimuovi accessi e licenze nello stesso momento.
10. **Rivedi regolarmente.** Almeno due volte l'anno, confronta il registro con la realtà per le classi di asset più importanti. Correggi il processo che ha causato qualsiasi differenza.
11. **Condividi i dati.** Rendi disponibili i dati degli asset a service desk, sicurezza, finanza e team, in una forma che possano usare. I dati che vede solo il responsabile degli asset valgono poco.
12. **Misura la pratica.** Monitora quanto è completo e accurato il registro, quanto tempo ci vuole per trovare un asset e il costo delle voci inutilizzate. Usali per migliorare, non per classificare le persone.

## Domande da discutere con il team

**Se qualcuno chiedesse quanti asset di ogni tipo abbiamo, quanto saremmo sicuri?**

Chiedi a ciascuno di stimare il numero di portatili, server, account cloud e abbonamenti, poi confronta con il registro. Le differenze mostrano quanto è ignoto. Chi facilita può chiedere di quale categoria le persone si fidano meno. Scegline una da riconciliare per prima.

**Chi possiede ciascuno dei nostri asset, e che cosa succede quando quella persona se ne va?**

Prendi un campione di asset e guarda il campo del responsabile. Conta quelli senza responsabile o con un responsabile che se n'è andato. Chiedi quale processo dovrebbe aggiornare i responsabili quando le persone si spostano. Concorda un innesco, come il processo per chi lascia l'organizzazione.

**Che cosa paghiamo che nessuno usa?**

Guarda licenze, abbonamenti e risorse cloud e chiedi quali non hanno un uso recente. Preparati a sorprese. Chiedi chi può autorizzare la cancellazione di qualcosa. Scegli le tre più grandi e verifica ciascuna.

**Come scopriamo una nuova risorsa cloud o un nuovo abbonamento?**

Ripercorri l'ultimo. Spesso la risposta è "alla fattura" o "quando si è rotto". Discuti come acquisti, etichettatura e rilevamento potrebbero coglierlo prima. Concorda un controllo, come tag obbligatori o un report mensile degli elementi senza tag.

**Che cosa succede a un portatile o a un server alla fine del suo ciclo di vita?**

Ripercorri i passaggi: chi decide, come i dati sono rimossi, che cosa dice il record. Le lacune compaiono spesso attorno alla cancellazione dei dati e ai record. Chiedi prove che una dismissione recente sia stata fatta correttamente. Pianifica una breve checklist.

**Di quali dati sugli asset hanno bisogno gli altri team che non diamo loro?**

Chiedi a service desk, sicurezza e finanza che cosa vorrebbero vedere. Le richieste tipiche includono responsabile, servizio e costo. Discuti come condividerlo e chi lo mantiene aggiornato. Scegli un report da produrre.

## Nella pratica: un esempio di ITIL agile

Un'agenzia nazionale di statistica ha 1.800 dipendenti e gestisce l'elaborazione delle sue indagini in un misto di data center on-premises e account cloud pubblico. Il team finanza nota che la fattura cloud è cresciuta di un terzo in un anno, e un audit di sicurezza trova tre server nel data center che nessuno sa identificare. La funzione ITAM è composta da due persone con un foglio di calcolo.

Il responsabile IT fissa un obiettivo modesto: conoscere gli asset principali, chi li possiede e quanto costano, partendo dal cloud. Una nuova regola richiede tag di responsabile, servizio e ambiente su ogni risorsa cloud. Un report settimanale elenca le risorse senza tag e i team hanno due settimane per rivendicarle o rimuoverle. Nel data center, le due persone dell'ITAM eseguono una scansione di rilevamento e la confrontano con il foglio di calcolo, trovando 40 dispositivi non in elenco. Rintracciano i responsabili per la maggior parte. Gli acquisti concordano che qualsiasi nuovo abbonamento software sia comunicato all'ITAM entro una settimana.

Dopo un trimestre, la quota di risorse cloud senza tag scende da circa un terzo a una manciata e la finanza può attribuire la fattura cloud ai servizi. Alcune risorse inutilizzate sono spente e due server vengono ritirati. Restano problemi. Un gruppo di ricerca compra strumenti con una carta del dipartimento e non li segnala, e il report settimanale è letto solo da pochi team. Il personale ITAM parla con il gruppo di ricerca di un semplice modulo di registrazione e chiede al responsabile finanziario di aggiungere gli abbonamenti alla revisione mensile. Decidono anche che il registro coprirà i servizi cloud per account e servizio, non ogni istanza di breve durata.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery creano molti asset. Etichetta ciò che crei, registra gli abbonamenti e le librerie che aggiungi e ritira ciò di cui non hai più bisogno. Tratta il registro come un servizio a cui contribuisci e da cui trai vantaggio.

### Team di servizio e di operations

I team operativi dipendono dal registro per supporto, patching e risposta agli incidenti. Mantienilo accurato aggiornandolo a deployment, modifica e dismissione. Usa il rilevamento per trovare ciò che manca e riferisci le differenze ai responsabili.

### Leadership e governance

Leader e finanza usano i dati degli asset per le decisioni su spesa, rischio e rinnovi. Chiedi pochi numeri affidabili, come la spesa per servizio e la quota di asset con responsabili, anziché un registro perfetto. Sostieni i piccoli controlli, come tag e segnalazione degli acquisti, che lo mantengono vero.

### Clienti e utenti

Gli utenti traggono vantaggio quando le loro attrezzature e i loro accessi sono gestiti bene: dispositivi funzionanti, sostituzioni rapide e nessun addebito a sorpresa. Di' al service desk delle attrezzature che aggiungi o di cui non hai più bisogno e aspettati che ti si chieda di confermare ciò che detieni.

## Modalità di fallimento comuni

- **Un registro di cui nessuno si fida.** È obsoleto e ignorato. Restringi invece l'ambito, usa il rilevamento e aggiorna a ogni evento del ciclo di vita.
- **Nessun responsabile.** Gli asset non appartengono a nessuno. Richiedi invece un responsabile per ogni asset o gruppo.
- **Tracciare tutto.** Lo sforzo seppellisce il valore. Parti invece da ciò che è costoso o rischioso e cresci.
- **Ignorare cloud e abbonamenti.** Il registro copre solo hardware acquistato. Etichetta invece le risorse cloud e cattura gli abbonamenti.
- **Acquisti fuori dal processo.** Gli acquisti con carta aggirano il registro. Collega invece acquisti e report di spesa all'ITAM.
- **Nessun processo di fine ciclo di vita.** I vecchi dispositivi conservano dati e accessi. Pianifica invece dismissione, cancellazione e smaltimento.
- **Dati tenuti per sé.** Solo l'ITAM vede il registro. Condividilo invece con service desk, sicurezza e finanza.
- **Contare senza agire.** I report mostrano asset inutilizzati e nulla viene cancellato. Assegna invece responsabili che agiscano sui risultati.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Inventario e rilevamento | Gli asset sono elencati in fogli di calcolo o per niente | Alcune classi di asset sono inventariate | Rilevamento e registro coprono le principali classi di asset e sono riconciliati regolarmente | Completezza e accuratezza sono misurate e le lacune corrette | L'inventario copre on-premises, cloud e fornitori con dati condivisi |
| Responsabilità | Pochi asset hanno responsabili | I responsabili sono nominati per alcuni asset | Ogni asset o gruppo ha un responsabile, tenuto aggiornato da un processo | Le lacune di responsabilità sono monitorate e risolte | I responsabili tra team e fornitori lavorano secondo regole condivise |
| Ciclo di vita e controllo finanziario | Acquisto e dismissione sono informali | Alcuni asset hanno dati di costo e contratto | Passaggi del ciclo di vita e dati finanziari sono registrati per gli asset principali | Costo, rinnovi e utilizzo sono rivisti e se ne tiene conto | I dati finanziari e di ciclo di vita sono collegati ai servizi e condivisi con la finanza |
| Uso dei dati | I dati sono usati da pochi | Il service desk usa a volte il registro | Desk, sicurezza e finanza usano abitualmente i dati degli asset | Qualità e uso dei dati sono misurati e migliorati | I dati alimentano le decisioni in tutta l'organizzazione e con i partner |

## Checklist

- [ ] Abbiamo un breve elenco dei tipi di asset e dei fatti che registriamo per ciascuno.
- [ ] Ogni asset o gruppo monitorato ha un responsabile nominato.
- [ ] I risultati del rilevamento sono confrontati con il registro a scadenza regolare.
- [ ] Le risorse cloud portano tag di responsabile, servizio e ambiente e quelle senza tag sono segnalate.
- [ ] I nuovi acquisti, compresi gli abbonamenti, creano o aggiornano un record.
- [ ] Gli asset sono collegati ai servizi che supportano.
- [ ] Dati di costo, contratto e rinnovo sono registrati per gli asset principali.
- [ ] La dismissione include rimozione dei dati, rimozione degli accessi e un record.
- [ ] Il registro è riconciliato con la realtà almeno due volte l'anno per le principali classi di asset.
- [ ] Service desk, sicurezza e finanza possono vedere i dati di cui hanno bisogno.

## Prompt per l'IA

**Scopo: riconciliare i risultati del rilevamento con il registro.**

```text
I have two lists of assets: what our register says we have, and what a discovery scan found. 

Register: [paste a table with asset name or ID, type, owner, and status; remove personal data].
Discovery: [paste a table with name or ID, type, and any identifying details].

Using only these lists, identify: items in the register not found by discovery; items found by discovery not in the register; and items where the details differ. For each group, suggest a question to ask the owner or the team. Do not guess what an unknown item is. If the lists are too thin to match, say what to add. List what you are unsure of.
```

**Scopo: redigere un breve standard di etichettatura per le risorse cloud.**

```text
Help me draft a one-page tagging standard for cloud resources.

Our cloud accounts and teams: [describe].
Facts we need to know about a resource: [for example owner, service, environment, cost center, data sensitivity].
Problems today: [for example untagged resources and unknown owners].

Propose three to six required tags with allowed values or formats, how untagged resources will be found and reported, who is responsible for fixing them, and a grace period (leave the length as [to be agreed]). Mark assumptions. Do not invent our tooling. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: pianificare una checklist di dismissione per un dispositivo o un server.**

```text
Help me write a retirement checklist for [asset type, for example "laptops" or "servers"].

Our current practice: [describe].
Data it may hold: [describe sensitivity].
Records we must keep: [list, or write "unknown"].
Rules or contracts that apply, with source text: [paste, or write "none known"].

Produce a checklist covering: approval, removing access and licenses, data wiping or destruction and evidence, updating the register, financial records, and disposal or return. Mark every item that is an assumption. Do not state that a law requires a step unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: trovare candidati al risparmio dai dati d'uso.**

```text
Here is a table of our subscriptions and licenses with cost per month, number of paid seats, and number of active users in the last 90 days: [paste real data].

Using only my numbers, list items where paid seats exceed active users and compute the difference and the cost of the unused seats. Rank by cost. For the top five, suggest a question to ask the owner before changing anything. Do not assume that inactive users can lose access; flag it as a question. List what you are unsure of.
```

## Competenze per l'IA

- [configuration-management](../../../../skills/configuration-management/SKILL.md): da usare per pianificare come asset e relazioni sono registrati e mantenuti veri.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): da usare per gestire i contratti e i rinnovi che stanno dietro gli asset.
- [budget-forecasting](../../../../skills/budget-forecasting/SKILL.md): da usare per prevedere il costo di asset e abbonamenti.
- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): da usare per chiarire chi possiede, supporta e approva ogni classe di asset.
- [data-governance](../../../../skills/data-governance/SKILL.md): da usare per decidere chi possiede i dati contenuti negli asset e come vengono ritirati.

## Fonti principali

- **IT asset management** (Wikipedia, attualmente all'interno dell'articolo sulla gestione dei data center): una breve definizione e una descrizione della gestione degli asset hardware.
- **Software asset management** (Wikipedia): la definizione, gli obiettivi, le tecnologie e le parti di ISO/IEC 19770.
- **Configuration management database** (Wikipedia): il termine ITIL per l'archivio di elementi di configurazione e relazioni.
- **ITIL** (Wikipedia): il framework che tratta l'ITAM insieme alla gestione dei servizi.

## Riferimenti

1. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
2. Software asset management — Wikipedia — https://en.wikipedia.org/wiki/Software_asset_management
3. Configuration management database — Wikipedia — https://en.wikipedia.org/wiki/Configuration_management_database
4. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
5. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
6. Data center management — Wikipedia — https://en.wikipedia.org/wiki/Data_center_management
7. Cloud computing — Wikipedia — https://en.wikipedia.org/wiki/Cloud_computing
8. Asset management — Wikipedia — https://en.wikipedia.org/wiki/Asset_management
9. Inventory — Wikipedia — https://en.wikipedia.org/wiki/Inventory
