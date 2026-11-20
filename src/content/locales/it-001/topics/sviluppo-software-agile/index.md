# Sviluppo software agile

**Lo sviluppo software agile è una famiglia di metodi per la consegna continua di software che consegnano a piccoli passi e imparano dal feedback, e le pratiche che ha prodotto, come i test automatizzati e l'integrazione continua, sono il fondamento pratico per gestire in sicurezza servizi in continuo cambiamento.**

## Perché è importante

La maggior parte dei team che gestiscono un servizio IT lo costruisce e lo modifica anche. Il modo in cui il software viene costruito decide quanto spesso il servizio cambia, quanto è rischiosa ogni modifica e quanto le persone di turno possono fidarsi di ciò che ricevono. Un team che costruisce in grandi lotti e passa le consegne di rado darà alle operations pochi rilasci grandi e spaventosi. Un team che costruisce a piccoli passi, con test e feedback rapido, può darne molti piccoli e comprensibili.

Lo sviluppo software agile è l'insieme di idee più noto per il secondo modo di lavorare. È anche molto frainteso. Alcuni usano "agile" per dire "niente piani e niente documenti", altri per qualsiasi processo con una riunione quotidiana. Questo argomento offre un quadro più chiaro: da dove vengono i metodi agili, che cosa hanno in comune, che cosa non affermano e quali pratiche contano di più per un team che deve mantenere in funzione un servizio.

Le prove richiedono una lettura attenta. L'[articolo di Wikipedia sullo sviluppo software agile](https://en.wikipedia.org/wiki/Agile_software_development) dice che le prove aneddotiche a favore dell'agile sono forti, ma quelle empiriche sono "limitate e meno che conclusive", e rimanda a indagini, come la State of Agile survey annuale, che riportano benefici ma provengono da opinioni dichiarate dagli stessi interessati. Considera i metodi agili come approcci promettenti da mettere alla prova nel tuo contesto.

## Concetti fondamentali

### Che cosa copre il termine

"Sviluppo software agile" è un termine ombrello. L'articolo di Wikipedia lo descrive come l'insieme di approcci nati dai valori e dai principi concordati nel 2001 da 17 professionisti (vedi Argomento 1.1 — Il Manifesto Agile e Argomento 1.2 — I principi agili). "Agile" con la maiuscola è spesso usato per le pratiche nate da quella mentalità, e "agile" in minuscolo per la qualità di saper adattarsi. La distinzione non è rigida, e sentirai usare entrambi.

I metodi agili puntano alla consegna continua di software. Si basano sulla collaborazione continua tra stakeholder e sviluppatori, costruiscono i progetti attorno a individui motivati e perseguono il miglioramento continuo tramite il feedback, con attenzione alla qualità. Differiscono per ciò che enfatizzano. Alcuni, come Extreme Programming, si concentrano sulle pratiche ingegneristiche, altri, come Scrum e Kanban, su come si gestisce il lavoro.

### Una breve storia

L'articolo di Wikipedia fa risalire lo sviluppo iterativo e incrementale al 1957, con la gestione evolutiva dei progetti e lo sviluppo software adattivo che compaiono nei primi anni Settanta. Negli anni Novanta comparve un gruppo di metodi leggeri in reazione ai processi pesanti e guidati dal piano, spesso chiamati [modello a cascata](https://en.wikipedia.org/wiki/Waterfall_model). L'articolo elenca il rapid application development (1991), lo unified process e il dynamic systems development method, DSDM (1994), Scrum (1995), Crystal Clear ed Extreme Programming (1996) e il feature-driven development (1997).

Nel febbraio 2001 diciassette professionisti si incontrarono a Snowbird, nello Utah, e scrissero il Manifesto. Dichiarazioni successive vi si sono basate: la PM Declaration of Interdependence nel 2005, il Software Craftsmanship Manifesto nel 2009 e la *Guide to Agile Practices* dell'Agile Alliance nel 2011, rinominata *Agile Glossary* nel 2016.

### Approcci adattivi e predittivi

