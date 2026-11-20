# Extreme Programming

**Extreme Programming (XP) è il metodo agile più specifico sulla pratica ingegneristica, e le sue abitudini di testare per primi, integrare di continuo e condividere la proprietà del codice sono ciò che rende sicuro il cambiamento frequente in un servizio in esercizio.**

## Perché è importante

Il cambiamento frequente è l'obiettivo della consegna continua e la preoccupazione della gestione dei servizi. Il modo di conciliarli non sono più riunioni di approvazione, ma una maggiore capacità di sapere che una modifica funziona prima che raggiunga gli utenti. Extreme Programming è il metodo agile che dice di più su come costruire questa capacità: scrivere prima i test, integrare più volte al giorno, mantenere semplice il design e condividere la responsabilità del codice.

Molti team prendono gli eventi e le lavagne di Scrum e lasciano da parte le pratiche ingegneristiche. Il risultato è un team che pianifica in sprint ma rilascia con timore. Le pratiche di XP sono la metà mancante. Contano per chiunque debba gestire il risultato, perché un servizio costruito con test automatici, rilasci piccoli e conoscenza condivisa è più facile da supportare di uno costruito da poche persone in grandi lotti non testati.

XP chiede anche all'organizzazione qualcosa che è facile trascurare: un ritmo sostenibile, un team intero con tutte le competenze necessarie e un cliente realmente disponibile. Sono condizioni dell'ambiente di lavoro, non solo abitudini dei programmatori. Questo argomento spiega il metodo, le prove sui suoi limiti e come le sue pratiche si collegano a pratiche ITIL come l'abilitazione dei cambiamenti, la gestione dei rilasci e la gestione della conoscenza.

## Concetti fondamentali

### Da dove viene XP

Kent Beck sviluppò XP lavorando al Chrysler Comprehensive Compensation System (C3), un progetto per le buste paga. Secondo l'[articolo di Wikipedia su Extreme programming](https://en.wikipedia.org/wiki/Extreme_programming), Beck divenne capo progetto nel marzo 1996 e vi perfezionò il metodo, con Ward Cunningham come influenza importante e Ron Jeffries che si unì per fare da coach al team. Il suo libro *Extreme Programming Explained* uscì nell'ottobre 1999. La Chrysler annullò il progetto C3 nel febbraio 2000 dopo che la Daimler-Benz acquisì l'azienda.

L'articolo sottolinea che molte pratiche di XP non erano nuove. Cita lo sviluppo test-first nel Project Mercury della NASA all'inizio degli anni Sessanta. La mossa di XP fu portare le buone pratiche a livelli "estremi": se testare è bene, testa sempre; se le revisioni sono buone, rivedi in continuazione lavorando in coppia. Beck e Cunningham erano tra le 17 persone che scrissero il Manifesto Agile (vedi Argomento 1.1 — Il Manifesto Agile).

### I cinque valori

XP enuncia cinque valori:

| Valore | Che cosa significa | Nel lavoro sui servizi |
|---|---|---|
| **Comunicazione** | Costruire una comprensione condivisa tra sviluppatori, utenti e clienti, soprattutto parlando e mantenendo semplici i design | Sviluppatori e personale operativo parlano di come si comporterà un rilascio prima che sia consegnato |
| **Semplicità** | Fare la cosa più semplice che funziona e non costruire per bisogni futuri ipotetici | Meno parti mobili da monitorare, proteggere e spiegare |
| **Feedback** | Imparare in fretta dai test, dai clienti e dalle stime del team stesso | Risultati rapidi dei test e monitoraggio in produzione accorciano il tempo per imparare |
| **Coraggio** | Fare refactoring, scartare il codice obsoleto e perseverare nei problemi difficili | Ritirare un vecchio componente che nessuno osa toccare |
| **Rispetto** | Rispetto per i compagni di squadra e per il proprio lavoro | Revisione senza attribuzione di colpe dopo i guasti e un carico di reperibilità equo |

L'articolo nota che il rispetto fu aggiunto nella seconda edizione di *Extreme Programming Explained*, dopo i quattro originali.

### Le pratiche

L'articolo sulle pratiche di XP raggruppa dodici pratiche in quattro insiemi. Si comprendono meglio come un sistema che si sostiene da solo.

