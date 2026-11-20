# Metriche e misurazione

**Una buona misurazione aiuta un team a vedere se il proprio lavoro sta aiutando gli utenti e migliorando, e il modo più sicuro di usare qualsiasi misura è come domanda da discutere, mai come obiettivo da raggiungere.**

## Perché è importante

I team hanno bisogno di numeri per orientarsi. Senza di essi, le decisioni si affidano alla memoria, alle voci più forti e a chi ha parlato per ultimo. Con i numeri sbagliati, le decisioni possono essere peggiori che senza: un team che conta i ticket chiusi impara a chiudere in fretta i ticket, che i problemi degli utenti siano risolti o no. La misurazione è potente e cambia il comportamento in modi che chi la progetta non sempre intende.

Questa guida ha già usato molte misure: le misure di consegna del software di DORA (vedi Argomento 3.4 — Abilitazione dei cambiamenti), le quattro misure di flusso della Kanban Guide (vedi Argomento 1.5 — Kanban), indicatori e obiettivi di livello di servizio (vedi Argomento 3.7 — Gestione dei livelli di servizio) e il carico di reperibilità (vedi Argomento 3.10 — Monitoraggio e gestione degli eventi). Questo argomento le riunisce, aggiunge la definizione degli obiettivi con objectives and key results e misure di soddisfazione dei clienti e le pone di fronte al più vecchio avvertimento del settore: la legge di Goodhart.

L'[articolo di Wikipedia sulla legge di Goodhart](https://en.wikipedia.org/wiki/Goodhart%27s_law) dà l'adagio nella sua forma usuale, "When a measure becomes a target, it ceases to be a good measure", e lo attribuisce all'economista britannico Charles Goodhart, che in un articolo del 1975 sulla politica monetaria del Regno Unito scrisse che qualsiasi regolarità statistica osservata tende a crollare quando su di essa si esercita pressione a fini di controllo. La formulazione usuale è successiva e l'articolo la attribuisce a Keith Hoskin (1996) e al lavoro di Marilyn Strathern del 1997. Il punto ha una lunga storia in campi diversi ed è il giusto punto di partenza per questo argomento.

## Concetti fondamentali

### Misure, obiettivi e legge di Goodhart

Una **misura** descrive qualcosa. Un **obiettivo** (target) è un numero che qualcuno deve raggiungere. Il passaggio dalla prima al secondo è dove iniziano i guai. Una volta che le persone sono premiate o punite per un numero, trovano modi di muovere il numero che non coincidono con migliorare la cosa che descrive. L'articolo dà esempi dalla politica monetaria, dai sistemi scolastici e dall'assistenza sanitaria. In un'organizzazione di servizio, esempi facili sono: il tempo di chiusura dei ticket che cala perché i ticket sono chiusi presto, i conteggi dei deployment che salgono perché le modifiche sono divise e la disponibilità che sembra salire perché le interruzioni sono riclassificate.

Il rimedio non è evitare di misurare ma misurare con cura:

- Usa più misure che tirano l'una contro l'altra, come velocità e qualità.
- Discuti i numeri con le persone il cui lavoro descrivono.
- Non legare ricompense o provvedimenti individuali a un unico numero.
- Cambia le misure quando smettono di essere informative.

### Tipi di misura

| Tipo | Domanda a cui risponde | Esempi |
|---|---|---|
| **Risultato** | Utenti e business stanno meglio? | Soddisfazione degli utenti, successo dei compiti, ricavi, incidenti che danneggiano gli utenti |
| **Flusso** | Quanto bene si muove il lavoro? | Cycle time, throughput, età dell'elemento di lavoro, lavoro in corso |
| **Prestazioni di consegna** | Quanto bene le modifiche raggiungono la produzione? | Change lead time, deployment frequency, change fail rate, tempo di ripristino |
| **Livello di servizio** | Il servizio soddisfa le esigenze degli utenti? | Disponibilità, latenza, tasso di errore rispetto agli obiettivi |
| **Salute e sostenibilità** | Si può andare avanti così? | Carico di reperibilità, toil, straordinari, umore del personale |
| **Costo** | Quanto costa per unità di valore? | Costo per transazione o per utente |

