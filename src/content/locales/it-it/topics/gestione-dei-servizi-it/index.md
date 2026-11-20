# Gestione dei servizi IT

**La gestione dei servizi IT (ITSM) è la disciplina che progetta, eroga, gestisce e migliora i servizi IT attorno a ciò di cui i clienti hanno bisogno, e i team agili che gestiscono servizi la praticano già, che usino o no questo nome.**

## Perché è importante

Quando un team rilascia software e poi lo gestisce, diventa un fornitore di servizi. Gli utenti dipendono da lui, si aspettano che sia disponibile e vogliono aiuto quando si guasta. L'ITSM è il corpo di pratiche nato attorno a questa relazione. I team che la ignorano spesso la riscoprono nel modo più duro: ricevendo chiamate di notte, perdendo traccia di ciò che è cambiato o discutendo con i clienti su ciò che era stato promesso.

L'ITSM ha fama di processo pesante, e una parte di quella fama è meritata. I team agili, a loro volta, hanno fama di muoversi in fretta e di lasciare alle operations il compito di gestire il risultato. Entrambe le reputazioni descrivono fallimenti, non l'intento dei due campi. L'ITSM chiede che cosa il cliente si aspetta da un servizio e come il fornitore lo erogherà e lo migliorerà. È una domanda a cui anche i team agili tengono.

Questo argomento fornisce il vocabolario usato nel resto della guida: che cos'è un servizio, chi sono i clienti e gli utenti, che cosa copre l'ITSM e da dove vengono i suoi principali framework. Usa come mappa l'[articolo di Wikipedia sulla gestione dei servizi IT](https://en.wikipedia.org/wiki/IT_service_management). Quell'articolo è breve ed elenca i framework più che spiegarli, quindi l'argomento aggiunge interpretazione pratica e segnala dove lo fa.

## Concetti fondamentali

### Che cos'è l'ITSM

L'articolo di Wikipedia definisce l'ITSM come l'insieme di attività che un'organizzazione svolge per progettare, costruire, erogare, gestire e controllare i servizi IT offerti ai clienti. Contrappone l'ITSM agli approcci orientati alla tecnologia come la gestione di rete e la gestione dei sistemi. L'ITSM, dice, adotta un approccio per processi, si concentra sui bisogni dei clienti anziché sui sistemi e sottolinea il miglioramento continuo.

L'articolo cita un'indagine del 2017 di CIO WaterCooler secondo cui le imprese usano l'ITSM soprattutto a sostegno dell'esperienza del cliente (35%) e della qualità del servizio (48%). È una sola indagine, e il suo campione non è descritto nell'articolo, quindi considera le cifre come un'illustrazione di come i professionisti descrivono i propri obiettivi e non come una misura di quanto sia comune ciascun obiettivo.

### Servizio, cliente e utente

Un **servizio** è un modo di fornire valore ad altri senza che debbano farsi carico di costi e rischi. I pagamenti online di una banca, la prenotazione degli appuntamenti di un ospedale e l'archiviazione condivisa di file di un'azienda sono tutti servizi. L'articolo distingue gli **utenti**, che usano il servizio, dai **clienti**, che lo pagano o lo commissionano. Nell'IT interno di un'azienda, il cliente può essere il responsabile di un'unità di business e gli utenti il suo personale. In un servizio pubblico, il cliente può essere un ministero e gli utenti i cittadini. I due gruppi hanno bisogni diversi, e un fornitore che ascolta solo il cliente può perdere ciò che gli utenti sperimentano.

### Attività tipiche dell'ITSM

L'articolo nomina alcune idee centrali, e la pratica ITSM standard ne aggiunge altre. Insieme danno una forma riconoscibile:

| Attività | A che cosa serve | Dove la tratta questa guida |
|---|---|---|
| **Service desk** | Un unico punto di contatto tra fornitori e utenti; gestisce incidenti e richieste di servizio | Argomento 3.1 — Service desk |
| **Gestione degli incidenti** | Ripristinare il servizio quando qualcosa lo interrompe o lo minaccia | Argomento 3.2 — Gestione degli incidenti |
| **Richieste di servizio** | Fornire le cose di routine che gli utenti chiedono, come accessi o attrezzature | Argomento 3.6 — Gestione delle richieste di servizio |
| **Problemi e cambiamenti** | Trovare e correggere le cause di fondo e controllare le modifiche ai servizi | Argomento 3.3 — Gestione dei problemi e Argomento 3.4 — Abilitazione dei cambiamenti |
| **Livelli di servizio e catalogo** | Concordare che cosa viene offerto e con quale qualità | Argomento 3.7 — Gestione dei livelli di servizio e Argomento 3.8 — Gestione del catalogo dei servizi |
| **Miglioramento continuo** | Migliorare i servizi nel tempo | Argomento 3.15 — Miglioramento continuo |

