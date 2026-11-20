# Responsabilità di prodotto e di servizio

**La responsabilità di prodotto e di servizio dà a ogni prodotto o servizio una persona responsabile e un team che lo costruisce e lo gestisce, così che le decisioni su valore, qualità e costo siano prese da chi vive con i risultati.**

## Perché è importante

In molte organizzazioni nessuno possiede un servizio nel suo insieme. Un progetto lo costruisce, un team operativo lo gestisce, un fornitore fornisce una parte e un reparto finanziario lo paga. Quando qualcosa va storto, ci sono quattro riunioni e nessuna decisione. Quando gli utenti vogliono un miglioramento, la richiesta va a una coda che non appartiene a nessuno. Il servizio si degrada tra i team.

La responsabilità affronta direttamente questo. Chiede due cose: una persona responsabile del valore del prodotto o servizio e un team che abbia le competenze e l'autorità per costruirlo, gestirlo e migliorarlo. L'idea è antica in certe forme e di moda in altre e i dettagli differiscono molto tra organizzazioni. Farla bene è una delle condizioni più importanti perché tutto il resto di questa guida funzioni.

Dietro l'argomento ci sono due idee. La prima è il Product Owner della Scrum Guide, che è responsabile di massimizzare il valore del prodotto e di ordinarne il backlog, ed è una persona e non un comitato (vedi Argomento 1.4 — Previsioni di consegna e metriche di pianificazione). La seconda è lo slogan "you build it, you run it", associato al direttore tecnologico di Amazon Werner Vogels in un'intervista pubblicata su ACM Queue nel 2006, che questa guida non ha potuto leggere direttamente (la pagina ha restituito un errore di accesso) e conosce da descrizioni secondarie. Come riferiscono quelle descrizioni, Vogels contrappose il vecchio modello, in cui gli sviluppatori gettano il software oltre un muro alle operations, a uno in cui gli sviluppatori restano a contatto quotidiano con la gestione del proprio software e con il cliente. L'[articolo di Wikipedia sulla gestione del prodotto](https://en.wikipedia.org/wiki/Product_management) dà una descrizione generale della disciplina ma non dice nulla sul ruolo agile di product owner o sulla responsabilità di servizio, quindi questo argomento fa il lavoro di collegamento e lo dice.

## Concetti fondamentali

### Prodotto, servizio, progetto

| Termine | Significato, nell'uso comune | Orizzonte temporale |
|---|---|---|
| **Progetto** | Uno sforzo temporaneo con ambito, inizio e fine definiti | Finisce quando l'ambito è consegnato |
| **Prodotto** | Qualcosa offerto a clienti o utenti che è sviluppato e migliorato nel tempo | Continua finché crea valore |
| **Servizio** | Un modo di fornire valore ad altri senza che ne possiedano costi e rischi (vedi Argomento 2.1 — Gestione dei servizi IT) | Continua finché è offerto |

Un prodotto digitale è spesso anche un servizio: gli utenti dipendono dal suo buon funzionamento. La distinzione tra prodotto e servizio conta meno del passaggio da progetto a responsabilità continuativa, come descrive l'Argomento 1.9 — Gestione agile.

### Gestione del prodotto

L'articolo di Wikipedia descrive la gestione del prodotto come il processo aziendale di pianificare, sviluppare, lanciare e gestire un prodotto o servizio, assicurando che i prodotti soddisfino i bisogni del mercato obiettivo e sostengano la strategia aziendale lungo il ciclo di vita del prodotto. Elenca le responsabilità dei product manager: gestire giorno per giorno la linea di prodotto, possedere il business case e la consegna al mercato, analizzare ricerche sui clienti e concorrenza, documentare i requisiti, fissare la strategia e creare la roadmap e allinearsi con progettazione, sviluppo, marketing, vendite, supporto e ufficio legale. Fa risalire il concetto a un memo del 1931 del presidente della Procter & Gamble Neil H. McElroy che chiedeva "Brand Men" per gestire i prodotti. Dice che i product manager sono spesso misurati su responsabilità di profitti e perdite.

