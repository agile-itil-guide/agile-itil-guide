# Gestione degli incidenti

**La gestione degli incidenti ripristina un servizio degradato il più in fretta possibile in sicurezza, e l'abitudine agile che la fa funzionare è avere ruoli chiari sotto pressione seguiti da una revisione senza attribuzione di colpe che trasforma ogni incidente in un cambiamento.**

## Perché è importante

Gli incidenti sono il momento in cui un servizio viene giudicato. Gli utenti non ricordano i mesi di buona disponibilità; ricordano l'interruzione e come è stata gestita. Un team che ha stabilito in anticipo chi fa che cosa, come comunica e quando chiede aiuto ripristina il servizio più in fretta e fa meno errori di uno che improvvisa.

I team agili che gestiscono ciò che costruiscono spesso gestiscono gli incidenti in modo informale. Funziona finché un incidente non è grande, non coinvolge più team o non avviene di notte. Allora la mancanza di ruoli e record si vede: gli ingegneri si accalcano sul problema tecnico, nessuno informa i clienti e due persone fanno modifiche in conflitto. La pratica ITSM della gestione degli incidenti, insieme alle pratiche della site reliability engineering, offre modi collaudati per prevenirlo.

L'[articolo di Wikipedia sulla gestione degli incidenti](https://en.wikipedia.org/wiki/Incident_management) copre diversi campi, dalla risposta alle emergenze alla sicurezza informatica. Per la gestione dei servizi IT dice che l'obiettivo è ripristinare il servizio normale entro il livello di servizio concordato il più rapidamente possibile, cita ITIL 2011 nel definire un incidente come un'interruzione non pianificata di un servizio IT o una riduzione della sua qualità ed elenca tre difficoltà: rumore degli allarmi, risoluzione lunga dei problemi e difficoltà a prevedere le interruzioni. Per i dettagli, questo argomento si basa molto su due capitoli del libro *Site Reliability Engineering* di Google, che descrivono un approccio di comando degli incidenti e post-mortem senza attribuzione di colpe tratti dalla pratica di una grande organizzazione. Considera quei capitoli come un approccio ben documentato, non l'unico.

## Concetti fondamentali

### Che cos'è un incidente

Un **incidente**, nell'uso ITSM, è un'interruzione non pianificata di un servizio o una riduzione della sua qualità. L'articolo sull'ITSM include anche un'interruzione "potenziale". Un incidente non è la stessa cosa di un **problema**, che è la causa di fondo, o di una **richiesta di servizio**, che è una domanda di routine (vedi Argomento 3.3 — Gestione dei problemi e Argomento 3.6 — Gestione delle richieste di servizio). Tenere separati i tre è importante perché ciascuno è gestito per un obiettivo diverso: ripristinare il servizio, rimuovere le cause ed evadere la domanda di routine.

### L'obiettivo: ripristinare il servizio, preservare le prove

Il primo scopo della gestione degli incidenti è ripristinare il servizio. Il capitolo SRE sulla gestione degli incidenti ne aggiunge un secondo: preservare le prove necessarie per trovare in seguito la causa radice. Le buone pratiche del capitolo stesso dicono di dare priorità al ripristino del servizio e alla conservazione delle prove, in questo spirito. Correggere la causa può venire dopo, nella gestione dei problemi.

### Perché gli incidenti non gestiti vanno male

Il capitolo SRE, scritto da Andrew Stribblehill, usa un esempio esteso di un ingegnere di turno la cui interruzione cresce fino a diventare un guasto totale. Nomina tre pericoli degli incidenti non gestiti:

- **Una messa a fuoco ristretta sul problema tecnico.** Gli ingegneri assorbiti da una correzione perdono di vista la mitigazione e il quadro più ampio.
- **Comunicazione scadente.** Nessuno sa che cosa fanno gli altri e gli stakeholder restano non informati.
- **Freelancing.** Modifiche non coordinate, come un deployment dell'ultimo minuto, peggiorano la situazione.

### Ruoli sotto pressione

Il capitolo basa il suo approccio sull'Incident Command System, nato dalla risposta alle emergenze (anche l'articolo di Wikipedia sulla gestione degli incidenti lo menziona). Le sue idee principali:

