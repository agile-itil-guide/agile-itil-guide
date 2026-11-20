# Monitoraggio e gestione degli eventi

**Il monitoraggio ti dice se un servizio funziona nel modo in cui gli utenti lo vivono, e una buona gestione degli eventi trasforma un diluvio di segnali in un piccolo numero di allarmi che una persona può capire e su cui può agire.**

## Perché è importante

Un servizio che non puoi vedere è un servizio che non puoi gestire. Senza monitoraggio, un team viene a sapere dei guasti dagli utenti e del lento degrado da nessuno. Con un monitoraggio scadente il problema è l'opposto: così tanti allarmi che l'ingegnere di turno smette di crederci e quello che conta si perde nel rumore. Entrambi gli estremi costano sonno, fiducia e tempo.

Monitoraggio e gestione degli eventi determinano anche con quale rapidità un incidente può essere trovato e corretto. Tutto nella gestione degli incidenti dipende dal sapere in fretta che qualcosa non va e dall'avere abbastanza informazioni per scoprire perché (vedi Argomento 3.2 — Gestione degli incidenti). I team agili che rilasciano spesso ne hanno ancora più bisogno, perché ogni rilascio è un'occasione per rompere qualcosa e ogni decisione di rollback dipende dal vederne l'effetto.

Il libro *Site Reliability Engineering* di Google ha due capitoli che trattano direttamente il tema: "Monitoring Distributed Systems" e "Practical Alerting from Time-Series Data". Descrivono la pratica di un'organizzazione e sostengono un approccio deliberatamente semplice e centrato sull'utente. Questo argomento li usa come fonte principale, perché gli articoli di Wikipedia consultati per questa guida dicono poco sulla pratica. Il vocabolario ITIL qui, come evento, allarme e gestione degli eventi, è tratto da descrizioni ampiamente pubblicate che questa guida non ha potuto confermare rispetto al testo del proprietario del framework. Leggi i capitoli SRE come un'opzione ben spiegata.

## Concetti fondamentali

### Monitoraggio

Il capitolo SRE definisce il **monitoraggio** come la raccolta, l'elaborazione e la visualizzazione di dati quantitativi in tempo reale su un sistema. Dice che il monitoraggio sostiene l'analisi delle tendenze a lungo termine, il confronto tra esperimenti, l'allerta, i cruscotti e il debug ad hoc a posteriori. Sottolinea che il monitoraggio è un significativo sforzo ingegneristico e che i team di solito assegnano ad esso almeno una persona.

### Eventi, allarmi e incidenti

Nell'uso ITSM, un **evento** è un cambiamento di stato significativo per la gestione di un servizio. La maggior parte degli eventi è informativa. Alcuni indicano un avvertimento o un'eccezione. Un **allarme** è, come lo dice il capitolo SRE, una notifica a un essere umano, consegnata come ticket, e-mail o pagina. Un **incidente** è un'interruzione non pianificata o una riduzione della qualità (vedi Argomento 3.2 — Gestione degli incidenti). La gestione degli eventi è la pratica di decidere quali eventi contano, che cosa farne e chi informare. Il flusso va da eventi ad allarmi a, talvolta, incidenti.

### Monitoraggio black-box e white-box

Il capitolo distingue due tipi:

| Tipo | Che cosa fa | Punto di forza |
|---|---|---|
| **Black-box** | Verifica il comportamento visibile dall'esterno, come lo vedrebbe un utente | Rileva i problemi attivi; adatto alla chiamata di reperibilità |
| **White-box** | Usa metriche esposte dall'interno del sistema, come log o gestori interni | Rivela problemi imminenti e guasti mascherati dai tentativi ripetuti; essenziale per il debug |

Il libro combina entrambi. Una sonda black-box ti dice che il checkout sta fallendo; i dati white-box aiutano a scoprire perché.

### Sintomi e cause