L'articolo definisce un **incidente** come un'interruzione o potenziale interruzione della disponibilità o della qualità del servizio e una **richiesta di servizio** come una richiesta di routine per un servizio. Nomina gli **accordi sul livello di servizio (SLA)** solo di passaggio, quindi la guida li spiega nell'Argomento 3.7 — Gestione dei livelli di servizio.

### Gestione dei servizi aziendale e automazione

L'articolo nota due estensioni. L'**enterprise service management (ESM)** applica strumenti e idee dell'ITSM ad altre parti di un'impresa, come le risorse umane o i servizi generali, che a loro volta ricevono richieste ed erogano servizi. L'**automazione dei processi IT** sostituisce i passaggi manuali di routine con passaggi automatizzati così che il personale possa concentrarsi sul lavoro a priorità più alta. Entrambe contano per i team agili: l'ESM mostra che la disciplina non è legata all'IT, e l'automazione è il modo in cui i piccoli team tengono il passo con il volume.

### Framework e standard

L'articolo elenca molti framework e standard. L'elenco seguente ripete le sue descrizioni di una riga ed è sviluppato nell'Argomento 2.7 — Framework e standard ITSM.

| Nome | Che cosa dice l'articolo |
|---|---|
| [ITIL](https://en.wikipedia.org/wiki/ITIL) | Pratiche dettagliate per l'ITSM e la gestione degli asset IT, che allineano l'IT agli obiettivi di business |
| [ISO/IEC 20000](https://en.wikipedia.org/wiki/ISO/IEC_20000) | Uno standard internazionale per i sistemi di gestione dei servizi, rispetto al quale un'organizzazione può essere certificata |
| [COBIT](https://en.wikipedia.org/wiki/COBIT) | Un framework di governance IT con obiettivi di controllo, metriche e modelli di maturità |
| [FitSM](https://en.wikipedia.org/wiki/FitSM) | Uno standard leggero, in gran parte allineato a ISO/IEC 20000 |
| [CMMI](https://en.wikipedia.org/wiki/CMMI) | Un modello per stabilire, gestire e migliorare i servizi |
| [TOGAF](https://en.wikipedia.org/wiki/TOGAF) | Un framework che collega gli obiettivi di business agli obiettivi architetturali |
| [Microsoft Operations Framework](https://en.wikipedia.org/wiki/Microsoft_Operations_Framework) | Indicazioni di gestione dei servizi basate sulle tecnologie Microsoft |
| [Application Services Library](https://en.wikipedia.org/wiki/Application_Services_Library) | Un framework per la gestione professionale delle applicazioni |
| [Business Information Services Library](https://en.wikipedia.org/wiki/Business_Information_Services_Library) | Un framework di buone pratiche per la gestione delle informazioni |
| Business Process Framework (eTOM) | Un framework di processi per i fornitori di telecomunicazioni |

L'articolo aggiunge che i framework ITSM hanno attinto a ISO 9000, ISO/IEC 27000 e CMMI, e che ITIL versione 2 e BS 15000, il precursore di ISO/IEC 20000, erano allineati tra loro. Descrive anche USM, un sistema di gestione basato su principi adottato dal governo olandese.

### Che cosa l'articolo non copre

L'articolo non ha una sezione storica, né critiche, né menzione di agile o DevOps. Quel silenzio conta. L'ITSM è stata criticata per l'onere dei processi e la lentezza del cambiamento, e i team agili sono stati criticati per aver trascurato le operations, ma non troverai nessuna delle due critiche lì. Questa guida colma la lacuna nella Parte 5, a partire dall'Argomento 5.1 — Gestione agile dei servizi. Dove questo argomento menziona problemi, attinge alle altre fonti della guida e all'esperienza pratica, e lo dice.

### ITSM e ITAM

L'articolo su ITIL descrive ITIL come comprensivo sia di ITSM sia di gestione degli asset IT (ITAM). L'ITAM è la disciplina del sapere quali asset IT ha un'organizzazione, quanto costano e come vengono usati. I servizi dipendono dagli asset, e le due discipline condividono informazioni, per questo la Parte 4 segue da vicino l'ITSM (vedi Argomento 4.1 — Gestione degli asset IT).

## Buone pratiche

1. **Definisci i servizi dal lato del cliente.** Elenca ciò che clienti e utenti usano davvero, con le loro parole, come "accedere", "prenotare un appuntamento" e "inviare una fattura". Raggruppa la tecnologia dietro ciascuno. È l'inizio di un catalogo dei servizi (vedi Argomento 3.8 — Gestione del catalogo dei servizi).
2. **Nomina chi sono i clienti e gli utenti.** Per ogni servizio, scrivi chi lo paga o lo commissiona e chi lo usa. Se sono persone diverse, verifica che entrambi i gruppi abbiano voce.
3. **Dai a ogni servizio un responsabile.** Nomina una persona responsabile di come il servizio funziona e migliora nel tempo. Senza un responsabile, i problemi del servizio non sono compito di nessuno.
4. **Parti dalle attività che fanno più male.** Se il dolore sono le interruzioni, rafforza prima la gestione degli incidenti. Se nessuno sa che cosa è cambiato, parti dai record dei cambiamenti. Non introdurre tutte le pratiche ITSM insieme.
5. **Usa un'unica porta d'ingresso.** Dai agli utenti un solo posto in cui chiedere aiuto e fare richieste e rendilo facile. Un service desk difficile da raggiungere viene aggirato, e allora perdi le informazioni da cui l'ITSM dipende.
6. **Separa gli incidenti dalle richieste e dai problemi.** Un incidente è un'interruzione, una richiesta è una domanda di routine e un problema è una causa di fondo. Code miste nascondono gli schemi e distorcono le misure.
7. **Registra ciò che conta e non di più.** Conserva i record di incidenti, cambiamenti e asset che userai per prendere decisioni. Elimina i campi che nessuno legge. I record sono un costo, e dovresti saper dire a che cosa serve ciascuno.
8. **Scegli i framework per problema, non per moda.** Usa ITIL, ISO/IEC 20000, COBIT o modelli più leggeri come fonti di idee per il problema che hai. Adotta le parti che aiutano e di' quali hai lasciato fuori.
9. **Automatizza la routine.** Cerca i passaggi ripetitivi, come il reset delle password e la concessione degli accessi, e automatizzali con cura. Rivedi periodicamente le azioni automatizzate perché non si allontanino da ciò di cui gli utenti hanno bisogno.
10. **Misura ciò che i clienti percepiscono.** Monitora disponibilità, tempo di ripristino del servizio e soddisfazione degli utenti prima di contare l'attività interna. Usa l'indagine dell'articolo di Wikipedia come promemoria che i professionisti già indicano esperienza del cliente e qualità come obiettivi principali.
11. **Guarda oltre l'IT.** Se altre parti dell'organizzazione gestiscono male le richieste, considera strumenti e pratiche condivisi tramite l'enterprise service management. Non imporre loro il vocabolario dell'IT.
12. **Migliora continuamente.** Riserva tempo regolare per rivedere ciò che funziona, usando i dati di incidenti e richieste, e per fare piccole modifiche (vedi Argomento 3.15 — Miglioramento continuo).

## Domande da discutere con il team

**Quali servizi forniamo, con le parole che userebbero i nostri utenti?**

Chiedi a ciascuno di scrivere le tre cose per cui gli utenti più spesso contano su di noi. Confronta gli elenchi. Le differenze di solito mostrano che il team ha immagini diverse del servizio, o che descrive i servizi per tecnologia anziché per uso. Chi facilita può chiedere quale servizio non ha un responsabile chiaro. Prosegui concordando un primo elenco di servizi.

**Chi sono i clienti e chi gli utenti del nostro servizio principale, e vogliono le stesse cose?**

Nomina la persona che commissiona o paga e le persone che usano. Chiedi che cosa vuole ciascuno dal servizio. Nell'IT interno il cliente può preoccuparsi di costi e rischi e gli utenti di velocità e facilità. Chiedi dove entrano in conflitto e come il team lo viene a sapere. Scegli un conflitto da discutere con persone reali.

**Dove vanno gli utenti quando hanno bisogno di aiuto, e quante vie ci sono?**

Conta i modi: un portale, un numero di telefono, e-mail, chat, la scrivania di un collega. Chiedi quale via preferiscono gli utenti e perché. Più vie informali significano che una parte della domanda è invisibile. La discussione dovrebbe concludersi con una decisione su quali vie tenere, quali unire e come catturare ciò che arriva per vie informali.

**Quanto bene sappiamo distinguere un incidente da una richiesta da un problema, e che cosa succede quando li mescoliamo?**

Prendi dieci ticket recenti e ordinali. I disaccordi mostrano che le definizioni differiscono nel team. Chiedi che cosa fanno le categorie miste a report e priorità. Per esempio, molte richieste dentro una coda di incidenti possono far sembrare lenta la gestione degli incidenti. Concorda definizioni semplici ed esempi.

**Quali pratiche ITSM ci mancano o facciamo solo sulla carta?**

Elenca le pratiche nella tabella sopra e valuta ciascuna come funzionante, parzialmente funzionante o solo sulla carta. Chiedi un esempio recente per ciascuna valutata come funzionante. Chi facilita dovrebbe resistere alla tentazione di colmare ogni lacuna e chiedere quale lacuna causa più danno ai clienti.

**Che cosa vorremmo che un framework facesse per noi, e che cosa temiamo che ci faccia?**

Raccogli speranze e timori sull'adozione di ITIL o ISO/IEC 20000. Le speranze sono spesso coerenza e credibilità. I timori sono spesso burocrazia e lentezza. Chiedi come ottenere le prime senza i secondi. Per esempio, adotta il vocabolario e alcune pratiche ed evita i moduli. Registra le condizioni di cui il team avrebbe bisogno.

## Nella pratica: un esempio di ITIL agile

Un rivenditore online di medie dimensioni è cresciuto da un sito web del fondatore a un'azienda con un team di dodici ingegneri, una base di clienti in crescita e un piccolo gruppo di personale di supporto. I clienti segnalano i problemi a una casella di posta condivisa e chiamano un cellulare personale quando il checkout si guasta. Gli ingegneri correggono ciò di cui vengono a sapere e raramente scrivono qualcosa. Dopo un'interruzione dei pagamenti durata tre ore, il fondatore chiede perché nessuno lo sapeva finché un cliente non ha chiamato.

Il responsabile dell'ingegneria propone l'ITSM più leggero possibile. Il team elenca i propri servizi in termini di cliente: navigazione e ricerca, checkout e pagamento, tracciamento degli ordini e account dei clienti. Ciascuno ottiene un responsabile. Un indirizzo di supporto condiviso diventa l'unica porta d'ingresso e alimenta un semplice strumento di ticket con tipi separati per incidenti e richieste. Ogni incidente che dura più di 30 minuti riceve una breve revisione, scritta in un documento condiviso. Le modifiche a checkout e pagamento sono annunciate in un canale del team prima che avvengano.

Dopo tre mesi, il team sa quanti incidenti gestisce e scopre che la maggior parte deriva da due cause. Le corregge entrambe, e l'interruzione del checkout non si ripete. Restano alcune difficoltà. I clienti continuano a telefonare al fondatore quando sono arrabbiati, quindi parte della domanda aggira lo strumento di ticket. Gli ingegneri brontolano anche che scrivere le revisioni richiede tempo, e due revisioni sono state saltate in un mese intenso. Il responsabile dell'ingegneria decide di mantenere brevi le revisioni, di chiedere al fondatore di inoltrare le chiamate all'indirizzo di supporto e di rivalutare dopo un altro trimestre di dati se serva un processo più completo in stile ITIL.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery che gestiscono anche ciò che costruiscono praticano già l'ITSM. Dai un nome ai tuoi servizi, registra incidenti e cambiamenti in modo leggero e condividi i dati con chi supporta i tuoi servizi. Tratta il service desk come una fonte di prove su ciò con cui gli utenti faticano.

### Team di servizio e di operations

Il personale operativo e del service desk porta la maggior parte della pratica ITSM. Le idee agili possono aiutare rendendo visibile il tuo lavoro, accorciando i cicli di feedback con gli utenti e spostando il miglioramento dai progetti annuali a piccole modifiche regolari. Spiega lo scopo dietro ogni regola ITSM così che i colleghi possano adattarla con buon senso.

### Leadership e governance

I leader decidono quanta struttura richiedere e quante prove chiedere. Chiedi risultati che i clienti percepiscono e poche misure che i team possano produrre dai propri strumenti. Sii cauto nell'acquistare un framework come segnale; l'articolo di Wikipedia ne elenca molti e nessuno sostituisce la conoscenza dei propri servizi.

### Clienti e utenti

Clienti e utenti sono la ragione per cui esiste l'ITSM. Aspettati un modo chiaro di chiedere aiuto, informazioni oneste su che cosa aspettarti e qualcuno che possieda ogni servizio. In cambio, fornisci informazioni tempestive e specifiche quando qualcosa va storto, così che il fornitore possa imparare.

## Modalità di fallimento comuni

- **Processo fine a se stesso.** Moduli e approvazioni si moltiplicano e nessuno ricorda perché. Collega invece ogni pratica a uno scopo ed elimina quelle che non ne servono più uno.
- **Nessuna porta d'ingresso unica.** Gli utenti si rivolgono a chi conoscono e la domanda è invisibile. Offri invece una via facile e porta dentro di essa le richieste informali.
- **Mescolare incidenti, richieste e problemi.** I report ingannano e le cause restano nascoste. Usa invece definizioni semplici e ordina i ticket in modo coerente.
- **Servizi descritti per tecnologia.** Gli utenti non trovano ciò che serve e i responsabili non sono chiari. Descrivi invece i servizi in termini di cliente e nomina un responsabile per ciascuno.
- **Adottare un framework in blocco.** I team copiano un grande framework e si seppelliscono di processi. Parti invece dal problema e prendi solo le parti che aiutano.
- **Ignorare gli utenti.** Il fornitore parla solo con il cliente che paga. Ascolta invece sia i clienti sia gli utenti e cerca i conflitti.
- **Misurare l'attività.** I conteggi di ticket e chiamate sostituiscono le prove della qualità del servizio. Misura invece disponibilità, tempo di ripristino del servizio e soddisfazione degli utenti.
- **Trattare l'ITSM come separato dalla delivery.** I team di delivery rilasciano e lasciano le operations a cavarsela. Collegali invece con servizi condivisi, dati condivisi e revisioni congiunte (vedi Argomento 5.1 — Gestione agile dei servizi).

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Definizione dei servizi | I servizi sono descritti per tecnologia o per niente | Alcuni servizi sono elencati con i responsabili | Tutti i servizi sono descritti in termini di cliente con responsabili nominati | Le descrizioni dei servizi sono verificate rispetto a uso e feedback | Le definizioni dei servizi sono condivise con clienti e fornitori e aggiustate insieme |
| Supporto e richieste | L'aiuto è chiesto per vie informali | Alcuni team hanno uno strumento di ticket o una casella condivisa | Una porta d'ingresso con tipi chiari per incidenti e richieste | Domanda e tempi di risoluzione sono monitorati e rivisti | Il supporto è coordinato tra team e fornitori con dati condivisi |
| Record e misure | Si conservano pochi record | Alcuni team registrano incidenti e cambiamenti | I record sono coerenti e ciascuno ha uno scopo dichiarato | Le misure rivolte al cliente sono riviste regolarmente | Le misure sono condivise tra i servizi e usate per fissare insieme le priorità |
| Miglioramento | Le correzioni seguono le crisi | Alcuni team rivedono gli incidenti | La revisione regolare dei dati di incidenti e richieste porta a modifiche pianificate | Il lavoro di miglioramento ha risorse e i suoi risultati sono verificati | Il miglioramento è routine tra i team e con i clienti |

## Checklist

- [ ] Abbiamo un elenco dei nostri servizi nel linguaggio dei clienti.
- [ ] Ogni servizio ha un responsabile nominato.
- [ ] Sappiamo chi sono i clienti e chi gli utenti di ciascun servizio.
- [ ] Gli utenti hanno un'unica porta d'ingresso chiara per aiuto e richieste.
- [ ] Incidenti, richieste e problemi sono registrati come cose diverse.
- [ ] Ogni tipo di record ha uno scopo dichiarato e i campi inutilizzati sono rimossi.
- [ ] Misuriamo almeno una cosa che i clienti percepiscono, come la disponibilità o il tempo di ripristino del servizio.
- [ ] Rivediamo regolarmente i dati di incidenti e richieste e agiamo di conseguenza.
- [ ] Sappiamo dire quali idee dei framework usiamo e quali abbiamo lasciato fuori.
- [ ] I compiti di routine che possono essere automatizzati in sicurezza sono stati individuati.

## Prompt per l'IA

**Scopo: redigere un elenco dei tuoi servizi nel linguaggio dei clienti.**

```text
Help me describe the services my team provides in the words our users would use.

Who we are and what we run: [describe the team and its main systems in a few sentences].
Who uses what: [list user groups and what each group does with our systems].
What we currently call our services: [paste a list, or write "none"].

Produce a draft list of 5 to 10 services, each with a one-sentence description from the user's point of view, the customer or user groups, and a suggested owner role. Mark each item that is a guess. Do not invent systems I did not mention. Ask clarifying questions first if information is missing, and list what you are unsure of.
```

**Scopo: ordinare i ticket recenti in incidenti, richieste e problemi.**

```text
Here are [number] recent tickets or messages to our team: [paste short, anonymized descriptions, one per line].

Definitions to use: an incident is an unplanned disruption or potential disruption to a service; a service request is a routine request for something the service normally provides; a problem is the underlying cause of one or more incidents.

Classify each item as incident, request, or possible problem, with one sentence of reasoning that uses only what I wrote. List items you could not classify and the question I should ask to decide. At the end, tell me the share in each category from my list only. Do not invent details, and list what you are unsure of.
```

**Scopo: scegliere un piccolo primo insieme di pratiche ITSM per la tua situazione.**

```text
Help me choose a first set of IT service management practices for a team in this situation.

Team size and type: [describe].
Our biggest pains (with a recent example for each): [list].
Existing tools and records: [list, or write "none"].
Rules we must follow (audit, security, contracts), with source text if you have it: [paste, or write "none known"].

From these practices: service desk, incident management, problem management, change enablement, service request management, service level management, service catalog management, knowledge management, continual improvement, propose the two or three to start with and say why, using only the information above. Say what you would leave for later. Mark assumptions, ask clarifying questions first, and list what you are unsure of.
```

**Scopo: preparare una conversazione tra un team di delivery e il service desk.**

```text
Plan a 45-minute conversation between a delivery team and the service desk about how new changes are handed over.

Delivery team: [describe]. Service desk: [describe].
Recent example of a handover that went badly: [describe factually].
What the service desk says it needs: [list, or write "unknown"].

Produce an agenda, five questions for each side, and a closing step that records one agreed change with an owner. Keep it free of any particular tool. Ask clarifying questions first if information is missing, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [service-catalog](../../../../skills/service-catalog/SKILL.md): da usare per redigere o rivedere un elenco di servizi nel linguaggio dei clienti, con responsabili e descrizioni.
- [service-level-agreement](../../../../skills/service-level-agreement/SKILL.md): da usare quando sei pronto a concordare con i clienti quale livello di servizio aspettarsi.
- [incident-response-plan](../../../../skills/incident-response-plan/SKILL.md): da usare per preparare come il tuo team gestisce un incidente prima che ne avvenga uno.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): da usare per capire quali tipi di richieste e incidenti arrivano e in quale volume.
- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): da usare per chiarire chi possiede ogni servizio e chi è consultato o informato.

## Fonti principali

- **IT service management** (Wikipedia): una breve definizione con un elenco di framework e standard correlati, utile come mappa.
- **ITIL** (Wikipedia): la storia e le versioni del più noto framework ITSM, compresi i cambi di proprietà.
- **ISO/IEC 20000** (Wikipedia): contesto sullo standard internazionale per i sistemi di gestione dei servizi.
- **Enterprise service management** (Wikipedia): un'introduzione all'applicazione delle idee ITSM oltre l'IT.

## Riferimenti

1. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
2. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
3. ISO/IEC 20000 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_20000
4. COBIT — Wikipedia — https://en.wikipedia.org/wiki/COBIT
5. FitSM — Wikipedia — https://en.wikipedia.org/wiki/FitSM
6. CMMI — Wikipedia — https://en.wikipedia.org/wiki/CMMI
7. TOGAF — Wikipedia — https://en.wikipedia.org/wiki/TOGAF
8. Microsoft Operations Framework — Wikipedia — https://en.wikipedia.org/wiki/Microsoft_Operations_Framework
9. Application Services Library — Wikipedia — https://en.wikipedia.org/wiki/Application_Services_Library
10. Business Information Services Library — Wikipedia — https://en.wikipedia.org/wiki/Business_Information_Services_Library
11. Enterprise service management — Wikipedia — https://en.wikipedia.org/wiki/Enterprise_service_management
12. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
