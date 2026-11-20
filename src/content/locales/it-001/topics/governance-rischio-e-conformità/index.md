# Governance, rischio e conformità

**Governance, rischio e conformità fissa la direzione, i limiti e le prove per il lavoro di un'organizzazione, e in un'organizzazione agile funziona meglio come guardrail incorporati nel modo in cui i team consegnano, non come cancelli posti alla fine.**

## Perché è importante

Ogni organizzazione che fornisce servizi risponde a qualcuno: clienti, un consiglio di amministrazione, un'autorità di vigilanza, il pubblico. Quella responsabilità assume alcune forme familiari. Devono esserci direzione e diritti decisionali chiari (governance). Deve esserci una visione onesta di che cosa potrebbe andare storto e di che cosa si sta facendo (rischio). E devono esserci prove che l'organizzazione rispetta le leggi, i contratti e le politiche che si applicano ad essa (conformità).

I team agili e le funzioni di governance si incontrano spesso in uno stato di reciproca diffidenza. I team vedono comitati di approvazione, lunghi moduli e regole di cui non vedono la ragione. Il personale di governance e di audit vede team che cambiano rapidamente la produzione e lasciano poche tracce. Entrambe le parti hanno ragione. La via d'uscita non è che una vinca, ma progettare una governance compatibile con il cambiamento frequente: limiti chiari, controlli basati sul rischio e prove prodotte dal lavoro stesso.

L'[articolo di Wikipedia su governance, gestione del rischio e conformità](https://en.wikipedia.org/wiki/Governance,_risk_management,_and_compliance) descrive il GRC come un approccio olistico a governance, gestione del rischio e conformità normativa, sviluppato negli anni Duemila per gestire requisiti di conformità finanziaria sempre più complessi. Non nomina critiche né framework specifici per l'IT. Questo argomento lo combina con gli articoli sulla gestione del rischio e sulla conformità normativa, con i precedenti argomenti su cambiamenti, sicurezza e continuità e con le indicazioni di DORA sull'approvazione. Non dà consulenza legale; le regole che si applicano a te dipendono da paese, settore e contratti, e la fonte giusta è il testo della regola.

## Concetti fondamentali

### Governance

L'articolo sul GRC descrive la corporate governance come i processi fissati dal consiglio di amministrazione che plasmano la struttura e assegnano i ruoli. Nell'IT, la governance riguarda chi decide che cosa, su quale base e come le decisioni sono verificate. COBIT, descritto da Wikipedia come un framework di ISACA per la gestione e la governance dell'IT, è un riferimento (vedi Argomento 2.7 — Framework e standard ITSM). Il sistema di valore del servizio di ITIL include la governance come componente (vedi Argomento 2.3 — Il sistema di valore del servizio ITIL).

Una buona governance in un'organizzazione agile è esplicita su:

- **Direzione:** obiettivi e priorità e chi li fissa.
- **Limiti:** che cosa i team possono decidere da soli e che cosa richiede escalation (vedi Argomento 1.9 — Gestione agile).
- **Responsabilità:** chi risponde di ogni servizio (vedi Argomento 5.5 — Responsabilità di prodotto e di servizio).
- **Prove:** come l'organizzazione sa che direzione e limiti sono rispettati.

### Gestione del rischio

Wikipedia descrive la gestione del rischio come l'individuazione, la valutazione e la prioritizzazione dei rischi, seguite dal minimizzare, monitorare e controllare il loro impatto o probabilità. L'articolo nomina quattro opzioni di trattamento:

| Opzione | Significato | Esempio |
|---|---|---|
| **Evitare** | Non svolgere l'attività rischiosa (il che rinuncia anche ai potenziali guadagni) | Decidere di non conservare certi dati |
| **Ridurre** | Abbassare la gravità o la probabilità | Test automatici, rollout a stadi, monitoraggio extra |
| **Condividere** | Trasferire l'onere o il beneficio, per esempio tramite assicurazione o esternalizzazione; l'articolo nota che "trasferimento del rischio" è spesso un termine improprio, perché la parte originale di solito conserva la responsabilità legale | Assicurazione, affidare a un fornitore |
| **Trattenere** | Accettare la perdita, tipicamente per rischi piccoli o non assicurabili | Una decisione di convivere con un rischio minore |

