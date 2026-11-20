# DevOps

**DevOps è lo sforzo di portare sviluppo e operations in un unico flusso di lavoro con responsabilità condivisa, automazione e feedback rapido, e integra la gestione dei servizi mettendo nella pipeline i controlli a cui ITIL tiene.**

## Perché è importante

DevOps è il nome che la maggior parte delle organizzazioni dà al punto d'incontro tra consegna continua e operazioni IT. È nato da una frustrazione: gli sviluppatori erano premiati per il cambiamento e il personale operativo per la stabilità, quindi i due gruppi tiravano in direzioni opposte, e il passaggio di consegne tra loro era il punto in cui si perdevano velocità e qualità. DevOps chiede a entrambi di condividere la responsabilità dell'intero percorso dall'idea al servizio in esercizio.

Per chi lavora nell'ITSM, DevOps può sembrare minaccioso o ridondante. Minaccioso, perché sembra liquidare i processi che le operations hanno costruito dopo dure esperienze. Ridondante, perché gran parte di ciò che raccomanda, come revisioni degli incidenti, automazione e miglioramento continuo, è già in ITIL. Nessuna delle due visioni è del tutto giusta. L'articolo di Wikipedia su DevOps contrappone DevOps a quello che chiama il framework "top-down" e rigido di ITIL degli anni Novanta, il che è vero per le versioni più vecchie; ITIL 4 è stato scritto per allinearsi ad agile, DevOps e lean (vedi Argomento 2.2 — ITIL).

La definizione di DevOps è contestata, e l'articolo di Wikipedia lo dice. Questo argomento usa l'articolo, le pagine di ricerca DORA e il racconto di Gene Kim dei "Three Ways" e indica che cosa è consolidato, che cosa è dibattuto e che cosa questa guida non ha potuto verificare.

## Concetti fondamentali

### Che cos'è DevOps

L'[articolo di Wikipedia su DevOps](https://en.wikipedia.org/wiki/DevOps) lo descrive come l'integrazione e l'automazione di sviluppo software e operazioni IT, che può accorciare i tempi di sviluppo e migliorare il ciclo di vita dello sviluppo. Cita i ricercatori accademici Len Bass, Ingo Weber e Liming Zhu, che lo descrivono come un insieme di pratiche che mirano a ridurre il tempo tra l'inserimento di una modifica in un sistema e il suo normale collocamento in produzione. L'articolo nota che il termine è usato in diversi contesti e che la sua definizione è dibattuta e che studi accademici dal 2015 al 2017 non hanno trovato consenso sulle sue caratteristiche.

L'articolo riferisce che proposte di combinare metodi di sviluppo con deployment e operations risalgono alla fine degli anni Ottanta e all'inizio dei Novanta e che la prima conferenza DevOps Days si tenne a Gand, in Belgio, nel 2009, fondata da Patrick Debois. Caratterizza generalmente DevOps con tre principi, responsabilità condivisa, automazione del flusso di lavoro e feedback rapido, e nota che questa caratterizzazione è essa stessa dibattuta.

### I Three Ways

Gene Kim, autore di *The Phoenix Project* e *The DevOps Handbook*, descrive tre principi da cui, sostiene, si possono derivare i modelli DevOps. Come riassunto nel post di Kim sul sito IT Revolution e in riassunti secondari:

| Way | Idea | Esempi |
|---|---|---|
| **Il primo Way: flusso** | Guardare alle prestazioni dell'intero sistema, non di un singolo silo; accelerare il lavoro dall'idea al valore | Non passare a valle difetti noti; non lasciare che l'ottimizzazione locale degradi l'insieme; cercare sempre di aumentare il flusso |
| **Il secondo Way: feedback** | Accorciare e amplificare i segnali che tornano dalle fasi successive a quelle precedenti | Telemetria, pipeline che falliscono in fretta, feedback dei clienti |
| **Il terzo Way: apprendimento continuo e sperimentazione** | Costruire una cultura che prende piccoli rischi deliberati e impara da essi | Riservare tempo all'apprendimento, trasformare le scoperte locali in miglioramenti globali |

