# Gestione finanziaria IT e FinOps

**La gestione finanziaria IT mostra quanto costano i servizi e quale valore restituiscono, e il FinOps è la pratica culturale che riunisce ingegneri, finanza e team di business perché la spesa tecnologica, soprattutto nel cloud, sia compresa e gestita mentre avviene.**

## Perché è importante

Il denaro decide quali servizi esistono, quanto bene sono dotati di personale e quanto durano. Per anni la finanza IT ha significato un budget annuale, un foglio di calcolo di allocazione dei costi e l'occasionale discussione su chi paga la rete. Il cloud computing ha cambiato questo. Le risorse possono essere create in pochi secondi da chiunque abbia i permessi giusti e la fatturazione segue l'uso. Un singolo job mal configurato può aggiungere migliaia di dollari a una fattura mensile prima che qualcuno se ne accorga, e una modifica ponderata può farne risparmiare altrettanti.

Per i team agili, il cambiamento è a doppio taglio. Guadagnano la libertà di sperimentare e scalare senza aspettare l'hardware. Si assumono anche una responsabilità che prima stava con finanza e acquisti: sapere quanto costano le proprie scelte. Nel frattempo, il personale finanziario che pianifica con cicli annuali affronta un uso che varia ogni giorno. Nessuna delle due parti può gestire bene il costo da sola.

La Wikipedia inglese non ha un articolo intitolato "FinOps" all'indirizzo verificato. Il sito della FinOps Foundation stessa definisce il FinOps come un framework operativo e una pratica culturale che massimizza il valore di business della tecnologia e crea responsabilità finanziaria attraverso la collaborazione tra team di ingegneria, finanza e business. L'articolo di Wikipedia sul cloud computing descrive modelli di prezzo e controllo dei costi e porta un avviso di manutenzione che parti di esso possono essere non verificate. Il vocabolario finanziario ITIL qui, come budgeting, contabilità e addebito, è tratto da descrizioni ampiamente pubblicate che questa guida non ha potuto confermare rispetto al testo del proprietario del framework.

## Concetti fondamentali

### Gestione finanziaria IT

La gestione finanziaria IT (in ITIL, "financial management for IT services") è ampiamente descritta come la pratica di gestire il denaro di un fornitore di servizi IT: pianificare i budget, contabilizzare i costi e, dove rilevante, addebitare i servizi. Il suo scopo è dare a chi decide le informazioni per bilanciare costo e valore. Le fonti lette per questa guida non definiscono la pratica, quindi queste descrizioni sono uso comune, offerte come tali.

| Attività | Domanda a cui risponde |
|---|---|
| **Budgeting e pianificazione** | Quanto spenderemo, e per che cosa, nel prossimo periodo? |
| **Contabilità dei costi** | Quanto costa fornire ciascun servizio? |
| **Addebito o allocazione** | Chi paga, e come? |
| **Analisi di valore e investimento** | Un servizio o una modifica vale il suo costo? |

### Showback e chargeback

Due accordi per condividere il costo sono ampiamente usati. Nello **showback**, ai consumatori viene mostrato ciò che usano e quanto costa, ma non sono fatturati. Nel **chargeback**, sono fatturati o il costo è spostato sul loro budget. Lo showback costruisce consapevolezza con poco attrito; il chargeback crea responsabilità e può creare dispute sulle regole di allocazione. Scegline uno chiedendo quale comportamento vuoi e se i dati sono abbastanza buoni da essere difesi.

### Cloud e modello a consumo

Wikipedia dice che il cloud computing può ridurre la spesa in conto capitale iniziale spostandosi a un modello di spesa operativa in cui i costi scalano con l'uso e che l'infrastructure as a service è fatturata su base di utility. Descrive il software come servizio come tipicamente una tariffa fissa mensile o annuale per utente, oppure a consumo. Il suo elenco di preoccupazioni sul controllo dei costi include risorse inutilizzate, configurazioni inefficienti e costi nascosti. Nota che i fornitori offrono strumenti di costo e cita il FinOps come framework per standardizzare le operazioni finanziarie del cloud.