L'articolo tratta anche le opportunità, eventi incerti positivi, con strategie parallele. Nota che la valutazione del rischio pesa gravità e probabilità e che i dati sui tassi sono spesso scarsi, soprattutto per gli eventi catastrofici. Cita critiche: Douglas Hubbard (2009) è citato come dicente che alcuni standard non mostrano un miglioramento misurabile del rischio, anche se la fiducia nelle decisioni sembra aumentare; ricerche successive suggeriscono che i benefici finanziari dipendono più da quanto spesso e con quale metodo i rischi sono valutati che dalla formula usata; e la distinzione di Benoit Mandelbrot tra rischio "mite" e "selvaggio", con la sottovalutazione della selvaggità come errore comune. L'articolo cita ISO 31000, "Risk management — Guidelines", ed è esso stesso segnalato come bisognoso di più citazioni.

### Il registro dei rischi

Un **registro dei rischi** è un record dei rischi individuati, con una descrizione, una valutazione, un responsabile, il trattamento scelto e lo stato. L'estratto dell'articolo letto per questa guida non lo menziona, quindi è pratica comune. Mantienilo breve, con responsabili e rivisto. I rischi per i servizi includono sicurezza, disponibilità, fallimento di fornitori, dipendenza da persone chiave e conformità (vedi Argomento 3.13 — Gestione della sicurezza delle informazioni, Argomento 3.12 — Gestione della continuità del servizio e Argomento 3.14 — Gestione dei fornitori).

### Conformità

L'articolo di Wikipedia sulla conformità normativa la descrive come l'obiettivo che le organizzazioni aspirano a raggiungere nel restare consapevoli e rispettare leggi, politiche e regolamenti rilevanti e nota che le organizzazioni combinano sempre più i controlli in framework condivisi per ridurre il lavoro duplicato. Dice che la definizione di un piano di conformità efficace è stata sfuggente e menziona standard come ISO 37301 e ISO 19600. Nomina regimi tra cui il Sarbanes–Oxley Act (2002), HIPAA, GDPR, PCI-DSS, il Gramm–Leach–Bliley Act e altri. Registra critiche: la ricerca psicologica citata nell'articolo sostiene che ricompense o multe possono indebolire la motivazione intrinseca e minare la conformità, i difensori della privacy mettono in dubbio i requisiti di conservazione dei dati, l'applicazione differisce tra giurisdizioni e i requisiti in rapido cambiamento sono difficili da seguire.

Un punto pratico: la conformità non è una cosa sola. Ogni regime ha il proprio ambito e i propri requisiti. Scopri dalla tua funzione legale o di conformità quali si applicano a quali dei tuoi servizi e ottieni il testo.

### GRC come un'unica visione

L'articolo sul GRC dice che il GRC copre tre sfaccettature correlate: corporate governance, gestione del rischio aziendale e conformità, e menziona varianti come GRC finanziario, legale e operativo. Attribuisce il termine all'articolo di Scott Mitchell del 2007 e all'Open Compliance and Ethics Group e nota che il software per il GRC esiste dal 2002 e che alcune aziende hanno iniziato a usare strumenti di IA per il GRC nel 2025. Il vantaggio della visione combinata è che i tre sono collegati: la governance fissa che cosa conta, la gestione del rischio trova ciò che lo minaccia e la conformità mostra che cosa si sta facendo.

### Guardrail, non cancelli

Un **cancello** (gate) è un punto di controllo, di solito manuale, in cui il lavoro aspetta l'approvazione. Un **guardrail** è un limite incorporato nel percorso che impedisce al lavoro di uscire di strada senza fermarlo. Esempi: test automatici che devono passare, controlli di policy nella pipeline che bloccano configurazioni non sicure, budget con allarmi e accesso basato sui ruoli. Le indicazioni di DORA sull'approvazione dei cambiamenti dicono che l'approvazione si ottiene al meglio con la revisione tra pari e l'automazione, che l'approvazione esterna pesante è associata a prestazioni di consegna peggiori e che aggiungere approvazioni in risposta all'instabilità tende a peggiorare le cose (vedi Argomento 3.4 — Abilitazione dei cambiamenti). I guardrail applicano la stessa idea alla governance: il controllo sta nel sistema e produce le proprie prove.

### Prove come sottoprodotto