Corrispondono ai temi di questa guida: flusso (vedi Argomento 1.5 — Kanban e Argomento 1.7 — Sviluppo software lean), feedback (vedi Argomento 3.10 — Monitoraggio e gestione degli eventi) e apprendimento (vedi Argomento 1.10 — Apprendimento agile). Una nota sulla terminologia: il post di Kim chiama il Secondo Way "amplify feedback loops", e l'Handbook lo chiama "feedback".

### Pratiche

Secondo Wikipedia, integrazione continua e consegna continua sono fondamentali per il successo di DevOps, insieme all'automazione. L'articolo menziona controllo di versione, macchine virtuali, containerizzazione e database DevOps, che applica controllo di versione, test automatici e CI/CD alle modifiche di schema e dati. Descrive GitOps come la gestione della configurazione di deployment nel controllo di versione e DevSecOps come l'integrazione della sicurezza nella consegna tramite test "shift left", compresa l'analisi statica e dinamica. L'elenco di capacità di DORA include consegna continua, integrazione continua, automazione del deployment, automazione dei test, sviluppo trunk-based, controllo di versione, gestione delle modifiche al database, monitoraggio e osservabilità, sicurezza pervasiva, lavoro a piccoli lotti e limiti al lavoro in corso (vedi Argomento 3.5 — Gestione di rilasci e deployment).

### Cultura

L'elenco di capacità di DORA, letto per questa guida, include elementi culturali: cultura organizzativa generativa, cultura dell'apprendimento, leadership trasformazionale, soddisfazione lavorativa, benessere e sperimentazione del team. La pagina che li elenca non li spiega e non li ordina. Un'altra pagina DORA dice che le sue metriche predicono prestazioni organizzative e benessere dei membri del team e mette in guardia dalla proprietà a silos, raccomandando una proprietà condivisa tra i team di sviluppo, operations e rilascio. Concorda con il Terzo Way: DevOps riguarda tanto come le persone lavorano insieme quanto gli strumenti.

Il comune mnemonico **CALMS** (culture, automation, lean, measurement, sharing) è spesso usato per riassumere DevOps. L'articolo di Wikipedia su DevOps non lo menziona e questa guida non ne ha verificato l'origine, quindi è nominato qui solo perché i lettori lo incontreranno.

### DevOps e agile

L'articolo dice che build e test automatici, integrazione continua e consegna continua hanno avuto origine nel mondo agile e che l'omissione delle pratiche ingegneristiche da parte di Scrum ha fatto sì che il lavoro di automazione si staccasse in DevOps. Si adatta all'Argomento 1.4 — Previsioni di consegna e metriche di pianificazione, che nota che Scrum non dice come costruire, testare, installare o gestire il software. Extreme Programming contiene già molte delle pratiche ingegneristiche (vedi Argomento 1.6 — Extreme Programming). DevOps estende la preoccupazione agile oltre il punto del rilascio.

### DevOps e ITIL

L'articolo contrappone DevOps al framework "top-down" e rigido di ITIL degli anni Novanta e non discute oltre l'ITSM. Un quadro più equo per oggi:

| | Tende a enfatizzare | Rischio se usato da solo |
|---|---|---|
| **DevOps** | Flusso, automazione, responsabilità condivisa, feedback rapido | Trascurare record, controlli e la visione più ampia del servizio |
| **ITIL 4** | Valore, pratiche, governance, un'ampia gamma di pratiche di servizio | Trattare le pratiche come processo pesante |

Lo schema di certificazione di ITIL 4 stesso include un modulo specialistico chiamato High Velocity IT (HVIT) nel percorso Managing Professional, come elenca l'articolo di Wikipedia su ITIL. Mostra che il proprietario tratta il lavoro digitale e rapido come un argomento a sé. Una combinazione pratica: usa le pratiche DevOps per implementare le pratiche ITIL nella pipeline, come registrare automaticamente i cambiamenti, eseguire test come controllo del rischio e monitorare come pratica degli eventi (vedi Argomento 3.4 — Abilitazione dei cambiamenti e Argomento 5.1 — Gestione agile dei servizi).

### DevOps e site reliability engineering

L'articolo di Wikipedia dice che Google sviluppò la site reliability engineering nel 2003 e che alcuni dei suoi autori originali vedono la SRE come un'implementazione di DevOps. L'articolo sulla SRE la chiama un'implementazione specifica di DevOps, più ristretta perché si concentra sul costruire sistemi affidabili (vedi Argomento 5.3 — Site reliability engineering).

