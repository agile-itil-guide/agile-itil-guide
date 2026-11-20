# Gestione della configurazione

**La gestione della configurazione mantiene un quadro accurato e utilizzabile delle parti di un servizio e di come si relazionano, e la sua forma moderna è un record costruito da codice e rilevamento di cui ci si fida perché il sistema stesso lo mantiene aggiornato.**

## Perché è importante

Quando qualcosa si rompe, le prime domande sono sempre le stesse. Che cos'è questo componente? A che cosa si collega? Che cosa è cambiato? Chi lo possiede? Se trovare le risposte richiede un'ora, un incidente che si sarebbe potuto correggere in pochi minuti si trascina. Quando si pianifica una modifica, le stesse domande decidono se capisci il rischio. Un buon quadro del servizio e delle sue parti è una delle cose più utili che un team operativo possa avere.

È anche una delle più difficili da mantenere vera. I documenti dell'infrastruttura, disegnati una volta, sono obsoleti nel giro di settimane. I database dei componenti, mantenuti a mano, sono sbagliati in modi che nessuno può vedere. I modi di lavorare agili e cloud peggiorano le cose in un senso, con molte parti piccole e in rapido cambiamento, e le migliorano in un altro, perché la configurazione può essere scritta come codice, conservata nel controllo di versione e applicata automaticamente.

L'articolo della Wikipedia inglese sulla gestione della configurazione la descrive come un processo di gestione per stabilire e mantenere la coerenza tra gli attributi di un prodotto e i suoi requisiti, il progetto e le informazioni operative durante la sua vita, con radici nel Dipartimento della Difesa degli Stati Uniti negli anni Cinquanta. L'articolo sui database di gestione della configurazione descrive il termine ITIL per l'archivio di elementi di configurazione e delle loro relazioni. L'articolo sull'infrastruttura come codice descrive la gestione delle risorse attraverso file di definizione leggibili dalla macchina. Insieme danno la visione tradizionale e quella moderna, e questo argomento le collega.

## Concetti fondamentali

### La gestione della configurazione in generale

Secondo Wikipedia, la gestione della configurazione (CM) è usata nei sistemi militari, nella gestione dei servizi IT sotto ITIL e nell'ingegneria civile. La sua storia comincia con il Dipartimento della Difesa degli Stati Uniti negli anni Cinquanta come disciplina tecnica per l'hardware, con standard militari alla fine degli anni Sessanta e Settanta che ne fanno una disciplina a sé. L'articolo nomina diversi standard, tra cui ANSI/EIA-649, ISO 10007 (edizione 2017) e IEEE 828-2012. Le discipline centrali che elenca, dai manuali militari e dallo standard EIA, sono:

| Disciplina | Che cosa fa |
|---|---|
| **Pianificazione e gestione** | Un piano che copre persone, formazione, convenzioni di denominazione, audit e requisiti dei fornitori |
| **Identificazione della configurazione** | Fissare e mantenere baseline che definiscono architettura e componenti; i prodotti tracciati sono gli **elementi di configurazione (CI)** |
| **Controllo della configurazione** | Valutare le richieste di modifica e approvarle o rifiutarle |
| **Registrazione dello stato della configurazione** | Registrare e riferire le descrizioni dei CI e gli scostamenti dalla baseline |
| **Verifica e audit** | Controlli indipendenti che il sistema corrisponda alla sua documentazione e ai requisiti |

Una **baseline** è un punto di riferimento concordato; una volta che un attributo è in baseline, le modifiche passano per un controllo formale, sono valutate, approvate e poi nuovamente messe in baseline. L'articolo distingue la gestione della configurazione dalla gestione degli asset, che si concentra sulla contabilità finanziaria e sul valore degli asset IT (vedi Argomento 4.1 — Gestione degli asset IT).

### Gestione della configurazione del software

L'articolo descrive la gestione della configurazione del software come l'individuazione degli attributi del software in vari punti e il controllo delle modifiche per mantenere integrità e tracciabilità, con le stesse quattro procedure di identificazione, controllo, registrazione dello stato e audit. I sistemi di controllo di versione, gli strumenti di build e i record dei rilasci ne sono istanze moderne.