Gli auditor hanno bisogno di prove che i controlli funzionino. Una pipeline che registra chi ha rivisto, che cosa ha testato e che cosa è stato installato dà prove per ogni modifica. Un catalogo dei servizi con responsabili dà prove di responsabilità. I post-mortem danno prove di apprendimento. È molto più forte di un documento trimestrale scritto per un audit. Discuti presto con gli auditor che cosa accetteranno (vedi Argomento 5.1 — Gestione agile dei servizi).

### Ambienti regolamentati

L'articolo di Wikipedia sullo sviluppo software agile riferisce che ambiti regolamentati come dispositivi medici, farmaceutica, finanza, nucleare, automotive e avionica furono dapprima ritenuti inadatti all'agile e che oggi esistono adattamenti, con preoccupazioni per assicurazione della qualità, sicurezza (safety e security), tracciabilità, verifica e validazione (vedi Argomento 1.3 — Sviluppo software agile). Lo schema che funziona è tipicamente mantenere i controlli richiesti, automatizzarne le prove e farli parte della definition of done, anziché rimuoverli.

### Limiti delle fonti

L'articolo sul GRC non nomina framework né critiche ed è stato letto per questa guida in forma breve. L'articolo sulla gestione del rischio è stato letto solo in parte ed è segnalato come bisognoso di citazioni. L'articolo sulla conformità non dà costi né procedure di audit. Usali come mappe e rivolgiti alle fonti primarie per i dettagli.

## Buone pratiche

1. **Scrivi i diritti decisionali.** Per ogni team o servizio, indica che cosa può decidere da solo, che cosa richiede consultazione e che cosa richiede approvazione. Pubblicali e rivedili con i team.
2. **Fissa direzione e limiti, non istruzioni dettagliate.** Indica risultati, budget, limiti di rischio e regole non negoziabili. Lascia che i team decidano come lavorare al loro interno.
3. **Tieni un breve registro dei rischi.** Per ogni servizio importante, elenca i rischi principali con un responsabile, un trattamento e una data di revisione. Rivedilo in una riunione regolare e abbandona i rischi che sono passati.
4. **Scegli il trattamento di proposito.** Per ogni rischio, decidi di evitarlo, ridurlo, condividerlo o trattenerlo e registra chi ha preso la decisione. Ricorda che condividere un rischio non rimuove la tua responsabilità.
5. **Valuta spesso, con metodi semplici.** L'articolo riferisce che i benefici dipendono più da frequenza e metodo che dalla formula. Rivedi regolarmente i rischi con un metodo che il team capisce.
6. **Sappi quali regole si applicano a quali servizi.** Chiedi alla tua funzione legale o di conformità un elenco dei regimi che si applicano, con il testo delle fonti. Registralo per ogni servizio.
7. **Incorpora guardrail nella pipeline.** Automatizza test, scansioni di sicurezza, controlli di policy e limiti di accesso così che il lavoro non sicuro sia fermato presto. Tratta i controlli come codice con responsabili.
8. **Cattura le prove come sottoprodotto.** Assicurati che gli strumenti registrino revisioni, approvazioni, risultati dei test, deployment e incidenti. Concorda con gli auditor che cosa accetteranno.
9. **Mappa i controlli una volta.** Se devi soddisfare più framework, descrivi i controlli una volta e mappali su ciascun requisito, come dice l'articolo sulla conformità che le organizzazioni fanno sempre più.
10. **Usa vie basate sul rischio per i cambiamenti.** Rendi rapide le modifiche a basso rischio, segnala quelle ad alto rischio per la revisione e mantieni un organismo centrale per coordinamento e compromessi (vedi Argomento 3.4 — Abilitazione dei cambiamenti).
11. **Includi la governance nelle retrospettive.** Chiedi periodicamente quali controlli hanno aiutato e quali hanno solo aggiunto ritardo. Rimuovi o riprogetta i secondi, con il responsabile e l'auditor.
12. **Pianifica il cambiamento delle regole.** Nomina qualcuno che segua i cambiamenti di leggi, standard e contratti e riferisca ciò che conta per i tuoi servizi.

## Domande da discutere con il team

**Quali approvazioni dobbiamo ottenere, e da che cosa protegge ciascuna?**

Elenca le approvazioni su una modifica o un acquisto tipici. Per ciascuna, chiedi quale rischio affronta e se ha mai rifiutato qualcosa. Le approvazioni che non proteggono nulla sono candidate alla rimozione. Quelle che proteggono da un rischio reale possono essere soddisfatte in modo più leggero. Chi facilita può chiedere quali prove l'approvatore accetterebbe al posto di una firma.