### Misure

Le misure di prestazione della consegna del software di DORA danno un vocabolario comune: change lead time, deployment frequency, failed deployment recovery time, change fail rate e deployment rework rate (vedi Argomento 3.4 — Abilitazione dei cambiamenti e Argomento 5.6 — Metriche e misurazione). L'articolo di Wikipedia riferisce che le metriche furono pubblicate nel 2016, che la misura di ripristino è stata rinominata nel rapporto 2023, che una misura di rilavorazione è stata aggiunta nel 2024 e che nel 2025 DORA ha sostituito i livelli di prestazione con sette archetipi di team. Registra anche che alcuni esperti hanno criticato la metodologia e le metriche della ricerca DORA. Tratta le misure come domande utili e non come punteggi.

### Critiche e limiti

Oltre alla mancanza di una definizione consolidata, l'articolo riferisce critiche alla metodologia DORA. Le critiche pratiche comuni, offerte qui come esperienza pratica e non come risultati delle fonti, includono "DevOps" usato come titolo professionale per il vecchio ruolo operativo, strumenti adottati senza cambiamento culturale e conformità trascurata nella ricerca della velocità. L'articolo non dà statistiche di adozione.

## Buone pratiche

1. **Concorda che cosa intendi per DevOps.** Scrivi una breve dichiarazione di che cosa significa per i tuoi team, come responsabilità condivisa di un servizio, consegna automatizzata e feedback rapido. Una definizione condivisa evita discussioni sulle etichette.
2. **Condividi la responsabilità del servizio.** Rendi le persone che costruiscono un servizio responsabili di come gira e dai loro i mezzi: reperibilità, monitoraggio e accessi. Sostienile con competenza operativa.
3. **Automatizza il percorso verso la produzione.** Costruisci una pipeline che compila, testa e installa ogni modifica. Registra che cosa ha fatto. Tratta la pipeline come un prodotto con utenti.
4. **Lavora a piccoli lotti.** Rilascia spesso piccole modifiche. Questo riduce il rischio e accelera il feedback, come suggerisce l'elenco di capacità di DORA.
5. **Accorcia i cicli di feedback.** Rendi visibili al team risultati dei test, monitoraggio e feedback degli utenti entro minuti o ore. Segui il Secondo Way: amplifica i segnali che tornano indietro.
6. **Guarda l'intero flusso.** Mappa il percorso dall'idea al servizio in esercizio e trova le attese più lunghe, comprese quelle fuori dal team di sviluppo. Segui il Primo Way: non ottimizzare un silo a scapito dell'insieme (vedi Argomento 5.4 — Gestione del flusso di valore).
7. **Incorpora sicurezza e conformità.** Metti nella pipeline controlli di sicurezza e di policy automatici e registra le prove come sottoprodotto (vedi Argomento 3.13 — Gestione della sicurezza delle informazioni e Argomento 5.7 — Governance, rischio e conformità).
8. **Tratta la cultura come una questione di prima classe.** Investi in apprendimento, revisioni senza colpe, sicurezza psicologica e obiettivi condivisi. L'elenco di capacità di DORA include la cultura accanto agli elementi tecnici per una ragione.
9. **Ritaglia tempo per imparare e sperimentare.** Riserva tempo e luoghi sicuri per gli esperimenti e condividi le lezioni. Segui il Terzo Way.
10. **Usa le pratiche ITIL dove aiutano.** Mantieni le pratiche di incidenti, problemi, cambiamenti e conoscenza, implementate attraverso automazione e record leggeri. Rimuovi i passaggi che non servono il loro scopo.
11. **Misura con cura.** Monitora misure in stile DORA per servizio, migliora rispetto alle tue prestazioni passate ed evita di fissarle come obiettivi (vedi Argomento 5.6 — Metriche e misurazione).
12. **Evita la trappola del titolo.** Non creare un "team DevOps" separato che diventa un nuovo silo tra sviluppo e operations. Diffondi le pratiche tra i team e usa team di piattaforma o di supporto per aiutare.

## Domande da discutere con il team

**Che cosa significa DevOps qui, e dove abbiamo sentito la parola per la prima volta?**