L'articolo descrive un continuum tra approcci predittivi e adattivi. Un metodo predittivo pianifica nel dettaglio la maggior parte del lavoro prima di iniziare e funziona bene quando i requisiti sono stabili e ben compresi. Un metodo adattivo si aspetta il cambiamento e pianifica su orizzonti brevi. Boehm e Turner, citati nell'articolo, sostengono che ciascun lato ha il proprio "terreno di casa", cioè che nessuno dei due è giusto ovunque.

Questo conta per un team di servizio perché il suo lavoro è misto. Sostituire la rete di un data center è più vicino al lavoro predittivo. Migliorare un'app rivolta ai clienti è più vicino al lavoro adattivo. Scegli l'approccio per tipo di lavoro, non una volta per tutta l'organizzazione.

### Metodi comuni

L'articolo elenca molti metodi. Quelli che più probabilmente incontrerai:

| Metodo | Enfasi principale | Trattato in |
|---|---|---|
| Scrum | Ruoli definiti, eventi regolari e una cadenza fissa | Argomento 1.4 — Previsioni di consegna e metriche di pianificazione |
| Kanban | Visualizzare il lavoro e limitare quanto è in corso | Argomento 1.5 — Kanban |
| Extreme Programming (XP) | Pratiche ingegneristiche come la programmazione in coppia e il test-driven development | Argomento 1.6 — Extreme Programming |
| Sviluppo software lean | Applicare idee lean, come eliminare gli sprechi, al software | Argomento 1.7 — Sviluppo software lean |
| Feature-driven development, DSDM, Crystal e sviluppo software adattivo | Altri metodi leggeri di consegna continua di software con ruoli e pratiche propri | Questo argomento |
| Scrumban | Un misto di eventi Scrum e flusso Kanban | Argomento 1.4 — Previsioni di consegna e metriche di pianificazione e Argomento 1.5 — Kanban |

Nessun metodo è "il" metodo agile. L'articolo cita l'opinione di Ken Schwaber secondo cui i team si mettono nei guai cercando una metodologia perfetta quando è l'impresa stessa a dover cambiare, e il suggerimento di Bas Vodde che Scrum fornisca le basi che i team estendono localmente.

### Pratiche comuni

L'articolo elenca pratiche che molti team agili usano. Una selezione, con la loro finalità:

- **User story e backlog:** descrivono il lavoro dal punto di vista dell'utente e mantengono un elenco prioritizzato di che cosa fare dopo.
- **Stand-up quotidiano:** una breve riunione quotidiana, spesso di circa 15 minuti, per condividere progressi e ostacoli.
- **Test-driven development (TDD) e acceptance test-driven development (ATDD):** scrivere prima i test, così che "fatto" sia definito prima che il lavoro inizi.
- **Integrazione continua (CI):** integrare spesso le modifiche e compilarle e testarle automaticamente. L'articolo nota che Grady Booch propose il termine per la prima volta nel 1991.
- **Programmazione in coppia e refactoring:** due persone condividono il lavoro per migliorare la qualità e diffondere la conoscenza, e il codice viene migliorato continuamente senza cambiare ciò che fa.
- **Retrospettive:** il team riflette a intervalli regolari su come migliorare.

Per un team di servizio, tre di queste meritano attenzione speciale. I test automatizzati e l'integrazione continua rendono sicuro il cambiamento frequente. Le retrospettive offrono un luogo stabile per migliorare il modo di lavorare del team. I backlog danno un unico elenco ordinato in cui i miglioramenti del servizio competono equamente con le nuove funzionalità.

### Esperienza, misurazione e insidie

L'articolo riferisce che le indagini, tra cui una della Shine Technologies nel 2002–2003 e la State of Agile survey dal 2006, rilevano miglioramenti percepiti in qualità, produttività e soddisfazione del business. Nota anche che un'indagine di VersionOne ha trovato la formazione insufficiente come causa più citata delle implementazioni fallite, ed elenca insidie come affidare il ruolo di product owner a un membro del team di sviluppo e la mancanza di sostegno da parte degli sponsor.

