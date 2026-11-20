# Le quattro dimensioni della gestione dei servizi

**Le quattro dimensioni di ITIL 4 sono una checklist per scoprire che cosa manca a un servizio: le persone e la struttura giuste, informazione e tecnologia, partner e fornitori e flussi di lavoro definiti, e una debolezza in una qualsiasi di esse limita il valore delle altre.**

## Perché è importante

Quando un servizio delude, i team tendono a cercare la correzione che conoscono meglio. Gli ingegneri sospettano la tecnologia, i manager il processo e le risorse umane le competenze. Ognuno può avere ragione, e le probabilità di correggere il problema sono migliori se si guarda in tutti e quattro i posti. Le quattro dimensioni offrono una cornice semplice per farlo.

Le dimensioni sono anche un utile freno a un comune fallimento agile. Un team eccellente nel consegnare codice può comunque consegnare un servizio scadente se nessuno ha pensato al fornitore da cui dipende la sua API, alle competenze necessarie per supportarlo di notte o alle informazioni di cui il service desk avrà bisogno quando si guasta. Allo stesso modo, un gruppo di gestione dei servizi che perfeziona i propri processi può trascurare la cultura e gli strumenti che li fanno funzionare.

Secondo la pagina ITIL 4 Foundation di PeopleCert, le quattro dimensioni sono organizzazioni e persone; informazione e tecnologia; partner e fornitori; flussi di valore e processi. Quell'elenco è l'unica parte di questo argomento presa direttamente dalle pagine pubbliche del proprietario del framework. Le descrizioni che seguono vengono da fonti di fornitori di formazione e di commento, che concordano tra loro ma sono secondarie. Controlla le pubblicazioni ITIL 4 quando ti serve la formulazione esatta.

## Concetti fondamentali

### Le quattro dimensioni

La tabella dà ciascuna dimensione, che cosa copre come ampiamente riassunto e una domanda da porre su un servizio.

| Dimensione | Che cosa copre | Una domanda da porre |
|---|---|---|
| **Organizzazioni e persone** | La struttura, la cultura, i ruoli, le competenze e la leadership necessari per svolgere il lavoro; si estende oltre il personale IT a tutti coloro che interagiscono con il servizio | Chi fa che cosa, con quali competenze, e la cultura lo sostiene? |
| **Informazione e tecnologia** | Le informazioni e la conoscenza che il servizio usa e crea, e gli strumenti e la tecnologia che lo supportano | Che cosa dobbiamo sapere, e su che cosa lo facciamo girare? |
| **Partner e fornitori** | Le relazioni con altre organizzazioni che contribuiscono al servizio, compreso come i fornitori sono selezionati, gestiti e integrati | Chi altro è coinvolto, e per che cosa dipendiamo da loro? |
| **Flussi di valore e processi** | Le attività e i flussi di lavoro attraverso cui si crea valore e come sono organizzati e controllati | Come si muove il lavoro, e dove aspetta? |

Le fonti formative sottolineano che le dimensioni sono interdipendenti. Dedicare troppa poca attenzione a una qualsiasi limita il valore che un'organizzazione può dare ai propri stakeholder.

### Relazione con il resto del framework

Le dimensioni si applicano a ogni parte del sistema di valore del servizio (vedi Argomento 2.3 — Il sistema di valore del servizio ITIL). Una pratica, come la gestione degli incidenti, può essere esaminata attraverso ciascuna: di quali persone e ruoli ha bisogno, quali informazioni e strumenti, quali fornitori e quali processi. Si collegano anche ai principi guida, in particolare a "pensare e lavorare in modo olistico" (vedi Argomento 2.4 — I principi guida di ITIL).

### Fattori esterni

Le fonti formative e di commento descrivono anche fattori esterni che influenzano tutte e quattro le dimensioni. Usano comunemente l'acronimo **PESTLE**: politici, economici, sociali (alcune fonti dicono socioculturali), tecnologici, legali e ambientali. Sono cose che l'organizzazione non può controllare ma deve considerare, perché possono creare rischi o innescare la necessità di cambiare un servizio. Un cambiamento di legge può alterare quali informazioni un servizio può conservare; uno spostamento economico può cambiare i prezzi di un fornitore; una nuova tecnologia può cambiare le aspettative dei clienti. Le fonti suggeriscono di rivederli ogni volta che si considera come rispondere a una domanda o a un'opportunità che cambiano.

### Le dimensioni in un team agile

I team agili già lavorano per abitudine con alcune dimensioni e ne trascurano altre.

