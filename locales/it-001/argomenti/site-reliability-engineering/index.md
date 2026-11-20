# Site reliability engineering

**La site reliability engineering tratta le operations come un problema ingegneristico, usando obiettivi di livello di servizio, error budget e un tetto al lavoro manuale ripetitivo per mantenere affidabili i servizi continuando a cambiare in fretta.**

## Perché è importante

Molte pratiche di gestione dei servizi furono progettate per un mondo in cui il personale operativo gestiva software scritto da altri e il costo della gestione cresceva con la dimensione del servizio. La site reliability engineering (SRE) è la risposta di un'organizzazione a ciò che accade quando quel modello raggiunge una scala molto grande: chiedere a ingegneri del software di progettare e gestire la funzione operativa e fare in modo che sia il sistema a svolgere il lavoro che le persone farebbero altrimenti a mano.

Per i lettori di questa guida, la SRE è utile per tre ragioni. Rende esplicito il compromesso tra velocità e affidabilità, con numeri che team di prodotto e operations possono leggere entrambi. Dà un'idea precisa di quanto lavoro manuale sia troppo. E mostra come molte pratiche ITIL, come gestione di incidenti, problemi, cambiamenti e capacità, possano essere svolte in termini ingegneristici. La SRE non è l'unico modo di farle e nasce dalle circostanze di una società Internet molto grande, quindi ciò che si trasferisce dipende dalla tua situazione.

Questo argomento si basa soprattutto su tre capitoli del libro *Site Reliability Engineering* di Google, integrati dall'articolo di Wikipedia sulla SRE. Il libro descrive la pratica in un'organizzazione e sostiene il proprio approccio; l'articolo di Wikipedia dà un quadro più ampio ma più sottile e non nomina critiche. Leggi entrambi come fonti di idee da mettere alla prova, non come uno standard.

## Concetti fondamentali

### Che cos'è la SRE