**Quali sono i primi cinque rischi per il nostro servizio principale, e chi possiede ciascuno?**

Chiedi alle persone di elencare i rischi indipendentemente, poi confronta. Le differenze mostrano che cosa vede il team. Verifica che ciascuno abbia un responsabile e un trattamento. Discuti quali sono accettati per impostazione predefinita, non per decisione.

**Quali regole si applicano a noi, e dov'è il testo?**

Chiedi l'elenco di leggi, standard e contratti che si applicano. Se nessuno sa dirlo, scopri chi può. Verifica che l'ingegneria sappia che cosa ciascuno le richiede. Concorda un modo di mantenere aggiornato l'elenco.

**Quali prove producono già i nostri strumenti che un auditor potrebbe usare?**

Elenca i record: revisioni, risultati dei test, cronologia dei deployment, revisioni degli incidenti. Chiedi che cosa un auditor ha chiesto di recente e se gli strumenti potrebbero fornirlo. Individua un record da automatizzare. Invita un auditor a guardare.

**Dove abbiamo aggiunto un controllo dopo un problema, e ha aiutato?**

Chiedi esempi. Confronta con l'avvertimento DORA che aggiungere approvazioni in risposta all'instabilità tende a peggiorare le cose. Chiedi se una risposta diversa, come test migliori o modifiche più piccole, avrebbe funzionato. Registra una lezione.

**Che aspetto avrebbe un guardrail per qualcosa che ora regoliamo con un cancello?**

Scegli un cancello. Chiedi che cosa il cancello deve impedire e come ciò potrebbe essere impedito automaticamente. Per esempio, un controllo di policy che blocca una configurazione rischiosa. Concorda una sperimentazione con il responsabile del cancello.

## Nella pratica: un esempio di ITIL agile

Un fondo pensione nazionale gestisce un calcolatore online di prestazioni e un servizio di pagamenti. È regolamentato, sottoposto ad audit ogni anno e soggetto a regole rigorose sulla gestione dei dati. L'ufficio di governance del fondo richiede che ogni modifica in produzione sia rivista da un comitato dei cambiamenti che si riunisce ogni settimana e che ogni progetto completi una valutazione dei rischi di 30 pagine prima del rilascio. Gli sviluppatori rilasciano di rado e in grandi lotti. Un recente rilascio ha causato un calcolo errato per un piccolo gruppo di iscritti e la risposta del comitato è stata aggiungere un'altra approvazione.

La responsabile del rischio e il responsabile dell'ingegneria decidono di provare un'altra via. Partono da un elenco dei regimi che si applicano al calcolatore e al servizio di pagamenti, ottenuto dall'ufficio legale del fondo con il testo di ciascuno, e mappano una volta i controlli del fondo su di essi. Il ruolo del comitato dei cambiamenti cambia: le modifiche di routine e ben testate con test automatici e revisione tra pari procedono senza di esso, le modifiche ad alto rischio (quelle che toccano le regole di calcolo o i pagamenti) sono segnalate da un breve elenco di segnali e riviste da uno specialista del rischio entro due giorni e il comitato si riunisce per coordinare e gestire le eccezioni. La pipeline registra chi ha rivisto e quali test sono passati e un controllo di policy blocca i rilasci che falliscono la suite di test sui calcoli. La valutazione dei rischi è sostituita da una voce di registro di una pagina per servizio, rivista ogni mese.

Un auditor interno vede i record della pipeline e il registro e chiede un campione di revisioni per verificare se la revisione tra pari è genuina; il responsabile dell'ingegneria organizza un campionamento trimestrale da parte di un ingegnere senior. Dopo sei mesi, i rilasci sono settimanali, il change fail rate è più basso e l'audit trova sufficienti le prove. Restano alcune difficoltà. Due team applicano in modo incoerente i segnali ad alto rischio, le indicazioni di un'autorità di vigilanza richiedono una firma esplicita per certe modifiche ai calcoli che la nuova via non cattura e le voci del registro sono scritte con poca cura in alcuni team. La responsabile del rischio aggiunge il passaggio di firma per quelle modifiche, emette esempi dei segnali e chiede ai team di portare una voce di registro a una revisione mensile.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery eseguono i controlli attraverso le proprie pipeline e pratiche. Scopri quali regole si applicano al tuo servizio e perché, offri modi di produrre le prove automaticamente e porta il rischio nella pianificazione. Tratta i guardrail come parte del prodotto.