| Gruppo | Pratiche | Scopo |
|---|---|---|
| **Feedback a piccola scala** | Programmazione in coppia, planning game, test-driven development, team intero | Ottenere feedback in minuti o giorni, non in mesi |
| **Processo continuo** | Integrazione continua, miglioramento del design (refactoring), rilasci piccoli | Mantenere il software sempre in uno stato rilasciabile |
| **Comprensione condivisa** | Standard di codifica, proprietà collettiva del codice, design semplice, metafora di sistema | Permettere a chiunque nel team di modificare in sicurezza qualsiasi parte |
| **Benessere dei programmatori** | Ritmo sostenibile | Mantenere le persone riposate ed efficaci per anni |

Una breve descrizione delle principali:

- **Programmazione in coppia:** due persone lavorano su un compito a una sola postazione, una scrive e una rivede, e cambiano spesso partner.
- **Test-driven development (TDD):** il programmatore scrive prima un test che fallisce, poi scrive solo il codice sufficiente a farlo passare.
- **Integrazione continua (CI):** gli sviluppatori integrano il proprio lavoro nel repository condiviso ogni poche ore, così i problemi di integrazione emergono presto.
- **Rilasci piccoli:** consegnare software funzionante a passi frequenti e piccoli così che i clienti vedano i progressi e rispondano.
- **Proprietà collettiva del codice:** chiunque nel team può modificare qualsiasi parte del codice.
- **Ritmo sostenibile:** evitare gli straordinari regolari e non consentire mai straordinari in due settimane successive.

### Controversie e limiti

L'articolo registra diverse critiche. Matt Stephens e Doug Rosenberg, in un libro del 2003, sostennero che le pratiche di XP dipendono l'una dall'altra, quindi adottarne solo alcune mina il processo. I critici hanno anche messo in dubbio la programmazione in coppia come modo normale di lavorare, l'assenza di una grande progettazione anticipata, il cliente sul posto come singolo punto di guasto e le richieste di modifica informali che portano a rilavorazioni e dilatazione dell'ambito. Anche P. McBreen, e Boehm e Turner, scrissero valutazioni critiche. L'articolo aggiunge che i professionisti agili ritengono molte di queste critiche dei fraintendimenti.

Sulla scala, l'articolo dice che Industrial XP, introdotto nel 2004, estese XP a team più grandi e distribuiti con 23 pratiche. Riferisce anche un'affermazione, segnalata come bisognosa di citazione, secondo cui ThoughtWorks avrebbe avuto un discreto successo con progetti XP distribuiti fino a sessanta persone. Leggi quell'affermazione con cautela e vedi l'Argomento 1.8 — Scalare l'agile per la discussione più ampia.

L'articolo non discute il deployment o il monitoraggio in produzione oltre all'integrazione continua e ai rilasci piccoli. XP dice poco su come si gestisce il software. Porti quella parte dalla gestione dei servizi e usi XP per rendere meno rischioso il passaggio di consegne.

### XP e la visione ITIL del cambiamento

La pratica di abilitazione dei cambiamenti di ITIL (vedi Argomento 3.4 — Abilitazione dei cambiamenti) si preoccupa di assicurare che le modifiche siano valutate, autorizzate e programmate in modo da controllare il rischio. XP controlla il rischio in un altro posto: nel codice, attraverso test, piccoli passi e conoscenza condivisa. Una modifica piccola, testata automaticamente, integrata e facile da annullare è una modifica a rischio più basso con qualsiasi valutazione ragionevole. Le due visioni si integrano quando le prove delle pratiche di XP sono usate nella decisione sul cambiamento.

## Buone pratiche