| Ruolo | Che cosa fa |
|---|---|
| **Incident commander** | Tiene lo stato di alto livello, struttura la risposta, rimuove gli ostacoli e ricopre ogni ruolo non ancora delegato |
| **Operations lead** | Applica gli strumenti al problema; solo il team operativo modifica il sistema durante un incidente |
| **Communications lead** | È il volto pubblico della risposta; emette aggiornamenti periodici e mantiene aggiornato il documento dell'incidente |
| **Planning lead** | Gestisce le questioni di più lungo periodo come aprire bug, organizzare passaggi di consegne e tracciare lo scostamento dalla normalità così che le modifiche possano essere annullate |

Il capitolo chiama il principio una separazione ricorsiva delle responsabilità. Ruoli chiari danno autonomia alle persone, perché non devono mettere in dubbio i colleghi, e una persona sovraccarica chiede più personale e delega parti del lavoro. I passaggi di consegne tra commander sono espliciti e riconosciuti.

### Il documento vivo dell'incidente

Il capitolo dice che il compito più importante del commander è mantenere un documento vivo dello stato dell'incidente, idealmente modificabile da più persone contemporaneamente. Può essere disordinato ma deve restare utile, con le informazioni chiave in alto, e viene conservato per l'analisi successiva. Un canale condiviso o una stanza fisica funge da posto di comando.

### Quando dichiarare un incidente

Il capitolo raccomanda di dichiarare un incidente presto, non ore dopo l'aggravarsi di un problema. Suggerisce di trattare un evento come incidente se per correggerlo deve essere coinvolto un secondo team, se l'interruzione è visibile ai clienti o se resta irrisolto dopo un'ora di analisi concentrata. Sono regole empiriche di un'organizzazione. Le tue soglie dovrebbero riflettere i tuoi servizi e i tuoi utenti.

### Priorità e gravità

Le fonti lette per questa guida non definiscono livelli di priorità o gravità, e l'articolo di Wikipedia non ne indica. Nella pratica i team definiscono i livelli in base all'impatto sugli utenti e all'urgenza del bisogno e decidono in anticipo chi viene chiamato a ciascun livello. Mantieni lo schema breve, con esempi, e verificalo applicandolo a incidenti passati.

### Comunicazione

La comunicazione ha due pubblici. Chi risponde deve conoscere lo stato e chi fa che cosa. Stakeholder e utenti devono sapere che cosa è interessato, che cosa si sta facendo e quando aspettarsi il prossimo aggiornamento. Il communications lead nel capitolo SRE serve il secondo pubblico e tiene il registro per il primo. Per le interruzioni rivolte al pubblico è utile un piano di comunicazione in una crisi (vedi la competenza sulla comunicazione di crisi più avanti).

### Post-mortem senza attribuzione di colpe

Il capitolo SRE sulla cultura dei post-mortem espone la metà dedicata all'apprendimento. Un post-mortem registra l'incidente, il suo impatto, la mitigazione, le cause radice e le azioni successive. I suoi obiettivi sono documentare l'incidente, comprendere tutte le cause radice concorrenti e mettere in atto azioni preventive efficaci. È senza attribuzione di colpe: individua le cause concorrenti senza incolpare individui o team e presume che tutti "had good intentions and did the right thing with the information they had". Nelle parole del capitolo, "You can't 'fix' people, but you can fix systems and processes."

Il capitolo suggerisce di definire in anticipo i trigger dei post-mortem, come un'indisponibilità visibile agli utenti oltre una soglia, qualsiasi perdita di dati, un intervento del turno come un rollback, un tempo di risoluzione sopra una soglia o un guasto del monitoraggio. Dice anche "An unreviewed postmortem might as well never have existed" e quindi raccomanda sessioni di revisione regolari e un archivio condiviso. Descrive attività di costruzione della cultura come una newsletter mensile, club di lettura e una "Wheel of Misfortune" in cui si rievocano incidenti passati.

### Incidenti maggiori

Molte pratiche ITSM definiscono un **incidente maggiore** come uno che richiede una risposta più formale del solito. Le fonti lette qui non lo definiscono, quindi fallo con parole tue: per esempio, un incidente che colpisce molti utenti o un servizio critico e richiede una risposta coordinata tra i team. Ciò che conta è che le persone sappiano in anticipo che cosa cambia: chi comanda, chi viene chiamato, con quale frequenza escono gli aggiornamenti.

