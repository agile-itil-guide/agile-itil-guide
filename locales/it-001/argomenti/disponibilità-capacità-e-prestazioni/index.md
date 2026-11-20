# Disponibilità, capacità e prestazioni

**Disponibilità, capacità e prestazioni sono tre modi di vedere se un servizio c'è, è abbastanza grande ed è abbastanza veloce quando gli utenti ne hanno bisogno, e l'approccio agile è scegliere gli obiettivi dalle esigenze degli utenti, dare loro un prezzo onesto e testarli prima che arrivi la domanda.**

## Perché è importante

Gli utenti non separano i tre aspetti. Un servizio "attivo" ma troppo lento per essere usato li ha delusi, e un servizio veloce in un giorno tranquillo e che crolla al picco li ha delusi nel momento in cui ne hanno più bisogno. I team che guardano separatamente a disponibilità, capacità e prestazioni spesso perdono i modi in cui interagiscono: aggiungere capacità cambia costo e complessità, inseguire una disponibilità perfetta limita la rapidità con cui puoi cambiare e ottimizzare per la velocità può ridurre la resilienza.

I team agili affrontano una versione particolare del problema. Cambiano spesso il servizio, e ogni modifica può alterare prestazioni o fabbisogno di risorse in modi che nessuno ha testato. Tendono anche a lavorare su orizzonti temporali brevi, quindi i fabbisogni di capacità che richiedono mesi per essere organizzati, come hardware, contratti o licenze, possono essere persi. Le pratiche di questo argomento offrono un modo di guardare avanti senza tornare alla pianificazione a lungo raggio fine a se stessa.

Il libro *Site Reliability Engineering* di Google, nel capitolo "Embracing Risk", è una fonte chiara sull'economia della disponibilità: dice che il suo approccio non punta al 100% di affidabilità, perché oltre un certo punto massimizzare la stabilità limita la rapidità con cui si sviluppano nuove funzionalità e i costi dell'affidabilità salgono ripidamente. L'[articolo di Wikipedia sulla pianificazione della capacità](https://en.wikipedia.org/wiki/Capacity_planning) dà definizioni e strategie generali. Entrambi sono parziali, e il vocabolario ITIL usato qui viene da descrizioni ampiamente pubblicate che questa guida non ha potuto confermare rispetto al testo del proprietario del framework.

## Concetti fondamentali

### Disponibilità

La **disponibilità** è la capacità di un servizio di fare ciò di cui gli utenti hanno bisogno quando ne hanno bisogno. Un modo comune di esprimerla è come percentuale in un periodo. Il capitolo SRE nota due modi di misurarla. Per un singolo sistema, la disponibilità è basata sul tempo: il 99,99% consente circa 52,56 minuti di indisponibilità non pianificata all'anno. Per i servizi distribuiti che sono parzialmente attivi in ogni momento, è meglio misurarla come tasso di successo delle richieste su una finestra mobile; l'esempio del capitolo è un servizio con 2,5 milioni di richieste giornaliere e un obiettivo del 99,99%, che consente fino a 250 errori. Il capitolo si concentra sull'indisponibilità non pianificata. L'indisponibilità pianificata richiede un proprio accordo con gli utenti.

### Il prezzo di ogni nove in più

Il capitolo dice che i costi dell'affidabilità salgono in modo non lineare: un nove in più può costare 100 volte l'incremento precedente, comprese le risorse ridondanti e il costo opportunità degli ingegneri che non costruiscono funzionalità per gli utenti. Dà un'illustrazione: portare la disponibilità dal 99,9% al 99,99% su un servizio con 1 milione di dollari di ricavi vale circa 900 dollari di valore, quindi l'investimento si ripaga solo se il nove in più costa meno di quello. I numeri sono l'esempio della fonte, e i tuoi devono venire dai tuoi ricavi o dal tuo valore. Il principio vale: scegli la disponibilità di cui gli utenti hanno bisogno e dai un prezzo a tutto ciò che va oltre.

### Tolleranza al rischio