Un insieme equilibrato attinge a più righe, così che migliorarne una non sia acquistato a spese di un'altra.

### Misure DORA

Le misure di prestazione della consegna del software di DORA sono change lead time, deployment frequency, failed deployment recovery time, change fail rate e deployment rework rate. La guida DORA sulle metriche dice che velocità e stabilità non sono un compromesso, perché le misure sono correlate per la maggior parte dei team. Mette in guardia dal fissarle come obiettivi, dall'affidarsi a una sola, dal confrontare applicazioni molto diverse e dal competere con altri team e consiglia di migliorare rispetto alle proprie prestazioni passate. L'articolo di Wikipedia su DevOps aggiunge che alcuni esperti hanno criticato la metodologia e le metriche della ricerca DORA, quindi trattale come domande utili con dei limiti (vedi Argomento 5.2 — DevOps).

### Misure di flusso

La Kanban Guide definisce quattro misure: lavoro in corso, throughput, età dell'elemento di lavoro e cycle time. Nota che i team possono rinominarle e dovrebbero aggiungerne altre secondo necessità e dice che le misure contano solo quando informano le pratiche di definire il workflow, gestirne gli elementi e migliorarlo. L'età dell'elemento di lavoro è particolarmente utile perché mostra i problemi quando c'è ancora tempo per agire (vedi Argomento 5.4 — Gestione del flusso di valore).

### Misure di livello di servizio

Indicatori e obiettivi di livello di servizio (vedi Argomento 3.7 — Gestione dei livelli di servizio) danno la visione più diretta di ciò che gli utenti vivono. Il libro SRE sostiene pochi indicatori scelti da ciò a cui gli utenti tengono, percentili e non solo medie e obiettivi che non siano la perfezione. Gli error budget trasformano il divario in una regola decisionale condivisa (vedi Argomento 5.3 — Site reliability engineering).

### Objectives and key results

**Objectives and key results (OKR)** sono un framework per fissare obiettivi. L'articolo di Wikipedia descrive un OKR come un obiettivo, una meta significativa, concreta e chiaramente definita, abbinato a da tre a cinque key result, che sono criteri di successo misurabili. Attribuisce ad Andrew Grove il merito di aver reso popolare l'approccio alla Intel negli anni Settanta e di averlo documentato in *High Output Management* (1983) e a John Doerr quello di averlo portato a Google nel 1999. L'articolo dice che gli OKR sono valutati da 0,0 a 1,0, che i key result ambiziosi puntano a circa 0,7 e che Doerr raccomanda un tasso di successo obiettivo di circa il 70 percento, quindi un key result sempre raggiunto andrebbe rivalutato. Consiglia di evitare obiettivi di ordinaria amministrazione e di favorire indicatori anticipatori rispetto a quelli ritardati.

L'articolo registra anche critiche: la maggior parte delle organizzazioni ha smesso di fissare OKR per i singoli collaboratori, che tendono ad assomigliare a elenchi di compiti e a confondersi con le valutazioni delle prestazioni, e gli OKR multilivello possono creare un approccio a cascata. Non dà prove indipendenti di efficacia e porta un'etichetta di manutenzione sull'affidarsi a fonti vicine all'argomento. Per i team di servizio, gli OKR possono collegare i risultati (per esempio, "gli utenti completano la registrazione senza aiuto") a key result misurabili, purché non siano trasformati in obiettivi individuali.

### Soddisfazione del cliente

Misurare che cosa pensano gli utenti è difficile da fare bene. Uno strumento comune è il **net promoter score (NPS)**. Secondo Wikipedia, si basa su una domanda sulla probabilità che gli intervistati raccomandino un'azienda, prodotto o servizio, con i promotori che danno 9 o 10, i passivi 7 o 8 e i detrattori 6 o meno; il punteggio è la percentuale di promotori meno la percentuale di detrattori. Fred Reichheld di Bain & Company lo rese popolare in un articolo del 2003 su *Harvard Business Review*. L'articolo registra i limiti: gli studiosi mettono in dubbio che preveda in modo affidabile la crescita aziendale, una singola voce richiede un gran numero di risposte, dice poco su problemi specifici, le troppe indagini attirano lamentele e legarlo alla retribuzione può distorcere il comportamento, quindi Reichheld raccomandò di separare i due. Esistono altri strumenti, come i punteggi di soddisfazione del cliente e di sforzo del cliente, ma l'articolo non li discute.