### Incidenti e consegna continua

Gli incidenti nascono spesso da modifiche recenti. I team agili sono ben posizionati per imparare da essi perché rilasciano spesso e hanno cicli di feedback brevi. L'apprendimento ha bisogno di una via: le azioni dei post-mortem vanno nel backlog con responsabili e date, e gli incidenti ricorrenti vanno alla gestione dei problemi. Senza quella via, la gestione degli incidenti diventa una routine di riparazioni.

## Buone pratiche

1. **Decidi in anticipo che cosa conta come incidente.** Scrivi una breve definizione con esempi e abbassa la soglia per dichiararne uno. La regola empirica del capitolo SRE è dichiarare presto quando serve un secondo team, i clienti possono vedere il problema o un'ora di analisi non l'ha risolto.
2. **Definisci pochi livelli di gravità con esempi.** Basali sull'impatto sugli utenti e indica chi viene chiamato a ciascun livello. Verifica lo schema su incidenti passati e correggilo.
3. **Assegna i ruoli all'inizio di ogni incidente.** Nomina un incident commander, un operations lead e un communications lead. Nei piccoli team una persona può avere più di un ruolo; dillo ad alta voce.
4. **Separa il correggere dal coordinare.** Le persone che modificano il sistema non dovrebbero anche rispondere alle domande. Lascia che il commander coordini e il communications lead informi.
5. **Tieni un registro vivo.** Usa un unico documento o canale condiviso con orari, decisioni e modifiche fatte. Sostiene i passaggi di consegne e dà al post-mortem il suo materiale.
6. **Consenti solo modifiche autorizzate.** Il capitolo SRE dice che solo il team operativo dovrebbe modificare il sistema durante un incidente. Indica chi può cambiare che cosa e chiedi agli altri di parlare con il commander.
7. **Comunica a scadenze fisse.** Concorda l'intervallo di aggiornamento per ogni gravità e rispettalo, anche quando non c'è nulla di nuovo. Il silenzio genera preoccupazione e domande duplicate.
8. **Passa le consegne in modo esplicito.** Quando un commander o un addetto viene sostituito, dillo ad alta voce e fai riconoscere il passaggio dall'altra persona. Passaggi poco chiari perdono contesto.
9. **Esercitati.** Esegui il processo degli incidenti su piccoli eventi e in esercitazioni, così che i ruoli siano familiari prima di un'interruzione grave. Fai ruotare le persone tra i ruoli.
10. **Tieni un post-mortem senza colpe quando i tuoi trigger sono soddisfatti.** Scrivilo con chi è stato coinvolto, concentrati sulle cause concorrenti e sulle correzioni del sistema e condividilo ampiamente (vedi la competenza sul post-mortem più avanti).
11. **Trasforma le azioni in elementi del backlog.** Dai a ogni azione successiva un responsabile e una data e rivedile in una riunione regolare. Un post-mortem non rivisto non produce alcun cambiamento.
12. **Passa le prove alla gestione dei problemi.** Collega gli incidenti ripetuti a un record di problema, così che le cause siano rimosse e non solo riparate (vedi Argomento 3.3 — Gestione dei problemi).

## Domande da discutere con il team

**Che cosa facciamo nei primi dieci minuti di un incidente, e chi decide?**

Ripercorri l'ultimo incidente significativo minuto per minuto. Annota chi ha preso la guida, chi ha comunicato e chi ha cambiato che cosa. Molti team scoprono che i ruoli erano presunti e non concordati. Chi facilita può chiedere che cosa sarebbe successo se il solito responsabile fosse stato assente. Prosegui concordando come saranno assegnati i ruoli la prossima volta.

**Quando chiamiamo qualcosa un incidente, e quando aspettiamo?**

Raccogli esempi di eventi dichiarati in ritardo. Chiedi che cosa ha trattenuto le persone: non voler disturbare gli altri, incertezza o paura di essere incolpati. Confronta con i trigger del capitolo SRE. Concorda una soglia e un modo di dichiarare un incidente senza fare storie.

**Come scoprono i nostri utenti che cosa sta succedendo durante un'interruzione, e con quale frequenza?**