Chiedi a ciascuno una definizione in una frase. Confronta. L'articolo di Wikipedia dice che la definizione è dibattuta, quindi le differenze sono attese. Scrivi una dichiarazione condivisa concreta: chi possiede che cosa, che cosa è automatizzato, quale feedback esiste. Chi facilita può chiedere che cosa è cambiato finora a causa della parola.

**Dove aspetta una modifica tra "pronta" e "live", e chi possiede l'attesa?**

Ripercorri una modifica recente ed elenca le attese: revisioni, approvazioni, ambienti, finestre di rilascio. Segna quelle fuori dal team. Chiedi quali attese proteggono da rischi reali e quali sono abitudine. Scegline una da accorciare, lavorando con il suo responsabile.

**Quando qualcosa si rompe in produzione, chi è di turno, e ha i mezzi per correggerlo?**

Chiedi chi viene chiamato e che cosa può fare da solo. Se chi costruisce non è di turno, chiedi perché. Se il personale operativo non può cambiare il codice, chiedi che cosa fa. Discuti che aspetto avrebbe qui la responsabilità condivisa e quale sostegno servirebbe.

**Quale feedback riceviamo dopo un rilascio, e con quale rapidità?**

Elenca i segnali: test, monitoraggio, ticket di supporto, commenti degli utenti. Chiedi quanto ci mette ciascuno a raggiungere il team. Risposte tipiche: i test in minuti, i ticket in giorni. Scegli un segnale da accelerare.

**Quanto è sicuro provare qualcosa e fallire?**

Chiedi un esempio recente di esperimento fallito e che cosa è successo alle persone coinvolte. Il Terzo Way dipende dall'imparare da piccoli fallimenti. Discuti che cosa renderebbe più sicuri gli esperimenti, come limiti, rollback e revisione senza colpe.

**Come compaiono le nostre pratiche ITIL nella pipeline, e dove non compaiono?**

Prendi le pratiche di cambiamento, incidenti e conoscenza e chiedi dove ciascuna appare nell'automazione. Le lacune indicano lavoro manuale o controlli non documentati da prove. Concorda una pratica da portare nella pipeline.

## Nella pratica: un esempio di ITIL agile

Un servizio postale nazionale ha un gruppo di sviluppo di 40 persone e un gruppo operativo di 25. Gli sviluppatori rilasciano una versione maggiore ogni trimestre e passano alle operations un pacchetto e un lungo documento, che lo installano in un fine settimana. Le operations si lamentano che gli sviluppatori non capiscono la produzione e gli sviluppatori che le operations non sono raggiungibili quando un difetto richiede una correzione rapida. Un recente rilascio ha richiesto 19 ore, ha rotto la pagina di tracciamento dei pacchi e ha portato a un giorno di rimpalli di colpe.

Un nuovo responsabile della piattaforma propone una sperimentazione con un team di prodotto, il servizio di tracciamento dei pacchi. Quattro sviluppatori e due ingegneri delle operations formano un unico team che possiede il servizio end-to-end. Gli sviluppatori entrano nel turno di reperibilità, sostenuti dagli ingegneri delle operations. Il team costruisce una pipeline che compila, testa e installa ogni modifica integrata su un ambiente di staging e installa in produzione con un passaggio di approvazione che dà il responsabile del servizio. I record dei cambiamenti sono creati dalla pipeline. Viene aggiunto il monitoraggio, gli allarmi vanno all'intero team e ogni incidente in produzione riceve una breve revisione senza colpe. Il team concorda di rilasciare almeno ogni settimana e il responsabile della piattaforma gli chiede di monitorare lead time, deployment frequency, change fail rate e tempo di ripristino.

Dopo quattro mesi il team rilascia due volte alla settimana, il tempo mediano dall'integrazione alla produzione è inferiore a un giorno e l'ultimo incidente è stato corretto in meno di un'ora dallo sviluppatore che aveva scritto la modifica. Non tutto funziona. Gli ingegneri delle operations trovano rumorosi gli allarmi degli sviluppatori e gli sviluppatori si risentono di essere di turno di notte. Un team vicino che dipende dal tracciamento dei pacchi non è stato informato del nuovo ritmo ed è stato sorpreso da una modifica. Il responsabile della piattaforma riserva al team tempo per regolare gli allarmi, aggiunge un turno con un limite alle chiamate notturne e organizza una riunione mensile con i team dipendenti. L'audit interno chiede di vedere le prove delle approvazioni e il responsabile della piattaforma mostra i record della pipeline e le revisioni degli incidenti.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery assumono la responsabilità operativa: monitoraggio, reperibilità e apprendimento dagli incidenti. Costruisci la pipeline e il feedback di cui hai bisogno e chiedi competenza operativa anziché consegnare. Mantieni piccole e visibili le modifiche.