Il capitolo descrive il lavoro con i product owner per trasformare gli obiettivi di business in obiettivi espliciti. I fattori includono la disponibilità richiesta, la forma dei guasti (un tasso di errore basso e costante contro occasionali interruzioni complete, con l'esposizione dei dati particolarmente grave), il costo e altre misure come la latenza. Nota che l'infrastruttura che serve molti clienti può essere offerta a livelli di servizio esplicitamente definiti, così che ogni cliente scelga il livello più economico che soddisfa le sue esigenze.

### Error budget

Il capitolo spiega l'error budget come misura condivisa e oggettiva tra i team di prodotto, misurati sulla velocità, e i team di affidabilità, misurati sull'affidabilità. Finché resta budget, i rilasci continuano. Quando è esaurito, i rilasci rallentano e lo sforzo si sposta sull'affidabilità (vedi Argomento 3.7 — Gestione dei livelli di servizio).

### Capacità

L'articolo di Wikipedia definisce la pianificazione della capacità come la determinazione della capacità produttiva di cui un'organizzazione ha bisogno per soddisfare una domanda mutevole, e dice che nell'IT è sinonimo di gestione della capacità: stimare le risorse di archiviazione, hardware, software e connettività necessarie in un periodo futuro. L'articolo distingue la **capacità di progetto**, il massimo output possibile, dalla **capacità effettiva**, l'output dopo i vincoli. Nella pratica, pianifica per la capacità effettiva, che è sempre inferiore al valore di progetto.

### Strategie di capacità

L'articolo descrive quattro strategie per aggiungere capacità:

| Strategia | Che cosa significa | Compromesso |
|---|---|---|
| **Lead** | Aggiungere capacità prima della domanda | Buon servizio e tempi brevi, ma rischiosa se la domanda è imprevedibile |
| **Lag** | Aggiungere capacità solo dopo aver lavorato a o oltre la piena capacità | Minor rischio di sovradimensionare, ma può far perdere clienti |
| **Match** | Aggiungere capacità a piccoli incrementi al cambiare della domanda | Equilibrata, richiede un buon monitoraggio |
| **Adjustment** | Aggiungere o ridurre la capacità in piccola o grande misura al cambiare di domanda o architettura | Flessibile, richiede un provisioning rapido |

L'articolo descrive la pianificazione a breve, medio e lungo termine (operativa, tattica e strategica), da giorni ad anni. In un contesto cloud, "match" e "adjustment" sono spesso più facili perché le risorse si aggiungono in fretta, ma costi e contratti richiedono comunque pianificazione (vedi Argomento 4.5 — Gestione finanziaria IT e FinOps).

### Prestazioni

Le **prestazioni** sono quanto in fretta e quanto bene risponde il servizio. Il capitolo sul monitoraggio del libro SRE suggerisce di misurare latenza, traffico, errori e saturazione e avverte che le medie nascondono i valori anomali lenti (vedi Argomento 3.10 — Monitoraggio e gestione degli eventi). La saturazione, quanto è "pieno" il servizio, collega le prestazioni alla capacità: il capitolo nota che le prestazioni spesso peggiorano prima del 100% di utilizzo.

### Come interagiscono i tre

- Più capacità può aumentare disponibilità e prestazioni, a un costo.
- Obiettivi di alta disponibilità richiedono di solito ridondanza, che è capacità aggiuntiva.
- Ottimizzare per le prestazioni di picco può ridurre il margine per i guasti.
- Le modifiche al servizio alterano tutti e tre, ed è per questo che i test contano.

Una disciplina utile è dichiarare gli obiettivi insieme per ogni servizio: quanto disponibile, quanto veloce e quanto carico deve sostenere.

### Domanda e previsione

La capacità dipende dalla domanda. La domanda viene dagli utenti e dal business: campagne di marketing, picchi stagionali, nuovi clienti. Il business sa del futuro più dell'IT, quindi chiedi. Pianifica con intervalli anziché con numeri singoli e rivedi regolarmente la previsione (vedi la competenza demand forecasting più avanti).

### Test

Le affermazioni su capacità e prestazioni sono ipotesi finché non sono testate. I test di carico e di prestazioni applicano una domanda realistica per vedere come si comporta il servizio, e il chaos testing introduce guasti per vedere se la disponibilità regge. Possono far parte della pipeline di delivery.

### Limiti delle fonti

L'articolo di Wikipedia sulla pianificazione della capacità non menziona la gestione della capacità di ITIL né analizza il rapporto tra capacità, prestazioni e disponibilità, e la sua sezione sugli asset è segnalata come priva di citazioni. Il capitolo SRE descrive le pratiche di un'organizzazione molto grande con un'economia particolare. Usale per i principi, non per i numeri.

## Buone pratiche

1. **Dichiara insieme obiettivi di disponibilità, prestazioni e carico.** Per ogni servizio, scrivi quanto deve essere disponibile, quanto in fretta deve rispondere e quanto carico deve sostenere. Basali sulle esigenze degli utenti e concordali con il responsabile del servizio e i clienti.
2. **Dai un prezzo agli obiettivi.** Stima quanto costa un livello in più di disponibilità o velocità, in denaro e in funzionalità ritardate. Confrontalo con ciò che utenti e business guadagnerebbero. Usa le tue cifre, non l'esempio di un libro.
3. **Misura la disponibilità in un modo che corrisponda al servizio.** Per i servizi parzialmente attivi in ogni momento, usa il tasso di successo su una finestra mobile come fa il capitolo SRE. Per i sistemi semplici, usa misure basate sul tempo. Conta separatamente l'indisponibilità pianificata e non pianificata.
4. **Pianifica per la capacità effettiva.** Stima ciò che il servizio può sostenere dopo vincoli reali come overhead, guasto dei componenti e manutenzione. Mantieni un margine.
5. **Scegli una strategia di capacità di proposito.** Decidi se anticipare (lead), ritardare (lag) o seguire (match) per ogni risorsa, in base ai tempi di approvvigionamento, al costo della carenza e al costo del sovradimensionamento. Scrivi la scelta e rivedila.
6. **Chiedi al business della domanda.** Incontra i responsabili di marketing, vendite e operations con un ciclo regolare per sapere di campagne, lanci e picchi stagionali. Registra il carico atteso con intervalli.
7. **Osserva la saturazione.** Monitora quanto sono piene le risorse chiave e imposta allarmi ben prima del punto in cui le prestazioni peggiorano. Conosci il livello a cui il tuo servizio inizia a rallentare.
8. **Testa prima del picco.** Esegui test di carico e di prestazioni che somiglino al traffico reale, prima dei picchi noti e dopo modifiche significative. Correggi ciò che trovi finché c'è tempo.
9. **Testa il guasto, non solo il carico.** Esercitati a perdere un componente, una zona o un fornitore in un ambiente sicuro e vedi se la disponibilità regge (vedi la competenza chaos testing più avanti).
10. **Includi la capacità nel lavoro di cambiamento e rilascio.** Chiedi in progettazione e revisione se una modifica altera il fabbisogno di risorse. Aggiungi controlli delle prestazioni alla pipeline per i percorsi che contano (vedi Argomento 3.5 — Gestione di rilasci e deployment).
11. **Usa l'error budget per risolvere i compromessi.** Quando c'è budget, spendilo in cambiamento. Quando è esaurito, spendi lo sforzo in affidabilità e capacità. Rivedi la regola con delivery e operations insieme.
12. **Confronta le previsioni con i consuntivi.** Ogni trimestre, confronta domanda prevista e reale e aggiusta il tuo metodo. Tratta le sorprese come informazioni.

## Domande da discutere con il team

**Di che cosa hanno davvero bisogno i nostri utenti in disponibilità, velocità e capacità, e chi l'ha deciso?**

Chiedi gli obiettivi attuali e da dove vengono. Spesso sono stati fissati molto tempo fa, o dal team senza chiedere agli utenti. Chiedi a utenti e clienti che cosa fa più male. Discuti se gli obiettivi corrispondono. Chi facilita può chiedere che cosa succederebbe se l'obiettivo fosse un gradino più in basso e che cosa libererebbe.

**Quanto ci costa il prossimo nove?**

Scegli un servizio con un alto obiettivo di disponibilità. Stima quanto costerebbe alzarlo o abbassarlo di un gradino, in denaro e in lavoro ritardato. Confronta con il valore per gli utenti. L'esempio del capitolo SRE mostra quanto rapidamente l'aritmetica possa rivoltarsi contro un obiettivo più alto. Fai il calcolo con i tuoi numeri e registra le ipotesi.

**Qual è il prossimo picco di domanda che conosciamo, e che cosa abbiamo fatto per prepararci?**

Elenca i picchi noti: una campagna, una scadenza, una corsa stagionale. Per ciascuno, chiedi chi conosce il carico atteso e se il servizio è stato testato a quel livello. Spesso nessuno l'ha chiesto. Concorda una persona che raccolga i numeri e una data per il test.

**Dove il nostro servizio è più vicino alla saturazione, e che cosa succede quando ci arriva?**

Chiedi la risorsa più usata. Guarda la tendenza. Chiedi che cosa fa il servizio a quel limite: rallenta, dà errori o si guasta. Se nessuno lo sa, testalo. Scegli una soglia a cui agire e un allarme per essa.

**Quale delle nostre ultime modifiche ha influito su prestazioni o capacità, e lo sapevamo in anticipo?**

Rivedi le modifiche recenti e chiedi come sono state verificate le prestazioni. Se non lo sono state, discuti che cosa sarebbe un controllo leggero. Le opzioni tipiche sono un test sul percorso critico o un canary release con monitoraggio. Concorda un controllo per il prossimo rilascio.

**Se un componente si guastasse ora, che cosa succederebbe alla disponibilità?**

Prendi un servizio chiave e ripercorri il guasto di un database, di una zona o di un fornitore. Chiedi che cosa presuppone il progetto e che cosa è stato testato. I divari tra ipotesi e prove sono rischi. Pianifica un test di guasto controllato in un ambiente sicuro.

## Nella pratica: un esempio di ITIL agile

Un ente previdenziale nazionale gestisce un servizio online in cui i cittadini controllano i propri diritti e inviano moduli. Il servizio ha un anno tranquillo tranne le settimane dopo l'invio degli estratti conto annuali, quando il traffico sale a diverse volte il livello normale. L'anno scorso il servizio è rallentato al punto che molti utenti hanno rinunciato e il call center è stato sopraffatto. Il team di piattaforma di nove persone e il responsabile delle operations vogliono evitare una ripetizione.

Il team parte chiedendo all'ufficio comunicazione il carico atteso. L'ufficio dice che gli estratti conto saranno inviati in due lotti e dà le date, ma nessuna cifra. Il team stima l'intervallo dai dati dell'anno scorso e fissa un obiettivo: la pagina dei moduli deve rispondere entro un tempo accettabile al picco atteso, e il servizio deve restare disponibile durante i due lotti. Eseguono un test di carico su una copia della produzione e scoprono che il database è la prima risorsa a saturarsi, ben al di sotto del picco previsto. Adottano una strategia "lead" per il database, perché il tempo per aggiungere capacità è lungo, e una strategia "match" per i server web, che si possono aggiungere in minuti. Un test di guasto mostra che perdere un nodo del database dimezza la capacità, il che sarebbe inaccettabile al picco, quindi aggiungono un nodo di riserva.

Al picco, il servizio resta attivo e i tempi di risposta reggono nel primo lotto. Nel secondo lotto un componente di conferma dei pagamenti che nessuno aveva testato rallenta sotto carico, e alcuni utenti vedono ritardi. Il team non conosceva il limite di quella dipendenza e non era stato informato che il secondo lotto sarebbe stato più grande. Aggiungono il componente al prossimo test di carico, chiedono all'ufficio comunicazione il volume di ogni lotto con più anticipo e concordano di rivedere il processo di previsione nel prossimo trimestre.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery influenzano tutti e tre gli aspetti attraverso progettazione e cambiamenti. Includi prestazioni e capacità nelle revisioni di progetto e nella pipeline. Di' alle operations delle modifiche che alterano il carico e chiedi al business la domanda attesa.

### Team di servizio e di operations

I team operativi di solito portano il monitoraggio e i piani di capacità. Monitora saturazione e tendenza, tieni una visione dei tempi di approvvigionamento delle risorse e porta prove alla pianificazione. Aiuta il business a capire quanto costa ogni livello di disponibilità.

### Leadership e governance

I leader fissano il prezzo che sono disposti a pagare per affidabilità e velocità. Chiedi obiettivi che corrispondano alle esigenze degli utenti, con i costi, e accetta che la disponibilità perfetta non sia un obiettivo sensato. Sostieni i test prima dei picchi noti e il budget per la resilienza dove conta.

### Clienti e utenti

Clienti e utenti ne avvertono il risultato. Di' al fornitore quando prevedi un carico extra, come una campagna o una scadenza, e che cosa conta di più per te in velocità e disponibilità. Segnala la lentezza oltre alle interruzioni, perché entrambe sono guasti dal tuo lato.

## Modalità di fallimento comuni

- **Obiettivi per abitudine.** I "cinque nove" sono pretesi senza chiedere perché. Ricava invece gli obiettivi dalle esigenze degli utenti e dai loro un prezzo.
- **Picchi a sorpresa.** Il business conosce una campagna e l'IT no. Incontratevi invece con un ciclo regolare e registra il carico atteso.
- **Medie per le prestazioni.** I valori anomali lenti restano invisibili. Guarda invece i percentili alti e la saturazione.
- **Capacità aggiunta solo dopo i guai.** La strategia lag è usata per caso. Scegli invece una strategia di proposito, in base ai tempi di approvvigionamento.
- **Resilienza non testata.** La ridondanza esiste sulla carta. Testa invece il guasto dei componenti in un ambiente sicuro.
- **Modifiche senza controlli delle prestazioni.** Un rilascio peggiora la velocità. Aggiungi invece controlli alla pipeline per i percorsi che contano.
- **Dimenticare le dipendenze.** Un componente di terze parti limita l'intero servizio. Elenca invece le dipendenze e testale.
- **Trattare la previsione come fissa.** I piani ignorano l'errore. Usa invece intervalli e confronta le previsioni con i consuntivi.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Obiettivi e costo | Gli obiettivi sono informali o copiati | Alcuni servizi hanno obiettivi dichiarati | I servizi hanno obiettivi concordati di disponibilità, prestazioni e carico con costi noti | Obiettivi e costi sono rivisti rispetto ai risultati | Gli obiettivi sono fissati congiuntamente con clienti e fornitori e aggiustati dalle prove |
| Pianificazione di domanda e capacità | La capacità è aggiunta dopo i guai | Alcuni team prevedono i picchi noti | La domanda è raccolta dal business a ciclo regolare, con una strategia di capacità dichiarata | L'accuratezza delle previsioni è monitorata e i metodi migliorati | La pianificazione è coordinata tra team, fornitori e business |
| Test | Pochi test di carico o di guasto | Alcuni test prima dei grandi eventi | I test di carico e di guasto sono routine per i servizi chiave | I risultati dei test guidano miglioramenti monitorati | I test sono condivisi e coordinati tra servizi dipendenti |
| Monitoraggio e risposta | I problemi sono notati tardi | Una parte della saturazione è monitorata | Saturazione, latenza ed errori sono monitorati con allarmi prima dei limiti | Tendenze e soglie sono regolate dai dati | Segnali e risposte sono coordinati tra team e fornitori |

## Checklist

- [ ] Ogni servizio ha obiettivi dichiarati per disponibilità, prestazioni e carico, con la loro fonte.
- [ ] Abbiamo stimato quanto costerebbe il livello successivo di disponibilità.
- [ ] Sappiamo come è misurata la disponibilità per ogni servizio e che cosa conta come indisponibilità.
- [ ] Abbiamo scelto una strategia di capacità per ogni risorsa chiave.
- [ ] Incontriamo regolarmente il business per conoscere la domanda attesa.
- [ ] La saturazione delle risorse chiave è monitorata con allarmi prima dei limiti.
- [ ] Sono stati eseguiti test di carico prima dell'ultimo picco noto.
- [ ] Il guasto di almeno un componente chiave è stato testato in un ambiente sicuro.
- [ ] Le modifiche che influiscono su prestazioni o capacità sono segnalate in revisione.
- [ ] Le previsioni sono confrontate con la domanda effettiva ogni trimestre.

## Prompt per l'IA

**Scopo: trasformare i dati misurati in una visione del margine di capacità.**

```text
Here are the measurements for [resource, e.g. "database CPU"] for [service] over [period]: [paste real values or summary figures such as daily peak and average].
Known limit at which performance degrades, if you know it: [paste, or write "unknown"].
Expected demand change: [describe, with source].

Using only my data, describe the trend and how much headroom there appears to be at the observed peak, in plain words. Show how headroom would change if demand grew by the amounts I gave. Do not invent limits or growth rates. Say what extra data would make the analysis more reliable, and list what you are unsure of.
```

**Scopo: dare un prezzo a un obiettivo di disponibilità più alto.**

```text
Help me compare the cost and value of raising the availability target for [service] from [current target] to [proposed target].

What the service is worth, with source (revenue, cost of an outage, or other value; use only figures I provide): [paste].
What the extra availability would require (redundancy, staff, tools), with cost estimates I have: [paste, or write "unknown"].
Current measured availability: [paste].

Calculate the allowed unplanned downtime or error count at each target using only the numbers I gave, show the difference, and compare with the value and cost figures if I provided them. State your assumptions. Do not invent costs or revenue. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: pianificare un test di carico prima di un picco noto.**

```text
Plan a load test for [service] before this event: [describe the peak, with date and source of the expected load].

Architecture, in brief: [describe components, dependencies, and suppliers].
Expected load range, with the source: [paste].
Test environment available: [describe].

Give a plan with: goals, what to measure (latency distribution, errors, saturation), scenarios to run, how to ramp up, what to do with results, and risks to production or to suppliers (for example agreements that need to be made before testing). Do not invent figures. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: progettare un test di guasto.**

```text
Help me design a controlled failure test for [service].

What I want to learn: [for example whether availability holds if one database node fails].
Environment for the test: [describe, e.g. a production-like test environment].
Safeguards available: [monitoring, rollback, people on hand].

Describe a step-by-step test plan: hypothesis, what to break and how, what to observe, who is present, what stops the test, and how to record what happened. Keep it away from production unless I say it is safe. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): da usare per stimare le risorse di cui un servizio ha bisogno nel tempo e scegliere una strategia per aggiungerle.
- [demand-forecasting](../../../../skills/demand-forecasting/SKILL.md): da usare per stimare il carico futuro come intervallo da dati passati e piani di business.
- [load-testing](../../../../skills/load-testing/SKILL.md): da usare per progettare test che applicano una domanda realistica prima di un picco.
- [performance-testing](../../../../skills/performance-testing/SKILL.md): da usare per verificare velocità e uso delle risorse sui percorsi critici come parte della delivery.
- [chaos-testing](../../../../skills/chaos-testing/SKILL.md): da usare per verificare se la disponibilità regge quando i componenti si guastano.

## Fonti principali

- **Embracing Risk** (*Site Reliability Engineering*, Google, sre.google): l'economia della disponibilità, la misurazione basata sulle richieste e l'error budget.
- **Capacity planning** (Wikipedia): definizioni e strategie lead, lag, match e adjustment.
- **Monitoring Distributed Systems** (*Site Reliability Engineering*, Google, sre.google): i segnali d'oro, compresa la saturazione.
- **High availability** (Wikipedia): contesto sulla progettazione di sistemi per il funzionamento continuo.

## Riferimenti

1. Embracing Risk — Google SRE book, sre.google — https://sre.google/sre-book/embracing-risk/
2. Capacity planning — Wikipedia — https://en.wikipedia.org/wiki/Capacity_planning
3. Monitoring Distributed Systems — Google SRE book, sre.google — https://sre.google/sre-book/monitoring-distributed-systems/
4. Service Level Objectives — Google SRE book, sre.google — https://sre.google/sre-book/service-level-objectives/
5. High availability — Wikipedia — https://en.wikipedia.org/wiki/High_availability
6. Scalability — Wikipedia — https://en.wikipedia.org/wiki/Scalability
7. Load testing — Wikipedia — https://en.wikipedia.org/wiki/Load_testing
8. Chaos engineering — Wikipedia — https://en.wikipedia.org/wiki/Chaos_engineering
9. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