### Team di servizio e di operations

I team operativi possiedono molti controlli: accessi, monitoraggio, continuità e record. Tieni le prove negli strumenti, di' alla governance che cosa funziona nella pratica e aiuta a riprogettare i cancelli che aggiungono solo ritardo. Partecipa alle revisioni dei rischi con dati reali sugli incidenti.

### Leadership e governance

I leader fissano direzione, limiti e responsabilità e decidono quali rischi accettare. Chiedi visioni del rischio in linguaggio semplice e prove, non volume di documenti. Sii disposto a sostituire un cancello con un guardrail quando lo scopo può essere raggiunto. Mantieni il ruolo del comitato concentrato su coordinamento e reali compromessi.

### Clienti e utenti

Clienti e utenti si affidano all'organizzazione perché tratti correttamente dati e denaro. Chiedi ai fornitori quali standard e regole seguono e come lo dimostrano. Aspettati onestà dopo un guasto. Se hai requisiti speciali, come la regola di un'autorità di vigilanza, dillo presto al fornitore.

## Modalità di fallimento comuni

- **Governance come cancello finale.** Le revisioni arrivano alla fine e rallentano tutto. Incorpora invece guardrail nel lavoro e rivedi per rischio.
- **Documenti come prove.** I rapporti sono scritti per l'auditor. Produci invece le prove dagli strumenti usati nel lavoro.
- **Una sola via per ogni modifica.** Le modifiche di routine aspettano con quelle rischiose. Classifica invece per rischio.
- **Un registro dei rischi che nessuno legge.** Diventa un lungo elenco. Mantienilo invece breve, con responsabili e rivisto.
- **Trattare il trasferimento del rischio come rimozione del rischio.** Si presume che assicurazione o esternalizzazione chiudano la responsabilità. Ricorda invece che la parte originale di solito conserva la responsabilità.
- **Regole sconosciute.** I team non sanno quali leggi e standard si applicano. Ottieni invece l'elenco e il testo da legale o conformità.
- **Controllo aggiunto dopo ogni incidente.** Il processo cresce e la velocità cala. Cerca invece la causa e correggila con test, modifiche più piccole o ripristino più rapido.
- **Conformità come punizione.** Dominano multe e paura. Spiega invece lo scopo delle regole e fai in modo che la via sicura sia quella facile.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Governance e diritti decisionali | Le decisioni seguono abitudine e gerarchia | Alcuni team hanno limiti scritti | Diritti decisionali, limiti e responsabili sono scritti e condivisi | L'efficacia della governance è rivista rispetto ai risultati | La governance è allineata tra team, fornitori e partner |
| Gestione del rischio | I rischi sono discussi in modo informale | Alcuni servizi hanno elenchi di rischi | Brevi registri dei rischi con responsabili e trattamenti sono rivisti regolarmente | Misure ed eventi di rischio informano valutazione e trattamento | Le visioni del rischio sono condivise e consolidate in tutta l'organizzazione |
| Conformità e prove | Le prove sono messe insieme per gli audit | Alcune prove sono prodotte dagli strumenti | Le regole applicabili sono elencate; i controlli sono mappati una volta; le prove vengono dagli strumenti | Funzionamento dei controlli e qualità delle prove sono misurati | Le prove sono condivise con auditor e partner in modo continuo |
| Guardrail e vie di cambiamento | I controlli sono cancelli manuali | Esistono alcuni controlli automatici | Vie basate sul rischio e guardrail di pipeline sono standard | Efficacia dei guardrail e falsi blocchi sono monitorati e regolati | I guardrail sono condivisi e migliorati tra i team |

## Checklist

- [ ] Diritti decisionali e limiti sono scritti per ogni team o servizio.
- [ ] Ogni servizio importante ha un breve registro dei rischi con responsabili, trattamenti e date di revisione.
- [ ] Abbiamo un elenco di leggi, standard e contratti che si applicano a ogni servizio, con il testo delle fonti.
- [ ] I nostri controlli sono descritti una volta e mappati su ciascun requisito.
- [ ] La pipeline registra revisioni, test e deployment come prove.
- [ ] Gli auditor hanno detto quali prove accettano al posto delle firme.
- [ ] Modifiche di routine e rischiose seguono vie diverse con criteri chiari.
- [ ] Ogni approvazione ha uno scopo dichiarato e le approvazioni che non rifiutano mai sono riviste.
- [ ] I controlli aggiunti dopo gli incidenti sono rivisti per il loro effetto.
- [ ] Qualcuno segue i cambiamenti delle regole applicabili e li riferisce.