Il capitolo dice che il monitoraggio dovrebbe rispondere a due domande: che cosa è rotto e perché. Consiglia di concentrare gli allarmi sui sintomi, che sono ciò che gli utenti vivono, e di chiamare per cause solo quando sono definite e imminenti. Che un singolo computer si guasti è, nelle sue parole nel capitolo sull'alerting, inaccettabile da segnalare, perché è troppo rumoroso. È il cuore di un buon approccio agli allarmi: avvisa una persona quando gli utenti sono o saranno danneggiati, non ogni volta che una parte ha un sussulto.

### I quattro segnali d'oro

Il capitolo propone quattro segnali da osservare per un sistema rivolto agli utenti:

- **Latenza:** il tempo per servire una richiesta. Monitora separatamente le richieste fallite, perché un "slow error is even worse than a fast error".
- **Traffico:** la domanda sul sistema.
- **Errori:** richieste fallite, esplicite, implicite o per policy.
- **Saturazione:** quanto è "pieno" il servizio. Le prestazioni spesso peggiorano prima del 100% di utilizzo.

Si associano naturalmente agli indicatori di livello di servizio (vedi Argomento 3.7 — Gestione dei livelli di servizio). Il capitolo avverte anche che le medie nascondono i valori anomali lenti e suggerisce di registrare i conteggi delle richieste in intervalli di latenza per vedere la distribuzione.

### Che cosa rende buono un allarme

Il capitolo offre domande da porre prima di scrivere un allarme: rileva una condizione urgente, azionabile e visibile all'utente; può essere ignorato in sicurezza; e la risposta può essere automatizzata? Le chiamate dovrebbero essere azionabili, richiedere giudizio e riguardare problemi nuovi. Dice che gli allarmi non dovrebbero mai scattare solo perché "something seems a bit weird". Le chiamate le cui risposte sono meccaniche e algoritmiche sono, a suo avviso, una bandiera rossa che richiede automazione o riparazione della causa radice.

### Instradare gli allarmi

Il capitolo sull'alerting descrive l'invio degli allarmi degni di chiamata al personale di turno, di quelli subcritici alle code di ticket e del resto ai cruscotti di stato. Descrive strumenti per instradare, deduplicare e inibire gli allarmi e nota che gli allarmi dovrebbero attendere una durata minima prima di scattare perché possono oscillare. Avverte che "you can only alert on the failures that you expected", ed è per questo che combinare sonde black-box con dati white-box conta.

### Mantieni semplice

Il capitolo sostiene sistemi semplici e veloci contro la "magia" che impara soglie o rileva causalità e nota che le gerarchie di dipendenze complesse hanno avuto un successo limitato. Dice di mantenere semplici le regole che catturano incidenti reali, rimuovere gli allarmi raramente esercitati e i segnali non usati e fare in modo che i costi di manutenzione crescano più lentamente della dimensione del servizio. I casi che descrive, come un team sommerso dagli allarmi che ha temporaneamente allentato il proprio obiettivo e disattivato gli allarmi e-mail per liberare tempo per correzioni durevoli, mostrano una disponibilità a rimuovere il rumore.

### Cruscotti e viste a lungo termine

Il capitolo tratta i cruscotti come viste riassuntive precostruite delle metriche chiave di un servizio e dice che i cruscotti sono meglio degli allarmi e-mail, che definisce di valore molto limitato. Raccomanda anche di rivedere nel tempo la frequenza delle chiamate, per esempio in rapporti trimestrali, per tenere informata la dirigenza del carico di reperibilità. Questo rende la qualità degli allarmi qualcosa che i manager possono vedere (vedi Argomento 1.2 — I principi agili sul ritmo sostenibile).

### Limiti delle fonti

I capitoli SRE non danno soglie oltre a un singolo esempio svolto, non discutono runbook o limiti di carico di reperibilità e non descrivono come rivedere e ritirare gli allarmi nel tempo, quindi sono questioni per la tua pratica. Provengono da una grande organizzazione con forti risorse ingegneristiche. I team più piccoli possono applicare i principi con strumenti più semplici.