L'introduzione del libro definisce la SRE come "what happens when you ask a software engineer to design an operations team". L'[articolo di Wikipedia sulla site reliability engineering](https://en.wikipedia.org/wiki/Site_reliability_engineering) la descrive come una disciplina all'interno dell'ingegneria del software e del supporto all'infrastruttura IT che monitora e migliora disponibilità e prestazioni del software installato e dei grandi servizi, con un'attenzione ad automazione e infrastruttura come codice. L'articolo chiama la SRE un'implementazione specifica di DevOps, più ristretta di ambito perché si concentra sul costruire sistemi affidabili (vedi Argomento 5.2 — DevOps). Il libro descrive DevOps come un insieme più ampio di principi che la SRE implementa in un modo specifico.

Secondo l'articolo, la pratica SRE di Google iniziò nel 2003 quando Benjamin Treynor Sloss entrò in azienda e formò un team da sette ingegneri di produzione; nel 2016 il team aveva più di 1.000 SRE e altre grandi società Internet avevano adottato la pratica. Un'indagine del 2020 su 572 professionisti ha trovato team SRE nel 64 percento delle organizzazioni con 10.000 o più dipendenti, nel 44 percento di quelle con da 101 a 1.000 e nel 32 percento di quelle con 100 o meno. La serie di conferenze SREcon si tiene ogni anno dal 2014.

### Il problema che la SRE affronta

L'introduzione descrive il modello tradizionale: sviluppatori e amministratori di sistema sono divisi in team separati. Nomina due tipi di costo:

- **Costi diretti.** La gestione manuale dei cambiamenti e degli eventi diventa costosa, perché il team operativo cresce con il carico.
- **Costi indiretti.** I team hanno vocabolari, incentivi e presupposti diversi sul rischio, il che porta a conflitti sui rilasci. Le operations aggiungono cancelli di lancio e gli sviluppatori rispondono con soluzioni aggiranti.

La SRE mira a evitare questa divisione trattando le operations come un problema ingegneristico. Il capitolo dice che la dimensione del team cresce più lentamente del sistema, perché l'ingegneria impedisce al carico operativo di crescere in misura pari al traffico.

### I principi

L'introduzione elenca le aree di cui i team SRE sono responsabili: disponibilità, latenza, prestazioni, efficienza, gestione dei cambiamenti, monitoraggio, risposta alle emergenze e pianificazione della capacità. L'articolo di Wikipedia elenca pratiche centrali che includono automatizzare il lavoro ripetitivo, definire obiettivi di affidabilità attraverso indicatori di livello di servizio (SLI), obiettivi (SLO) ed error budget, progettare sistemi per ridurre il rischio, osservabilità e monitoraggio, gestione del toil, un processo di gestione degli incidenti testato e pianificazione della capacità, gestione dei rilasci e chaos engineering.

### Obiettivi di livello di servizio ed error budget

La SRE lega l'affidabilità a obiettivi espliciti (vedi Argomento 3.7 — Gestione dei livelli di servizio per la trattazione completa). In breve:

- Scegli pochi indicatori che riflettono ciò a cui gli utenti tengono.
- Fissa un obiettivo che non pretenda la perfezione.
- Ammetti un **error budget**: lo spazio tra il perfetto e l'obiettivo.
- Usa il budget per decidere il ritmo dei rilasci: finché resta budget, i rilasci continuano; quando è esaurito, i rilasci rallentano e lo sforzo si sposta sull'affidabilità.

Il capitolo "Embracing Risk" spiega perché: i team di prodotto sono misurati sulla velocità e i team di affidabilità sull'affidabilità, il che crea tensione, e il budget dà a entrambi una misura condivisa e oggettiva. Lo stesso capitolo dice che i costi dell'affidabilità salgono ripidamente e che l'obiettivo è adeguare il rischio di un servizio a ciò che il business accetterà (vedi Argomento 3.11 — Disponibilità, capacità e prestazioni).

### Toil

Il capitolo "Eliminating Toil" definisce il **toil** come lavoro operativo legato alla gestione di un servizio in produzione e dice che non è semplicemente un lavoro che a qualcuno non piace ed è distinto dall'overhead come le riunioni. Il toil tende a essere:

| Caratteristica | Significato |
|---|---|
| **Manuale** | Richiede sforzo umano diretto, anche se uno script esegue i passaggi |
| **Ripetitivo** | Fatto più e più volte, non un problema nuovo |
| **Automatizzabile** | Una macchina potrebbe farlo, o il bisogno potrebbe essere eliminato per progetto |
| **Tattico** | Guidato dalle interruzioni e reattivo, come rispondere alle chiamate |
| **Senza valore duraturo** | Il servizio è nello stesso stato dopo |
| **Lineare con la crescita** | Lo sforzo scala con dimensione del servizio, traffico o utenti |

Il libro dice che gli SRE puntano a tenere il toil sotto il 50 percento del loro tempo, con almeno metà speso in lavoro di progetto ingegneristico, e l'introduzione fissa un tetto del 50 percento al lavoro "ops" aggregato, rimandando l'eccesso ai team di sviluppo. Dice che troppo toil causa stagnazione di carriera, basso morale e burnout, rallenta il lavoro sulle funzionalità e spinge all'abbandono; "toil becomes toxic when experienced in large quantities", anche se piccole quantità possono essere calmanti e parte è inevitabile. Il capitolo dà un modo di calcolare il minimo che la reperibilità impone (per esempio un limite inferiore del 33 percento per un turno di sei persone nelle sue ipotesi d'esempio) e riferisce che le interruzioni erano la fonte maggiore di toil, seguite dalla risposta alla reperibilità e poi dai rilasci. Definisce il lavoro ingegneristico come nuovo, che richiede giudizio, produce miglioramento permanente e segue una strategia.

### Risposta alle emergenze e monitoraggio

L'introduzione dice che il monitoraggio non dovrebbe richiedere a una persona di interpretare gli allarmi: il software interpreta i dati e le persone sono avvisate solo quando serve un'azione (vedi Argomento 3.10 — Monitoraggio e gestione degli eventi). Dice che gli SRE di turno dovrebbero ricevere al massimo circa due eventi per turno. Sostiene che i playbook producono un miglioramento di circa tre volte nel tempo medio di riparazione rispetto all'improvvisare. La gestione degli incidenti segue un approccio di comando degli incidenti e i post-mortem sono senza colpe e scritti per tutti gli incidenti significativi (vedi Argomento 3.2 — Gestione degli incidenti).

### Gestione dei cambiamenti

L'introduzione afferma che circa il 70 percento delle interruzioni deriva da modifiche a un sistema in esercizio e raccomanda rollout progressivi, rilevamento rapido dei problemi e rollback sicuri. È un'affermazione del libro stesso, dall'esperienza di Google, e può non valere per ogni organizzazione. Il suo messaggio è coerente con le indicazioni DORA sul cambiamento (vedi Argomento 3.4 — Abilitazione dei cambiamenti e Argomento 3.5 — Gestione di rilasci e deployment).