## Prompt per l'IA

**Scopo: trasformare una catena di approvazione in opzioni di guardrail.**

```text
Here is an approval chain we use for [type of change or purchase]: [list each approval, who gives it, what they check, how long it takes, and how many times it has refused something in the last year (use real figures or write "unknown")].
Rules we know require some of it, with source text: [paste, or write "none known"].

For each approval, state the purpose as best you can from the text, suggest what evidence or automated check could meet the same purpose, and say what risk would remain. Do not remove anything required by the pasted rules. Do not claim any law or standard requires something unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: redigere una voce del registro dei rischi.**

```text
Help me write a risk register entry for [service].

The risk, in my words: [describe].
What could cause it and what could result: [describe].
What controls exist: [list].
What I know about likelihood and impact (facts only): [paste, or write "unknown"].

Produce an entry with: a clear statement ("If … then … resulting in …"), causes, consequences, existing controls, a proposed treatment option (avoid, reduce, share, or retain) with reasoning, a suggested owner role, and review date placeholder. Do not invent likelihoods or numbers. Mark assumptions. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: elencare le prove che i tuoi strumenti già producono per un controllo.**

```text
An auditor will ask us about this control: [describe the control and how it is described in the requirement; paste the text].

Our tools and records for the activity: [list version control, pipeline, ticketing, monitoring, and what each records].
How the activity works: [describe].

Make a table of what evidence each tool produces for the control, where it is stored, who can alter it, and the gaps. Suggest three lightweight ways to close the gaps. Do not claim the requirement demands anything beyond the pasted text. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: preparare una conversazione di governance tra team di delivery e audit.**

```text
Plan a 60-minute conversation between [number] delivery team members and [number] audit or governance colleagues about how an agile team shows control.

Concerns from audit, in their words: [paste].
Concerns from teams, in their words: [paste].
Evidence the teams produce today: [list].

Provide a timed agenda, questions for each side, a template to record what evidence is acceptable for each control, and a closing step that records actions with owners and dates. Keep it free of any particular tool. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [risk-register](../../../../skills/risk-register/SKILL.md): da usare per registrare e rivedere rischi, trattamenti e responsabili.
- [risks-actions-issues-decisions](../../../../skills/risks-actions-issues-decisions/SKILL.md): da usare per tenere un registro leggero di rischi, azioni, questioni e decisioni.
- [key-risk-indicators](../../../../skills/key-risk-indicators/SKILL.md): da usare per scegliere misure di allerta precoce per i rischi.
- [legal-compliance-audit](../../../../skills/legal-compliance-audit/SKILL.md): da usare per prepararsi agli audit e organizzare le prove.
- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): da usare per rendere espliciti diritti decisionali e responsabilità.

## Fonti principali

- **Governance, risk management, and compliance** (Wikipedia): una breve panoramica del GRC, dei suoi componenti e della sua storia.
- **Risk management** (Wikipedia): la definizione, le opzioni di trattamento e le avvertenze sulla valutazione del rischio.
- **Regulatory compliance** (Wikipedia): la definizione, i regimi nominati e le critiche.
- **Streamlining change approval** (DORA, dora.dev): indicazioni basate sulla ricerca per sostituire l'approvazione pesante con revisione tra pari e automazione.

## Riferimenti

1. Governance, risk management, and compliance — Wikipedia — https://en.wikipedia.org/wiki/Governance,_risk_management,_and_compliance
2. Risk management — Wikipedia — https://en.wikipedia.org/wiki/Risk_management
3. Regulatory compliance — Wikipedia — https://en.wikipedia.org/wiki/Regulatory_compliance
4. Streamlining change approval — DORA, dora.dev — https://dora.dev/capabilities/streamlining-change-approval/
5. COBIT — Wikipedia — https://en.wikipedia.org/wiki/COBIT
6. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
7. ISO 31000 — Wikipedia — https://en.wikipedia.org/wiki/ISO_31000
8. Sarbanes–Oxley Act — Wikipedia — https://en.wikipedia.org/wiki/Sarbanes%E2%80%93Oxley_Act
9. Internal control — Wikipedia — https://en.wikipedia.org/wiki/Internal_control