## Buone pratiche

1. **Monitora ciò che gli utenti vivono.** Aggiungi almeno una sonda black-box che esegue un'azione utente reale, come accedere o effettuare un ordine, e avvisa quando fallisce.
2. **Osserva i quattro segnali d'oro.** Per ogni servizio, monitora latenza, traffico, errori e saturazione. Aggiungi altre misure solo se rispondono a una domanda che hai posto.
3. **Avvisa sui sintomi.** Chiama quando gli utenti sono danneggiati o lo saranno presto. Tratta le condizioni interne, come il guasto di un singolo computer, come informazioni a più bassa priorità a meno che siano definite e imminenti.
4. **Rendi ogni chiamata azionabile.** Prima di creare un allarme, scrivi che cosa dovrebbe fare chi risponde. Se non c'è nulla da fare, non è una chiamata.
5. **Instrada per urgenza.** Invia gli allarmi urgenti al personale di turno, quelli meno urgenti a una coda di ticket e le informazioni a un cruscotto. Non inviare allarmi e-mail a persone che li ignoreranno.
6. **Usa le distribuzioni, non solo le medie.** Guarda i percentili alti per la latenza, o gli intervalli, così che i valori anomali lenti siano visibili.
7. **Fissa una durata minima.** Richiedi che una condizione duri per un breve tempo prima di avvisare, per evitare le oscillazioni. Regola la durata con dati reali.
8. **Ritira gli allarmi rumorosi.** Rivedi quali allarmi scattano di più e non hanno portato ad alcuna azione. Rimuovili o correggili. Il capitolo SRE tratta le risposte meccaniche come segnale per automazione o riparazione.
9. **Verifica il tuo monitoraggio.** Rompi deliberatamente qualcosa in un ambiente di test e verifica che scatti l'allarme giusto. Includi nei controlli il sistema di monitoraggio stesso, così che il suo guasto sia notato.
10. **Rivedi il carico di reperibilità.** Conta le chiamate per turno, le interruzioni fuori orario e i falsi allarmi ogni trimestre. Condividi i risultati con i manager e usali nella pianificazione.
11. **Tieni il monitoraggio nella definition of done.** Per ogni nuova funzionalità, chiedi quali segnali mostrano se funziona e di quale allarme, se ce n'è uno, ha bisogno (vedi Argomento 3.5 — Gestione di rilasci e deployment).
12. **Mantieni semplice.** Preferisci poche regole comprensibili a uno schema complesso. Rimuovi i segnali non usati e rivedi le regole dopo gli incidenti.

## Domande da discutere con il team

**Come abbiamo scoperto i nostri ultimi tre incidenti?**

Elenca ogni incidente e come è stato notato per primo: un allarme, un utente, un collega. Se la maggior parte è venuta dagli utenti, il monitoraggio perde i sintomi che contano. Chi facilita può chiedere che cosa avrebbe mostrato una sonda. Scegli per primo un'azione utente da monitorare.

**Quali allarmi ignoriamo, e perché?**

Chiedi agli ingegneri di turno gli allarmi che silenziano o saltano. Ciascuno è un candidato da correggere o eliminare. Chiedi che cosa fa fidare o diffidare le persone di un allarme. Una risposta franca spesso rivela allarmi che scattano su condizioni su cui nessuno può agire. Concorda di ritirarne o correggerne tre.

**Qual è stata la nostra peggior notte di reperibilità, e che cosa l'avrebbe migliorata?**

Raccogli storie senza attribuire colpe. Cerca schemi: chiamate ripetute, allarmi poco chiari, mancanza di runbook, nessuna escalation. Ogni schema è un miglioramento. Chiedi quali due cambiamenti aiuterebbero di più. Lo scopo è un carico più leggero e un segnale più chiaro.

**Se il nostro sistema di monitoraggio si guastasse, come lo sapremmo?**