| Dimensione | Che cosa i team agili di solito fanno bene | Che cosa spesso manca |
|---|---|---|
| Organizzazioni e persone | Team auto-organizzati, retrospettive, attenzione alla motivazione | Carico di reperibilità, competenze fuori dal team, cultura dei gruppi che supportano il servizio |
| Informazione e tecnologia | Automazione, strumenti, controllo di versione | Conoscenza per il personale di supporto, proprietà dei dati, documentazione che altri usano |
| Partner e fornitori | Usare rapidamente servizi di terze parti e open source | Chi supporta una dipendenza, che cosa succede quando un fornitore cambia condizioni o fallisce |
| Flussi di valore e processi | Cicli brevi, lavagne visibili | Le parti del flusso fuori dal team, come approvazioni, revisioni di sicurezza e passaggio alle operations |

### Usare le dimensioni per diagnosticare

Un uso pratico è prendere un incidente o una modifica fallita e chiedere in quale dimensione stava la debolezza. Alcuni esempi mostrano l'idea, senza pretendere che siano tipici:

- Una correzione ha richiesto ore perché solo una persona capiva il sistema: organizzazioni e persone.
- Un allarme è stato ignorato perché non diceva nulla di utile: informazione e tecnologia.
- Un ripristino si è bloccato perché la linea di supporto di un fornitore era chiusa: partner e fornitori.
- Una modifica ha atteso tre giorni una firma che non serviva a nulla: flussi di valore e processi.

La maggior parte dei problemi reali tocca più di una dimensione. Il valore dell'esercizio è accorgersi di quale dimensione si trascura abitualmente.

### Limiti

Le dimensioni sono una cornice e non un metodo. Non dicono come correggere una dimensione debole e sono abbastanza ampie da poter collocare quasi qualsiasi problema in più di una. L'articolo di Wikipedia su ITIL non le descrive, e questa guida non ha trovato prove indipendenti su quanto funzionino nella pratica. Consideralo come stimoli che aiutano un team a porre domande migliori.

## Buone pratiche

1. **Rivedi ogni servizio attraverso tutte e quattro le dimensioni.** Per ogni servizio importante, scrivi due o tre righe sotto ciascuna dimensione: che cosa esiste e che cosa manca. Fallo quando progetti un servizio e di nuovo una volta l'anno.
2. **Metti le persone in cima all'elenco.** Controlla chi è reperibile, quali competenze servono e se il carico è equo. Un servizio che dipende da poche persone esauste è a rischio (vedi Argomento 1.2 — I principi agili sul ritmo sostenibile).
3. **Tratta l'informazione come parte del servizio.** Individua le informazioni di cui utenti, personale di supporto e altri team hanno bisogno e chi le possiede. Rendile facili da trovare (vedi Argomento 3.9 — Gestione della conoscenza).
4. **Conosci la tua tecnologia e mantienila supportabile.** Mantieni un elenco dei componenti principali e di chi può supportare ciascuno. Ritira ciò che nessuno capisce.
5. **Elenca i tuoi fornitori e ciò per cui dipendi da loro.** Includi fornitori cloud, fornitori di software e team interni fuori dal tuo. Registra chi chiamare, come e che cosa hanno promesso (vedi Argomento 3.14 — Gestione dei fornitori).
6. **Includi i fornitori nelle tue revisioni.** Invita i partner chiave alla pianificazione congiunta o alle revisioni degli incidenti. Un fornitore che viene a sapere tardi dei tuoi piani non può aiutare.
7. **Mappa il flusso di valore e i passaggi di consegne.** Disegna come il lavoro scorre dalla richiesta al valore, segnando dove attraversa un team o un fornitore. I passaggi di consegne sono il luogo in cui informazioni e tempo si perdono più spesso (vedi Argomento 5.4 — Gestione del flusso di valore).
8. **Guarda prima la dimensione meno sviluppata.** Quando migliori un servizio, parti dalla dimensione più debole, non da quella che il team preferisce. Mostra le prove dietro la tua scelta.
9. **Esamina i fattori esterni una o due volte l'anno.** Usa le intestazioni PESTLE per elencare ciò che potrebbe cambiare per ogni servizio: leggi, prezzi, tecnologia, atteggiamenti pubblici. Annota quale dimensione ciascuno potrebbe influenzare.
10. **Usa le dimensioni nelle revisioni di incidenti e cambiamenti.** Aggiungi una domanda al modello di revisione: quale dimensione era la più debole qui? Col tempo emergeranno schemi.
11. **Mantieni leggero.** Una pagina per servizio basta. Se la revisione richiede più di un'ora, probabilmente stai raccogliendo informazioni che nessuno userà.
12. **Non usare le dimensioni per assegnare colpe.** Lo scopo è una visione completa del servizio. Tratta una lacuna come un problema di progettazione da risolvere insieme, non come un fallimento di un team.