Guarda l'ultima interruzione dal lato dell'utente. Chiedi chi li ha informati, che cosa è stato detto e quanto è durato il vuoto. Spesso la risposta è un lungo silenzio seguito da una breve nota. Chiedi chi dovrebbe possedere la comunicazione e che cosa dovrebbe dire il primo messaggio. Concorda un modello e un ritmo di aggiornamento.

**Che cosa ha cambiato il nostro ultimo post-mortem, e come lo sappiamo?**

Chiedi le azioni, i responsabili e lo stato. Se nessuna è stata completata, chiedi perché: nessun responsabile, nessun tempo o valore poco chiaro. Scopri se i post-mortem sono letti da qualcuno oltre al team. Concorda una sessione regolare per rivedere le azioni aperte.

**Le persone si sentono al sicuro nel dire che cosa hanno sbagliato?**

Questa domanda mette alla prova l'assenza di colpe. Chiedi alle persone di descrivere come si sentirebbero a scrivere del proprio errore in un post-mortem. Ascolta la paura delle conseguenze e gli esempi di quando c'è stata attribuzione di colpe. Non pretendere apertura; chiedi che cosa team e leader dovrebbero fare per renderla sicura. Scegli un passo visibile.

**Come ci esercitiamo, e quando l'abbiamo fatto l'ultima volta?**

Chiedi se il team ha condotto un'esercitazione o un incidente simulato e che cosa ha imparato. Se mai, discuti un piccolo inizio, come rigiocare un incidente passato in un'ora. Il capitolo SRE menziona di esercitare il processo su modifiche di routine e esercitazioni di disaster recovery. Pianificane una per il prossimo trimestre.

## Nella pratica: un esempio di ITIL agile

Il portale clienti di un'azienda elettrica regionale permette alle famiglie di segnalare interruzioni e consultare le bollette. Lo costruisce e lo gestisce un team di undici persone, con un turno di reperibilità di quattro. Durante una tempesta, il traffico di segnalazioni sale, il portale rallenta e poi si guasta. L'ingegnere di turno prova a riavviare il database, un secondo ingegnere contemporaneamente installa una correzione di configurazione e un terzo annulla un rilascio precedente. Il portale torna dopo tre ore, e il call center, che non era mai stato informato, ha gestito migliaia di chiamate arrabbiate.

Al post-mortem il team vede i tre pericoli del capitolo SRE: tutti concentrati sulla correzione tecnica, nessuno ha comunicato e le modifiche si sono scontrate. Scrivono un processo di gestione degli incidenti di una pagina. Chiunque può dichiarare un incidente, e un secondo team coinvolto, la visibilità ai clienti o un'ora senza progressi significano che devono farlo. L'ingegnere di turno diventa operations lead, e un turno indica un incident commander e un communications lead dal team più ampio. Solo l'operations lead modifica la produzione. Il communications lead invia un aggiornamento ogni 30 minuti al call center e alla sala di controllo. Un canale condiviso contiene il registro vivo.

Alla tempesta successiva il portale rallenta di nuovo, un incidente viene dichiarato entro dieci minuti e il servizio viene ripristinato in 70 minuti con aggiornamenti al call center per tutto il tempo. Restano problemi. Il turno dei commander ha buchi nei giorni festivi, e il team scopre che una dipendenza, un fornitore di messaggi di testo, non ha un contatto di escalation. Il post-mortem produce due azioni con responsabili: completare il turno con una riserva e concordare un percorso di escalation con il fornitore. Il team programma una rievocazione dell'incidente della tempesta per i nuovi membri del turno.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery causano e correggono molti incidenti. Entra nel turno di reperibilità o fornisci supporto diretto ad esso e tratta le azioni dei post-mortem come elementi del backlog. Incorpora nei tuoi rilasci i mezzi per rilevare e annullare i problemi. Partecipa alle esercitazioni così che i ruoli siano familiari.

### Team di servizio e di operations

I team operativi possiedono il processo. Mantienilo breve e allenato, dai alle persone l'autorità di agire e tieni record che altri possano usare. Condividi ciò che impari con i team di delivery e porta le lezioni nella gestione dei problemi e nella pianificazione.

### Leadership e governance