1. **Adotta le pratiche come insieme.** Il rilievo dei critici che le pratiche di XP si sostengono a vicenda è un utile avvertimento. Testare senza integrare, o integrare senza piccoli passi, dà meno della somma. Introducile insieme dove puoi e scopri da quali dipendono le altre.
2. **Scrivi prima il test per le modifiche che contano.** Per un nuovo comportamento o una correzione di bug, scrivi un test che fallisce e mostra il problema, poi correggilo. Il test resta come difesa contro il ritorno del problema, il che è particolarmente utile per i difetti che hanno causato incidenti.
3. **Integra più volte al giorno.** Mantieni i rami di breve durata e compila e testa automaticamente a ogni integrazione. Una build rotta è la prima priorità del team.
4. **Rilascia a piccoli passi.** Ogni rilascio piccolo comporta meno rischio ed è più facile da capire e annullare. Punta al più piccolo intervallo che la tua pipeline può sostenere in sicurezza e accorcialo quando cresce la fiducia.
5. **Fai refactoring in continuazione.** Migliora un po' il design ogni giorno invece di riservarlo a una riscrittura. È la suite di test a rendere sicura questa pratica.
6. **Mantieni il design il più semplice possibile.** Costruisci ciò che serve ora ed elimina ciò che non è usato. Un sistema più piccolo ha meno da monitorare, aggiornare e spiegare.
7. **Condividi la proprietà del codice.** Lascia che qualsiasi membro del team modifichi qualsiasi parte, con il sostegno di test e standard condivisi. Questo riduce la dipendenza da pochi esperti, che è anche un rischio di disponibilità per il servizio.
8. **Lavora in coppia sul lavoro rischioso o poco familiare.** Usa la coppia per modifiche difficili, per l'inserimento e per l'affiancamento in reperibilità. Trattala come uno strumento per diffondere la conoscenza e individuare errori, e non farne una regola per ogni compito.
9. **Mantieni un ritmo sostenibile.** Pianifica il lavoro in modo che gli straordinari siano rari e non ripetuti settimana dopo settimana. Un ingegnere di turno stanco è un rischio per il servizio (vedi Argomento 1.2 — I principi agili sul ritmo).
10. **Fai del cliente una parte del team.** Trova un utente reale o un rappresentante degli utenti che possa rispondere alle domande durante il lavoro. Ricorda la critica che una sola persona è un singolo punto di guasto, quindi coinvolgi più di una voce.
11. **Scrivi i criteri di accettazione come test dove possibile.** Trasforma le aspettative del cliente in controlli automatici che girano a ogni build. Così documentano il comportamento e lo proteggono allo stesso tempo.
12. **Includi controlli operativi nei test.** Aggiungi alla pipeline controlli su monitoraggio, logging e comportamento di ripristino, così che la prontezza operativa sia verificata a ogni modifica (vedi Argomento 3.5 — Gestione di rilasci e deployment).

## Domande da discutere con il team

**Come sappiamo che una modifica funziona prima che raggiunga gli utenti, e quanto tempo ci vuole per saperlo?**

Ripercorri i controlli che una modifica supera tra il portatile di uno sviluppatore e la produzione. Conta quanti sono automatici e quanto richiede ciascuno. Le risposte tipiche includono un test manuale, una revisione e una speranza. Chiedi quale controllo ha intercettato più problemi e quale non ne ha mai intercettato nessuno. Prosegui scegliendo un controllo manuale da automatizzare.

**Chi può modificare quali parti del nostro sistema, e che cosa succede quando quelle persone sono assenti?**

Elenca i componenti e le persone che capiscono ciascuno. I componenti con una sola persona dietro sono rischi per il servizio. La proprietà collettiva è la risposta di XP, e per essere sicura richiede test e standard condivisi. Chiedi che cosa una persona potrebbe insegnare a un'altra nel giro di un mese. Chi facilita può chiedere se ferie o malattie abbiano mai ritardato una correzione.

**Dove ci aiuterebbe di più lavorare in coppia, e dove ci rallenterebbe soltanto?**

La programmazione in coppia è controversa, quindi invita a opinioni oneste. Chiedi alle persone delle migliori e peggiori sessioni in coppia che hanno fatto. Lavorare in coppia spesso aiuta con sistemi poco familiari, modifiche difficili e inserimento. Aiuta meno con il lavoro di routine che una persona può fare bene. Concorda una situazione in cui provare la coppia per un mese e come la giudicherete.

**Che cosa succede alla nostra qualità quando siamo sotto pressione, e che cosa lasciamo cadere per primo?**

Chiedi un recente periodo di corsa e che cosa è stato saltato: test, revisioni, documentazione. Chiedi che cosa è successo dopo. Spesso il lavoro saltato è tornato sotto forma di incidenti. Il punto è accorgersi dello schema e decidere in anticipo quali pratiche sono protette. Evita le colpe e collega la risposta al ritmo sostenibile.