### Team di servizio e di operations

I team operativi portano la conoscenza di come i servizi si guastano e di quali controlli contano. Aiuta a costruire la piattaforma e i controlli, condividi la reperibilità e insegna. Evita di essere un cancello; diventa un abilitatore che rende facile la via sicura.

### Leadership e governance

I leader creano le condizioni: obiettivi condivisi tra sviluppo e operations, tempo per l'automazione, una cultura che impara dai fallimenti e fiducia nelle prove della pipeline. Evita di rinominare i team senza cambiare gli incentivi e chiedi risultati, non l'adozione di DevOps.

### Clienti e utenti

Clienti e utenti vedono DevOps come miglioramento più rapido e ripristino più rapido. Aspettati modifiche piccole e frequenti e comunicazione chiara su di esse. Dai feedback in fretta, perché il team è organizzato per usarli.

## Modalità di fallimento comuni

- **Un team DevOps come nuovo silo.** Sviluppo e operations ancora non si parlano. Diffondi invece le pratiche tra i team e usa i team di piattaforma per rendere possibile.
- **Strumenti senza cultura.** Si costruisce una pipeline e nient'altro cambia. Cambia invece insieme responsabilità, incentivi e feedback.
- **Velocità senza sicurezza.** I rilasci accelerano e i guasti salgono. Investi invece prima in test, monitoraggio e rollback rispetto al ritmo.
- **Abbandonare del tutto ITIL.** Record e controlli spariscono. Mantieni invece le pratiche e implementale nella pipeline.
- **Sviluppatori di turno senza sostegno.** Segue il burnout. Condividi invece il turno, regola gli allarmi e limita le chiamate notturne.
- **Metriche come obiettivi.** I team manipolano i conteggi dei deployment. Usa invece più misure e confronta con la tua storia.
- **Ignorare i team dipendenti.** Le modifiche sorprendono i vicini. Comunica invece ritmo e modifiche ai team che dipendono dal tuo.
- **Trattare la parola come obiettivo.** Le etichette sostituiscono i risultati. Chiedi invece che aspetto hanno flusso, feedback e apprendimento migliori per i tuoi utenti.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Responsabilità condivisa | Sviluppo e operations si passano le consegne al rilascio | Alcuni team condividono la reperibilità | I team possiedono i propri servizi end-to-end con sostegno | Gli effetti della responsabilità su qualità e carico sono misurati | I modelli di responsabilità sono coordinati tra team, piattaforme e fornitori |
| Automazione e flusso | La consegna è manuale e a lotti | Esistono alcune pipeline | Una pipeline comune compila, testa, installa e registra le modifiche | Lead time, frequenza, fallimenti e ripristino sono misurati e regolati | Pipeline e flusso sono ottimizzati tra team e flussi di valore |
| Feedback | Il feedback arriva dagli utenti dopo i problemi | Alcuni team monitorano i rilasci | Test, monitoraggio e feedback degli utenti raggiungono i team in minuti o ore | Velocità e qualità del feedback sono misurate e migliorate | I cicli di feedback attraversano team, fornitori e clienti |
| Cultura e apprendimento | La colpa segue il fallimento | Alcune revisioni senza colpe | Revisioni senza colpe, esperimenti e tempo di apprendimento sono routine | Le azioni di apprendimento sono monitorate e i risultati verificati | L'apprendimento si diffonde in modo continuo in tutta l'organizzazione |

## Checklist