I leader fissano la cultura. Chiedi i post-mortem e leggili, elogia chi segnala problemi e rifiuta di cercare qualcuno da incolpare. Proteggi il tempo per esercitarsi e per completare le azioni. Decidi chi può spendere denaro o invocare il livello di risposta più alto.

### Clienti e utenti

Clienti e utenti hanno bisogno di aggiornamenti tempestivi e onesti e di un modo chiaro di segnalare i problemi. Chiedi al tuo fornitore che cosa puoi aspettarti durante un'interruzione e come sarai informato. Quando ti viene condiviso un post-mortem, leggilo per vedere che cosa il fornitore cambierà.

## Modalità di fallimento comuni

- **Nessun ruolo.** Tutti lavorano sulla correzione tecnica e nessuno coordina o comunica. Nomina invece ogni volta un incident commander, un operations lead e un communications lead.
- **Dichiarare in ritardo.** Le persone aspettano che il problema sia grave. Fissa invece soglie basse e chiare e rendi normale dichiarare.
- **Freelancing.** Più persone modificano il sistema insieme. Consenti invece modifiche solo tramite l'operations lead.
- **Silenzio.** Utenti e stakeholder non sentono nulla. Concorda invece un intervallo di aggiornamento e un modello.
- **Colpa.** Un post-mortem cerca la persona in difetto. Chiedi invece che cosa nel sistema ha permesso l'errore e correggilo.
- **Post-mortem che non vanno da nessuna parte.** Le azioni non hanno responsabili. Mettile invece nel backlog con date e rivedile regolarmente.
- **Non esercitarsi mai.** La prima volta che il processo viene usato è un incidente maggiore. Esercitati invece su piccoli eventi ed esercitazioni.
- **Trattare la riparazione come risoluzione.** Lo stesso incidente ritorna. Collega invece le ripetizioni alla gestione dei problemi e correggi la causa.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Rilevamento e dichiarazione | Gli incidenti sono notati tramite i reclami degli utenti | Esistono alcuni allarmi e alcuni incidenti sono dichiarati | Soglie scritte e un semplice schema di gravità sono usati in modo coerente | Tempi di rilevamento e dichiarazione sono monitorati e ridotti | Rilevamento e dichiarazione sono condivisi tra team e fornitori |
| Risposta e ruoli | Chi risponde improvvisa | Alcuni team nominano un responsabile | Ruoli, passaggi di consegne e un registro vivo sono standard | Tempi di risposta e prestazioni dei ruoli sono rivisti | La risposta è coordinata tra team e fornitori, con esercitazioni congiunte |
| Comunicazione | Gli aggiornamenti sono estemporanei | Alcuni aggiornamenti vanno ad alcuni pubblici | Esistono ritmo di aggiornamento e modelli per ogni gravità | La tempestività della comunicazione è misurata e agli utenti viene chiesto | La comunicazione è coordinata con clienti e partner |
| Apprendimento | Le revisioni seguono solo gli incidenti peggiori | Alcuni post-mortem sono scritti | I post-mortem senza colpe seguono trigger definiti, con azioni tracciate | Completamento delle azioni e ricorrenza sono misurati | Le lezioni sono condivise tra i team e alimentano il cambiamento in tutta l'organizzazione |

## Checklist

- [ ] Abbiamo una breve definizione di incidente con esempi.
- [ ] Abbiamo un piccolo schema di gravità con esempi di impatto sugli utenti ed elenchi di chiamata.
- [ ] Ogni incidente inizia nominando un incident commander, un operations lead e un communications lead.
- [ ] Per ogni incidente viene tenuto un registro vivo.
- [ ] Solo l'operations lead nominato modifica la produzione durante un incidente.
- [ ] Gli intervalli di aggiornamento sono concordati per ogni gravità.
- [ ] I trigger dei post-mortem sono scritti.
- [ ] I post-mortem sono senza colpe, condivisi e rivisti.
- [ ] Ogni azione dei post-mortem ha un responsabile e una data e le azioni aperte sono riviste.
- [ ] Abbiamo esercitato il processo negli ultimi sei mesi.

## Prompt per l'IA

**Scopo: redigere un processo di gestione degli incidenti di una pagina dalla tua pratica attuale.**