Misurare "quanto è agile" un team ha prodotto diverse autovalutazioni, come il Nokia test, e un indice che valuta i progetti per durata, rischio, novità, impegno e interazione. Fai attenzione a qualsiasi punteggio di questo tipo. Un numero è uno spunto di conversazione, e un team che ottimizza per il punteggio può perdere il senso.

### Lavoro su larga scala, distribuito e regolamentato

L'articolo dice che scalare oltre una ventina di sviluppatori, o su più sedi, porta difficoltà, e che sono stati proposti diversi framework, anche se i pareri divergono su quanto funzionino (vedi Argomento 1.8 — Scalare l'agile). Riferisce inoltre che ambiti regolamentati come dispositivi medici, farmaceutica, finanza, nucleare, automotive e avionica furono dapprima ritenuti inadatti all'agile, e che oggi esistono adattamenti. Le preoccupazioni che elenca sono assicurazione della qualità, sicurezza (safety e security), tracciabilità, verifica e validazione.

Sono esattamente le preoccupazioni della gestione dei servizi. Quando un'autorità di vigilanza o un auditor chiede prove, un team agile può fornirle dagli strumenti che già usa, come la cronologia del controllo di versione, i risultati dei test automatici e i record dei cambiamenti (vedi Argomento 5.7 — Governance, rischio e conformità).

### Critiche da conoscere

Steven Rakitin, in una lettera a *IEEE Computer* nel 2001, definì l'agile "l'ennesimo tentativo di minare la disciplina dell'ingegneria del software" e lesse la preferenza del Manifesto per il software funzionante come una licenza a saltare la documentazione. I sostenitori rispondono che la documentazione dovrebbe essere "appena abbastanza buona", nelle parole di Scott Ambler. I team di servizio conoscono entrambi i lati: troppo poca documentazione rallenta i passaggi di consegne e la risposta agli incidenti, e troppa diventa obsoleta.

## Buone pratiche

1. **Abbina il metodo al tipo di lavoro.** Usa la consegna continua di software e il feedback frequente dove i requisiti cambiano, e usa più pianificazione anticipata dove sono fissi e il costo dell'errore è alto. Decidilo per ogni tipo di lavoro e rivedilo quando le circostanze cambiano.
2. **Parti dal lotto utile più piccolo.** Suddividi il lavoro in pezzi che possano essere costruiti, testati e rilasciati in giorni. Lotti piccoli danno feedback più rapido e rendono più facile capire e annullare una modifica fallita.
3. **Automatizza i test prima di accelerare i rilasci.** Rilasci frequenti senza test automatici spostano il rischio sugli utenti. Costruisci una suite che giri a ogni modifica e fallisca in modo rumoroso, e tratta una build rotta come la prima priorità del team.
4. **Integra in continuazione.** Porta spesso il lavoro su un ramo condiviso e compilalo automaticamente. I rami di lunga durata nascondono i conflitti finché non diventano costosi da risolvere.
5. **Fai in modo che "fatto" includa le operations.** Una story non è finita finché non può essere monitorata, supportata e annullata. Aggiungi questi controlli alla tua definition of done e chiedi al personale operativo di aiutarti a scriverla (vedi Argomento 3.5 — Gestione di rilasci e deployment).
6. **Mantieni un backlog ordinato per team.** Metti funzionalità, difetti e miglioramenti del servizio nello stesso elenco prioritizzato perché competano apertamente. Le code laterali nascoste sono il luogo in cui il lavoro operativo muore silenziosamente di fame.
7. **Scrivi documentazione appena sufficiente.** Conserva i documenti che le persone usano, come runbook, descrizioni dei servizi e note di architettura, e dai a ciascuno un responsabile e una data di revisione. Elimina il resto. Questo risponde alla preoccupazione di Rakitin senza tornare ai documenti pesanti.
8. **Tieni retrospettive regolari e agisci di conseguenza.** Scegli un cambiamento da ciascuna, con un responsabile e una data. Una retrospettiva che produce solo discussione diventa un rituale.
9. **Investi in formazione e sponsorizzazione.** Le prove delle indagini nell'articolo di Wikipedia indicano formazione e sostegno degli sponsor come punti deboli comuni. Pianifica entrambi prima di chiedere ai team di cambiare il modo di lavorare.
10. **Adatta, e spiega perché.** Adatta un metodo al tuo contesto e annota che cosa hai cambiato e la ragione. Cambiare una pratica perché è scomoda, senza una ragione, è il modo in cui i team si allontanano dai benefici.
11. **Misura i risultati, non i punteggi di agilità.** Segui cose come il lead time di una modifica, quanto spesso i rilasci causano incidenti e quanto velocemente il servizio viene ripristinato (vedi Argomento 5.6 — Metriche e misurazione). Usa le autovalutazioni solo come spunti di discussione.
12. **Riporta i dati del servizio nello sviluppo.** Alimenta il backlog con gli incidenti ricorrenti e i record dei problemi, così che lo sviluppo impari dalle operations (vedi Argomento 3.3 — Gestione dei problemi).