## Domande da discutere con il team

**Per il nostro servizio principale, che cosa scriveremmo sotto ciascuna delle quattro dimensioni, e quale è la più scarsa?**

Dividi il team in quattro gruppi, uno per dimensione, e dai loro dieci minuti. Confronta gli elenchi. Quella scarsa spesso sorprende: i team di delivery spesso trovano poco sotto partner e fornitori, mentre i team operativi possono trovare lo stesso sotto informazione. Chi facilita può chiedere che cosa è costata la dimensione scarsa negli ultimi sei mesi.

**Da chi dipendiamo che non abbiamo mai contattato?**

Elenca i fornitori e i team interni su cui il servizio fa affidamento, compresi quelli nascosti dietro un prodotto cloud. Segna per quali hai un contatto e per quali no. Chiedi che cosa succederebbe se ciascuno si guastasse. È un buon posto per trovare rischi che nessuno possiede. Scegli una dipendenza da comprendere meglio.

**Quale conoscenza esiste solo nella testa di una persona?**

Chiedi alle persone di nominare compiti che solo una persona sa svolgere e quali informazioni mancano al service desk per supportare il servizio. Tratta le risposte come un elenco di rischi. Chiedi come la conoscenza potrebbe essere condivisa entro un mese, per esempio con la coppia o scrivendo una breve guida. Registra il primo passo e il responsabile.

**Dove aspetta il lavoro fuori dal nostro team?**

Ripercorri una richiesta recente tra i team e segna ogni attesa. Le attese in approvazioni, revisioni di sicurezza o code dei fornitori sono fuori dal controllo del team ma non fuori dalla sua influenza. Chiedi chi potrebbe cambiare ciascuna attesa e quali prove aiuterebbero. Scegli un'attesa da sollevare con il responsabile.

**Che cosa è successo l'ultima volta che qualcosa fuori dal nostro controllo è cambiato, come una legge, un prezzo o una piattaforma?**

Chiedi un caso reale. Guarda quanto ci è voluto per accorgersene, chi ha deciso e quale dimensione ha subito il colpo. Lo scopo è imparare come il team osserva il cambiamento esterno. Chiedi chi ha la responsabilità di osservare e che cosa osserva.

**Se potessimo rafforzare una sola dimensione questo trimestre, quale darebbe il massimo beneficio ai nostri utenti?**

Lascia che le persone sostengano una dimensione con un esempio recente. Evita di votare all'inizio; chiedi prove. Poi concorda un'azione nella dimensione scelta con un responsabile e una misura. Ricorda di dire quali dimensioni hai scelto di non lavorare, così che la scelta sia esplicita.

## Nella pratica: un esempio di ITIL agile

Un'agenzia ambientale nazionale gestisce un portale di dati pubblici che pubblica letture della qualità dell'aria da migliaia di sensori. Lo costruisce e lo gestisce un team di nove persone. Il team rilascia modifiche ogni settimana e i suoi processi sembrano sani. Eppure, durante un'ondata di caldo, il portale rallenta fino a trascinarsi, l'interesse del pubblico esplode e l'ufficio stampa dell'agenzia scopre il problema dai social media.

La responsabile del portale usa le quattro dimensioni per rivedere l'incidente. Su organizzazioni e persone, solo due ingegneri conoscono la pipeline di acquisizione dei dati, e uno era in ferie. Su informazione e tecnologia, il monitoraggio mostrava che il database era occupato ma non quali letture erano in ritardo, quindi il team non ha saputo dire all'ufficio stampa che cosa era interessato. Su partner e fornitori, i dati dei sensori vengono da agenzie regionali e da un fornitore cloud, e nessuno aveva chiesto a nessuno dei due che cosa aspettarsi durante i picchi di domanda. Su flussi di valore e processi, l'ufficio stampa non ha una via nel processo degli incidenti, quindi il suo primo contatto è arrivato tramite un giornalista.