```text
Help me draft a one-page incident process for a team of [number] people who run [service].

How we handle incidents today: [describe in a few sentences].
Our on-call arrangement: [describe].
Who needs to be told during an incident: [list audiences].
Rules we must follow (contracts, regulations), with source text if you have it: [paste, or write "none known"].

Produce a short process with: what counts as an incident, a simple severity scheme with user-impact examples (leave numeric thresholds as [to be agreed]), the roles and what each does, how to communicate, and when to hold a postmortem. Mark every item that is an assumption. Do not invent obligations. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: trasformare un registro di incidente in una bozza di post-mortem senza colpe.**

```text
Below is the log of an incident: [paste timestamps, messages, and actions; remove personal data].
Impact as we know it: [describe users affected and for how long, using only facts].

Draft a blameless postmortem with: summary, impact, timeline, how it was detected, how it was mitigated, contributing causes (separate known from suspected), what went well, what went badly, and proposed actions with a suggested type (prevent, detect, respond) but no owners or dates. Describe actions of people neutrally, as roles. Do not invent facts or causes. Mark gaps with [UNKNOWN], and list what you are unsure of.
```

**Scopo: scrivere un aggiornamento di stato dell'incidente per stakeholder non tecnici.**

```text
Write a status update for stakeholders who are not technical about this incident.

Facts: what is affected: [describe]; since when: [time]; what we know about the cause: [what is known, or "not yet known"]; what we are doing: [describe]; when the next update will come: [time].

Write under 120 words in plain language. State what we know and what we do not, without guessing at the cause or the time of recovery. Do not promise a resolution time unless I gave one. Offer two versions: one for customers and one for internal staff. List what you are unsure of.
```

**Scopo: progettare una piccola esercitazione sugli incidenti.**

```text
Design a 60-minute incident exercise for [number] people who run [service].

Scenario basis: [describe a past incident or a plausible failure, using only facts you want to use].
Roles to practice: incident commander, operations lead, communications lead.
Constraints: [for example no use of production systems].

Give a timed plan: briefing, the scenario released in three stages, prompts for each role, and a short review with questions on roles, communication, and records. Do not use real production access. Ask clarifying questions first if information is missing, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [incident-response-plan](../../../../skills/incident-response-plan/SKILL.md): da usare per scrivere il piano che fissa ruoli, soglie e comunicazione per il tuo team.
- [postmortem](../../../../skills/postmortem/SKILL.md): da usare per condurre una revisione senza colpe e registrare le azioni dopo un incidente.
- [runbook](../../../../skills/runbook/SKILL.md): da usare per trasformare le correzioni note in brevi procedure per chi risponde.
- [on-call-rotation](../../../../skills/on-call-rotation/SKILL.md): da usare per progettare un turno equo con riserva e passaggi di consegne.
- [crisis-communication-plan](../../../../skills/crisis-communication-plan/SKILL.md): da usare per pianificare che cosa dire a utenti, personale e pubblico durante una grande interruzione.

## Fonti principali

- **Managing Incidents** (Andrew Stribblehill, in *Site Reliability Engineering*, Google, sre.google): il resoconto pubblico più chiaro del comando degli incidenti per i team di servizio.
- **Postmortem Culture: Learning from Failure** (*Site Reliability Engineering*, Google, sre.google): le ragioni dei post-mortem senza colpe, con trigger e idee per costruire la cultura.
- **Incident management** (Wikipedia): una panoramica multi-settore con una sezione sulla gestione dei servizi IT.
- **IT service management** (Wikipedia): la definizione di incidente e il posto della gestione degli incidenti nel service desk.

## Riferimenti

1. Managing Incidents — Andrew Stribblehill, Google SRE book, sre.google — https://sre.google/sre-book/managing-incidents/
2. Postmortem Culture: Learning from Failure — Google SRE book, sre.google — https://sre.google/sre-book/postmortem-culture/
3. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
4. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
5. Incident Command System — Wikipedia — https://en.wikipedia.org/wiki/Incident_Command_System
6. Root cause analysis — Wikipedia — https://en.wikipedia.org/wiki/Root_cause_analysis
7. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
8. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
9. Computer security incident management — Wikipedia — https://en.wikipedia.org/wiki/Computer_security_incident_management