**Con quale frequenza integriamo il nostro lavoro, e che cosa ci fa aspettare?**

Chiedi quanto vive un ramo tipico e che cosa lo trattiene. I rami lunghi riflettono di solito modifiche grandi, revisioni lente o una build inaffidabile. Ciascuno è una correzione diversa. Chiedi che cosa il team potrebbe fare per rendere normale l'integrazione in poche ore. Scegli un ostacolo da rimuovere.

**Abbiamo un cliente o un utente a disposizione del team, o indoviniamo che cosa vuole?**

Chiedi chi risponde alle domande su ciò di cui gli utenti hanno bisogno e quanto ci mette. Se la risposta è una lunga catena, chiedi quale domanda è stata più costosa da sbagliare. Ricorda i critici di XP stesso: un singolo rappresentante del cliente può essere un collo di bottiglia. Discuti come raggiungere più utenti brevemente e spesso.

## Nella pratica: un esempio di ITIL agile

Il team digitale di un'azienda di trasporto pubblico, di nove persone, costruisce e gestisce la propria app per la pianificazione dei viaggi e un feed di dati sugli arrivi in tempo reale usato da altri sviluppatori della città. Il team rilascia ogni mese dopo un ciclo di test manuali di quattro giorni. Quando un rilascio va male, il rollback richiede mezza giornata, quindi il team è riluttante a rilasciare più spesso. Il responsabile delle operations, che è anche lo sviluppatore più esperto, risponde alla maggior parte delle chiamate fuori orario perché nessun altro sa come funziona il feed.

Il team decide di adottare insieme alcune pratiche XP. Imposta un'integrazione continua che compila ed esegue i test unitari a ogni integrazione. Per ogni bug trovato in produzione, scrive un test che fallisce prima di correggerlo. Due sviluppatori lavorano in coppia con il responsabile delle operations sul feed per un'ora al giorno. Il team aggiunge anche un passaggio di deployment che può tornare alla versione precedente in pochi minuti.

Dopo quattro mesi, il team rilascia ogni settimana. La suite di test intercetta prima del rilascio due regressioni che il ciclo manuale avrebbe trovato solo l'ultimo giorno. Tre sviluppatori ora sanno gestire la maggior parte delle chiamate sul feed. Non tutto funziona: la suite di test impiega 25 minuti a girare, quindi gli sviluppatori integrano meno spesso del previsto, e una modifica difettosa al feed degli arrivi sfugge perché i suoi test usavano dati di esempio che non corrispondevano a un caso limite reale. Il team sposta i test lenti a una seconda fase in modo che i primi risultati arrivino entro cinque minuti e aggiunge un controllo di monitoraggio sull'output del feed. Concordano anche che la coppia resterà uno strumento per i problemi difficili e per l'inserimento, non una regola per ogni compito.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery possiedono le pratiche di XP. Inizia da quelle che danno feedback più rapido: test automatici e integrazione continua. Tratta la tua suite di test come un prodotto usato anche dalle operations. Descrive che cosa il servizio dovrebbe fare e ti dice in fretta quando smette di farlo.

### Team di servizio e di operations

Il personale operativo può usare le idee di XP per il proprio lavoro: modifiche a infrastruttura e configurazione testate prima di essere eseguite, piccole modifiche integrate spesso e conoscenza condivisa nel team attraverso la coppia e la proprietà collettiva. Chiedi ai team di delivery test che coprano i guasti che vedi in produzione e offri la cronologia degli incidenti per guidare ciò che viene testato.

### Leadership e governance

I leader rendono possibile XP proteggendo il ritmo, finanziando l'infrastruttura di build e test e accettando che la qualità sia incorporata nel lavoro e non ispezionata dopo. Chiedi prove di sicurezza che vengano dalla pipeline, come risultati dei test e cronologie dei rilasci, e non pretendere prove manuali duplicate.

### Clienti e utenti

I clienti hanno il ruolo più diretto in XP: fanno parte del ciclo di feedback del team. Aspettati che ti si chieda di provare rilasci piccoli, rispondere rapidamente alle domande e dire che cosa conta di più questa settimana. In cambio, dovresti vedere meno sorprese e correzioni più rapide ai problemi che segnali.