### Il database di gestione della configurazione

Wikipedia descrive un **configuration management database (CMDB)** come un termine ITIL per un database che memorizza informazioni sugli asset hardware e software di un'organizzazione, i CI, e sulle relazioni tra essi. "Represents the authorized configuration of the significant components of the IT environment". Punti chiave dall'articolo:

- **I CI hanno attributi** come identificatore, nomi, descrizioni, proprietà e importanza, che possono essere centinaia.
- **Le relazioni** di solito collegano un CI di origine a un CI di destinazione. Relazioni più avanzate aggiungono un descrittore, come un database che è componente di un'applicazione.
- **Federazione:** le implementazioni spesso federano dati da fonti come la gestione degli asset, così che ciascuna fonte mantenga il controllo dei propri dati; l'articolo lo contrappone al copiare i dati nel CMDB.
- **Usi:** analisi dell'impatto, analisi delle cause radice, gestione dei cambiamenti, gestione degli incidenti, inventario e build.
- **Tipi di CI:** hardware, software, comunicazioni e reti, luoghi, documentazione e persone; le organizzazioni mature aggiungono tipi di business come prodotti e fornitori.
- **Difficoltà:** rilevanza (raccogliere dati lungo il ciclo di vita di ogni CI), manutenzione (mantenere alta la qualità dei dati, il che richiede diversi ruoli specialistici) e usabilità (i CMDB sono spesso semplici database privi di visualizzazione, quindi può servire uno strato applicativo ulteriore).

L'articolo indica il rilevamento automatico dei CI e il tracciamento dei cambiamenti come fattori chiave di successo. Non indica una data di fondazione, una versione specifica di ITIL né dati di adozione ed è segnalato come bisognoso di più citazioni. Dice anche che ITIL ha rinominato il processo Service Asset and Configuration Management in ITIL versione 3 (questo viene dall'articolo sulla gestione della configurazione).

### Infrastruttura come codice

L'articolo sull'infrastruttura come codice descrive la pratica di gestire e fornire risorse del data center attraverso file di definizione leggibili dalla macchina, anziché con configurazione manuale o strumenti interattivi, con le definizioni conservate nel controllo di versione. Distingue:

- Approcci **dichiarativi**, che descrivono lo stato finale desiderato e lasciano al sistema il compito di ricavare i passaggi, e approcci **imperativi**, che specificano i comandi in ordine. L'articolo dice che l'IaC usa più spesso definizioni dichiarative.
- Metodi **push**, in cui un sistema di controllo invia istruzioni ai server, e metodi **pull**, in cui i server recuperano le proprie istruzioni.

Nomina molti strumenti da CFEngine (1993) a Terraform, Ansible, Puppet, Chef, Pulumi e OpenTofu e collega la pratica a DevOps coinvolgendo gli sviluppatori nella configurazione e portando prima le operations. Le sue affermazioni sui benefici, su costo, velocità e riduzione dell'errore umano, sono etichettate come bisognose di citazioni. Cita un rapporto del 2020 di Unit 42 che ha trovato circa 200.000 potenziali vulnerabilità nei modelli IaC, un promemoria che anche il codice può portare difetti. L'articolo non menziona la deriva della configurazione né l'idempotenza.

### Configurazione dichiarata e rilevata

Un modo utile di pensare alla gestione moderna della configurazione è che esistono due fonti di verità, e il valore sta nel confrontarle:

| Fonte | Che cosa dice | Punto di forza | Debolezza |
|---|---|---|---|
| **Dichiarata** (codice, definizioni nel controllo di versione) | Che cosa intendiamo che il sistema sia | Rivedibile, versionata, ripetibile | Può non corrispondere a ciò che gira |
| **Rilevata** (scansioni, API cloud, agenti) | Che cosa esiste ora | Riflette la realtà | Non dice che cosa è inteso o perché |

Un CMDB alimentato da entrambe può mostrare la **deriva** (drift), la differenza tra stato inteso ed effettivo. Le fonti lette per questa guida non usano la parola, ma nomina il problema che le discipline CM di registrazione dello stato e audit sono pensate per cogliere.

### Gestione della configurazione e cambiamento