L'articolo non collega la gestione del prodotto al Product Owner agile, quindi il collegamento è una lettura di questa guida: un Product Owner è responsabile del valore del prodotto e ne ordina il backlog, e in molte organizzazioni un product manager svolge il ruolo di business più ampio. Nei piccoli team una persona può fare entrambi.

### Il product owner e il service owner

| Ruolo | Responsabile di | Domande tipiche |
|---|---|---|
| **Product owner** (Scrum) | Massimizzare il valore del prodotto; ordinare il product backlog | Che cosa dovremmo costruire o migliorare dopo, e perché? |
| **Product manager** | Il business case, la strategia e la roadmap di un prodotto | È il prodotto giusto, per il mercato giusto? |
| **Service owner** (uso ITSM) | Le prestazioni e il miglioramento di un servizio nel corso della sua vita | Il servizio soddisfa le esigenze degli utenti, a un costo e rischio accettabili? |

I ruoli si sovrappongono. Per un servizio IT interno, una persona può essere product owner e service owner. La Scrum Guide sottolinea che il Product Owner è una persona, non un comitato, così che le decisioni sull'ordine abbiano un responsabile chiaro. Qualunque sia il titolo, il test è se una persona nominata può fare compromessi tra nuove funzionalità, affidabilità e costo.

### "You build it, you run it"

Come descritto nei riassunti secondari dell'intervista di Vogels del 2006, la frase esprime un modello in cui il team che costruisce un servizio lo gestisce anche, e quindi resta a contatto quotidiano con gli utenti e con le conseguenze della sua progettazione. L'intervista fu condotta da Jim Gray e pubblicata su ACM Queue nel 2006; il blog di Amazon stesso la segnalò quando uscì. Questa guida non ha letto l'originale, quindi non lo cita. Il modello ha costi oltre ai benefici:

| Beneficio | Costo o rischio |
|---|---|
| I costruttori sentono il dolore della scarsa operabilità e la correggono | I costruttori portano il carico di reperibilità e possono andare in burnout |
| Feedback più breve da utenti e incidenti | Le competenze di operations, sicurezza e conformità devono esistere nel team |
| Nessun passaggio di consegne in cui perdere conoscenza | Gli standard tra team richiedono altri meccanismi |
| Responsabilità chiara | I piccoli team possono trovare troppo pesante l'intero carico |

La site reliability engineering e DevOps offrono modi di sostenere tali team (vedi Argomento 5.2 — DevOps e Argomento 5.3 — Site reliability engineering). I team di piattaforma possono fornire strumenti comuni così che ogni team di prodotto non debba ricostruirli.

### Team che possiedono