Chiedi chi sorveglia il sorvegliante. Molti team non hanno un controllo che il monitoraggio funzioni. Discuti un semplice heartbeat o una sonda da un sistema separato. Concorda un controllo da aggiungere.

**Che cosa mostrano i nostri cruscotti, e chi li guarda?**

Elenca i cruscotti e chiedi chi ha usato ciascuno nell'ultimo mese. I cruscotti inutilizzati sono ingombro; quelli utili raccontano una storia sul servizio. Chiedi a quale domanda risponde ciascuno. Mantieni un piccolo insieme che risponde a domande reali.

**Come sapremmo che un rilascio ha peggiorato le cose?**

Scegli un rilascio recente e chiedi quale segnale mostrerebbe un problema. Se la risposta è "lo sapremmo dagli utenti", discuti quali segnali osservare dopo un rilascio e chi ne è responsabile. Questa domanda collega il monitoraggio al deployment. Scrivi una breve checklist post-rilascio.

## Nella pratica: un esempio di ITIL agile

L'azienda di trasporto pubblico di una città gestisce un sito web e un'app per la pianificazione dei viaggi usati da 400.000 persone al giorno. Un team di piattaforma di dieci persone possiede il servizio con un turno di reperibilità di quattro. Il team ha centinaia di allarmi: CPU su ogni server, spazio su disco, lunghezze delle code e conteggi di errori. Gli ingegneri di turno ricevono 40 chiamate in una settimana tipica, per lo più fuori orario, e due incidenti dell'ultimo trimestre sono stati segnalati per primi dagli utenti sui social media.

Il responsabile del team e un ingegnere rivedono tre mesi di chiamate. Scoprono che tre quarti riguardavano condizioni che non richiedevano azioni o che si risolvevano da sole. Concordano di seguire un approccio semplice dal libro SRE: avvisare su ciò che gli utenti vivono. Aggiungono una sonda che pianifica un viaggio standard ogni minuto e ne misura successo e velocità e tengono un piccolo insieme di allarmi sulla saturazione del database e della coda. Spostano il resto su un cruscotto e un ticket quotidiano. Ogni chiamata rimasta ottiene una breve voce di runbook che dice che cosa controllare.

Dopo un mese, le chiamate scendono a circa cinque alla settimana e i due incidenti successivi sono stati entrambi rilevati dalla sonda prima che gli utenti si lamentassero. Restano alcuni problemi. La sonda copre solo un tipo di viaggio e un guasto che colpiva i viaggi in bicicletta è passato inosservato per un giorno. Un ingegnere riferisce anche che la decisione "sposta sul cruscotto" ha nascosto un lento problema del disco che poi ha causato un guasto. Il team aggiunge sonde per altri tipi di viaggio, aggiunge al turno una revisione quotidiana del cruscotto e concorda di rivedere il carico di reperibilità ogni trimestre.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery sanno che cosa il software è pensato per fare e dove è probabile che fallisca. Incorpora i segnali nel codice: log utili, metriche e controlli di salute. Definisci sonde per le azioni utente chiave e tratta il monitoraggio come parte del fatto. Partecipa alle revisioni degli allarmi così che le chiamate riflettano problemi reali.

### Team di servizio e di operations

I team operativi portano il cercapersone e i cruscotti. Mantieni gli allarmi pochi e azionabili, instrada per urgenza e monitora il carico di reperibilità. Rimanda gli allarmi rumorosi ai team che li possiedono, con prove, e condividi ciò che impari dagli incidenti su che cosa osservare.

### Leadership e governance

I leader dovrebbero chiedere dati sul carico di reperibilità e sul rilevamento degli incidenti, non più allarmi. Sostieni il tempo per ritirare il rumore e aggiungere segnali utili. Tratta un numero crescente di chiamate fuori orario come un rischio per il servizio e per le persone.

### Clienti e utenti

Clienti e utenti traggono vantaggio quando i problemi sono trovati prima che se ne accorgano. Segnala i problemi con dettagli, come che cosa hai provato e quando, perché aiuta a regolare il monitoraggio. Chiedi ai fornitori come rilevano i guasti e con quale rapidità e se pubblicano informazioni di stato.

