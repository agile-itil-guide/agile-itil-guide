# Gestione degli asset software

**La gestione degli asset software assicura che un'organizzazione compri il software di cui ha bisogno, usi ciò che compra e rispetti i termini che ha accettato, e per i team agili significa oggi tracciare componenti open source e abbonamenti oltre ai prodotti con licenza.**

## Perché è importante

Il software è uno dei costi più grandi e meno visibili dell'IT. Si comprano licenze per persone che se ne sono andate, gli abbonamenti si rinnovano inosservati e i prodotti sono installati in modi che la licenza non consente. Ciascuno è un costo o un rischio. Un audit di un fornitore può trasformare una piccola discrepanza in una fattura salata, e un componente non aggiornato in un'applicazione dimenticata può aprire una porta a un attaccante.

I team agili cambiano il quadro. Gli sviluppatori importano librerie con un solo comando e le applicazioni moderne sono in gran parte assemblate da parti di terzi e open source. L'articolo di Wikipedia sulla catena di fornitura del software riferisce che il software open source è stato trovato nel 96 percento delle basi di codice commerciali analizzate da un fornitore nel 2024, citando Synopsys. I team comprano anche servizi cloud e abbonamenti con carte, fuori dal processo degli acquisti. La gestione degli asset software (SAM) è quindi cresciuta oltre il contare le installazioni di pochi grandi prodotti, diventando una pratica che copre ciò che si usa, ciò che si deve e ciò di cui ci si fida.

L'[articolo di Wikipedia sulla gestione degli asset software](https://en.wikipedia.org/wiki/Software_asset_management) descrive la SAM come una pratica di business per gestire e ottimizzare acquisto, deployment, manutenzione, utilizzo e dismissione del software, con obiettivi di ridurre i costi IT, limitare il rischio aziendale e legale e migliorare la produttività degli utenti finali. Non copre servizi cloud, SBOM o modelli di maturità, quindi questo argomento aggiunge gli articoli sulla catena di fornitura del software e sul software open source. Questo argomento descrive la pratica e non dà consulenza legale; i termini di licenza differiscono e la fonte giusta è il testo della licenza o del contratto.

## Concetti fondamentali

### Che cos'è la SAM

Secondo Wikipedia, la SAM fa parte della gestione degli asset IT (vedi Argomento 4.1 — Gestione degli asset IT). Cita ITIL come descrivente una gestione che comprende l'efficace gestione, controllo e protezione degli asset software. I suoi obiettivi strategici, come li elenca l'articolo, includono ridurre i costi di software e di supporto tramite contratti a volume e riassegnazione delle licenze inutilizzate, far rispettare policy di sicurezza e standard per desktop, server e dispositivi mobili, migliorare la produttività installando la tecnologia in modo più rapido e affidabile, limitare l'onere di gestione tramite automazione e stabilire policy per acquisizione, distribuzione, uso e dismissione.

### Conformità delle licenze

L'articolo descrive la SAM come il bilanciare il numero di licenze acquistate rispetto a quelle effettivamente consumate e assicurare che l'uso corrisponda ai termini di licenza di ciascun fornitore. Nota che le installazioni sono la misura più comune del consumo, ma alcuni software sono concessi in licenza per utenti, capitale, processori o core di CPU. Le organizzazioni possono ridurre la responsabilità durante gli audit da parte di fornitori o terze parti come la Business Software Alliance, dice l'articolo, tramite inventari software continui, policy di acquisto e strumenti. L'articolo non descrive le procedure di audit. Il punto dell'esercizio è conoscere il tuo **diritto d'uso** (entitlement: ciò che ti è consentito usare), il tuo **consumo** (ciò che usi) e il divario tra i due.

### Le tre domande

Una pratica SAM risponde a tre domande per ogni prodotto importante:

| Domanda | Che cosa richiede |
|---|---|
| A che cosa abbiamo diritto? | Contratti, termini di licenza, fatture e prova d'acquisto |
| Che cosa stiamo usando? | Inventario e dati d'uso da rilevamento e misurazione |
| Qual è il divario, e che cosa facciamo? | Confronto, decisioni su comprare, riassegnare o rimuovere |

Un divario può andare in entrambe le direzioni: sotto-licenziamento, che è un rischio di conformità, e sovra-licenziamento, che è spreco.