L'articolo riferisce risultati di indagini: un sondaggio Gartner su 200 responsabili IT ha trovato che il 69 percento ha avuto sforamenti del budget cloud nel 2023, mentre gli altri attribuivano merito a previsione, monitoraggio della spesa e ottimizzazione; e il rapporto 2024 di Flexera ha indicato la gestione della spesa cloud come la principale sfida, riferendo che la spesa nel cloud pubblico ha superato i budget in media del 15 percento. L'articolo porta un avviso su testo non verificato, quindi controlla queste cifre sui rapporti originali prima di citarle.

### Che cos'è il FinOps

Il sito della FinOps Foundation definisce il FinOps come "an operational framework and cultural practice" che "maximizes the business value of technology" e "creates financial accountability through collaboration between engineering, finance, and business teams". Dice che il nome combina "Finance" e "DevOps" e che il focus si estende oltre il cloud a software as a service, licenze, data center e altro. Punti chiave dal sito:

- **È uno sport di squadra.** Il sito nomina questi gruppi: dirigenti, ingegneri, professionisti FinOps, operations e finanza e acquisti e dice che il FinOps cambia il modo in cui team disparati lavorano insieme. Un singolo team non può farlo da solo.
- **Usa un approccio di maturità** descritto come "Crawl, Walk, Run".
- **La Foundation** è descritta come un progetto sotto LF Projects, una serie della Linux Foundation, e sostiene una specifica tecnica open source chiamata FOCUS (FinOps Open Cost and Usage Specification). Offre anche formazione e certificazione.

La pagina letta per questa guida non elenca i principi né le fasi, quindi questo argomento non li indica. Consulta direttamente le pagine della Foundation su principi e fasi.

### Dati di costo ed etichettatura

Comunque si chiami la pratica, dipende dalla capacità di attribuire il costo. Questo richiede due cose: tag o etichette sulle risorse che dicono chi le possiede e quale servizio supportano (vedi Argomento 4.1 — Gestione degli asset IT), e dati di fatturazione che possano essere raggruppati per quei tag. FOCUS esiste per standardizzare il formato dei dati di costo e uso tra i fornitori. Il costo senza tag è costo senza responsabile.

### Costi unitari e valore

Una fattura totale dice poco. Dividi il costo per qualcosa che significhi qualcosa per il business: per transazione, per utente, per servizio, per ambiente. Un costo totale in crescita con un costo unitario in calo può essere crescita sana. Un costo totale in calo con un costo unitario in crescita può segnalare un problema. Il costo unitario collega la finanza ai livelli di servizio e al valore (vedi Argomento 3.7 — Gestione dei livelli di servizio).

### Costo, affidabilità e velocità

Il denaro compra affidabilità e velocità, e ogni livello in più ha un prezzo (vedi Argomento 3.11 — Disponibilità, capacità e prestazioni). Un team che taglia i costi con leggerezza può ridurre la resilienza. Un team che non guarda mai ai costi può sovradimensionare. Le conversazioni FinOps sono un luogo per rendere esplicito quel compromesso, con gli ingegneri che descrivono le opzioni e finanza e business che le valutano.

### Governance e rischio

I controlli finanziari includono budget e allarmi, approvazione per impegni elevati, limiti su chi può creare risorse costose e revisioni regolari. Gli impegni verso i fornitori, come gli accordi di acquisto a lungo termine, possono abbassare il costo e aggiungere rischio se l'uso cala. Sono decisioni per finanza, acquisti e ingegneria insieme (vedi Argomento 5.7 — Governance, rischio e conformità e Argomento 3.14 — Gestione dei fornitori).

### Limiti delle fonti