### SRE e ITIL

La SRE può essere letta come un modo ingegneristico di svolgere diverse pratiche ITIL:

| Pratica ITIL | Approccio SRE |
|---|---|
| Gestione degli incidenti | Ruoli di comando degli incidenti, un registro vivo dell'incidente, post-mortem senza colpe |
| Gestione dei problemi | Azioni dei post-mortem nel backlog, rimozione del toil alla causa |
| Abilitazione dei cambiamenti | Rollout progressivi, rilevamento rapido, rollback sicuro, controlli automatici |
| Gestione dei livelli di servizio | SLI, SLO, error budget |
| Monitoraggio e gestione degli eventi | Allarmi basati sui sintomi, i quattro segnali d'oro |
| Gestione della capacità | Pianificazione della capacità come compito ingegneristico, con test di carico |
| Miglioramento continuo | Un tetto al toil, progetti ingegneristici come lavoro principale |

L'associazione è di questa guida, non delle fonti. Né il libro né l'articolo di Wikipedia dichiarano di implementare ITIL.

### Modelli di impiego

L'articolo di Wikipedia descrive sei modelli organizzativi per la SRE: "Kitchen Sink", infrastruttura, strumenti, prodotto o applicazione, incorporato e consulenza. Dice che un ibrido è comune nelle grandi organizzazioni, ma segna quell'affermazione come bisognosa di citazione. Quale modello ti si addice dipende dalla tua dimensione e dal numero di servizi.

### Limiti e critiche

L'articolo di Wikipedia non indica critiche, costi o modalità di fallimento, e il libro descrive il successo di un'organizzazione. I limiti pratici sono ben noti dall'esperienza e offerti qui come tali: la SRE ha bisogno di ingegneri che sappiano scrivere software e siano disposti a fare operations; il tetto del 50 percento ha bisogno del sostegno del management; gli error budget funzionano solo se i team di prodotto li rispettano; e l'approccio è difficile da copiare senza la scala e gli strumenti che l'hanno prodotto. Le organizzazioni più piccole possono adottare le idee, come obiettivi, budget, misurazione del toil e revisione senza colpe, senza creare un team.

## Buone pratiche

1. **Scegli un servizio e fissa un obiettivo.** Scegli da due a quattro indicatori che riflettono l'esperienza dell'utente, fissa un primo obiettivo largo e misura per qualche mese prima di stringerlo.
2. **Concorda una policy sull'error budget.** Scrivi che cosa succede quando il budget è quasi esaurito e quando è esaurito e chi può derogare. Falla una regola congiunta di prodotto e operations.
3. **Misura il toil.** Chiedi alle persone di registrare quanto del loro tempo va in lavoro operativo manuale e ripetitivo. Usa le sei caratteristiche per classificarlo. Guarda le fonti principali.
4. **Fissa un tetto al lavoro manuale.** Stabilisci un massimale per il toil, come metà del tempo di una persona, e rivedilo. Quando il tetto è superato, rimanda il lavoro in eccesso ai team che possiedono le cause o riduci l'ambito.
5. **Automatizza prima il toil più grande.** Scegli la voce che costa più tempo ed è più ripetibile, automatizzala con test e misura il risparmio. Preferisci eliminare il bisogno per progetto all'automatizzarlo.
6. **Proteggi il tempo di ingegneria.** Pianifica il lavoro di progetto per gli ingegneri delle operations come lavoro reale con responsabili e date. Senza di esso, il toil si espande.
7. **Limita le interruzioni.** Punta a pochi eventi per turno di reperibilità, regola gli allarmi in modo che le chiamate siano azionabili e correggi le cause ricorrenti. L'indicazione del libro è al massimo circa due eventi per turno.
8. **Scrivi playbook.** Per i guasti comuni, scrivi brevi passaggi di risposta testati. Il libro sostiene che migliorano il tempo di riparazione rispetto all'improvvisare.
9. **Rendi le modifiche progressive e reversibili.** Distribuisci gradualmente, rileva rapidamente i problemi e annulla in sicurezza. Poiché le modifiche sono la causa più comune di interruzioni nell'esperienza del libro, investi prima qui.
10. **Conduci post-mortem senza colpe per gli incidenti significativi,** compresi i quasi-incidenti che non hanno innescato chiamate. Trasforma le azioni in elementi del backlog.
11. **Parti dalle idee, non dal team.** Le organizzazioni più piccole possono adottare obiettivi, budget, misure del toil e post-mortem con il personale esistente prima di creare un team dedicato.
12. **Scegli di proposito un modello organizzativo.** Se crei una funzione SRE, decidi se fornisce strumenti, si incorpora con i team di prodotto o fa consulenza e rivedi la scelta man mano che cresci.