Il team fa quattro modifiche, una per dimensione: un terzo ingegnere viene formato sulla pipeline, il cruscotto mostra la freschezza dei dati per regione, le agenzie regionali e il fornitore cloud sono invitati a una breve revisione della capacità e l'ufficio stampa viene aggiunto alle notifiche degli incidenti. Un'ondata di caldo successiva viene gestita senza reclami del pubblico. Restano alcuni problemi: un'agenzia regionale invia ancora dati in un formato vecchio che rompe la pipeline, e l'ufficio stampa trova che i messaggi di stato tecnici sono difficili da tradurre in linguaggio semplice. Il team concorda di chiedere all'agenzia regionale un calendario per cambiare formato e di scrivere con l'ufficio stampa un breve modello di messaggio di stato.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery di solito controllano tecnologia e processo ma possono trascurare persone e fornitori. Chiedi chi supporterà ciò che costruisci, di quali competenze ha bisogno e da quali parti esterne dipende il tuo servizio. Fornisci le informazioni di cui altri hanno bisogno e invitali alle tue revisioni.

### Team di servizio e di operations

I team operativi spesso vedono per primi le debolezze nelle dimensioni perché ne vivono le conseguenze. Usa le dimensioni per descrivere i problemi in un modo su cui team di delivery e manager possano agire e per sostenere il tempo dedicato alla condivisione della conoscenza e alle relazioni con i fornitori.

### Leadership e governance

I leader controllano struttura, competenze, contratti con i fornitori e processi che attraversano i team. Chiedi una revisione a quattro dimensioni dei servizi importanti e guarda la dimensione scarsa. Sii pronto a finanziare le parti poco glamour, come formazione e relazioni con i fornitori.

### Clienti e utenti

Clienti e utenti sperimentano il risultato di tutte e quattro le dimensioni senza vederle. Quando qualcosa va storto, di' al fornitore che cosa hai visto e di che cosa avevi bisogno. Quell'informazione lo aiuta a trovare la dimensione debole. Chiedi ai fornitori come organizzano supporto, fornitori e informazioni per i servizi che usi.

## Modalità di fallimento comuni

- **Correggere la dimensione familiare.** Gli ingegneri aggiungono tecnologia a ogni problema. Chiedi invece a quale dimensione puntano le prove.
- **Dimenticare i fornitori.** Il servizio dipende da parti che nessuno ha incontrato. Elenca invece i fornitori e registra contatti, impegni e rischi.
- **Trattare le persone come un dato.** Competenze e carico di reperibilità sono presunti. Rivedili invece come parte del servizio.
- **Processi che si fermano al confine del team.** I passaggi di consegne non sono gestiti. Mappa invece il flusso tra i team e concorda i passaggi.
- **Informazioni che nessuno trova.** La documentazione esiste ma il personale di supporto non può usarla. Chiedi invece a chi usa le informazioni di che cosa ha bisogno.
- **Analisi eccessiva.** La revisione diventa un grande documento. Mantienila invece a una pagina per servizio.
- **Usare la cornice per incolpare.** I team sono giudicati per le lacune. Tratta invece le lacune come problemi di progettazione condivisi.
- **Ignorare il cambiamento esterno.** Leggi, prezzi e tecnologia cambiano senza preavviso. Esamina invece regolarmente i fattori PESTLE e annota quale dimensione ciascuno influenza.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Organizzazioni e persone | Ruoli e competenze sono informali | Alcuni team elencano competenze e carico di reperibilità | Ruoli, competenze e carico di lavoro sono descritti per ogni servizio | Competenze e carico sono misurati e rivisti | Personale e competenze sono pianificati tra team e partner |
| Informazione e tecnologia | Conoscenza e strumenti sono sparsi | Alcuni team tengono elenchi di componenti e conoscenza | Componenti e informazioni hanno responsabili e sono reperibili | L'uso di informazioni e strumenti è monitorato e le lacune sono corrette | Informazioni e strumenti sono condivisi e migliorati tra team e fornitori |
| Partner e fornitori | I fornitori sono gestiti da singoli individui | Alcuni fornitori chiave sono elencati con i contatti | Tutti i fornitori chiave hanno responsabili, contatti e aspettative | Prestazioni e rischio dei fornitori sono rivisti | I fornitori partecipano a pianificazione e miglioramento |
| Flussi di valore e processi | Il lavoro scorre per abitudine | Alcuni flussi sono disegnati | I flussi chiave sono mappati tra i team con responsabili | Flusso e attese sono misurati e ridotti | I flussi sono migliorati congiuntamente con clienti e fornitori |

## Checklist

- [ ] Per ogni servizio importante, abbiamo scritto che cosa esiste e che cosa manca in ciascuna dimensione.
- [ ] Persone e competenze necessarie per gestire ogni servizio sono individuate, con il carico di reperibilità rivisto.
- [ ] Le informazioni di cui hanno bisogno utenti e personale di supporto hanno un responsabile e sono reperibili.
- [ ] I componenti principali del servizio sono elencati, con qualcuno in grado di supportare ciascuno.
- [ ] Fornitori chiave e fornitori interni sono elencati con contatti e aspettative.
- [ ] Il flusso di lavoro di un servizio è stato mappato tra i team.
- [ ] Abbiamo esaminato i fattori esterni (PESTLE) almeno una volta nell'ultimo anno.
- [ ] Le revisioni di incidenti e cambiamenti chiedono quale dimensione era la più debole.
- [ ] La revisione di ogni servizio sta su una pagina.
- [ ] Abbiamo scelto una dimensione debole da rafforzare questo trimestre.