La responsabilità richiede un team con le competenze per consegnare e gestire e l'autorità di agire. Scrum descrive un piccolo team cross-funzionale e auto-gestito che non dipende da altri per l'intero lavoro. Nella pratica, i team di prodotto dipendono anche da piattaforme condivise, sicurezza e servizi dati. Gestire queste dipendenze fa parte della responsabilità (vedi Argomento 1.8 — Scalare l'agile).

### Finanziamento e obiettivi

La responsabilità richiede finanziamenti stabili e obiettivi chiari. Un team finanziato progetto per progetto viene sciolto quando il progetto finisce, e un responsabile del servizio non ha un team. Un team stabile finanziato per un prodotto o servizio, con obiettivi che cambiano man mano che impara, è la risposta usuale (vedi Argomento 1.9 — Gestione agile). Gli obiettivi dovrebbero riguardare i risultati per utenti e business ed essere fissati con il responsabile.

### Responsabilità nella gestione dei servizi

Le pratiche ITIL richiedono responsabili: ogni servizio ha un responsabile, ogni pratica ha un responsabile e ogni processo importante ha un responsabile (vedi Argomento 5.1 — Gestione agile dei servizi). Il responsabile del servizio detiene il livello di servizio, la voce di catalogo, l'elenco dei miglioramenti e la relazione con i clienti (vedi Argomento 3.7 — Gestione dei livelli di servizio e Argomento 3.8 — Gestione del catalogo dei servizi).

### Limiti e cautele

Le fonti lette per questa guida non offrono prove su quanto bene funzionino i modelli di responsabilità, e l'articolo di Wikipedia sulla gestione del prodotto non elenca critiche. Le cautele pratiche offerte dall'esperienza includono responsabili con il titolo ma senza autorità, responsabili sovraccarichi di più prodotti, "you build it, you run it" senza sostegno che porta a esaurimento e responsabilità che si ferma al confine del team mentre il flusso di valore lo attraversa (vedi Argomento 5.4 — Gestione del flusso di valore).

## Buone pratiche

1. **Nomina una persona responsabile per ogni prodotto o servizio.** Scrivi il nome nel catalogo dei servizi. Assicurati che abbia autorità sulle priorità e voce sul finanziamento.
2. **Definisci che cosa decide il responsabile.** Indica quali decisioni il responsabile prende da solo, quali con il team e quali richiedono escalation. Senza questo, la responsabilità è un titolo.
3. **Dai tempo al responsabile.** Non fare responsabili di più grandi prodotti, né responsabili con anche un lavoro di delivery a tempo pieno. La responsabilità è lavoro vero.
4. **Finanzia il team per la vita del servizio.** Evita di sciogliere i team quando i progetti finiscono. Rivedi il finanziamento con un ciclo regolare rispetto ai risultati.
5. **Fissa gli obiettivi di risultato con il responsabile.** Descrivi che cosa dovrebbe essere migliore per utenti e business, con poche misure che il team può produrre da solo (vedi Argomento 5.6 — Metriche e misurazione).
6. **Metti costruzione e gestione in un unico team dove puoi.** Includi le competenze di sviluppo, operations e supporto e dai al team accesso ai dati e agli strumenti di produzione entro limiti sicuri. Dove non puoi, crea forti accordi di lavoro.
7. **Sostieni il team con una piattaforma.** Fornisci strumenti condivisi per deployment, monitoraggio e sicurezza così che ogni team non costruisca i propri. Tratta la piattaforma come un prodotto con utenti.
8. **Condividi equamente il carico di reperibilità.** Limita le chiamate notturne, regola gli allarmi e osserva il burnout. "You build it, you run it" fallisce quando chi lo gestisce è esausto.
9. **Tieni un backlog per prodotto.** Includi funzionalità, difetti, lavoro operativo e voci di miglioramento in un unico elenco ordinato, così che il responsabile possa confrontarli.
10. **Collega i responsabili tra loro.** Tieni conversazioni regolari tra i responsabili di prodotti e servizi dipendenti, per risolvere conflitti e allineare i piani.
11. **Rivedi la responsabilità ogni anno.** Verifica che ogni servizio abbia ancora un responsabile attivo, un team e un backlog e che i ruoli siano ancora adatti.
12. **Prevedi i piccoli team.** Dove un team possiede molti piccoli servizi, raggruppali in modo sensato e usa pratiche leggere. Non applicare un modello pesante a un piccolo servizio.

## Domande da discutere con il team

**Chi è responsabile di ciascuno dei nostri servizi, e lo direbbe?**

Elenca i servizi principali e nomina il responsabile. Poi chiedi a ogni persona nominata se si definirebbe responsabile. I divari tra l'elenco e le risposte rivelano quanto la responsabilità sia nominale. Chi facilita può chiedere quale servizio non ha responsabile e che cosa è costato.

**Che cosa può decidere oggi il nostro responsabile senza chiedere a nessuno?**

Chiedi esempi: priorità, spesa, un rilascio, un impegno con un cliente. Se la maggior parte delle decisioni richiede l'approvazione di altri, discuti quali dovrebbero essere delegate e con quali limiti. Concorda una decisione da spostare.

**Quando qualcosa va storto in produzione, chi viene svegliato, e ha i mezzi per correggerlo?**

Chiedi chi è di turno e che cosa può cambiare. Se non sono i costruttori, chiedi perché. Discuti come il feedback dagli incidenti raggiunge chi progetta il servizio. Concorda una via da accorciare.

**Come finanziamo questo servizio, e che cosa succede quando un progetto finisce?**

Ripercorri il finanziamento di un servizio principale. Chiedi chi può spendere in miglioramenti e chi decide di fermarsi. Se il team viene sciolto dopo un progetto, discuti il costo della conoscenza perduta. Proponi una sperimentazione di finanziamento stabile per un servizio.

**Quali competenze ci mancano per costruire e gestire il nostro servizio, e come potremmo averle?**

Elenca le competenze di cui il lavoro ha bisogno: sviluppo, operations, sicurezza, dati, supporto. Segna le lacune. Discuti coppia, formazione, prendere in prestito uno specialista o una piattaforma condivisa. Scegli una lacuna da colmare.

**Quanti responsabili stiamo chiedendo a una persona di essere?**

Conta i prodotti e i servizi di cui ciascun responsabile risponde. I responsabili sovraccarichi non possono prendere buone decisioni. Discuti se dividere, delegare o ritirare servizi. Concorda un massimo e un piano per un responsabile che lo supera.

## Nella pratica: un esempio di ITIL agile

Un'agenzia nazionale per l'impiego gestisce un servizio online di incontro tra domanda e offerta di lavoro usato da chi cerca lavoro e da datori di lavoro. Il servizio fu costruito da un team di progetto, consegnato a un gruppo operativo ed è ora finanziato come una serie di piccoli progetti. Il responsabile dei servizi digitali scopre che nessuno sa dire chi lo possiede: lo sponsor originale del progetto è andato in pensione, le operations gestiscono gli incidenti e un'unità di politiche chiede modifiche attraverso una coda che richiede mesi. I datori di lavoro si lamentano di un modulo di registrazione che non cambia da tre anni.

Il responsabile nomina una responsabile del servizio dall'unità di relazioni con i datori di lavoro, una persona che capisce sia i datori di lavoro sia il servizio, e le dà voce sul backlog e una quota del budget. Un team stabile di otto persone, che combina sviluppatori, un ingegnere delle operations, un tester e un designer, è formato dalle persone che già lavoravano sul servizio. Il team entra nel turno di reperibilità, con un limite alle chiamate notturne, e usa una piattaforma condivisa per deployment e monitoraggio mantenuta da un team centrale. Le richieste dell'unità di politiche vanno nell'unico backlog, dove la responsabile le ordina rispetto a miglioramenti e correzioni. Il team e la responsabile concordano tre obiettivi di risultato per l'anno con poche misure: la quota di registrazioni dei datori di lavoro completate, il tempo che chi cerca lavoro impiega a trovare una corrispondenza e il numero di incidenti ripetuti.

Dopo otto mesi, il modulo di registrazione è ricostruito, il completamento migliora e gli incidenti ripetuti calano. La responsabile può rispondere alle domande dei datori di lavoro su che cosa è pianificato. Restano alcune difficoltà. La responsabile risponde anche di un altro piccolo servizio ed è sotto pressione, l'unità di politiche si risente di dover competere per le posizioni nel backlog e gli ingegneri di turno dicono che alla piattaforma condivisa manca uno strumento di cui hanno bisogno. Il responsabile dei servizi digitali riduce gli altri compiti della responsabile, chiede all'unità di politiche e alla responsabile di organizzare una riunione mensile di pianificazione e mette la richiesta di piattaforma nel backlog del team centrale.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery dovrebbero lavorare con un responsabile chiaro e farsi carico della gestione di ciò che costruiscono. Offri al responsabile prove da utenti, incidenti e costi e sii onesto sui compromessi. Chiedi gli strumenti e il sostegno di cui hai bisogno per portare equamente la reperibilità.

### Team di servizio e di operations

I team operativi sostengono i team di prodotto con competenza, piattaforme e standard condivisi. Dove gestiscono servizi per altri, nomina responsabili e concorda livelli di servizio. Resisti a passare ogni problema operativo a un gruppo centrale che non possiede nulla.

### Leadership e governance

I leader creano la responsabilità nominando responsabili, dando loro autorità e tempo e finanziando team stabili. Chiedi risultati e prove ai responsabili ed evita di scavalcarne le priorità senza discussione. Fai attenzione ai responsabili che hanno il titolo ma non il potere.

### Clienti e utenti

Clienti e utenti traggono vantaggio quando sanno chi risponde di un servizio e possono raggiungerlo. Di' al responsabile che cosa conta di più e che cosa fa male. Aspettati informazioni chiare su che cosa è pianificato e voce in capitolo su come sono fissate le priorità.

## Modalità di fallimento comuni

- **Titolo senza autorità.** Un responsabile non può decidere nulla. Indica invece che cosa decide il responsabile e sostienilo.
- **Responsabilità a comitato.** Nessuno è responsabile. Nomina invece una persona per ogni prodotto o servizio.
- **Responsabili sovraccarichi.** Una persona possiede troppi prodotti. Limita invece il numero e delega.
- **Sciogliere i team dopo i progetti.** La conoscenza se ne va. Finanzia invece team stabili per i servizi che continuano.
- **"You build it, you run it" senza sostegno.** I team vanno in burnout. Fornisci invece una piattaforma, reperibilità condivisa e allarmi regolati.
- **Responsabilità che si ferma al team.** Il flusso di valore attraversa i team. Collega invece i responsabili dei servizi dipendenti.
- **Più backlog.** Funzionalità, difetti e operations competono in code nascoste. Tieni invece un unico backlog ordinato per prodotto.
- **Copiare un modello senza contesto.** Uno schema da grande azienda è applicato a un piccolo servizio. Adatta invece il modello a dimensione e rischio.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Responsabilità | I servizi non hanno un responsabile chiaro | Alcuni servizi hanno responsabili informali | Ogni servizio ha un responsabile nominato con diritti decisionali e tempo definiti | Efficacia e risultati dei responsabili sono rivisti | I responsabili si coordinano tra servizi dipendenti e con i clienti |
| Team e competenze | Costruzione e gestione sono team separati | Alcuni team condividono la reperibilità | Team stabili possiedono costruzione e gestione con le competenze necessarie | Lacune di competenze e carico sono misurati e affrontati | Competenze e piattaforme sono condivise tra team e fornitori |
| Finanziamento e obiettivi | Il finanziamento è per progetto | Esistono alcuni team stabili | I servizi hanno finanziamento stabile e obiettivi di risultato | Il finanziamento segue i risultati misurati | Finanziamento e obiettivi sono allineati tra servizi e con i clienti |
| Backlog e priorità | Le priorità vengono da molte code | Alcuni responsabili tengono un elenco | Un backlog ordinato per prodotto include tutti i tipi di lavoro | Flusso del backlog e priorità sono rivisti con gli stakeholder | Le priorità sono allineate tra responsabili e con i clienti |

## Checklist

- [ ] Ogni prodotto o servizio ha un responsabile nominato, indicato nel catalogo dei servizi.
- [ ] Che cosa ogni responsabile decide da solo, con il team e per escalation è scritto.
- [ ] I responsabili hanno tempo per il ruolo e un numero gestibile di servizi.
- [ ] Un team stabile è finanziato per ogni servizio continuativo.
- [ ] Ogni servizio ha obiettivi di risultato con poche misure.
- [ ] Il team che costruisce un servizio ha le competenze e l'accesso per gestirlo, o ha chiari accordi di lavoro con chi lo fa.
- [ ] Il carico di reperibilità è condiviso equamente con limiti e allarmi regolati.
- [ ] Una piattaforma condivisa sostiene i team con deployment, monitoraggio e sicurezza.
- [ ] Ogni prodotto ha un backlog ordinato che copre funzionalità, difetti, operations e miglioramento.
- [ ] La responsabilità è rivista almeno una volta l'anno.

## Prompt per l'IA

**Scopo: redigere i diritti decisionali per il responsabile di un prodotto o servizio.**

```text
Help me draft decision rights for the owner of [product or service].

What the service does and who uses it: [describe].
Decisions that come up often: [list 8-12, such as priorities, spending, releases, customer commitments, supplier choices].
Rules we must follow (financial, security, legal), with source text if you have it: [paste, or write "none known"].
Current arrangement: [describe].

Produce a table with three columns: owner decides alone, owner decides with the team, and escalate. Place each decision in one column with a one-sentence reason. Mark any placement that is a guess. Do not invent rules. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: trovare i servizi senza un responsabile chiaro.**

```text
Here is a list of our services with the owner we have recorded, the team that builds, the team that runs, and who funds each: [paste].

Using only this list, identify services with no owner, with different people named as owner by different columns, or with build and run split between teams. For each, suggest a question to ask. Do not decide who should own anything. List what you are unsure of.
```

**Scopo: pianificare un modello di reperibilità per un team che costruisce e gestisce.**

```text
Help me plan an on-call model for a team of [number] people who build and run [service].

Current incidents and pages (counts by week, out-of-hours share): [paste real data].
Skills in the team: [list].
Constraints: [for example time zones, leave rules].

Propose a rota design, limits on night calls, how alerts will be tuned, what support the team needs from a platform or operations group, and what to review each quarter. Leave numeric limits as [to be agreed]. Do not invent data. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: preparare le ragioni per un finanziamento stabile di un servizio.**

```text
Help me prepare a short case for funding [service] with a standing team instead of by project.

How it is funded today and what happens at the end of each project: [describe].
Costs of the current arrangement, in facts (rework, lost knowledge, delays; use only real examples): [paste].
What a standing team would need: [describe roles and rough size].
Outcome goals proposed: [list].

Write a one-page case with the problem, the proposal, risks (including the risk of a standing team becoming complacent), what we will measure, and how funding would be reviewed. Do not invent figures. Ask clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): da usare per chiarire chi possiede, supporta ed è consultato per ogni prodotto o servizio.
- [product-roadmap](../../../../skills/product-roadmap/SKILL.md): da usare per descrivere direzione e piani a breve termine di un prodotto o servizio.
- [agile-charter](../../../../skills/agile-charter/SKILL.md): da usare per fissare all'inizio scopo, risultati e limiti di un team.
- [feature-prioritization](../../../../skills/feature-prioritization/SKILL.md): da usare per aiutare un responsabile a ordinare il backlog per valore e costo.
- [agile-discovery](../../../../skills/agile-discovery/SKILL.md): da usare per convalidare che cosa un prodotto o servizio dovrebbe fare dopo prima di costruirlo.

## Fonti principali

- **The Scrum Guide** (Ken Schwaber e Jeff Sutherland, scrumguides.org): la definizione della responsabilità del Product Owner e del team cross-funzionale e auto-gestito.
- **Product management** (Wikipedia): una descrizione generale della disciplina, delle sue responsabilità e della sua storia.
- **A Conversation with Werner Vogels** (Jim Gray, ACM Queue, 2006): l'intervista in cui è descritto "you build it, you run it"; leggi l'originale per la formulazione esatta.
- **Site Reliability Engineering** (Google, sre.google): un modo di sostenere i team che gestiscono ciò che costruiscono.

## Riferimenti

1. The Scrum Guide (November 2020) — Ken Schwaber and Jeff Sutherland, scrumguides.org — https://scrumguides.org/scrum-guide.html
2. Product management — Wikipedia — https://en.wikipedia.org/wiki/Product_management
3. ACM Queue interview with Werner Vogels (2006), noted on the AWS News Blog — Amazon Web Services — https://aws.amazon.com/blogs/aws/acm_queue_inter/
4. Introduction — Google SRE book, sre.google — https://sre.google/sre-book/introduction/
5. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
6. Scrum (software development) — Wikipedia — https://en.wikipedia.org/wiki/Scrum_(software_development)
7. Project management — Wikipedia — https://en.wikipedia.org/wiki/Project_management
8. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
9. Platform engineering — Wikipedia — https://en.wikipedia.org/wiki/Platform_engineering