## Domande da discutere con il team

**Su quale servizio metteremmo per primo un obiettivo, e quale sarebbe?**

Chiedi a ciascuno di nominare il servizio e l'indicatore che meglio riflette l'esperienza dell'utente. Confronta. Le differenze mostrano priorità poco chiare. Chi facilita può chiedere che cosa succede oggi quando il servizio è più lento o meno disponibile di quanto gli utenti si aspettano. Concorda un servizio da cui partire e che cosa misurare.

**Che cosa faremmo se esaurissimo l'intero error budget questo mese?**

Chiedi al team e a un rappresentante del prodotto di descrivere le azioni, chi decide e che cosa è protetto. Molti team non hanno mai concordato. Discuti se una pausa nei rilasci rischiosi sarebbe accettata. Redigi una policy di una pagina.

**Quanto della nostra settimana è toil, e quali sono le tre fonti principali?**

Chiedi alle persone di stimare e poi tieni un registro per due settimane. Confronta le stime con i registri. Lo scopo è vedere la forma del lavoro, non incolpare. Scegli la fonte più grande e chiedi se può essere eliminata per progetto.

**Quale compito manuale ricorrente potrebbe essere eliminato da uno script o da una modifica di progetto?**

Elenca i compiti che le persone temono. Per ciascuno, stima frequenza e tempo. I candidati migliori sono frequenti, stabili e a basso rischio. Chiedi che cosa renderebbe sicura l'automazione, come limiti e log. Scegline uno da automatizzare.

**Quanti eventi riceve ogni turno di reperibilità, e quanti richiedono azione?**

Conta per l'ultimo trimestre. Se il numero è alto, discuti da dove viene. L'introduzione suggerisce di puntare a circa due eventi per turno. Scegli una fonte di allarmi da correggere.

**Che cosa perderemmo e guadagneremmo se creassimo un team di affidabilità dedicato?**

Chiedi pareri onesti. I guadagni possono essere concentrazione e competenze; le perdite un nuovo silo o lo scarico del lavoro operativo. Discuti alternative come ingegneri incorporati o una rotazione. Decidi che cosa provare in piccolo.

## Nella pratica: un esempio di ITIL agile

Un distributore regionale di elettricità gestisce un'app per la segnalazione dei guasti e un sistema di invio delle squadre sul campo. Un team combinato di diciotto persone costruisce e gestisce entrambi. Il personale operativo del team spende gran parte del tempo in lavoro manuale: riavviare job bloccati, regolare i feed di dati e rispondere alle chiamate. Il responsabile del gruppo nota che hanno poco tempo per il miglioramento e due di loro hanno chiesto di passare ad altri team.

Il responsabile del team propone un approccio ispirato alla SRE. Per l'app di segnalazione dei guasti, il team fissa due indicatori: la quota di invii di segnalazioni che riescono e il tempo per mostrare una conferma. Concorda con il responsabile del servizio clienti un obiettivo largo e un error budget mensile e scrive una policy di una pagina: quando più dei tre quarti del budget sono spesi, i rilasci rischiosi aspettano. Il team chiede agli ingegneri di registrare il toil per un mese. Il registro mostra che un terzo del loro tempo va nel riavviare un job di importazione dati che fallisce e in aggiustamenti manuali dopo le tempeste, quando la domanda sale. Fissano un tetto della metà del loro tempo sul toil, decidono di correggere per prima la causa del job di importazione e di automatizzare gli aggiustamenti per le tempeste con uno script con limiti e un registro. Le chiamate sono regolate in modo che solo i sintomi visibili agli utenti avvisino l'ingegnere di turno.