### Standard: ISO/IEC 19770

L'articolo elenca le parti della famiglia ISO/IEC 19770: 19770-1:2017 (requisiti del sistema di gestione degli asset IT, un framework di processo che può essere implementato in livelli graduali), 19770-2:2015 (tag di identificazione del software), 19770-3:2016 (uno schema di gestione dei diritti d'uso per dettagli di licenza, contratto e fattura), 19770-4:2017 (dati di misurazione dell'uso delle risorse) e 19770-5:2015 (panoramica e vocabolario). L'articolo dice che lo standard di identificazione del software è sostenuto da IBM, Microsoft e Adobe. Controlla gli standard per le edizioni correnti e il contenuto esatto.

### Tecnologie SAM e loro limiti

L'articolo elenca strumenti per inventario del software, gestione delle licenze, misurazione, controllo delle applicazioni, deployment, gestione delle patch, gestione delle richieste e catalogazione dei prodotti. Dà anche un esempio di scala: le regole di misurazione in System Center Configuration Manager di Microsoft funzionano bene per piccoli parchi ma generano volumi di dati ingestibili su scala aziendale. Gli strumenti aiutano, ma hanno bisogno di una domanda chiara e di un responsabile.

### Software open source

Wikipedia definisce il software open source come software il cui codice sorgente è pubblicamente disponibile e che gli utenti possono usare, studiare, modificare e distribuire, tipicamente con una licenza aperta. L'Open Source Initiative mantiene la definizione più comune, con dieci criteri e un elenco di licenze approvate, anche se l'articolo dice che l'OSI non ha autorità legale sul termine. Descrive due famiglie di licenze:

| Famiglia | Che cosa chiede ai destinatari | Esempi citati |
|---|---|---|
| **Permissiva** | Conservare le note di copyright e includere la licenza; nessun obbligo di rilasciare il proprio codice con la stessa licenza | BSD, MIT, Apache |
| **Copyleft** | Usare la stessa licenza per almeno alcune parti di ciò che si distribuisce (il copyleft forte si applica a tutte le opere derivate; quello debole solo a certe condizioni) | GNU GPL (forte); MPL, EPL (debole) |

Entrambe le famiglie, dice l'articolo, richiedono di conservare le note di copyright e di fornire una copia della licenza con il codice. Cita *Jacobson v Katzer* (2008), in cui un tribunale ha fatto rispettare i termini di una licenza aperta, compresa l'attribuzione, in base alla legge sul diritto d'autore. Nota che le organizzazioni stanno istituendo uffici di programma open source per gestire le proprie strategie. I termini open source sono obblighi reali. Quali si applicano dipende da come usi e distribuisci il software; chiedi alla tua funzione legale e leggi la licenza.

### La catena di fornitura del software e le SBOM

L'articolo sulla catena di fornitura del software la descrive come i componenti, le librerie, gli strumenti e i processi usati per sviluppare, costruire e pubblicare un artefatto software. Nomina rischi: gli attaccanti possono compromettere un componente a monte per raggiungere tutti gli utenti a valle, e cita esempi tra cui Log4Shell nel 2021, l'attacco SolarWinds nel 2020 e la backdoor XZ Utils nel 2024. Descrive una **software bill of materials (SBOM)** come un inventario dei componenti di un artefatto software, comprese parti open source e proprietarie, l'equivalente software di una distinta base di produzione. Le SBOM sostengono l'analisi di vulnerabilità e licenze.

L'articolo riferisce limiti: i fogli di calcolo non possono essere arricchiti automaticamente con dati sulle vulnerabilità e dovrebbero essere conservati in un repository interrogabile; le SBOM guidate da policy sono rare, con uno studio che ha trovato circa lo 0,56 percento dei repository GitHub popolari che le contengono; meno della metà dei progetti testati include SBOM nei rilasci e molte sono incomplete; e uno studio su sei strumenti SBOM per Java ha trovato frequenti inesattezze. Nota che la sola visibilità non può garantire l'integrità. Riferisce anche che l'Executive Order 14028 degli Stati Uniti, firmato il 12 maggio 2021, ha chiesto a NIST e NTIA di emettere indicazioni sulla sicurezza della catena di fornitura del software, comprese le SBOM, e che gli elementi minimi dell'NTIA si dividono in campi di dati, supporto all'automazione e pratiche e processi. L'articolo non nomina formati SBOM né descrive il Cyber Resilience Act dell'Unione Europea. Le regole sulle SBOM differiscono per paese e settore; chiedi alla tua funzione di conformità che cosa si applica a te.

### SaaS e abbonamenti cloud

L'articolo sulla SAM non discute il software come servizio (SaaS) o il cloud. L'esperienza pratica mostra che il software in abbonamento crea nuovi problemi: acquisti fuori dagli acquisti, postazioni che nessuno rimuove, strumenti sovrapposti e dati affidati ai fornitori senza revisione (vedi Argomento 3.14 — Gestione dei fornitori e Argomento 4.5 — Gestione finanziaria IT e FinOps). La SAM per gli abbonamenti si concentra sullo scoprire che cosa è acquistato, chi lo possiede, chi lo usa e quando si rinnova.

### Limiti delle fonti

L'articolo sulla SAM non copre procedure di audit, cataloghi di tipi di licenza o modelli di maturità, e i suoi riferimenti principali includono voci datate dal 2006 al 2009. L'articolo sulla catena di fornitura del software riferisce cifre da indagini e studi di qualità disomogenea. Usa le fonti per inquadrare le domande e usa i testi delle licenze e dei contratti per le risposte.

## Buone pratiche

1. **Parti dai prodotti che contano di più.** Scegli i pochi prodotti più grandi o più rischiosi per costo o esposizione legale e metti in ordine per primi diritto d'uso, inventario e uso.
2. **Conserva la prova del diritto d'uso.** Conserva contratti, fatture e termini di licenza dove si possano trovare e collegali ai record del prodotto. Non puoi difendere una posizione in un audit senza prove.
3. **Conosci la metrica della licenza.** Per ogni prodotto, registra come viene contato: per utente, dispositivo, processore, core o altro. Contare le installazioni quando la licenza è per core produce la risposta sbagliata.
4. **Confronta regolarmente diritto d'uso e utilizzo.** Almeno ogni trimestre per i prodotti principali, confronta ciò che puoi usare con ciò che usi. Agisci sul divario comprando, riassegnando o rimuovendo.
5. **Recupera le licenze inutilizzate.** Usa i dati d'uso per trovare licenze che nessuno ha usato per un periodo definito e riassegnale o cancellale dopo aver verificato con il responsabile.
6. **Controlla come entra il software.** Rendi facile richiedere il software approvato e difficile comprare fuori dal processo. Includi abbonamenti e acquisti con carta nelle revisioni di spesa.
7. **Tratta i componenti open source come asset.** Tieni un inventario dei componenti open source nei tuoi prodotti, con licenza e versione. Verifica le licenze rispetto a come usi e distribuisci il software, con consulenza legale.
8. **Genera le SBOM nella build.** Produci automaticamente una software bill of materials per ogni build, conservala in un posto interrogabile e usala per rispondere alle vulnerabilità e alle domande dei clienti. Verifica la SBOM rispetto alla build, perché gli strumenti possono essere inesatti.
9. **Monitora gli abbonamenti.** Per ciascuno, registra responsabile, scopo, costo, numero di postazioni, utenti, data di rinnovo e dati custoditi. Rivedi prima del rinnovo.
10. **Collega il software ai servizi.** Registra quali servizi usano quale software e versioni, così che una vulnerabilità o un cambiamento di licenza possa essere ricondotto ai servizi interessati (vedi Argomento 4.4 — Gestione della configurazione).
11. **Preparati con calma agli audit.** Mantieni aggiornati i record, nomina un referente e conosci diritti e doveri dal contratto. Non aspettare la notifica per iniziare a organizzarti.
12. **Ritira correttamente il software.** Rimuovilo dai sistemi, chiudi licenze e abbonamenti e aggiorna i record. Il software inutilizzato è un costo e una superficie d'attacco.

## Domande da discutere con il team

**Per i nostri tre prodotti software più costosi, sappiamo che cosa possiamo usare e che cosa usiamo?**

Chiedi il numero di licenze detenute e il numero in uso per ciascuno. Confronta. Gli esiti comuni sorprendono: più postazioni che utenti, o utenti oltre le postazioni. Chi facilita può chiedere dove sono conservate le prove del diritto d'uso. Pianifica di riconciliare il divario più grande.

**Che software hanno comprato o installato le persone senza dirlo a nessuno?**

Sii onesto e senza giudizio. Chiedi di strumenti comprati con carte, strumenti gratuiti usati al lavoro ed estensioni del browser. Le ragioni tipiche sono velocità e processo poco chiaro. Discuti che cosa renderebbe abbastanza veloce la via approvata. Concorda un passaggio di registrazione.

**Da quali componenti open source dipendono i nostri prodotti, e quali sono le loro licenze?**

Chiedi se qualcuno può produrre un elenco. In caso contrario, discuti come generarlo dalla build. Poi chiedi come sono verificate le licenze. Ricorda che gli obblighi differiscono tra licenze permissive e copyleft. Pianifica con l'ufficio legale di rivedere i casi ad alto rischio.

**Se domani comparisse una grave vulnerabilità in una libreria comune, quanto ci vorrebbe per sapere se la usiamo?**

Ripercorri i passaggi: chi viene informato, come si cerca, come si conosce la versione in ogni servizio. La risposta mostra quanto aiuterebbero SBOM e inventari. Concorda un primo miglioramento, come generare una bill of materials nella pipeline.

**Quali abbonamenti si rinnovano il prossimo trimestre, e chi decide se mantenerli?**

Elenca i rinnovi. Per ciascuno, chiedi chi lo possiede, quante postazioni sono attive e che cosa succede se è cancellato. Spesso nessuno possiede la decisione. Assegna i responsabili e aggiungi una data di revisione prima di ogni rinnovo.

**Come risponderemmo a una notifica di audit del fornitore?**

Chiedi chi la gestirebbe e quali prove ha. Discuti se i record sono completi. Lo scopo è un piano calmo, non la paura degli audit. Concorda un referente e una checklist.

## Nella pratica: un esempio di ITIL agile

Un servizio postale nazionale gestisce circa 60 applicazioni interne e una piattaforma di tracciamento dei pacchi rivolta ai clienti costruita da un team di quindici persone. Un fornitore notifica al reparto IT un audit di licenza su un prodotto database. L'addetto ITAM scopre che i record di licenza sono sparsi in tre fogli di calcolo e che nessuno sa dire su quanti core di processore giri ora il database, perché le macchine virtuali sono state spostate tra host molte volte.

L'addetto ITAM, un amministratore di database e il responsabile degli acquisti mettono insieme le prove. Raccolgono il contratto, la metrica di licenza (per core di processore), le fatture e i dati di rilevamento su dove gira il database. Scoprono che il prodotto gira su più core di quelli acquistati in un ambiente e su meno in un altro, dove le licenze sono inutilizzate. Dopo aver parlato con il fornitore, riassegnano le licenze inutilizzate, ne comprano un piccolo numero in più e spostano un ambiente non essenziale su un'alternativa gratuita. Il costo è molto inferiore a ciò che sarebbe stato un rilievo di audit, ma non è trascurabile.

Nello stesso periodo, al team della piattaforma un grande cliente chiede un elenco dei componenti software della piattaforma di tracciamento dei pacchi. Il team si rende conto di non poterne produrre uno. Aggiunge un passaggio di build che genera una bill of materials per ogni rilascio e la conserva in un repository. Il primo risultato include una libreria con una licenza che l'ufficio legale non aveva rivisto, e decidono di sostituirla. Restano problemi. Lo strumento SBOM del team non vede i componenti in un linguaggio, e un gruppo di ricerca separato continua a comprare abbonamenti con una carta del dipartimento. L'addetto ITAM chiede al fornitore dello strumento del divario e convince il dipartimento a registrare i propri abbonamenti.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery portano nell'organizzazione la maggior parte del software. Registra i componenti e gli abbonamenti che aggiungi, genera bill of materials nelle tue build e chiedi prima di usare una libreria con una licenza poco familiare. Condividi i risultati con ufficio legale e sicurezza.

### Team di servizio e di operations

I team operativi gestiscono inventario, patching e misurazione. Mantieni collegato ai servizi l'inventario del software, applica rapidamente le patch quando compaiono vulnerabilità e recupera le licenze inutilizzate. Aiuta gli acquisti a capire come i prodotti sono davvero usati.

### Leadership e governance

I leader possiedono il rischio di non conformità e la spesa. Chiedi diritto d'uso e consumo per i prodotti più grandi, una visione degli abbonamenti e un piano per i rischi di open source e catena di fornitura. Sostieni una via d'acquisto abbastanza veloce da essere usata.

### Clienti e utenti

Clienti e utenti traggono vantaggio quando il software è disponibile e sicuro. Richiedi ciò di cui hai bisogno attraverso la via appropriata, restituisci ciò che non usi più e di' al team degli strumenti che hai trovato utili. I clienti dei tuoi prodotti possono chiedere bill of materials; aspettati che ti venga chiesto.

## Modalità di fallimento comuni

- **Contare solo le installazioni.** La metrica di licenza è per core o utente. Registra invece la metrica e conta la cosa giusta.
- **Prova del diritto d'uso persa.** Contratti e fatture non si trovano. Conservali invece con il record del prodotto.
- **Shelfware.** Le licenze sono acquistate e inutilizzate. Confronta invece diritto d'uso e utilizzo e recupera.
- **Acquisti ombra.** Gli abbonamenti comprati con carte sfuggono al processo. Rendi invece veloce la via approvata e rivedi la spesa per le eccezioni.
- **Componenti open source sconosciuti.** Nessuno sa elencarli. Genera invece automaticamente bill of materials nelle build.
- **Ignorare i termini di licenza dell'open source.** Gli obblighi del copyleft sono mancati. Verifica invece le licenze rispetto a uso e distribuzione con consulenza legale.
- **Fidarsi ciecamente degli strumenti.** Gli strumenti perdono componenti o ne elencano di sbagliati. Convalida invece i risultati su un campione e chiedi ai fornitori dei divari.
- **Panico da audit.** I record sono messi insieme dopo la notifica. Mantieni invece aggiornati i record e nomina un referente per l'audit.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Diritto d'uso e utilizzo | I record sono sparsi; l'uso è ignoto | I prodotti principali hanno record dei diritti d'uso | Diritto d'uso e utilizzo sono registrati per i prodotti principali e confrontati regolarmente | Divari e licenze inutilizzate sono misurati e trattati | Diritto d'uso e utilizzo sono condivisi con finanza, acquisti e fornitori |
| Acquisizione e abbonamenti | Il software è comprato da chiunque | Esiste una via approvata per alcuni acquisti | Acquisti e abbonamenti seguono un'unica via con responsabili e date di rinnovo | Spesa e uso delle postazioni sono rivisti prima del rinnovo | Acquisti, utilizzo e contratti sono coordinati in tutta l'organizzazione |
| Open source e catena di fornitura | I componenti sono ignoti | Alcuni team elencano le librerie | Le bill of materials sono generate nelle build e le licenze sono riviste | Risultati su vulnerabilità e licenze sono seguiti fino alla chiusura | Le bill of materials sono condivise con clienti e fornitori come richiesto |
| Audit e conformità | Le notifiche di audit causano panico | Esiste un referente | I record sono tenuti aggiornati ed esiste una routine di audit | Il rischio di conformità è misurato e rivisto | La pratica di conformità è allineata tra fornitori e giurisdizioni |

## Checklist

- [ ] Per i nostri prodotti software più grandi conosciamo il diritto d'uso, la metrica di licenza e l'utilizzo.
- [ ] Contratti, fatture e termini di licenza sono conservati con i record dei prodotti.
- [ ] Diritto d'uso e utilizzo sono confrontati almeno ogni trimestre per i prodotti principali.
- [ ] Le licenze inutilizzate sono recuperate dopo aver verificato con i responsabili.
- [ ] Acquisti e abbonamenti seguono un'unica via, con responsabili e date di rinnovo registrati.
- [ ] Generiamo una bill of materials nella build per i prodotti che rilasciamo o gestiamo.
- [ ] Le licenze open source nei nostri componenti sono riviste rispetto al nostro uso, con consulenza legale.
- [ ] Sappiamo trovare quali servizi usano un dato componente o prodotto.
- [ ] Una persona nominata gestisce le notifiche di audit dei fornitori.
- [ ] Il software ritirato è rimosso da sistemi e record.

## Prompt per l'IA

**Scopo: confrontare diritto d'uso e consumo per un prodotto.**

```text
Help me compare entitlement and usage for [product].

License metric (how the vendor counts, with the exact wording from the contract): [paste].
Entitlement (what we purchased, with dates): [paste].
Usage data (installations, users, cores, or whatever the metric requires): [paste real data].

Using only this information, compute the difference between entitlement and usage, in the vendor's unit, and say whether it indicates a shortfall or a surplus. List what is unclear in the contract wording as questions for the vendor or legal. Do not interpret legal terms beyond the text. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: rivedere un elenco di componenti open source per questioni di licenza.**

```text
Here is a list of open-source components in our product with name, version, and license as reported by our tooling: [paste].
How we use and distribute the product: [for example internal use only, hosted service, shipped to customers].

Group the licenses into permissive and copyleft families based on the license names. For each group, list the types of question we should put to our legal team given how we use and distribute the product. Flag components with missing or unknown licenses. Do not give legal advice or say what the licenses require; list questions only. List what you are unsure of.
```

**Scopo: preparare una ricerca di risposta alle vulnerabilità usando una bill of materials.**

```text
Help me plan how we would answer: "Do we use [component name and version range] and where?"

What we have today: [for example bills of materials in a repository, a spreadsheet, nothing].
Systems and services in scope: [list].

Describe the steps to find out, who does each, what data they need, what could go wrong, and how long each step might take (leave durations as [to be measured]). Propose one improvement that would shorten the answer. Do not invent our tools. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: costruire una revisione degli abbonamenti per il prossimo trimestre.**

```text
Here is a list of our subscriptions with owner, monthly cost, paid seats, active users in the last 90 days, renewal date, and data held: [paste real data].

Using only this data, list renewals in the next 90 days, compute unused seats and their cost for each, and highlight subscriptions with no owner. For each, suggest a question for the owner before renewal. Do not recommend canceling anything; flag candidates for review. List what you are unsure of.
```

## Competenze per l'IA

- [vendor-management](../../../../skills/vendor-management/SKILL.md): da usare per gestire contratti, rinnovi e relazioni con i fornitori di software.
- [legal-compliance-audit](../../../../skills/legal-compliance-audit/SKILL.md): da usare per prepararsi a un audit di un fornitore o di conformità.
- [budget-forecasting](../../../../skills/budget-forecasting/SKILL.md): da usare per prevedere i costi di software e abbonamenti.
- [risk-register](../../../../skills/risk-register/SKILL.md): da usare per registrare i rischi di licenze, vulnerabilità e catena di fornitura.
- [security-testing](../../../../skills/security-testing/SKILL.md): da usare per verificare dipendenze e build alla ricerca di debolezze note.

## Fonti principali

- **Software asset management** (Wikipedia): la definizione, gli obiettivi, le tecnologie e le parti di ISO/IEC 19770.
- **Software supply chain** (Wikipedia): rischi, software bill of materials, cifre di adozione e contesto normativo.
- **Open-source software** (Wikipedia): la definizione, le famiglie di licenze e note su rischi e obblighi.
- **ISO/IEC 19770** (International Organization for Standardization): la famiglia di standard stessa; leggi le parti correnti per i requisiti esatti.

## Riferimenti

1. Software asset management — Wikipedia — https://en.wikipedia.org/wiki/Software_asset_management
2. Software supply chain — Wikipedia — https://en.wikipedia.org/wiki/Software_supply_chain
3. Open-source software — Wikipedia — https://en.wikipedia.org/wiki/Open-source_software
4. IT asset management — Wikipedia — https://en.wikipedia.org/wiki/IT_asset_management
5. Software license — Wikipedia — https://en.wikipedia.org/wiki/Software_license
6. Copyleft — Wikipedia — https://en.wikipedia.org/wiki/Copyleft
7. Permissive software license — Wikipedia — https://en.wikipedia.org/wiki/Permissive_software_license
8. Software as a service — Wikipedia — https://en.wikipedia.org/wiki/Software_as_a_service
9. Open Source Initiative — Wikipedia — https://en.wikipedia.org/wiki/Open_Source_Initiative