Controllo della configurazione e abilitazione dei cambiamenti sono partner stretti (vedi Argomento 3.4 — Abilitazione dei cambiamenti). Le discipline CM dicono che le modifiche agli elementi in baseline sono valutate e approvate. In un'impostazione basata su pipeline, una modifica al codice che definisce l'infrastruttura è rivista e testata come qualsiasi altra e il record della pipeline mostra chi ha cambiato che cosa e quando. Il CMDB o il suo equivalente riflette poi il risultato.

### Usi nella gestione dei servizi

Le relazioni registrate nei dati di configurazione rispondono a domande in tutte le altre pratiche:

- **Incidenti:** che cosa dipende da questo componente guasto e chi lo possiede (vedi Argomento 3.2 — Gestione degli incidenti)?
- **Problemi:** quali componenti erano coinvolti in incidenti ripetuti (vedi Argomento 3.3 — Gestione dei problemi)?
- **Cambiamenti:** qual è il raggio d'azione di questa modifica?
- **Continuità:** che cosa deve essere ripristinato e in che ordine (vedi Argomento 3.12 — Gestione della continuità del servizio)?
- **Sicurezza:** che cosa è esposto e che cosa è cambiato?

### Limiti delle fonti

L'articolo sulla gestione della configurazione è segnalato come bisognoso forse di una riscrittura e dice poco sull'implementazione pratica. L'articolo sul CMDB non ha una sezione di critiche e poche citazioni. L'esperienza sul campo è che i CMDB falliscono spesso cercando di contenere troppo, troppo accuratamente, per troppo tempo. Consideralo un'esperienza pratica che questa guida offre, non un risultato delle fonti.

## Buone pratiche

1. **Parti dalle domande a cui devi rispondere.** Elenca le domande che chi risponde agli incidenti, chi rivede i cambiamenti e chi pianifica la continuità pongono, come "che cosa dipende da questo?" e "chi lo possiede?". Registra solo ciò che vi risponde.
2. **Definisci un piccolo insieme di tipi di elementi di configurazione.** Parti da servizi, applicazioni, host o container, database e dipendenze esterne chiave. Aggiungi tipi quando una domanda lo richiede.
3. **Registra le relazioni, non solo gli elementi.** Cattura quali elementi dipendono da quali e quale servizio supportano. Le relazioni rendono utili i dati per l'analisi dell'impatto.
4. **Nomina un responsabile per ogni elemento.** Un elemento senza responsabile è un rischio. Fai della responsabilità parte di come gli elementi sono creati.
5. **Tieni la configurazione intesa nel controllo di versione.** Esprimi infrastruttura e configurazione come codice, rivedila come altro codice e lascia che la pipeline la applichi. Il repository è allora un record di intenzione e storia.
6. **Usa il rilevamento per trovare la realtà.** Scansiona reti e account cloud per vedere che cosa esiste e confrontalo con la configurazione dichiarata. Indaga sulle differenze (drift) anziché ignorarle.
7. **Federa invece di copiare dove puoi.** Lascia che ogni fonte di dati (registro degli asset, account cloud, strumenti di deployment) possieda i propri fatti e collegati ad essi dai dati di configurazione, come descrive l'articolo sul CMDB.
8. **Automatizza gli aggiornamenti.** Alimenta i dati di configurazione dalla pipeline e dal rilevamento così che cambino al cambiare del sistema. Gli aggiornamenti manuali resteranno indietro.
9. **Metti in baseline ciò che conta.** Per i servizi critici, registra la configurazione approvata e applica un controllo formale dei cambiamenti agli scostamenti da essa. Per il resto basta un controllo più leggero.
10. **Fai audit regolari.** Confronta i dati con la realtà per un campione di elementi ogni trimestre e correggi il processo dietro qualsiasi differenza. È la disciplina di verifica e audit nella pratica.
11. **Rendi i dati facili da usare.** Fornisci visualizzazione e ricerca per chi risponde e chi pianifica, perché dati che non si leggono in fretta non saranno usati.
12. **Tieni presente la sicurezza.** Tratta il codice di configurazione come sensibile, scansiona i modelli per debolezze e controlla chi può cambiare la baseline. La cifra di Unit 42 nell'articolo sull'infrastruttura come codice è un promemoria del rischio.