Quattro mesi dopo, il toil scende a circa un terzo del tempo del team, il job di importazione non fallisce più e la policy sull'error budget è stata usata una volta, in un mese con un'interruzione di un fornitore, per rinviare il rilascio di una funzionalità. Restano difficoltà. Il sistema di invio non ha ancora obiettivi e il responsabile del servizio clienti è stato tentato due volte di derogare alla policy del budget per funzionalità urgenti. Il responsabile del team e il responsabile concordano di rivedere le deroghe ogni mese e di fissare per prossimo gli obiettivi per l'invio. Scoprono anche che il "tetto" è una guida, non una promessa: dopo una grande tempesta, il toil è salito ben oltre la metà per due settimane e devono decidere che cosa tagliare.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery partecipano a fissare gli obiettivi e rispettano il budget. Incorpora l'operabilità nelle funzionalità, accetta che il toil torni al team che lo causa e aiuta ad automatizzare. Tratta un budget esaurito come un'informazione sul servizio, non come una punizione.

### Team di servizio e di operations

I team operativi possono svolgere il lavoro SRE o adottarne le idee. Misura il toil, proteggi il tempo per l'ingegneria e rimanda il lavoro ripetuto alla sua fonte. Usa gli obiettivi per spiegare perché alcuni lavori andrebbero rifiutati.

### Leadership e governance

I leader devono sostenere il tetto al toil e la regola dell'error budget; senza sostegno falliscono. Chiedi obiettivi e stato del budget, non un conteggio di incidenti. Dai tempo al lavoro di ingegneria e sii pronto a dire no alle funzionalità quando il budget è esaurito.

### Clienti e utenti

Clienti e utenti traggono vantaggio da livelli di servizio chiari e da un ripristino più rapido quando le cose si guastano. Di' al team che cosa conta di più, così che gli obiettivi riflettano la tua esperienza. Aspettati conversazioni oneste sui compromessi tra nuove funzionalità e affidabilità.

## Modalità di fallimento comuni

- **Copiare il titolo.** Le operations sono rinominate e nulla cambia. Adotta invece prima obiettivi, budget e misure del toil.
- **Un error budget che nessuno rispetta.** Le funzionalità lo scavalcano sempre. Concorda invece la regola con i product owner e rivedi le deroghe.
- **Nessun tempo per l'ingegneria.** Il toil riempie la settimana. Fissa invece un tetto e proteggi il tempo di progetto.
- **Automatizzare la cosa sbagliata.** Si automatizza un compito raro mentre quello frequente resta. Ordina invece per tempo e frequenza.
- **Obiettivi di perfezione.** Gli obiettivi pretendono il 100 percento. Fissa invece obiettivi larghi dalle esigenze degli utenti e stringi con i dati.
- **Un team di affidabilità come discarica.** Lo sviluppo gli manda tutto il lavoro operativo. Rimanda invece il lavoro in eccesso alla sua fonte.
- **Copiare la scala di Google.** Pratiche che richiedono una grande organizzazione sono adottate da una piccola. Prendi invece le idee che si adattano, come obiettivi e post-mortem.
- **Ignorare le persone.** Il carico di reperibilità logora. Limita invece gli eventi per turno e condividi il turno.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Obiettivi e budget | Gli obiettivi di affidabilità sono informali | Alcuni servizi hanno obiettivi | I servizi chiave hanno obiettivi e una policy concordata sull'error budget | I budget guidano i rilasci e le deroghe alla policy sono riviste | Obiettivi e budget sono allineati tra servizi dipendenti |
| Toil e automazione | Il toil non è misurato | Alcuni team stimano il toil | Il toil è misurato e limitato; il lavoro di automazione è pianificato | Fonti e risparmi del toil sono monitorati e ridotti | L'automazione è condivisa e il toil è ridotto tra i team |
| Risposta alle emergenze | La risposta è improvvisata | Esistono alcuni playbook e un turno | Ruoli, playbook e post-mortem senza colpe sono standard | Carico di eventi e tempi di riparazione sono misurati e migliorati | La risposta è esercitata e coordinata tra team e fornitori |
| Cambiamento e capacità | Le modifiche sono rischiose e manuali | Alcuni rollout sono a stadi | Rollout progressivo e pianificazione della capacità sono routine | Fallimenti dei cambiamenti e previsioni di capacità sono misurati | Le pratiche di cambiamento e capacità sono condivise in tutta l'organizzazione |

## Checklist