- [ ] Abbiamo una definizione scritta e condivisa di che cosa DevOps significa per noi.
- [ ] I team che costruiscono un servizio condividono la responsabilità di gestirlo.
- [ ] Una pipeline compila, testa e installa le modifiche e registra che cosa ha fatto.
- [ ] Le modifiche sono rilasciate in piccoli lotti, spesso.
- [ ] Feedback di test, monitoraggio e utenti raggiungono rapidamente il team.
- [ ] Controlli di sicurezza e di policy girano nella pipeline.
- [ ] La reperibilità è condivisa, con limiti alle chiamate notturne e allarmi regolati.
- [ ] Le revisioni degli incidenti sono senza colpe e producono azioni con responsabile.
- [ ] Monitoriamo lead time, deployment frequency, change fail rate e tempo di ripristino per ogni servizio.
- [ ] I team dipendenti sono informati del nostro ritmo di rilascio e delle modifiche importanti.

## Prompt per l'IA

**Scopo: mappare le attese tra "pronto" e "live".**

```text
Help me map the waits for a typical change in [team or service].

The steps from "ready" to "live," who does each, whether it is manual or automated, and how long work waits before it (use real data; mark estimates as estimates): [paste].

Produce a simple text diagram, highlight the three longest waits and which team owns each, and suggest, for each, a question to ask about whether the wait protects against a real risk. Do not invent durations. If the data are too thin, say what to collect. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: verificare dove le pratiche ITIL compaiono nella tua pipeline.**

```text
Help me compare our pipeline with service management practices.

What our pipeline does today, step by step: [paste].
The practices we want to check: change enablement, release and deployment, incident management, problem management, knowledge management, configuration management.

For each practice, say what in the pipeline description appears to support it (quote my words), what is missing, and one question to ask. Do not claim that a standard requires anything unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: pianificare una sperimentazione di responsabilità condivisa con un team.**

```text
Plan a four-month pilot of shared ownership for [service], bringing together [number] developers and [number] operations engineers.

Today's arrangement: [describe who builds, who runs, who is on call].
Concerns from each side: development [list]; operations [list].
Measures we have: [list].

Give a plan with: team formation, on-call arrangements with limits, pipeline and monitoring work, how the team learns from incidents, which measures to review (leave targets as [to be agreed]), what evidence to keep for audit, and how to tell dependent teams. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: progettare una revisione di incidente senza colpe per un team misto.**

```text
Design a 45-minute blameless review for this incident: [describe the incident factually].

People involved: [roles from development and operations].
Information available (timeline, alerts, changes): [list].

Provide an agenda that builds the timeline first, identifies contributing causes in systems and processes, notes what went well, and ends with at most three actions with owners. Include prompts that avoid blame. Ask clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [agile-delivery](../../../../skills/agile-delivery/SKILL.md): da usare per pianificare rilasci piccoli e frequenti e i controlli attorno ad essi.
- [test-driven-development](../../../../skills/test-driven-development/SKILL.md): da usare per costruire i test automatici da cui dipende una pipeline.
- [shift-left-testing](../../../../skills/shift-left-testing/SKILL.md): da usare per anticipare test e controlli di sicurezza nella pipeline.
- [on-call-rotation](../../../../skills/on-call-rotation/SKILL.md): da usare per progettare una reperibilità condivisa con limiti equi.
- [postmortem](../../../../skills/postmortem/SKILL.md): da usare per condurre revisioni senza colpe che alimentano il Terzo Way.

## Fonti principali

- **DevOps** (Wikipedia): una panoramica di definizioni, pratiche, rapporti con agile, SRE e DevSecOps e metriche DORA, con i dibattiti annotati.
- **The Three Ways: The Principles Underpinning DevOps** (Gene Kim, IT Revolution): la fonte di flusso, feedback e apprendimento continuo.
- **DORA capabilities and metrics** (dora.dev): l'elenco di capacità del programma di ricerca e le sue misure di consegna del software.
- **The DevOps Handbook** e **The Phoenix Project** (Gene Kim e coautori): i libri che sviluppano in dettaglio i Three Ways.

## Riferimenti

1. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
2. The Three Ways: The Principles Underpinning DevOps — Gene Kim, IT Revolution — https://itrevolution.com/the-three-ways-principles-underpinning-devops/
3. DORA capabilities — DORA, dora.dev — https://dora.dev/capabilities/
4. DORA's software delivery performance metrics — DORA, dora.dev — https://dora.dev/guides/dora-metrics-four-keys/
5. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
6. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
7. Continuous delivery — Wikipedia — https://en.wikipedia.org/wiki/Continuous_delivery
8. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
9. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