## Domande da discutere con il team

**Quando avviene un incidente, quanto tempo ci vuole per scoprire che cosa dipende dal componente guasto?**

Guarda l'ultimo incidente e il tempo speso su questa domanda. Chiedi da dove è venuta la risposta: un diagramma, una persona, una ricerca. Chi facilita può chiedere che cosa avrebbe fatto risparmiare più tempo. Spesso è un elenco di dipendenze e responsabili per i servizi più importanti. Concorda di produrne uno per un servizio.

**Dove è definita la nostra infrastruttura, e corrisponde a ciò che gira?**

Chiedi se gli ambienti principali sono costruiti da codice e con quale frequenza qualcuno li cambia a mano. Cerca le differenze. Se non lo sai, pianifica un confronto per un ambiente. Discuti come evitare le modifiche manuali o rilevarle rapidamente.

**Quali elementi nei nostri record di configurazione non hanno un responsabile o non sono stati confermati di recente?**

Prendi un campione e conta. Chiedi perché sono in quello stato: nessun processo per i responsabili, nessun promemoria, nessuna conseguenza. Discuti un meccanismo leggero, come una conferma annuale o un tag di responsabile richiesto alla creazione. Scegline uno.

**Quali dati teniamo che nessuno usa?**

Elenca i campi e i tipi di record e chiedi chi li ha usati nell'ultimo trimestre. L'articolo sul CMDB nomina la manutenzione come difficoltà centrale, e i dati inutilizzati sono un costo senza beneficio. Rimuovi o smetti di mantenere ciò che nessuno usa.

**Che cosa dovremmo vedere per approvare con fiducia una modifica a un servizio critico?**

Chiedilo ai revisori. Risposte tipiche: che cosa tocca la modifica, che cosa ne dipende, che cosa ha fatto l'ultima volta. Chiedi quali di queste i dati di configurazione possono dare. Scegli un elemento mancante da aggiungere.

**Chi può cambiare la baseline dei nostri servizi critici, e come sappiamo quando lo fa?**

Chiedi l'elenco e le prove dei cambiamenti. Discuti se le modifiche fuori dalla pipeline sono rilevate. Concorda come sarà trovata la deriva e chi agisce.

## Nella pratica: un esempio di ITIL agile

Un'agenzia fiscale nazionale gestisce 120 applicazioni e un misto di server on-premises e servizi cloud. Un team di sei ingegneri operativi mantiene un CMDB caricato da un foglio di calcolo tre anni fa. Durante un incidente maggiore sul portale delle dichiarazioni, gli ingegneri scoprono che il CMDB elenca un server di database ritirato un anno prima e omette il bilanciatore di carico che si è effettivamente guastato. L'incidente richiede tre ore in più per essere risolto perché ci vuole altrettanto per capire da che cosa dipende il portale.

La responsabile delle operations e un ingegnere rivedono quali domande pongono chi risponde. Restringono l'ambito del CMDB a servizi, applicazioni, principali componenti di infrastruttura dietro di essi e dipendenze esterne chiave ed eliminano i tipi di basso valore. L'infrastruttura del portale delle dichiarazioni viene spostata in codice nel controllo di versione e la pipeline scrive nel CMDB un record di ogni componente installato. Una scansione di rilevamento della rete e degli account cloud gira ogni notte e un report elenca le differenze tra dati dichiarati e rilevati. Ogni elemento ha un campo responsabile, che anche il report verifica. Dai dati viene costruita una semplice vista delle dipendenze per il portale delle dichiarazioni.

Un trimestre dopo, la vista delle dipendenze del portale è abbastanza accurata da essere usata dal team del successivo incidente nei primi dieci minuti. Il report notturno delle differenze trova 14 server non gestiti, la maggior parte dei quali ritirati o rivendicati dai responsabili. Restano problemi. I servizi fuori dal portale delle dichiarazioni si affidano ancora ai vecchi dati, e un team continua a fare modifiche a mano a un server di database che la pipeline poi sovrascrive, causando una breve interruzione. La responsabile delle operations estende l'approccio ai tre servizi successivi, aggiunge una regola per cui le modifiche in produzione passano per la pipeline e chiede al report di rilevamento di segnalare le modifiche manuali.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery definiscono la configurazione attraverso il codice. Metti infrastruttura e impostazioni nel controllo di versione, rivedile e lascia che la pipeline le applichi. Etichetta le risorse con responsabile e servizio e descrivi le dipendenze nel repository o nel record del servizio.