Qualunque sia lo strumento, poni una domanda breve, consenti sempre una risposta in testo libero, leggi i commenti e dai seguito a ciò che impari.

### Misurare le persone e la sostenibilità

Le misure di carico e salute del personale, come carico di reperibilità, toil, straordinari e umore, sono misure della sostenibilità del servizio (vedi Argomento 5.3 — Site reliability engineering). Trattale come informazioni sul sistema e non come misure delle prestazioni degli individui.

### Misurare IA e automazione

Quando si introduce un passaggio automatizzato o assistito dall'IA, aggiungi misure della sua qualità: quanto spesso gli esseri umani lo scavalcano, quanto spesso sbaglia e quanto costa (vedi Argomento 6.2 — L'IA nella gestione dei servizi IT).

### Limiti

Le misure sono parziali. Omettono ciò che è difficile da contare, come fiducia, maestria e giudizio. Possono ingannare quando i dati sono incompleti o le definizioni differiscono tra team. Gli articoli letti qui offrono poche prove empiriche sul fatto che i programmi di misurazione migliorino i risultati. Tratta qualsiasi programma come un esperimento e rivedilo.

## Buone pratiche

1. **Parti dalla domanda.** Chiedi quale decisione una misura informerebbe e chi agirebbe. Se nessuno lo farebbe, non raccoglierla.
2. **Scegli un piccolo insieme equilibrato.** Scegli poche misure tra risultato, flusso, consegna, livello di servizio e salute. Assicurati che alcune tirino l'una contro l'altra.
3. **Definisci ogni misura con precisione.** Scrivi che cosa è contato, da dove e che cosa è escluso. Due team che usano la stessa parola per cose diverse producono numeri non confrontabili.
4. **Misura per servizio o team e confronta con il suo passato.** Evita di classificare i team. DORA consiglia di migliorare rispetto alle proprie prestazioni passate e di fare attenzione al confronto tra applicazioni diverse.
5. **Non fare di un singolo numero un obiettivo.** Usa le misure come stimoli di discussione e fissa gli obiettivi come risultati. Quando una misura è un obiettivo, osserva la manipolazione (vedi legge di Goodhart).
6. **Abbina i numeri alle storie.** Per ogni tendenza, guarda alcuni casi reali. I numeri ti dicono dove guardare; i casi ti dicono perché.
7. **Guarda le distribuzioni.** Usa percentili e intervalli, non solo medie, per le misure di tempo e dimensione.
8. **Preferisci indicatori anticipatori dove puoi.** Misure come l'età dell'elemento di lavoro mostrano il guaio prima che arrivi, a differenza delle misure di risultati passati.
9. **Fissa gli obiettivi con objectives and key results con cura.** Se usi gli OKR, tienili a livello di team e organizzazione, evita obiettivi di ordinaria amministrazione e tratta un risultato sempre raggiunto come un segno per puntare più in alto.
10. **Chiedi agli utenti, brevemente e spesso.** Usa una domanda breve con testo libero, leggi i commenti e rispondi. Non legare i punteggi delle indagini alla retribuzione individuale.
11. **Fai attenzione al costo del misurare.** Preferisci i dati che gli strumenti producono come sottoprodotto del lavoro. Abbandona il reporting manuale che nessuno usa.
12. **Rivedi le misure stesse.** Una o due volte l'anno, chiedi quali misure hanno portato a decisioni e quali no e ritira le seconde.

## Domande da discutere con il team

**Quale delle nostre misure ha portato a una decisione negli ultimi sei mesi?**

Elenca le misure e chiedi una decisione collegata a ciascuna. Le misure senza legame sono candidate alla rimozione. Chi facilita può chiedere di quale misura le persone si fidano meno e perché. Rimuovine o correggine una.