## Domande da discutere con il team

**Quali pratiche agili usiamo davvero, e di quali abbiamo solo il nome?**

Elenca le pratiche che pensi di seguire: stand-up, retrospettive, backlog, test automatici. Per ciascuna, chiedi l'ultima volta in cui ha cambiato una decisione. Le pratiche che nessuno riesce a collegare a una decisione sono rituali. Chi facilita dovrebbe chiedere prove senza insinuare colpe. Prosegui scegliendo un rituale da migliorare o abbandonare.

**Per quale parte del nostro lavoro sarebbe più saggio un approccio più predittivo, e perché?**

L'articolo di Wikipedia riferisce che ciascun approccio ha un "terreno di casa". Chiedi alle persone di ordinare il lavoro recente in stabile e in rapido cambiamento. Il lavoro tipicamente stabile include rinnovi hardware, trasferimenti di data center e grandi rinnovi di contratto. Chiedi che cosa un piano più accurato avrebbe procurato in ciascun caso. Lo scopo è evitare di applicare un unico stile a tutto.

**Con quanta rapidità scopriamo che qualcosa che abbiamo costruito non funziona, e che cosa lo renderebbe più veloce?**

Ripercorri il cammino dalla scrittura di una modifica alla scoperta di come si comporta in uso. Conta le fasi e le attese: revisione, build, test, rilascio, monitoraggio. Chiedi di quale fase il team si fida meno. Spesso la risposta è un test manuale o un passaggio di rilascio che dipende da una sola persona. Scegli una fase da accorciare e concorda come saprai che si è accorciata.

**Che cosa avrebbe bisogno di vedere da noi un auditor o un'autorità di vigilanza, e il nostro modo di lavorare lo produce già?**

Chiedi a una persona con esperienza di audit o sicurezza di partecipare. Raccogli le prove che i tuoi strumenti già producono: cronologia delle modifiche, risultati dei test, approvazioni. Poi elenca ciò che manca. I team sono spesso sorpresi di scoprire che modifiche piccole e frequenti con controlli automatici producono prove migliori di modifiche grandi e rare. Registra le lacune per la discussione sulla governance nell'Argomento 5.7 — Governance, rischio e conformità.

**Dove la nostra documentazione aiuta le persone, e dove esiste solo perché ci è stato detto di scriverla?**

Chiedi alle persone quali documenti hanno usato nell'ultimo mese. Un runbook usato e mantenuto aggiornato conta. Un documento di progettazione che nessuno ha letto dal giorno in cui è stato approvato no. Fai decidere al team quali tenere, quali fondere e quali eliminare, e assegna i responsabili. È un modo sicuro di applicare l'idea di "appena abbastanza buona".

**Che cosa abbiamo cambiato per ultimo nel nostro modo di lavorare in base a ciò che abbiamo imparato, e qual è il prossimo cambiamento?**

Chiedi l'ultimo cambiamento concreto uscito da una retrospettiva e se ha funzionato. Se nessuno ne sa nominare uno, la retrospettiva non svolge il suo compito. Cerca il perché: le azioni possono essere troppo grandi, senza responsabili o in competizione con il lavoro di consegna. Concludi scegliendo un piccolo cambiamento da fare nelle prossime due settimane.