La pagina della FinOps Foundation è un riassunto dell'organizzazione che promuove la pratica e non dà data di fondazione, cifre dei membri né prove di risultati. L'articolo sul cloud computing è segnalato per testo non verificato e non dà i meccanismi di prezzo, le tariffe di uscita né i dettagli di una pratica FinOps. Questo argomento va trattato come un'introduzione; leggi i materiali della Foundation e la documentazione del tuo fornitore per i dettagli.

## Buone pratiche

1. **Rendi visibile il costo a chi lo causa.** Mostra a ogni team il costo dei servizi che possiede, almeno ogni mese, in una forma che possa capire. Le persone gestiscono ciò che vedono.
2. **Etichetta tutto ciò che costa denaro.** Richiedi tag di responsabile, servizio e ambiente sulle risorse cloud e riferisci sulla spesa senza tag. Correggilo prima di ottimizzare qualsiasi altra cosa.
3. **Parti dallo showback.** Mostra ai team i loro costi prima di addebitarli. Passa al chargeback solo quando i dati sono affidabili e il beneficio è chiaro.
4. **Usa i costi unitari.** Esprimi il costo per transazione, utente o servizio, oltre che in totale. Rivedi la tendenza insieme a domanda e qualità.
5. **Fissa budget e allarmi.** Concorda budget per servizio o team e imposta allarmi ben prima del limite. Rivedi gli allarmi con i responsabili, non solo con la finanza.
6. **Porta finanza e ingegneria in un'unica conversazione.** Tieni una revisione regolare in cui gli ingegneri spiegano che cosa guida il costo e la finanza spiega i vincoli. Includi un responsabile di business che possa giudicare il valore.
7. **Cerca prima lo spreco.** Trova risorse inutilizzate o sovradimensionate, ambienti inattivi e abbonamenti dimenticati. Questi risparmi comportano poco rischio (vedi Argomento 4.2 — Gestione degli asset software per gli abbonamenti).
8. **Pesa i risparmi rispetto all'affidabilità.** Prima di tagliare, chiedi che cosa fa la modifica a disponibilità, prestazioni e ripristino. Registra il compromesso.
9. **Pianifica con cura gli impegni.** Gli impegni d'acquisto verso i fornitori possono ridurre il costo, ma bloccano la spesa. Basali su un uso stabile e rivedili regolarmente.
10. **Dai ai team autorità e limiti.** Lascia che i team prendano decisioni di costo entro limiti concordati e richiedi l'approvazione per quelle oltre i limiti. Autonomia con visibilità funziona meglio del solo controllo centrale.
11. **Includi il costo nella progettazione e nella definition of done.** Chiedi nelle revisioni di progetto quanto costerà far girare una funzionalità e verifica dopo il rilascio.
12. **Impara e condividi.** Pubblica brevi note su che cosa ha fatto risparmiare e che cosa si è ritorto contro. Usa un approccio di maturità come "crawl, walk, run" per far crescere la pratica.

## Domande da discutere con il team

**Sappiamo quanto costa far girare il nostro servizio principale, e chi possiede quel numero?**

Chiedi il costo mensile del servizio più grande e come è calcolato. Spesso nessuno sa rispondere, o la risposta viene da fonti diverse. Chi facilita può chiedere che cosa servirebbe per produrre il numero in modo affidabile, come tag e un report. Scegli un servizio da cui partire.

**Quale quota della nostra spesa cloud possiamo attribuire a un responsabile nominato?**

Chiedi la quota senza tag. Una grande quota significa che il costo non può essere gestito. Discuti perché le risorse non hanno tag: nessuna regola, nessuno strumento o nessun incentivo. Concorda una regola di etichettatura e una data per un primo report.

**Quando abbiamo trovato per l'ultima volta una sorpresa di costo, e come l'abbiamo scoperta?**