**Che cosa succede al nostro comportamento quando un numero è un obiettivo?**

Chiedi un esempio recente in cui un numero era un obiettivo. Indaga che cosa hanno fatto le persone per raggiungerlo. L'adagio di Goodhart è la cornice. Chiedi che aspetto avrebbero una misura migliore o un abbinamento di misure. Concorda un cambiamento.

**Misuriamo insieme velocità e qualità?**

Elenca le misure di velocità e quelle di qualità. Se gli elenchi sono sbilanciati, discuti l'effetto. Per esempio, misurare il tempo di chiusura dei ticket senza i contatti ripetuti invita alla chiusura anticipata. Scegli un abbinamento.

**Che cosa ci dicono gli utenti su come va, e come lo chiediamo?**

Guarda le domande che poni agli utenti e con quale frequenza. Leggi ad alta voce alcune risposte in testo libero. Chiedi che cosa è cambiato grazie ad esse. Concorda una domanda breve da provare.

**Quali delle nostre misure potrebbero essere usate per giudicare gli individui, e che cosa dovremmo fare al riguardo?**

Individua le misure che le persone potrebbero temere. Discuti i rischi e concorda regole esplicite su per che cosa i numeri non saranno usati. Scrivile.

**Se potessimo tenere solo cinque misure, quali terremmo?**

Chiedi a ciascuno di sceglierne cinque e confronta. La sovrapposizione mostra il nucleo; le differenze mostrano esigenze diverse. Il risultato è un insieme di partenza. Verifica che copra risultati, flusso, livelli di servizio e salute.

## Nella pratica: un esempio di ITIL agile

Il gruppo IT di una ferrovia nazionale gestisce i sistemi dietro l'informazione ai passeggeri. Il gruppo riferisce ogni mese al team dirigente un cruscotto di 40 misure. Il cruscotto è letto da pochi e due misure dominano la discussione: il numero di incidenti chiusi entro il tempo obiettivo e il numero di rilasci per trimestre. Il team degli incidenti ha imparato a chiudere in fretta gli incidenti e a riaprirne di nuovi per lo stesso guasto, e diversi team di delivery dividono il lavoro in rilasci banali per raggiungere il conteggio.

Il responsabile del gruppo IT chiede a un piccolo team di ricostruire le misure. Iniziano chiedendo quali decisioni il cruscotto dovrebbe informare. Per ogni servizio scelgono una manciata di misure: un indicatore e obiettivo di livello di servizio rivolto all'utente, change lead time e change fail rate, età dell'elemento di lavoro per le voci di problema aperte, carico di reperibilità per ingegnere e una indagine mensile di soddisfazione a una domanda per il personale delle stazioni con una casella di testo libero. I vecchi conteggi sono ritirati. Il team dirigente concorda che nessuna misura sarà usata per classificare i team o fissare premi individuali e il responsabile IT lo scrive come regola sul cruscotto. Ai team viene chiesto di fissare obiettivi di miglioramento per i servizi che possiedono come objectives con key results, solo a livello di team.

Dopo un anno, il cruscotto ha dodici misure e la revisione mensile è diventata una conversazione sui problemi aperti più vecchi e sui commenti in testo libero. Gli incidenti ripetuti calano e i rilasci sono più significativi. Restano alcune difficoltà. L'indagine di soddisfazione riceve poche risposte dal personale notturno, il lead time di un team sembra scadente perché è l'unico che conta il tempo dall'idea e non dal commit e un manager ha iniziato a citare il punteggio dell'indagine in una valutazione delle prestazioni. Il responsabile IT chiede al team di allineare le definizioni, ricorda la regola ai manager e organizza una breve indagine condotta al passaggio di consegne del turno di notte.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery dovrebbero scegliere misure che li aiutino a orientarsi, prendere i numeri dai propri strumenti e discuterli nelle retrospettive. Fai attenzione alle misure che premiano la divisione del lavoro o il nascondere i fallimenti. Condividi ciò che impari con gli altri team.

### Team di servizio e di operations