## Nella pratica: un esempio di ITIL agile

Un rivenditore online di medie dimensioni ha un team di sviluppo di dieci persone che costruisce il suo sistema di gestione degli ordini e un team operativo separato di sei che lo gestisce. Il team di sviluppo ha scelto di usare sprint e rilasci ogni due settimane. Il team operativo riceve ogni rilascio con una breve nota e la richiesta di installarlo in una finestra del giovedì sera. Il personale operativo si lamenta di venire a sapere che cosa è cambiato solo quando qualcosa si rompe, e gli sviluppatori si lamentano che una finestra del giovedì è troppo tardi per correggere ciò che emerge dai test.

In una retrospettiva congiunta, i due team ripercorrono passo per passo un rilascio recente. Scoprono che gli unici test automatici coprono circa metà del flusso degli ordini, che nessuno sul lato operativo ha visto il rilascio prima della nota del giovedì e che il passaggio di rollback non è mai stato provato. Concordano tre cambiamenti. Il team di sviluppo aggiungerà un controllo di monitoraggio e un test di rollback alla propria definition of done. Un ingegnere operativo parteciperà a ogni sprint review. I rilasci che superano l'intera suite automatica saranno installati appena pronti, non solo il giovedì.

Nei due mesi successivi, due dei quattro rilasci seguenti vengono installati a metà settimana. L'ingegnere operativo individua in una sprint review un messaggio di log mancante, il che fa risparmiare un'ora di ricerca in un incidente successivo. Non tutto migliora: la suite automatica salta ancora il percorso dei rimborsi, e un difetto nei rimborsi raggiunge i clienti. I team aggiungono test sui rimborsi allo sprint successivo e concordano di rivedere ogni mese le lacune di copertura. L'ingegnere operativo dice anche che partecipare alla sprint review richiede un tempo che il turno non prevede, quindi il responsabile delle operations sposta alcune altre mansioni di quell'ingegnere.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery possiedono le pratiche che rendono sicuro il cambiamento: test, integrazione continua, lotti piccoli e una chiara definition of done. Tratta le operations come un cliente del tuo lavoro. Chiedi di che cosa hanno bisogno per gestire un rilascio e inseriscilo nel backlog come faresti con una funzionalità.

### Team di servizio e di operations

Il personale operativo può usare le pratiche agili sul proprio lavoro: un backlog visibile di miglioramenti, cicli di feedback brevi sugli incidenti e retrospettive regolari. Chiedi di partecipare presto alle sessioni di pianificazione e di revisione. Porta la conoscenza di come i servizi falliscono, che è il contributo più utile che un team di delivery possa ricevere.

### Leadership e governance

I leader decidono se i team ottengono il tempo e la formazione per lavorare in questo modo. Le prove delle indagini nell'articolo di Wikipedia indicano formazione e sponsorizzazione come punti deboli comuni. Chiedi di quali controlli hai bisogno e come un team può soddisfarli con i propri strumenti, invece di aggiungere un processo parallelo.

### Clienti e utenti

I clienti vedono il beneficio dei metodi agili come un miglioramento visibile a ritmo costante, non come una cerimonia. Aspettati di rivedere regolarmente modifiche funzionanti e che ti venga chiesto che cosa conta di più. In cambio, il team ha bisogno di risposte tempestive e della disponibilità ad accettare rilasci piccoli e imperfetti che migliorano nel tempo.

## Modalità di fallimento comuni