### Team di servizio e di operations

I team operativi usano e mantengono i dati di configurazione. Mantieni piccolo l'ambito, confronta la configurazione dichiarata e quella rilevata e insegui la deriva. Riporta ciò che impari dagli incidenti nei tipi e nelle relazioni che registri.

### Leadership e governance

I leader decidono quanto sforzo meritano i dati di configurazione. Chiedi quali decisioni sostengono, come analisi dell'impatto e pianificazione della continuità, e giudica dall'uso. Evita di finanziare un enorme database per se stesso. Sostieni i controlli di pipeline che mantengono veri i record.

### Clienti e utenti

Clienti e utenti traggono vantaggio quando gli incidenti sono risolti più in fretta e le modifiche rompono meno, cosa che buoni dati di configurazione aiutano a ottenere. Raramente vedono i dati. Chiedi ai fornitori come sanno che cosa una modifica influenza e come trovano la causa di un'interruzione.

## Modalità di fallimento comuni

- **Cercare di registrare tutto.** I dati sono troppo grandi per essere mantenuti veri. Parti invece dalle domande e dai servizi critici.
- **Manutenzione manuale.** I record restano indietro. Alimenta invece i dati dalla pipeline e dal rilevamento.
- **Nessuna relazione.** Gli elementi sono elencati ma non collegati. Cattura invece dipendenze e il servizio che ogni elemento supporta.
- **Nessun responsabile.** Nessuno conferma o corregge i record. Richiedi invece un responsabile e verifica regolarmente.
- **Modifiche manuali fuori dalla pipeline.** Realtà e intenzione divergono. Instrada invece i cambiamenti attraverso la pipeline e rileva la deriva.
- **Dati illeggibili.** Chi risponde non può usare il database. Fornisci invece ricerca e visualizzazione.
- **Copiare invece di federare.** I dati duplicati diventano obsoleti. Collegati invece alla fonte che possiede i fatti.
- **Il codice di configurazione trattato come innocuo.** I modelli portano vulnerabilità. Scansionali e rivedili invece.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Ambito e relazioni | I componenti sono noti in modo informale | Alcuni servizi hanno elenchi di componenti | I servizi chiave hanno elementi, responsabili e dipendenze registrati | Copertura e accuratezza sono misurate e le lacune colmate | I dati di configurazione coprono team, cloud e fornitori |
| Configurazione dichiarata | I sistemi sono configurati a mano | Alcuni ambienti usano codice | Infrastruttura e configurazione dei servizi chiave sono codice nel controllo di versione | Storia dei cambiamenti e deriva sono monitorate | Il codice di configurazione è condiviso e riusato tra i team |
| Rilevamento e verifica | La realtà è presunta | Si eseguono scansioni occasionali | Il rilevamento regolare è confrontato con i dati dichiarati | Differenze e cause sono misurate e ridotte | Rilevamento e verifica sono automatizzati in tutta l'organizzazione |
| Uso dei dati | I dati sono raramente consultati | Usati in alcuni incidenti | Usati abitualmente per incidenti, cambiamenti e pianificazione della continuità | Uso e beneficio sono misurati e i dati migliorati | I dati sostengono le decisioni in tutta l'organizzazione e con i partner |

## Checklist

- [ ] Abbiamo elencato le domande a cui chi risponde e chi rivede hanno bisogno che i dati di configurazione rispondano.
- [ ] Registriamo un piccolo insieme di tipi di elementi con responsabili e relazioni.
- [ ] Infrastruttura e configurazione dei servizi chiave sono nel controllo di versione.
- [ ] Le modifiche in produzione a quei servizi passano per la pipeline.
- [ ] I risultati del rilevamento sono confrontati con la configurazione dichiarata a scadenza fissa.
- [ ] Le differenze (drift) sono indagate e corrette.
- [ ] I record sono alimentati automaticamente dalla pipeline e dal rilevamento dove possibile.
- [ ] Un campione di record è verificato rispetto alla realtà ogni trimestre.
- [ ] I dati possono essere ricercati e visualizzati facilmente da chi risponde.
- [ ] Il codice di configurazione è rivisto e scansionato per debolezze.