## Modalità di fallimento comuni

- **Avvisare su tutto.** Il cercapersone suona di continuo e la fiducia va persa. Chiama invece sui sintomi e invia il resto a ticket o cruscotti.
- **Monitorare i sistemi, non gli utenti.** Tutte le macchine sono verdi mentre gli utenti non riescono ad accedere. Aggiungi invece sonde black-box di azioni utente reali.
- **Nessuna azione allegata.** Le chiamate arrivano senza nulla da fare. Richiedi invece che ogni chiamata abbia una risposta descritta, o rimuovila.
- **Solo medie.** Un gruppo di utenti soffre mentre la media sembra a posto. Guarda invece i percentili alti o le distribuzioni.
- **Regole complesse e ingegnose.** Soglie apprese e alberi di dipendenze confondono chi risponde. Preferisci invece regole semplici e comprensibili.
- **Monitoraggio non sorvegliato.** Il sistema di monitoraggio si guasta in silenzio. Controllalo invece con heartbeat e test.
- **Risposte meccaniche.** Le persone ripetono la stessa correzione dopo ogni chiamata. Automatizza invece la risposta o correggi la causa.
- **Ignorare il carico di reperibilità.** Le chiamate notturne sono trattate come normali. Misurale invece e rivedile e tratta un carico alto come un rischio.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Visibilità dell'esperienza dell'utente | Gli utenti segnalano la maggior parte dei problemi | Alcuni servizi hanno sonde o metriche per le azioni utente | Le azioni utente chiave sono sondate e i segnali d'oro sono monitorati per ogni servizio | Tempo di rilevamento e copertura sono misurati e le lacune corrette | Il monitoraggio è condiviso tra team, fornitori e clienti |
| Qualità degli allarmi | Molti allarmi, poca azione | Alcuni team sfoltiscono gli allarmi | Le chiamate sono basate sui sintomi, azionabili e instradate per urgenza | Precisione e rumore degli allarmi sono misurati e rivisti | La progettazione degli allarmi è migliorata tra i team da prove condivise |
| Risposta e automazione | Le risposte sono improvvisate | Esistono alcuni runbook | Le chiamate rimandano ai runbook e le risposte meccaniche sono automatizzate | Tempo di risposta e uso dell'automazione sono misurati | Le risposte sono coordinate tra team e fornitori |
| Persone e carico | Il carico di reperibilità non è monitorato | Alcuni team contano le chiamate | Il carico di reperibilità è rivisto ogni trimestre | Il carico è bilanciato e ridotto dai dati | Carico e apprendimento sono condivisi tra i team e riflessi nella pianificazione |

## Checklist

- [ ] Ogni servizio importante ha almeno una sonda di un'azione utente reale.
- [ ] Monitoriamo latenza, traffico, errori e saturazione per ogni servizio.
- [ ] Ogni chiamata ha una risposta scritta e riguarda una condizione visibile all'utente o imminente.
- [ ] Gli allarmi sono instradati per urgenza al personale di turno, ai ticket o ai cruscotti.
- [ ] Percentili alti o distribuzioni sono visibili per la latenza.
- [ ] Rivediamo quali allarmi scattano di più e ritiriamo quelli che non portano ad alcuna azione.
- [ ] Il sistema di monitoraggio stesso è controllato.
- [ ] Il carico di reperibilità (chiamate per turno, interruzioni fuori orario) è rivisto ogni trimestre.
- [ ] Le nuove funzionalità includono il monitoraggio nella loro definition of done.
- [ ] Dopo ogni rilascio, qualcuno verifica i segnali rispetto a un breve elenco.

## Prompt per l'IA

**Scopo: rivedere un elenco di allarmi per rumore e azionabilità.**