## Modalità di fallimento comuni

- **Adottare solo i rituali.** I team prendono gli stand-up e le lavagne e saltano test e integrazione. Inizia invece con test automatici e integrazione continua, perché danno il ritorno maggiore.
- **Trattare la coppia come una regola.** La coppia imposta su tutto il lavoro frustra le persone e rallenta i compiti di routine. Usala invece per problemi difficili, inserimento e trasferimento di conoscenza e rivedi come funziona.
- **Una suite di test di cui nessuno si fida.** I test lenti o inaffidabili vengono ignorati. Mantieni invece la suite veloce e correggi o elimina subito i test instabili.
- **Proprietà collettiva senza standard.** Chiunque può cambiare qualsiasi cosa e il codice si degrada. Abbinala invece a standard di codifica condivisi, revisione e controlli automatici.
- **Un solo rappresentante del cliente.** Una persona diventa il collo di bottiglia o la fonte di distorsione. Distribuisci invece il contatto su più utenti e verifica le decisioni con l'uso reale.
- **Saltare del tutto il design.** I team fanno refactoring ripetuti senza una direzione. Mantieni invece un quadro leggero dell'architettura e rivedilo a intervalli regolari.
- **Gli straordinari come norma.** Le lunghe ore erodono la qualità e causano incidenti. Pianifica invece a un ritmo sostenibile e tratta gli straordinari ripetuti come un segnale per ridurre l'ambito.
- **Ignorare le operations.** XP dice poco su come si gestisce il software, e i team assumono che sia coperto. Aggiungi invece controlli operativi ai test e invita il personale operativo alla pianificazione.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Test | I test sono manuali e tardivi | Alcuni team hanno test unitari automatici | I team scrivono test insieme al codice e li eseguono a ogni modifica | Risultati dei test e difetti sfuggiti sono monitorati e rivisti | La strategia di test è coordinata tra i servizi e condivisa con le operations |
| Integrazione e rilascio | L'integrazione è rara e i rilasci sono grandi | Alcuni team usano l'integrazione continua | Una pipeline condivisa compila, testa e installa ogni modifica | Frequenza di rilascio e tasso di fallimento sono misurati e migliorati | Le pipeline sono coordinate tra team e fornitori |
| Proprietà e conoscenza condivise | La conoscenza è in mano a pochi individui | Alcuni team lavorano in coppia o ruotano il lavoro | La proprietà collettiva con standard è la norma | Le lacune di conoscenza sono monitorate e ridotte | La conoscenza circola liberamente tra i team e nei runbook |
| Ritmo e benessere | Gli straordinari sono routine | Alcuni team osservano il proprio carico di lavoro | Il ritmo sostenibile è una politica dichiarata | Carico di reperibilità e straordinari sono misurati e rivisti | Il carico di lavoro è bilanciato tra i team in base a dati condivisi |

## Checklist

- [ ] Il team ha concordato quali pratiche XP usa e le ha provate insieme.
- [ ] I test automatici girano a ogni modifica e una build fallita viene corretta per prima.
- [ ] Ogni bug in produzione ha un test che l'avrebbe intercettato.
- [ ] Il lavoro viene integrato nel ramo condiviso più volte al giorno.
- [ ] I rilasci sono piccoli e un rollback si può fare rapidamente.
- [ ] Più di una persona può modificare e supportare ogni parte del sistema.
- [ ] La coppia è usata per i problemi difficili e per l'inserimento, e il suo effetto è rivisto.
- [ ] Gli straordinari sono rari e non ripetuti settimana dopo settimana.
- [ ] Un utente o un rappresentante degli utenti è disponibile a rispondere alle domande durante il lavoro.
- [ ] I test includono controlli sul monitoraggio e sul comportamento di ripristino.

## Prompt per l'IA

**Scopo: trasformare un incidente in produzione in un test e in un elenco di lezioni.**