I team operativi portano molte delle misure di livello di servizio e di salute. Mantieni chiare le definizioni e affidabili i dati, includi carico di reperibilità e toil e presenta i numeri con casi e commento. Reagisci quando una misura è usata come obiettivo.

### Leadership e governance

I leader plasmano la cultura della misurazione. Di' per che cosa i numeri saranno e non saranno usati, chiedi tendenze e storie e non classifiche e resisti ad aggiungere misure per ogni nuova preoccupazione. Rivedi di tanto in tanto l'intero insieme.

### Clienti e utenti

Clienti e utenti sono sia una fonte di misure sia soggetti di esse. Rispondi a brevi indagini quando puoi e di' che cosa conta. Chiedi ai fornitori che cosa misurano della tua esperienza e che cosa hanno fatto dei risultati.

## Modalità di fallimento comuni

- **Misure come obiettivi.** Segue la manipolazione. Usa invece le misure per la discussione e fissa gli obiettivi come risultati.
- **Un solo numero.** Una singola misura distorce il comportamento. Usa invece un insieme equilibrato che tira contro se stesso.
- **Definizioni incoerenti.** I team contano in modo diverso. Definisci invece ogni misura e la sua fonte.
- **Classifiche.** I team competono e nascondono i problemi. Confronta invece ogni team con la propria storia.
- **Solo medie.** Le code lunghe restano nascoste. Guarda invece distribuzioni e percentili.
- **Misurare ciò che è facile.** I numeri comodi sostituiscono quelli importanti. Parti invece dalle decisioni e dai risultati degli utenti.
- **OKR individuali come elenchi di compiti.** Gli obiettivi diventano valutazioni delle prestazioni. Tieni invece gli OKR a livello di team e organizzazione.
- **Affaticamento da indagini e legami con la retribuzione.** Gli utenti smettono di rispondere, o i punteggi sono manipolati. Mantieni invece brevi le indagini e separate dalla retribuzione.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Scelta e definizione | Le misure sono estemporanee | Alcuni team definiscono poche misure | Un insieme equilibrato con definizioni chiare è usato per servizio | L'insieme è rivisto per utilità e lacune | Le misure sono allineate tra team, fornitori e clienti |
| Uso nelle decisioni | I numeri sono riferiti ma raramente usati | Alcuni team li discutono nelle revisioni | Le misure alimentano decisioni e miglioramento regolari | Le decisioni legate alle misure sono monitorate e se ne impara | Le misure guidano le decisioni in tutta l'organizzazione |
| Difendersi dalla manipolazione | Si fissano obiettivi su singoli numeri | Qualche consapevolezza della distorsione | Regole su come le misure possono essere usate sono scritte e seguite | I segni di manipolazione sono monitorati e le misure aggiustate | La cultura della misurazione è condivisa in tutta l'organizzazione |
| Misure di utenti e salute | Pochi dati su utenti o personale | Alcune indagini o dati di carico | Brevi indagini sugli utenti e misure di sostenibilità sono routine | I risultati portano ad azioni pianificate e sono verificati | Le voci di utenti e personale plasmano le priorità tra i servizi |

## Checklist

- [ ] Ogni misura che riferiamo ha una decisione dichiarata che informa.
- [ ] Usiamo un piccolo insieme equilibrato che include misure di risultato, flusso, livello di servizio, consegna e salute.
- [ ] Ogni misura ha una definizione scritta e una fonte.
- [ ] I team sono confrontati con la propria storia, non classificati.
- [ ] Abbiamo scritto per che cosa le misure non saranno usate.
- [ ] Le misure di tempo mostrano distribuzioni o percentili.
- [ ] Agli utenti viene posta regolarmente una domanda breve con spazio per i commenti e le risposte sono lette.
- [ ] Se usiamo gli OKR, sono a livello di team o organizzazione e non obiettivi individuali.
- [ ] I dati sono presi dagli strumenti come sottoprodotto del lavoro dove possibile.
- [ ] Rivediamo le misure stesse almeno una volta l'anno.

## Prompt per l'IA