Raccogli esempi: un ambiente dimenticato, un job fuori controllo, un abbonamento rinnovato. Chiedi quanto è rimasto in funzione prima della scoperta. Discuti allarmi e revisioni che l'avrebbero colto. Scegli un allarme da aggiungere.

**Che cosa taglieremmo se il budget calasse del dieci percento, e che cosa perderemmo?**

Chiedi al team di proporre opzioni e di nominare le conseguenze, anche per l'affidabilità. Questa domanda rende espliciti i compromessi. Non trattare le risposte come un piano; usale per avviare una conversazione con finanza e business sul valore.

**Quali decisioni di spesa prendono oggi gli ingegneri, e quali dovrebbero prendere?**

Elenca le decisioni di costo che i team prendono: dimensioni, ambienti, strumenti, acquisti. Chiedi quali informazioni usano. Discuti quali limiti sarebbero ragionevoli. Concorda una decisione da affidare con limiti.

**Come parlano tra loro finanza e ingegneria, e quando?**

Chiedi a entrambi i gruppi. Risposte tipiche: al momento del budget, o quando qualcosa va male. Discuti una revisione congiunta regolare. La pagina della FinOps Foundation nomina la collaborazione tra ingegneri, finanza e team di business come cuore della pratica. Concorda chi organizzerà la prima.

## Nella pratica: un esempio di ITIL agile

Un servizio bibliotecario nazionale ha spostato nell'arco di tre anni il proprio catalogo digitale, la ricerca e gli archivi pubblici su un fornitore cloud. Al direttore IT il reparto finanza chiede perché la fattura mensile del cloud sia triplicata dal trasferimento e perché sia difficile da spiegare. Un team di dieci persone gestisce la piattaforma e ciascuno dei cinque team di progetto ha il proprio account cloud.

Il direttore IT e un analista finanziario partono chiedendo i dati di costo raggruppati per servizio. La maggior parte delle risorse non ha tag, quindi solo un terzo del costo può essere attribuito. Concordano una regola di etichettatura con i cinque team e fanno girare un report settimanale che elenca la spesa senza tag per account. In sei settimane la quota senza tag scende sotto un decimo. L'analista imposta poi un report mensile di showback per ogni team, che mostra il costo per servizio e il costo per mille ricerche per il servizio di ricerca. Nella prima revisione, gli ingegneri individuano un ambiente di sviluppo che gira a dimensione di produzione da un anno e un job di elaborazione dati che scansiona un archivio più spesso del necessario. Entrambi vengono corretti. Una riunione mensile con il responsabile delle collezioni della biblioteca permette agli ingegneri di spiegare che cosa guida il costo, come il grande volume di immagini scansionate, e al responsabile di decidere quali collezioni digitalizzare per prime.

Dopo due trimestri, i costi unitari calano e la fattura è prevedibile. Non tutto va liscio. Una modifica per risparmiare sull'indice di ricerca riduce la velocità nei momenti di punta e gli utenti si lamentano finché il team non ripristina la capacità. Il reparto finanza vuole anche acquistare un impegno di un anno con il fornitore, mentre gli ingegneri non sono sicuri che l'uso resti stabile, perché è prevista una migrazione. Concordano di impegnarsi solo per la parte stabile dell'uso e di rivedere l'impegno quando il piano di migrazione sarà chiaro.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery prendono la maggior parte delle decisioni di costo attraverso progettazione e configurazione. Etichetta ciò che crei, osserva i tuoi costi e chiedi quanto costerà far girare una funzionalità. Spiega i fattori di costo a finanza e business in termini semplici.

### Team di servizio e di operations

I team operativi vedono utilizzo e spreco. Condividi i dati su risorse inattive e sovradimensionate, aiuta a impostare allarmi sensati e assicurati che i risparmi non minino la resilienza. Mantieni visibile il legame tra costo, capacità e livelli di servizio.

### Leadership e governance