```text
Help me learn from a production incident using Extreme Programming habits.

Incident description (factual, blameless, in order): [paste what happened, how it was detected, and how it was fixed].
The part of the system involved: [describe the component and what it does].
Our current tests for that part: [describe what is tested today, or write "unknown"].

Propose: (1) a test, described in plain words, that would have caught this before release; (2) two other tests worth adding nearby; (3) one change to our release process to make a similar fault less likely. Do not invent details about our system. Ask clarifying questions first if the description is too thin, mark assumptions, and list what you are unsure of.
```

**Scopo: valutare quanto è sicuro per il tuo team rilasciare piccole modifiche.**

```text
I want to understand how safe it is for our team to release small changes often.

Our path from change to production, step by step: [paste the steps, who does each, and roughly how long each takes].
Our automated checks: [list tests, builds, and scans, or write "none"].
How we roll back: [describe].
The last two releases that went wrong: [paste short factual descriptions].

Identify the steps that rely on manual work or one person's knowledge. For each, suggest one small automation or sharing step. Do not claim any standard requires something unless I pasted its text. Separate what the text shows from what you assume, and list what you are unsure of.
```

**Scopo: progettare un esperimento di un mese con la programmazione in coppia.**

```text
Help me design a one-month experiment with pair programming for a team of [number] people working on [type of system].

Our reasons for trying it: [for example "reduce single points of failure on the feed service"].
Constraints: [for example remote working, on-call duties, mixed experience levels].

Propose which kinds of work to pair on and which to leave alone, how to rotate partners, what to observe (use observations such as questions answered and defects found, and do not invent numbers), and how the team will decide at the end whether to continue. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: verificare una Definition of Done rispetto alla prontezza operativa.**

```text
Here is our current Definition of Done: [paste it].
Things the operations or support team has asked for: [paste, or write "unknown"].

Compare the two. List items operations would need that are missing, and for each one say whether it could be checked automatically in a build pipeline, and how. Do not state that any standard requires an item unless I have pasted its text. Mark assumptions and list what you are unsure of.
```

## Competenze per l'IA

- [extreme-programming](../../../../skills/extreme-programming/SKILL.md): da usare per rivedere o introdurre pratiche XP come la coppia, il test-driven development e l'integrazione continua.
- [user-story](../../../../skills/user-story/SKILL.md): da usare per trasformare i bisogni dei clienti in story con criteri di accettazione che possano diventare test automatici.
- [agile-delivery](../../../../skills/agile-delivery/SKILL.md): da usare per pianificare rilasci piccoli e frequenti e i controlli che li rendono sicuri.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): da usare per rivedere quanto bene funzionano le pratiche e scegliere un cambiamento.
- [runbook](../../../../skills/runbook/SKILL.md): da usare per trasformare la conoscenza in mano a una sola persona in una procedura condivisa e collaudata.

## Fonti principali

- **Extreme programming** ed **Extreme programming practices** (Wikipedia): una panoramica di storia, valori, pratiche e critiche, con citazioni.
- **Extreme Programming Explained** (Kent Beck): l'enunciazione originale del metodo; la seconda edizione aggiunge il valore del rispetto.
- **Manifesto for Agile Software Development** (agilemanifesto.org): XP è uno dei metodi i cui autori scrissero il Manifesto.
- **Extreme Programming Refactored: The Case Against XP** (Matt Stephens e Doug Rosenberg, 2003): la critica più nota, utile per mettere alla prova le proprie ipotesi.

## Riferimenti

1. Extreme programming — Wikipedia — https://en.wikipedia.org/wiki/Extreme_programming
2. Extreme programming practices — Wikipedia — https://en.wikipedia.org/wiki/Extreme_programming_practices
3. Pair programming — Wikipedia — https://en.wikipedia.org/wiki/Pair_programming
4. Test-driven development — Wikipedia — https://en.wikipedia.org/wiki/Test-driven_development
5. Continuous integration — Wikipedia — https://en.wikipedia.org/wiki/Continuous_integration
6. Code refactoring — Wikipedia — https://en.wikipedia.org/wiki/Code_refactoring
7. Kent Beck — Wikipedia — https://en.wikipedia.org/wiki/Kent_Beck
8. Ward Cunningham — Wikipedia — https://en.wikipedia.org/wiki/Ward_Cunningham
9. Manifesto for Agile Software Development — Beck et al., agilemanifesto.org — https://agilemanifesto.org/