```text
Here is a list of our alerts with how often each fired in the last [period], and what happened after (acted on, ignored, resolved by itself): [paste as a table; use real data].

Using only my data, group the alerts into: fired often with no action; fired and led to action; rarely fired. For each of the first group, suggest a question to ask its owner (for example whether it can be removed, routed to a ticket, or turned into a symptom-based alert). Do not invent frequencies or outcomes. Tell me what additional data would help, and list what you are unsure of.
```

**Scopo: definire una sonda per un percorso utente.**

```text
Help me define a black-box probe for this user action in [service]: [describe, for example "a user searches for a journey and receives results"].

What counts as success: [describe].
What is too slow: [say "unknown" or describe in words, not numbers].
What systems the action touches: [list].

Describe the steps the probe should perform, what it should record (success, time taken, and where it failed), what alert condition to propose (leave thresholds as [to be agreed]), and what a responder would check first. Mark assumptions. Do not invent system details. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: scrivere la sezione di risposta per un allarme.**

```text
For this alert, write a short response entry for on-call staff.

Alert name and condition: [paste].
What it means for users: [describe].
What I know to check first: [list].
Who to escalate to: [role, or write "unknown"].

Write: what the alert means, the first three checks, how to tell whether users are affected, when to escalate, and a note on whether the response could be automated. Use only my information; mark anything you added as [CHECK]. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: preparare una revisione trimestrale del carico di reperibilità.**

```text
Help me prepare a quarterly pager load review for [team].

Data for the quarter (pages by week, out-of-hours pages, pages with no action, incidents detected by monitoring versus by users): [paste real figures].
Context: [describe changes in the period].

Summarize the data in plain language, using only my figures. Highlight trends and outliers as questions, not conclusions. Suggest three questions for the team and one for management. Do not invent causes. If the data is incomplete, say what to collect. List what you are unsure of.
```

## Competenze per l'IA

- [runbook](../../../../skills/runbook/SKILL.md): da usare per scrivere la risposta che accompagna ogni chiamata.
- [on-call-rotation](../../../../skills/on-call-rotation/SKILL.md): da usare per progettare un turno equo e per pianificare come il carico di reperibilità è condiviso e rivisto.
- [software-engineering-metrics](../../../../skills/software-engineering-metrics/SKILL.md): da usare per scegliere e interpretare misure di prestazione del servizio e della consegna.
- [performance-testing](../../../../skills/performance-testing/SKILL.md): da usare per verificare latenza e saturazione sotto carico prima che i problemi raggiungano gli utenti.
- [chaos-testing](../../../../skills/chaos-testing/SKILL.md): da usare per verificare che i guasti siano rilevati e gestiti provocandoli deliberatamente in un ambiente sicuro.

## Fonti principali

- **Monitoring Distributed Systems** (*Site Reliability Engineering*, Google, sre.google): definizioni, i quattro segnali d'oro, sintomi contro cause e consigli su allarmi semplici.
- **Practical Alerting from Time-Series Data** (*Site Reliability Engineering*, Google, sre.google): come funzionano nella pratica regole di allarme, instradamento e oscillazioni.
- **Service Level Objectives** (*Site Reliability Engineering*, Google, sre.google): il legame tra indicatori, obiettivi e allarmi.
- **IT service management** (Wikipedia): il posto di monitoraggio e incidenti nell'ITSM.

## Riferimenti

1. Monitoring Distributed Systems — Google SRE book, sre.google — https://sre.google/sre-book/monitoring-distributed-systems/
2. Practical Alerting from Time-Series Data — Google SRE book, sre.google — https://sre.google/sre-book/practical-alerting/
3. Service Level Objectives — Google SRE book, sre.google — https://sre.google/sre-book/service-level-objectives/
4. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
5. Network monitoring — Wikipedia — https://en.wikipedia.org/wiki/Network_monitoring
6. Observability (software) — Wikipedia — https://en.wikipedia.org/wiki/Observability_(software)
7. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
8. Alarm fatigue — Wikipedia — https://en.wikipedia.org/wiki/Alarm_fatigue
9. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