**Scopo: scegliere un insieme equilibrato di misure per un servizio.**

```text
Help me choose a small balanced set of measures for [service].

What the service does and who uses it: [describe].
Decisions the team and its owner need to make in the next quarter: [list].
Data we already have: [list tools and records].
Measures we currently report: [list].

Propose five to eight measures across outcome, flow, delivery performance, service level, and health (for example work item age, change lead time, an availability indicator, pager load, and a short satisfaction question). For each, say what decision it informs, what data it needs, and one way it could be gamed. Do not set targets. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: trovare come una misura potrebbe essere manipolata.**

```text
Here is a measure we use and how it is used: [describe the measure, its definition, and who sees it or is rewarded for it].

List ways people might change their behavior to improve the number without improving the underlying work, using only the description. Suggest a paired measure that would reveal each distortion and a question to ask the team. Do not accuse anyone. List what you are unsure of.
```

**Scopo: scrivere OKR per un team di servizio senza trasformarli in compiti.**

```text
Help me draft OKRs for [team] for the next quarter.

Context: [describe the service and the main problem users face].
Outcomes we want for users: [list].
Measures we already collect: [list].
Risks we have seen with goals in the past: [for example, gaming or task lists].

Draft two or three objectives, each with three to five key results that are measurable outcomes (not tasks), using only measures we can collect, and leave target values as [to be agreed with the team]. For each key result, name the data source and a possible distortion. Do not set individual OKRs. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: analizzare i commenti in testo libero di un'indagine.**

```text
Here are free-text comments from our latest user survey: [paste anonymized comments].

Group the comments into themes based only on what they say. For each theme, give a name, the number of comments from my list, two short example quotes, and a question for the team. Highlight themes that appear in both positive and negative comments. Do not infer demographics or sentiment beyond the text. If the sample is small, say so. List what you are unsure of.
```

## Competenze per l'IA

- [software-engineering-metrics](../../../../skills/software-engineering-metrics/SKILL.md): da usare per scegliere e interpretare misure di consegna e di prestazione del servizio.
- [key-risk-indicators](../../../../skills/key-risk-indicators/SKILL.md): da usare per scegliere misure di allerta precoce per i rischi di un servizio.
- [survey-design](../../../../skills/survey-design/SKILL.md): da usare per progettare brevi indagini su utenti e personale che producano risposte utilizzabili.
- [getting-feedback](../../../../skills/getting-feedback/SKILL.md): da usare per raccogliere e rispondere al feedback di utenti e colleghi.
- [feature-prioritization](../../../../skills/feature-prioritization/SKILL.md): da usare per collegare le misure dei risultati a ciò su cui il team lavora dopo.

## Fonti principali

- **DORA's software delivery performance metrics** (dora.dev): definizioni delle cinque misure e avvertenze sul loro uso.
- **Goodhart's law** (Wikipedia): l'origine e la formulazione dell'adagio per cui una misura usata come obiettivo smette di essere una buona misura.
- **Objectives and key results** (Wikipedia): il framework, le sue origini, la valutazione e le critiche.
- **Net promoter score** (Wikipedia): la definizione, gli usi e le critiche di una misura di soddisfazione.

## Riferimenti

1. DORA's software delivery performance metrics — DORA, dora.dev — https://dora.dev/guides/dora-metrics-four-keys/
2. Goodhart's law — Wikipedia — https://en.wikipedia.org/wiki/Goodhart%27s_law
3. Objectives and key results — Wikipedia — https://en.wikipedia.org/wiki/Objectives_and_key_results
4. Net promoter score — Wikipedia — https://en.wikipedia.org/wiki/Net_promoter_score
5. The Kanban Guide — John Coleman, Daniel Vacanti, and contributors, kanbanguides.org — https://kanbanguides.org/english/
6. Service Level Objectives — Google SRE book, sre.google — https://sre.google/sre-book/service-level-objectives/
7. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
8. Performance indicator — Wikipedia — https://en.wikipedia.org/wiki/Performance_indicator
9. Customer satisfaction — Wikipedia — https://en.wikipedia.org/wiki/Customer_satisfaction