## Prompt per l'IA

**Scopo: decidere che cosa registrare elencando le domande a cui devi rispondere.**

```text
Help me decide what configuration data to record for [service].

The questions responders and change reviewers ask, in our words: [list].
What we record today: [describe, or write "nothing"].
Where data lives (tools, repositories, cloud accounts): [list].

For each question, say what item types and relationships would be needed to answer it, where the data could come from automatically, and what would still need a person. Propose a minimal set of item types and fields. Mark guesses. Do not invent tools we do not have. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: riassumere la deriva tra configurazione dichiarata e rilevata.**

```text
Here is a list of items found by discovery and a list of items declared in our configuration code or records.

Discovered: [paste names or IDs, with type and key attributes].
Declared: [paste names or IDs, with type and key attributes].

Using only these lists, identify items found but not declared, items declared but not found, and items where attributes differ. Group them and suggest a question to ask about each group (for example whether it is retired, owned by someone else, or created by hand). Do not guess the cause. List what you are unsure of.
```

**Scopo: costruire una vista delle dipendenze per un servizio.**

```text
Help me describe the dependencies of [service] so that responders can use them in an incident.

What the service does: [describe].
Components I know (applications, databases, network, cloud services, external suppliers): [list with how they connect].
Owners I know: [list].

Produce a simple text diagram and a table with: component, what depends on it, owner (or "unknown"), and what to check first if it fails (only from my text; otherwise "ask owner"). Highlight single points of failure that appear in my description. Do not invent components. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: pianificare un audit trimestrale dei record di configurazione.**

```text
Plan a one-hour quarterly audit of our configuration records for [scope].

How records are created and updated today: [describe].
Sample size we can handle: [number].

Give a method: how to choose a sample, how to check each item against reality, what to record, how to calculate the share that is accurate (from the audit results only), and how to turn errors into process fixes. Keep it tool-free. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [configuration-management](../../../../skills/configuration-management/SKILL.md): da usare per pianificare che cosa registrare, come mantenerlo vero e come usarlo.
- [change-request](../../../../skills/change-request/SKILL.md): da usare per scrivere record di cambiamento che rimandano agli elementi interessati.
- [runbook](../../../../skills/runbook/SKILL.md): da usare per trasformare la conoscenza di configurazione in passaggi che chi risponde può seguire.
- [enterprise-architecture](../../../../skills/enterprise-architecture/SKILL.md): da usare per collocare servizi, applicazioni e infrastruttura in un quadro architetturale.
- [evolutionary-architecture](../../../../skills/evolutionary-architecture/SKILL.md): da usare per mantenere configurazione e progetto in cambiamento sicuro nel tempo.

## Fonti principali

- **Configuration management** (Wikipedia): storia, discipline centrali, baseline e standard della gestione della configurazione.
- **Configuration management database** (Wikipedia): la definizione, i contenuti, gli usi e le difficoltà di un CMDB.
- **Infrastructure as code** (Wikipedia): gestire le risorse attraverso definizioni leggibili dalla macchina, con un elenco di strumenti e note su benefici e rischi.
- **ITIL** (Wikipedia): il framework in cui compaiono il CMDB e la gestione della configurazione.

## Riferimenti

1. Configuration management — Wikipedia — https://en.wikipedia.org/wiki/Configuration_management
2. Configuration management database — Wikipedia — https://en.wikipedia.org/wiki/Configuration_management_database
3. Infrastructure as code — Wikipedia — https://en.wikipedia.org/wiki/Infrastructure_as_code
4. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
5. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
6. Software configuration management — Wikipedia — https://en.wikipedia.org/wiki/Software_configuration_management
7. Version control — Wikipedia — https://en.wikipedia.org/wiki/Version_control
8. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
9. Change management — Wikipedia — https://en.wikipedia.org/wiki/Change_management