Leader e finanza fissano budget, regole e responsabilità. Chiedi costi unitari e tendenze, sostieni un modello di showback o chargeback di cui le persone si fidino e prendi con gli ingegneri le decisioni sugli impegni. Evita tagli che danneggiano l'affidabilità senza discutere il compromesso.

### Clienti e utenti

Clienti e utenti pagano i servizi direttamente o indirettamente. Chiedi ai fornitori che cosa guida il prezzo dei servizi che usi e di' loro quale valore conta di più. Se ti viene addebitato il costo, aspettati spiegazioni chiare e un modo di mettere in discussione le cifre.

## Modalità di fallimento comuni

- **Costo senza tag.** Nessuno possiede la fattura. Richiedi invece i tag e riferisci sul divario.
- **Finanza e ingegneria in stanze separate.** Ciascuna parte agisce su informazioni parziali. Tieni invece una revisione congiunta regolare con un responsabile di business.
- **Chargeback prima che i dati siano affidabili.** Le dispute consumano tempo. Parti invece dallo showback e migliora i dati.
- **Totali senza costi unitari.** La crescita sembra spreco o il contrario. Monitora invece il costo per transazione, utente o servizio.
- **Tagliare i costi a spese della resilienza.** I risparmi causano interruzioni. Indica invece il compromesso e coinvolgi il responsabile del servizio.
- **Impegnarsi troppo.** Acquisti a lungo termine bloccano una spesa che l'uso non può sostenere. Impegnati invece solo per l'uso stabile e rivedi.
- **Solo controllo centrale.** I team aspettano l'approvazione e aggirano il processo. Dai invece ai team autorità entro limiti, con visibilità.
- **Citare cifre di indagini come fatto.** Numeri da indagini dei fornitori guidano le decisioni. Controlla invece le fonti originali e usa i tuoi dati.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Visibilità e attribuzione | Il costo si vede solo come fattura totale | Alcuni team vedono il proprio costo | La maggior parte della spesa è etichettata e attribuita a servizi e responsabili | Costi unitari e tendenze sono rivisti rispetto a domanda e qualità | I dati di costo sono condivisi tra team, fornitori e finanza in un formato comune |
| Governance e budget | I budget sono annuali e fissi | Esistono alcuni budget e allarmi | Budget, allarmi e limiti di approvazione sono standard | Gli scostamenti sono indagati e le regole regolate | Le regole di budget sono allineate in tutta l'organizzazione e con i partner |
| Collaborazione | Finanza e ingegneria si incontrano al momento del budget | Alcune conversazioni congiunte | Una revisione congiunta regolare con un responsabile di business | Decisioni ed esiti sono monitorati e migliorati | Finanza, ingegneria, business e fornitori condividono obiettivi e dati |
| Ottimizzazione | I risparmi vengono dalle crisi | Una parte dello spreco è trovata | Spreco, dimensionamento e impegni sono rivisti regolarmente | I risparmi sono misurati rispetto ai rischi per l'affidabilità | L'ottimizzazione è routine, condivisa e bilanciata con gli obiettivi di servizio |

## Checklist

- [ ] Sappiamo indicare il costo mensile di ogni servizio principale e chi lo possiede.
- [ ] Le risorse cloud portano tag di responsabile, servizio e ambiente e la spesa senza tag è segnalata ogni settimana o ogni mese.
- [ ] I team ricevono un report di costo regolare per i servizi che possiedono (showback).
- [ ] Monitoriamo almeno un costo unitario per ogni servizio principale.
- [ ] Esistono budget e allarmi con responsabili e gli allarmi scattano ben prima dei limiti.
- [ ] Finanza, ingegneria e un responsabile di business si incontrano regolarmente su costo e valore.
- [ ] Rivediamo risorse e abbonamenti inutilizzati e sovradimensionati almeno ogni trimestre.
- [ ] I tagli di costo sono rivisti per gli effetti su affidabilità e prestazioni.
- [ ] Gli impegni d'acquisto sono basati su un uso stabile e rivisti.
- [ ] Abbiamo controllato le cifre delle indagini dei fornitori sulle fonti originali prima di usarle.