- **Adottare i rituali senza le pratiche ingegneristiche.** Compaiono riunioni quotidiane e lavagne, ma non ci sono test automatici, quindi i rilasci restano rischiosi. Investi invece in test, integrazione e automazione dei rilasci insieme alle cerimonie.
- **Chiamare "agile" un processo di cambiamento senza cambiare i diritti decisionali.** I team aspettano ancora approvazioni lontane. Sposta invece le decisioni verso le persone che hanno la conoscenza e fissa limiti chiari.
- **Usare l'agile come scusa per non documentare.** I passaggi di consegne e gli incidenti ne soffrono. Mantieni invece i documenti brevi che le persone usano e dai a ciascuno un responsabile.
- **Saltare la formazione.** Il risultato di VersionOne nell'articolo di Wikipedia indica la formazione insufficiente come causa più citata delle implementazioni fallite. Forma invece team e leader prima e durante il cambiamento.
- **Mettere un membro del team di sviluppo nel ruolo di product owner.** L'articolo lo elenca come insidia. Scegli invece qualcuno che rappresenti il business e abbia il tempo di decidere.
- **Scalare copiando un framework.** Un grande framework installato senza comprenderlo aggiunge processo e rallenta i team. Parti invece dal problema che hai e adotta solo ciò che aiuta (vedi Argomento 1.8 — Scalare l'agile).
- **Inseguire un punteggio di agilità.** I team ottimizzano per la metrica. Segui invece risultati come lead time, fallimenti dei rilasci e tempo di ripristino del servizio.
- **Tenere separati sviluppo e operations.** Il team di delivery consegna e quello operativo eredita. Coinvolgili invece in pianificazione, revisioni e apprendimento dagli incidenti condivisi (vedi Argomento 5.2 — DevOps).

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Consegna continua di software | Il lavoro è consegnato in grandi rilasci | Alcuni team consegnano in cicli brevi | I team condividono una cadenza di consegna comune e una definition of done | Lead time ed esiti dei rilasci sono misurati e rivisti | I ritmi di rilascio sono coordinati tra team e fornitori |
| Pratiche ingegneristiche | Test e build sono per lo più manuali | Alcuni team hanno test e build automatizzati | Una pipeline condivisa esegue i test a ogni modifica | Copertura dei test e tassi di fallimento sono monitorati e le lacune corrette | Pipeline e pratiche sono migliorate tra i team da prove condivise |
| Backlog e prioritizzazione | Le richieste arrivano per e-mail e in modo estemporaneo | I team tengono i propri backlog | Ogni team ha un backlog ordinato che include il lavoro sul servizio | Flusso ed età del backlog sono rivisti con gli stakeholder | Le priorità sono allineate tra team, clienti e fornitori |
| Apprendimento e adattamento | Le revisioni seguono solo i guasti maggiori | Alcuni team tengono retrospettive | Tutti i team tengono retrospettive regolari e registrano le azioni | Le azioni sono seguite fino al completamento e gli effetti verificati | Le lezioni passano tra i team e nelle policy senza direzione centrale |

## Checklist

- [ ] Il team sa dire quale metodo o quali pratiche agili usa e perché li ha scelti.
- [ ] Il lavoro è ordinato in tipi predittivi e adattivi, con un approccio dichiarato per ciascuno.
- [ ] I test automatici girano a ogni modifica e una build fallita ferma la linea.
- [ ] La nostra definition of done include monitoraggio, note di supporto e un rollback collaudato.
- [ ] Ogni team ha un backlog ordinato che include miglioramenti del servizio e difetti.
- [ ] Runbook e descrizioni dei servizi hanno responsabili e date di revisione.
- [ ] Le retrospettive si tengono a un ritmo regolare e ciascuna si conclude con un'azione con responsabile.
- [ ] Team e leader hanno ricevuto formazione sul modo di lavorare che chiediamo loro.
- [ ] Sappiamo di quali prove hanno bisogno gli auditor e come i nostri strumenti le forniscono.
- [ ] Misure di risultato, come lead time e tempo di ripristino del servizio, sono riviste regolarmente.

## Prompt per l'IA

**Scopo: mappare le tue pratiche attuali sulle pratiche agili comuni e trovare le lacune.**

```text
You are helping a team understand which agile software development practices it actually uses.

Practices to consider: user stories and backlogs, daily stand-ups, retrospectives, test-driven development, continuous integration, pair programming, refactoring, definition of done, regular reviews with customers.

Our team: [team size and what you build and run].
What we do today, in our own words: [paste a short description of a typical week, including meetings, tools, and how a change reaches production].

For each practice, say whether the description shows it in use, partly in use, or not mentioned, and quote the words you based that on. Do not assume a practice exists if it is not described. Then list three questions I should ask my team to fill gaps. Ask me clarifying questions first if the description is too thin, and list what you are unsure of.
```

**Scopo: redigere una definition of done che includa le operations.**

```text
Help us write a definition of done for [type of work, e.g. "backend changes to our order service"] that covers both building and running the service.

Our current definition of done is: [paste it, or write "none"].
Things operations staff tell us they need before they accept a release: [paste a list, or write "unknown"].
Rules we must follow: [list any known audit, security, or safety rules, or write "none known"].

Produce a checklist of 8 to 12 items, grouped as build quality, release readiness, and operational readiness. Mark each item that you added by assumption. Do not claim that any standard requires an item unless I have pasted its text. Ask me clarifying questions first, and list what you are unsure of.
```

**Scopo: preparare le prove per un auditor a partire dai tuoi strumenti agili.**

```text
An auditor has asked: [paste the question, e.g. "show me how changes are reviewed and approved"].

Our tools and records: [list your version control, build, test, ticket, and release tools, and what each records].
Our practice: [describe how a change goes from idea to production].

List what evidence each tool already produces that relates to the question, what gaps remain, and three lightweight ways to close each gap. Do not state that any law or standard requires something unless I have pasted its text. Separate facts from assumptions, and list what you are unsure of.
```

**Scopo: pianificare una retrospettiva su come il tuo team adotta le pratiche agili.**

```text
Plan a 60-minute retrospective for a team of [number] people who are [adopting / improving] agile practices. The main problem right now is [problem].

Include: a timed agenda, a way to gather facts first, a short discussion of two or three of these questions: [paste questions from the "Questions to discuss" section], and a closing step that records exactly one action with an owner and a date.

Keep the plan free of any specific tool. If anything is missing, ask me clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [scrum](../../../../skills/scrum/SKILL.md): da usare per impostare o rivedere ruoli, eventi e artefatti di un team Scrum.
- [kanban](../../../../skills/kanban/SKILL.md): da usare per progettare una lavagna visiva con limiti al lavoro in corso per un team di servizio o di operations.
- [extreme-programming](../../../../skills/extreme-programming/SKILL.md): da usare per rivedere o adottare pratiche ingegneristiche come il test-driven development e l'integrazione continua.
- [user-story](../../../../skills/user-story/SKILL.md): da usare per scrivere user story con criteri di accettazione che includano le esigenze operative.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): da usare per condurre una retrospettiva che si conclude con un cambiamento con responsabile.

## Fonti principali

- **Manifesto for Agile Software Development** e **Principles behind the Agile Manifesto** (agilemanifesto.org): l'enunciazione primaria di valori e principi.
- **Agile software development** (Wikipedia): un'ampia panoramica di storia, metodi, pratiche, adozione e critiche con molte fonti citate.
- **Agile Glossary** (Agile Alliance): definizioni di pratiche e termini agili, mantenute dalla comunità nata dal Manifesto.

## Riferimenti

1. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
2. Manifesto for Agile Software Development — Beck et al., agilemanifesto.org — https://agilemanifesto.org/
3. Principles behind the Agile Manifesto — Beck et al., agilemanifesto.org — https://agilemanifesto.org/principles.html
4. Waterfall model — Wikipedia — https://en.wikipedia.org/wiki/Waterfall_model
5. Scrum (software development) — Wikipedia — https://en.wikipedia.org/wiki/Scrum_(software_development)
6. Extreme programming — Wikipedia — https://en.wikipedia.org/wiki/Extreme_programming
7. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
8. Test-driven development — Wikipedia — https://en.wikipedia.org/wiki/Test-driven_development
9. Continuous integration — Wikipedia — https://en.wikipedia.org/wiki/Continuous_integration
10. Feature-driven development — Wikipedia — https://en.wikipedia.org/wiki/Feature-driven_development
11. Dynamic systems development method — Wikipedia — https://en.wikipedia.org/wiki/Dynamic_systems_development_method
12. Agile Glossary — Agile Alliance — https://www.agilealliance.org/agile101/agile-glossary/