- [ ] Almeno un servizio ha indicatori e un obiettivo largo, misurati nel tempo.
- [ ] Una policy sull'error budget è concordata con i product owner e scritta.
- [ ] Il toil è misurato con una definizione coerente e le fonti principali sono note.
- [ ] Esiste un massimale per il toil ed è rivisto.
- [ ] Il tempo per i progetti ingegneristici è pianificato e protetto.
- [ ] Il carico di reperibilità è misurato e le chiamate sono azionabili.
- [ ] Esistono playbook per i guasti più comuni e sono stati testati.
- [ ] I rollout sono progressivi e i rollback testati.
- [ ] Incidenti significativi e quasi-incidenti ricevono post-mortem senza colpe con azioni con responsabile.
- [ ] Abbiamo scelto di proposito come è organizzato il lavoro sull'affidabilità.

## Prompt per l'IA

**Scopo: classificare il tuo lavoro come toil, ingegneria o overhead.**

```text
Here is a list of what our operations engineers did in the last two weeks, with the time spent on each: [paste real data].

Classify each item as toil, engineering work, or overhead, using these definitions. Toil: manual, repetitive, automatable, tactical, without enduring value, and growing linearly with the service. Engineering work: novel, requires judgment, produces permanent improvement. Overhead: administrative work not tied to running a service. Give a one-sentence reason from my text for each. Compute the share of time in each class from my numbers only, and list the three largest toil items. Mark items you could not classify. Do not invent time figures. List what you are unsure of.
```

**Scopo: redigere una policy sull'error budget.**

```text
Draft a one-page error budget policy for [service].

Objective and period: [for example, "99.9% of purchase requests succeed, per month"].
Release rhythm and who decides: [describe].
Customer and product concerns: [list].

Write sections: how the budget is calculated and shown, what happens at three stages of consumption (leave thresholds as [to be agreed]), who can override and how overrides are recorded, how the policy is reviewed, and what we do after an exhausted budget. Do not invent numbers. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: scegliere una voce di toil da automatizzare per prima.**

```text
Here are our top toil items with how often each occurs, time per occurrence, risk if the automation fails, and whether the cause could be designed away: [paste].

Rank them by total time saved per month (computed from my numbers only). For the top three, say whether I should design the need away or automate it, and what safeguards the automation needs (tests, limits, logs). Do not invent numbers. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: scrivere una voce di playbook.**

```text
Write a playbook entry for this recurring failure: [describe symptom and impact].

What I know about causes and fixes: [paste].
Who to escalate to: [role, or "unknown"].

Provide a short entry: how to confirm the failure, the first checks, the usual fix, how to confirm recovery, when to escalate, and what to record. Mark any step you inferred with [CHECK]. Ask clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [on-call-rotation](../../../../skills/on-call-rotation/SKILL.md): da usare per progettare un turno equo con limiti agli eventi per turno.
- [runbook](../../../../skills/runbook/SKILL.md): da usare per scrivere i playbook che accelerano la riparazione.
- [postmortem](../../../../skills/postmortem/SKILL.md): da usare per condurre revisioni senza colpe e monitorare le azioni.
- [chaos-testing](../../../../skills/chaos-testing/SKILL.md): da usare per verificare che i progetti di affidabilità funzionino provocando guasti in sicurezza.
- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): da usare per pianificare la capacità come compito ingegneristico legato alla domanda.

## Fonti principali

- **Introduction** (*Site Reliability Engineering*, Google, sre.google): la definizione di SRE, il tetto del 50 percento, i principi e la divisione dev/ops che mira a evitare.
- **Eliminating Toil** (*Site Reliability Engineering*, Google, sre.google): la definizione di toil e le ragioni per limitarlo.
- **Embracing Risk** (*Site Reliability Engineering*, Google, sre.google): l'economia dell'affidabilità e l'error budget.
- **Site reliability engineering** (Wikipedia): un riassunto più ampio della disciplina, dei modelli di impiego, dell'indagine di adozione e di ulteriori letture.

## Riferimenti

1. Introduction — Google SRE book, sre.google — https://sre.google/sre-book/introduction/
2. Eliminating Toil — Google SRE book, sre.google — https://sre.google/sre-book/eliminating-toil/
3. Embracing Risk — Google SRE book, sre.google — https://sre.google/sre-book/embracing-risk/
4. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
5. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
6. Chaos engineering — Wikipedia — https://en.wikipedia.org/wiki/Chaos_engineering
7. Infrastructure as code — Wikipedia — https://en.wikipedia.org/wiki/Infrastructure_as_code
8. Observability (software) — Wikipedia — https://en.wikipedia.org/wiki/Observability_(software)
9. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