## Prompt per l'IA

**Scopo: redigere una revisione a quattro dimensioni di un servizio.**

```text
Help me draft a four-dimension review of the service [name]. The dimensions are: organizations and people; information and technology; partners and suppliers; value streams and processes.

About the service: [describe what it does and who uses it].
For each dimension, what I know: [write a few lines each; write "unknown" where you do not know].

For each dimension, say what exists, what appears to be missing, and one question I should ask the team, using only my text. Highlight the thinnest dimension and say why. Do not invent suppliers, people, or tools. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: classificare la dimensione più debole negli incidenti recenti.**

```text
Here are short, factual descriptions of [number] recent incidents or failed changes: [paste, one per item].

For each, say which of the four ITIL dimensions (organizations and people; information and technology; partners and suppliers; value streams and processes) the weakness most likely lay in, with one sentence of reasoning drawn only from the text. Where more than one applies, say so. Then count how many fall under each dimension, from my list only, and suggest two questions about the pattern. Do not invent causes, and list what you are unsure of.
```

**Scopo: elencare fornitori e dipendenze di un servizio.**

```text
Help me build a dependency and supplier list for [service].

What I know about how it is built and run: [describe components, cloud services, data sources, other teams].
Contracts or support arrangements I know about: [list, or write "unknown"].

Produce a table with columns: dependency, who provides it, what we rely on it for, what happens if it fails (from my text only), and the question I should ask the supplier. Mark anything you inferred. Do not invent contracts or service levels. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: esaminare i fattori esterni per un servizio.**

```text
Help me prepare a scan of external factors using the PESTLE headings (political, economic, social, technological, legal, environmental) for the service [name].

Context: [describe the sector, countries served, and users].
Known upcoming changes: [list laws, price changes, technology shifts you actually know about, or write "none known"].

For each heading, propose questions we should research (not answers), and note which of the four ITIL dimensions each factor could affect. Do not state that any law or regulation exists or applies unless I have listed it. Mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [stakeholder-analysis](../../../../skills/stakeholder-analysis/SKILL.md): da usare per mappare partner, fornitori e gruppi che dipendono da un servizio o vi contribuiscono.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): da usare per pianificare come selezioni, gestisci e rivedi i fornitori.
- [value-stream-map](../../../../skills/value-stream-map/SKILL.md): da usare per mappare il flusso di lavoro tra i team per la dimensione dei flussi di valore e dei processi.
- [swot-analysis](../../../../skills/swot-analysis/SKILL.md): da usare insieme all'esame dei fattori esterni per riassumere punti di forza, debolezze, opportunità e minacce.
- [training-needs-analysis](../../../../skills/training-needs-analysis/SKILL.md): da usare per trovare lacune di competenze nella dimensione di organizzazioni e persone.

## Fonti principali

- **ITIL 4 Foundation** (PeopleCert): la pagina del proprietario che nomina le quattro dimensioni tra gli argomenti studiati.
- **The ITIL Four Dimensions of Service Management** (itsm.tools): il riassunto di un sito di professionisti di ciascuna dimensione e di PESTLE; secondario.
- **PESTLE analysis** (Wikipedia): contesto sullo strumento dei fattori esterni.
- **ITIL** (Wikipedia): contesto su ITIL 4 e sul suo posto nella storia del framework.

## Riferimenti

1. ITIL 4 Foundation — PeopleCert — https://www.peoplecert.org/browse-certifications/it-governance-and-service-management/ITIL-1/itil-4-foundation-2565
2. The ITIL Four Dimensions of Service Management — itsm.tools (practitioner site; secondary source) — https://itsm.tools/the-itil-four-dimensions-of-service-management/
3. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
4. PESTLE analysis — Wikipedia — https://en.wikipedia.org/wiki/PEST_analysis
5. Systems thinking — Wikipedia — https://en.wikipedia.org/wiki/Systems_thinking
6. Value-stream mapping — Wikipedia — https://en.wikipedia.org/wiki/Value-stream_mapping
7. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
8. Supply chain management — Wikipedia — https://en.wikipedia.org/wiki/Supply_chain_management