## Prompt per l'IA

**Scopo: analizzare un report di costo per spesa senza responsabile e insolita.**

```text
Here is a cost report for the last [period], grouped by account, service, and tag: [paste real data; remove sensitive details].

Using only this data, calculate: total cost, the share with no owner tag, the five largest cost items and their share of total, and any item whose cost changed by more than [threshold you choose, e.g. 25%] from the previous period if I included it. For each unusual item, suggest a question for its owner. Do not guess at causes or invent numbers. List what you are unsure of.
```

**Scopo: definire un costo unitario per un servizio.**

```text
Help me define a unit cost for [service].

What the service does: [describe].
What the business cares about (transactions, users, searches, documents): [describe].
Cost data we have: [describe sources and how they are grouped].
Demand data we have: [describe].

Propose two or three candidate unit costs, how to calculate each from the data I listed, what could distort them, and what decisions each would help. Do not invent figures. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: prepararsi a una revisione congiunta tra ingegneria e finanza.**

```text
Plan a 45-minute monthly review between engineering, finance, and a business owner about the cost of [service or portfolio].

Inputs: [cost report, unit cost, budget status, forecast; describe what you have].
Concerns on each side: engineering [list]; finance [list]; business [list].

Provide a timed agenda, five questions for each group, a one-page summary template with only the figures I supply, and a closing step that records decisions and owners. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: pesare una proposta di risparmio rispetto all'affidabilità.**

```text
We are considering this cost-saving change: [describe].
Expected saving, with source: [paste, or write "not estimated"].
What the service promises to users (service levels): [paste].
Current performance against those promises: [paste].
Known dependencies: [list].

List the ways the change could affect availability, performance, recovery, and security, as questions for the service owner. Suggest a small trial, what to monitor, and what would make us reverse it. Do not invent estimates. Ask clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [budget-forecasting](../../../../skills/budget-forecasting/SKILL.md): da usare per prevedere la spesa IT e cloud e spiegare gli scostamenti.
- [demand-forecasting](../../../../skills/demand-forecasting/SKILL.md): da usare per stimare il carico futuro così che le previsioni di costo riflettano la domanda.
- [capacity-planning](../../../../skills/capacity-planning/SKILL.md): da usare per collegare i fabbisogni di risorse a costo e livelli di servizio.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): da usare per gestire contratti e impegni con i fornitori.
- [portfolio-management](../../../../skills/portfolio-management/SKILL.md): da usare per scegliere e finanziare servizi e iniziative in base a valore e costo.

## Fonti principali

- **What is FinOps?** (FinOps Foundation, finops.org): la definizione della Foundation stessa e la descrizione della collaborazione tra team di ingegneria, finanza e business.
- **Cloud computing** (Wikipedia): contesto su modelli di prezzo, controllo dei costi e responsabilità condivisa, con un avviso su testo non verificato.
- **Total cost of ownership** (Wikipedia): contesto sul contare tutti i costi di un asset o servizio lungo la sua vita.
- **Software as a service** (Wikipedia): contesto sui prezzi in abbonamento.

## Riferimenti

1. What is FinOps? — FinOps Foundation, finops.org — https://www.finops.org/introduction/what-is-finops/
2. Cloud computing — Wikipedia — https://en.wikipedia.org/wiki/Cloud_computing
3. Total cost of ownership — Wikipedia — https://en.wikipedia.org/wiki/Total_cost_of_ownership
4. Software as a service — Wikipedia — https://en.wikipedia.org/wiki/Software_as_a_service
5. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
6. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
7. Operating expense — Wikipedia — https://en.wikipedia.org/wiki/Operating_expense
8. Capital expenditure — Wikipedia — https://en.wikipedia.org/wiki/Capital_expenditure
9. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
