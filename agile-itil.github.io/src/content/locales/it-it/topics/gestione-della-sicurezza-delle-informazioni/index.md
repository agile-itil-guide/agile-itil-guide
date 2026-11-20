# Gestione della sicurezza delle informazioni

**La gestione della sicurezza delle informazioni protegge la riservatezza, l'integrità e la disponibilità delle informazioni attraverso controlli basati sul rischio, e in un'organizzazione agile i controlli funzionano meglio quando sono incorporati nella pipeline di consegna e nelle abitudini quotidiane dei team anziché aggiunti come cancello alla fine.**

## Perché è importante

Ogni servizio custodisce informazioni a cui qualcuno tiene: i dati dei clienti, i registri dei pagamenti, i dati sanitari, i piani interni. Un fallimento della sicurezza danneggia le persone che le informazioni descrivono, danneggia la reputazione dell'organizzazione e può comportare sanzioni legali e finanziarie. I team di gestione dei servizi sono spesso i primi a vedere il guasto, come un incidente, e quelli che devono ripristinare dopo il normale funzionamento.

Sicurezza e consegna continua sono spesso presentate come opposti: la sicurezza dice di rallentare, la delivery di accelerare. Questa visione non aiuta. La sicurezza che arriva solo alla fine di un rilascio produce sorprese tardive ed eccezioni affrettate. La sicurezza incorporata nel lavoro, con controlli che girano automaticamente e rischi discussi presto, protegge il servizio senza bloccarlo. Lo stesso vale per la gestione dei servizi: le pratiche che rendono sicuro il cambiamento rendono sicure anche le modifiche di sicurezza.

Questo argomento usa come fonti principali l'[articolo di Wikipedia sulla sicurezza delle informazioni](https://en.wikipedia.org/wiki/Information_security) e l'[articolo su ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001). Entrambi sono generali. Il primo è un articolo lungo, e questa guida ha letto solo i primi 100.000 dei suoi circa 243.000 caratteri. Questo argomento non dà consulenza legale; leggi, regolamenti e obblighi contrattuali differiscono per paese e settore, e la fonte giusta è il testo della regola che si applica a te.

## Concetti fondamentali

### Che cos'è la sicurezza delle informazioni

Wikipedia definisce la sicurezza delle informazioni come la protezione delle informazioni attraverso la mitigazione dei rischi informativi, con lo scopo di prevenire o ridurre accesso, uso, divulgazione, interruzione, cancellazione, corruzione, modifica o svalutazione non autorizzati delle informazioni e di ridurre l'impatto degli incidenti. Si applica a informazioni elettroniche, fisiche e intangibili ed è parte della gestione del rischio informativo.

### La triade CIA

Gli obiettivi centrali sono **riservatezza**, **integrità** e **disponibilità**, bilanciati rispetto all'efficienza delle policy e alla produttività dell'organizzazione. L'articolo li descrive così:

| Obiettivo | Significato | Esempio in un servizio |
|---|---|---|
| **Riservatezza** | Le informazioni sono protette dalla divulgazione non autorizzata | Solo il personale autorizzato può vedere le cartelle dei pazienti |
| **Integrità** | Le informazioni sono accurate e complete e non possono essere modificate in modo non autorizzato o non rilevato | L'importo di un pagamento non può essere alterato senza lasciare traccia |
| **Disponibilità** | Le informazioni sono accessibili quando servono | Il servizio resta attivo e resiste agli attacchi di negazione del servizio |

L'articolo nota che la riservatezza differisce dalla privacy, che definisce un concetto più ampio. Nota anche che le organizzazioni possono aggiungere obiettivi come autenticità, responsabilità, non ripudio e affidabilità e che il Parkerian Hexad, un modello esteso, ha meriti discussi. La disponibilità si collega direttamente alla gestione dei servizi (vedi Argomento 3.11 — Disponibilità, capacità e prestazioni).

### Gestione del rischio

L'articolo descrive il rischio come la probabilità di danno a un asset informativo. Le **vulnerabilità** sono debolezze, le **minacce** sono potenziali cause di danno e l'**impatto** è la perdita risultante. La gestione del rischio è un processo continuo e iterativo in cui la direzione può accettare, mitigare, trasferire (per esempio tramite assicurazione) o evitare un rischio. Ciò che resta è detto **rischio residuo**. L'articolo elenca sei passaggi: individuare gli asset, valutare le minacce, valutare le vulnerabilità, calcolare l'impatto, selezionare e implementare i controlli e valutare quei controlli.

### Controlli e difesa in profondità

I controlli proteggono riservatezza, integrità o disponibilità. L'articolo descrive la **difesa in profondità** (defense in depth), la stratificazione di controlli sovrapposti, con tipi di controllo descritti come amministrativi (policy, procedure), logici (misure tecniche come controllo degli accessi e cifratura) e fisici (serrature, strutture). Nessun controllo singolo basta; gli strati coprono i reciproci guasti.

### Incidenti di sicurezza

L'articolo descrive la gestione degli incidenti di sicurezza informatica come monitoraggio, rilevamento e risposta agli eventi di sicurezza, con piani di risposta agli incidenti attivati quando si rilevano violazioni, di solito condotti da un team di risposta agli incidenti. Gli incidenti di sicurezza sono un tipo di incidente e traggono vantaggio dagli stessi ruoli, dalla stessa comunicazione e dallo stesso apprendimento senza colpe (vedi Argomento 3.2 — Gestione degli incidenti), più passaggi specifici come la conservazione delle prove e la notifica alle autorità di vigilanza o alle persone interessate dove richiesto.

### ISO/IEC 27001 e 27002

Secondo Wikipedia, **ISO/IEC 27001** fissa i requisiti per stabilire, implementare, mantenere e migliorare continuamente un sistema di gestione della sicurezza delle informazioni (ISMS), compresa la valutazione e il trattamento dei rischi per la sicurezza delle informazioni. I suoi requisiti sono generici e pensati per organizzazioni di qualsiasi tipo, dimensione o natura. La prima edizione uscì nell'ottobre 2005 dallo standard britannico BS 7799-2, la seconda nel 2013 e la terza nell'ottobre 2022, allineata a ISO/IEC 27002:2022; un emendamento del febbraio 2024 ha aggiunto una considerazione sul cambiamento climatico.

Fatti chiave dall'articolo:

- I requisiti dell'ISMS sono nelle clausole da 4 a 10: contesto, leadership, pianificazione, supporto, operatività, valutazione delle prestazioni e miglioramento.
- L'Annex A dell'edizione 2022 ha 93 controlli di riferimento in quattro temi: organizzativi, relativi alle persone, fisici e tecnologici. L'edizione 2013 ne elencava 114. L'Annex A è un insieme di riferimento e non una checklist obbligatoria: le organizzazioni producono una **Dichiarazione di Applicabilità** (Statement of Applicability) che giustifica quali controlli includono ed escludono.
- La certificazione è facoltativa a meno che una legge, un contratto o uno schema la richieda. ISO non certifica le organizzazioni; lo fanno organismi di certificazione indipendenti, per fasi, seguite da audit di sorveglianza e ricertificazione su un ciclo di tre anni. Un certificato si applica solo entro il suo ambito dichiarato.
- **ISO/IEC 27002** fornisce indicazioni sui controlli dell'Annex A. È una guida e non ci si può certificare rispetto ad essa.

L'articolo nota che una revisione della letteratura del 2021 ha trovato pochi studi empirici sugli esiti della certificazione. Un certificato mostra che esiste un sistema di gestione; non è la prova che una specifica violazione non possa avvenire.

### Altri framework e leggi

L'articolo sulla sicurezza delle informazioni nomina molti altri standard e schemi, come il NIST Cybersecurity Framework, Cyber Essentials nel Regno Unito, gli Essential Eight in Australia e lo standard del settore delle carte di pagamento. Elenca anche leggi, tra cui il Computer Misuse Act (1990) e il Data Protection Act (1998) del Regno Unito e l'HIPAA (1996), il Gramm–Leach–Bliley Act (1999) e il Sarbanes–Oxley Act (2002) degli Stati Uniti. L'elenco mostra quanto siano varie le regole. Quali si applicano a te dipende da dove operi, dal settore e dai dati che detieni; chiedi alla tua funzione legale o di conformità (vedi Argomento 5.7 — Governance, rischio e conformità).

### Sicurezza nella pipeline di consegna

Le pratiche che si adattano alla consegna continua includono:

- **Discussione precoce delle minacce:** chiedi in pianificazione che cosa potrebbe andare storto con una funzionalità e chi vorrebbe farne un uso improprio.
- **Controlli automatizzati:** scansione di codice, dipendenze e configurazione a ogni modifica, con i risultati visibili al team (vedi Argomento 3.4 — Abilitazione dei cambiamenti).
- **Privilegio minimo:** dare a persone e sistemi solo l'accesso di cui hanno bisogno.
- **Gestione dei segreti:** tenere le credenziali fuori dal codice e ruotarle.
- **Test di sicurezza:** penetration test e test automatici come parte del ciclo (vedi la competenza sul test di sicurezza più avanti).
- **Logging e monitoraggio:** rilevare attività sospette (vedi Argomento 3.10 — Monitoraggio e gestione degli eventi).

Le indicazioni DORA, citate altrove in questa guida, elencano la sicurezza pervasiva tra le pratiche che sostengono la consegna continua (vedi Argomento 3.5 — Gestione di rilasci e deployment).

### Cultura e persone

L'articolo sulla sicurezza delle informazioni menziona ricerche sulla cultura della sicurezza, comprese sette dimensioni culturali individuate da Roer e Petric (2017). Qualunque sia il modello, il punto è che molte violazioni iniziano con le persone: un messaggio di phishing, un errore, una scorciatoia sotto pressione. La formazione, vie di segnalazione chiare e un atteggiamento senza colpe verso gli errori in buona fede migliorano la sicurezza più della colpa.

### Limiti delle fonti

L'articolo di Wikipedia non indica critiche specifiche alla triade CIA ed è stato letto solo in parte. L'articolo su ISO/IEC 27001 non discute il rapporto con ISO/IEC 20000 o con il ciclo plan-do-check-act. Questo argomento non dà istruzioni tecniche; usa indicazioni specialistiche per le tue piattaforme e il testo degli standard se devi dichiarare la conformità.

## Buone pratiche

1. **Sappi quali informazioni detieni e dove.** Fai un elenco dei principali tipi di informazioni, di chi possiede ciascuno, di dove è conservato e di quanto è sensibile. Non puoi proteggere ciò che non hai individuato.
2. **Fai le valutazioni del rischio in linguaggio semplice.** Per ogni servizio importante, chiedi che cosa potrebbe andare storto con riservatezza, integrità e disponibilità, con quale probabilità e quanto grave. Registra le decisioni di accettare, ridurre, trasferire o evitare ciascun rischio (vedi Argomento 5.7 — Governance, rischio e conformità).
3. **Stratifica i tuoi controlli.** Combina policy, controlli tecnici e controlli fisici così che un solo guasto non basti. Rivedi quali strati proteggono le tue informazioni più sensibili.
4. **Incorpora i controlli nella pipeline.** Esegui controlli di sicurezza automatici su codice, dipendenze e configurazione a ogni modifica e rendi visibili i controlli falliti. Correggi i problemi nel punto della modifica.
5. **Dai per impostazione predefinita il privilegio minimo.** Concedi l'accesso per ruolo e bisogno, rivedilo regolarmente e rimuovilo prontamente quando le persone se ne vanno o cambiano ruolo (vedi Argomento 3.6 — Gestione delle richieste di servizio).
6. **Gestisci bene i segreti.** Tieni le credenziali fuori dal codice sorgente, conservale in un vault gestito e ruotale. Verifica di poterle ruotare rapidamente dopo un incidente.
7. **Tratta gli incidenti di sicurezza come incidenti.** Usa gli stessi ruoli, la stessa comunicazione e la stessa revisione degli altri incidenti e aggiungi passaggi per prove, contenimento e notifica. Esercita il piano.
8. **Conosci i tuoi obblighi di notifica.** Scopri dalla tua funzione legale o di conformità quali leggi o contratti richiedono di notificare autorità o persone interessate dopo una violazione e con quale rapidità. Scrivilo nel piano degli incidenti, citando il testo della fonte.
9. **Includi i fornitori.** Chiedi ai fornitori critici come proteggono le tue informazioni e metti le aspettative nei contratti (vedi Argomento 3.14 — Gestione dei fornitori).
10. **Forma e parla.** Offri una formazione breve e regolare basata su esempi reali e rendi facile segnalare un errore o un messaggio sospetto senza colpe.
11. **Usa gli standard come fonte di struttura.** Se adotti ISO/IEC 27001, tratta l'Annex A come un insieme di riferimento, scrivi una Dichiarazione di Applicabilità giustificata e mantieni leggero l'ISMS. La certificazione è facoltativa a meno che sia richiesta.
12. **Impara dai quasi-incidenti.** Rivedi quasi-incidenti ed eventi a bassa gravità per schemi e portali nel backlog e nel registro dei rischi.

## Domande da discutere con il team

**Quali informazioni deteniamo che farebbero male alle persone se trapelassero, e dove sono?**

Chiedi a ciascuno di nominare i dati più sensibili che gestisce e dove vivono. Confronta. Le sorprese sono comuni: copie negli ambienti di test, esportazioni in cartelle condivise, log che contengono dati personali. Chi facilita può chiedere quale copia è meno protetta. Scegline una da ridurre o proteggere meglio.

**Quando abbiamo preso per l'ultima volta la decisione di accettare un rischio di sicurezza, e chi l'ha presa?**

Chiedi un esempio. I rischi accettati sono spesso accettati in silenzio, per ritardo. Discuti chi dovrebbe decidere, di quali informazioni ha bisogno e dove è registrato. L'elenco dell'articolo dei modi di trattare il rischio (accettare, mitigare, trasferire, evitare) è una cornice utile. Concorda un posto semplice dove registrare la prossima decisione.

**Quali controlli di sicurezza girano automaticamente a ogni modifica, e quali ignoriamo?**

Elenca i controlli nella pipeline e i risultati. Chiedi quali segnalazioni sono ignorate di routine e perché. Le segnalazioni ignorate di solito significano rumore, mancanza di responsabilità o mancanza di tempo. Decidi quali correggere, quali sopprimere con una ragione e chi possiede l'elenco.

**Chi ha accesso a che cosa, e quando l'abbiamo rivisto per l'ultima volta?**

Scegli un sistema sensibile ed elenca chi può raggiungerlo. Confronta con chi ne ha bisogno. Spesso gli accessi si sono accumulati. Chiedi con quale rapidità l'accesso viene rimosso quando qualcuno se ne va. Concorda una data di revisione e un responsabile.

**Che cosa faremmo nella prima ora di una sospetta violazione?**

Ripercorri i passaggi: chi viene informato, che cosa viene conservato, che cosa viene spento, chi parla con chi. Le lacune compaiono di solito attorno ad autorità e prove. Chiedi dove sta il piano e quando è stato usato l'ultima volta. Programma un'esercitazione tabletop.

**Quali regole su sicurezza o privacy si applicano a noi, e come lo sappiamo?**

Chiedi chi è responsabile di saperlo. Se la risposta è "l'ufficio legale" o "nessuno", chiedi come l'ingegneria viene a sapere dei requisiti. Le regole differiscono per paese e settore, quindi elenca i luoghi in cui operi. Concorda di chiedere alla funzione legale o di conformità un breve elenco, con il testo della fonte.

## Nella pratica: un esempio di ITIL agile

Il servizio di calcolo per la ricerca di un'università custodisce dataset di studi medici e dà ai ricercatori accesso a server di analisi. Lo gestisce un team di otto persone. Dopo un incidente in cui un ricercatore ha copiato un dataset non protetto in una cartella cloud personale, il responsabile della sicurezza dell'università pretende che ogni modifica e ogni richiesta di accesso passino per una revisione di sicurezza di tre settimane. I ricercatori obiettano che questo renderà il servizio inutilizzabile.

Il responsabile del servizio propone un approccio diverso e incontra il responsabile della sicurezza e due ricercatori. Elencano le informazioni custodite, raggruppando i dataset come pubblici, interni e sensibili. Per i dati sensibili, concordano controlli più rigidi: accesso per ruolo nominato e progetto, nessuna copia fuori dal servizio e registrazione delle esportazioni dei dati. Per gli altri dati si applicano regole più leggere. Il team aggiunge alla pipeline di delivery controlli automatici per l'archiviazione mal configurata e per i segreti nel codice, e il responsabile della sicurezza rivede i risultati ogni settimana invece di rivedere ogni modifica. Le richieste di accesso ai dataset sensibili seguono un modello di richiesta con approvazione da parte del responsabile dei dati del progetto e una data di scadenza. Viene tenuta per i ricercatori una breve sessione di formazione basata sull'incidente precedente.

Sei mesi dopo, non sono state trovate altre copie fuori dal servizio e le revisioni degli accessi richiedono un pomeriggio ogni trimestre. Restano alcune difficoltà. Un gruppo di ricercatori usa uno strumento che esporta i dati in un modo che la registrazione non cattura, e i controlli automatici producono falsi allarmi che il team ha cominciato a ignorare. Concordano con il responsabile della sicurezza di aggiungere lo strumento all'ambito della registrazione, di regolare i controlli e di rivedere gli allarmi ogni mese. Chiedono anche all'ufficio legale una dichiarazione scritta degli obblighi di notifica che si applicano ai dataset sensibili, così che il piano degli incidenti possa citare la fonte.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery rendono reale la sicurezza nel codice e nella configurazione. Discuti presto le minacce, tieni i segreti fuori dal codice, rispondi ai risultati automatici ed evita di condividere dati sensibili nei test. Di' a sicurezza e operations delle modifiche che alterano l'esposizione.

### Team di servizio e di operations

I team operativi gestiscono i controlli: accessi, monitoraggio, patching e backup. Tratta gli eventi di sicurezza come incidenti, conserva le prove e partecipa alle esercitazioni. Riporta gli schemi degli incidenti ai team di delivery e al registro dei rischi.

### Leadership e governance

I leader possiedono le decisioni sul rischio e la cultura che le circonda. Chiedi riassunti dei rischi in linguaggio semplice, sostieni il tempo per formazione ed esercitazioni e assicurati che qualcuno sia responsabile di ogni decisione di accettare un rischio. Non pretendere la certificazione come etichetta senza una ragione.

### Clienti e utenti

Clienti e utenti affidano al servizio le proprie informazioni. Usa l'autenticazione forte dove offerta, segnala i messaggi sospetti e chiedi ai fornitori come proteggono i tuoi dati e come ti informerebbero di una violazione. Aspettati onestà e rapidità se qualcosa va storto.

## Modalità di fallimento comuni

- **La sicurezza come cancello finale.** Le revisioni arrivano alla fine e ritardano i rilasci. Discuti invece presto le minacce e automatizza i controlli nella pipeline.
- **La conformità come obiettivo.** Un certificato nasconde pratiche deboli. Usa invece gli standard per la struttura e misura la protezione reale.
- **Dati non tracciati.** Le copie si diffondono nei sistemi di test e nell'archiviazione personale. Sappi invece dove vivono i dati sensibili e limita le copie.
- **Accessi in eccesso.** I diritti si accumulano e non vengono mai rimossi. Rivedi invece regolarmente gli accessi e fai scadere.
- **Segreti nel codice.** Le credenziali sono conservate nei repository. Usa invece un vault e ruota i segreti.
- **Nessun piano di incidente testato.** Il primo uso è una violazione reale. Esercita invece il piano e scrivi gli obblighi di notifica.
- **Colpa per gli errori.** Le persone nascondono gli errori. Rendi invece facile la segnalazione e rispondi con l'apprendimento.
- **Ignorare i fornitori.** Terze parti detengono dati senza protezioni chiare. Chiedi invece, stipula contratti e rivedi.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Informazioni e rischio | I dati sensibili non sono elencati; i rischi sono impliciti | Alcuni servizi registrano tipi di dati e rischi | Dati e rischi sono registrati per servizio con responsabili e decisioni | I rischi sono rivisti rispetto a incidenti e metriche | Le visioni del rischio sono condivise con clienti e fornitori e allineate |
| Controlli nella delivery | La revisione di sicurezza avviene alla fine, se avviene | Alcuni team eseguono scansioni di sicurezza | I controlli di sicurezza sono automatizzati in una pipeline comune, con responsabili per i risultati | Risultati, correzioni e sfuggiti sono misurati e rivisti | I controlli sono migliorati tra i team da prove condivise |
| Accessi e segreti | Gli accessi sono concessi in modo estemporaneo; segreti nel codice | Esistono alcune revisioni e vault | Accesso basato sui ruoli con scadenza e segreti gestiti sono standard | Le revisioni degli accessi e la rotazione sono misurate | Le pratiche di accessi e segreti sono coordinate con i partner |
| Risposta agli incidenti e cultura | Gli incidenti di sicurezza sono improvvisati | Esistono alcuni piani | Gli incidenti di sicurezza seguono il processo degli incidenti con passaggi aggiuntivi definiti e sono esercitati | Tempi di rilevamento e risposta sono misurati e l'apprendimento è condiviso | La risposta è coordinata con fornitori, clienti e autorità |

## Checklist

- [ ] Abbiamo elencato i principali tipi di informazioni, i loro responsabili, le posizioni e la sensibilità.
- [ ] I rischi per riservatezza, integrità e disponibilità sono valutati per i servizi importanti e le decisioni sono registrate.
- [ ] I controlli di sicurezza automatici girano a ogni modifica e le segnalazioni hanno responsabili.
- [ ] L'accesso è per ruolo e bisogno, rivisto regolarmente e rimosso quando non serve più.
- [ ] I segreti sono conservati in un vault gestito e possono essere ruotati rapidamente.
- [ ] Esiste un piano degli incidenti di sicurezza, è stato esercitato e include gli obblighi di notifica con il testo della fonte.
- [ ] Ai fornitori che detengono le nostre informazioni sono state chieste le loro protezioni.
- [ ] Il personale riceve una formazione breve e regolare e può segnalare errori senza colpe.
- [ ] Se usiamo ISO/IEC 27001, abbiamo una Dichiarazione di Applicabilità giustificata e un ISMS leggero.
- [ ] I quasi-incidenti sono rivisti per schemi.

## Prompt per l'IA

**Scopo: fare l'inventario delle tue informazioni e ordinarle per sensibilità.**

```text
Help me make a simple inventory of the information our service holds.

What the service does: [describe].
Data we know about (types, where stored, who can access): [paste a list; remove any real personal data].
Rules or contracts that apply, with source text: [paste, or write "none known"].

Produce a table with: information type, where it lives, who owns it, a suggested sensitivity level (public, internal, sensitive) with a one-sentence reason from my text, and one question to ask about protection. Mark guesses. Do not state that any law applies unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: condurre una breve discussione sulle minacce per una nuova funzionalità.**

```text
Help me run a 30-minute threat discussion for this new feature: [describe what it does, what data it handles, who uses it, and what it connects to].

Provide questions to ask under these headings: who might misuse it and how; what data could be exposed, changed, or made unavailable; what could go wrong through dependencies or suppliers; what we would see if it went wrong; and what safeguards we already have. Then give a template for recording risks with an owner and a decision (accept, reduce, transfer, or avoid). Do not invent attacks or vulnerabilities in my system. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: rivedere i risultati dei controlli di sicurezza automatici per rumore e priorità.**

```text
Here are findings from our automated security checks in the last [period]: [paste, with counts and short descriptions; remove sensitive details].
What we did about each (fixed, suppressed, ignored): [paste, or write "unknown"].

Group the findings by type. For each group, suggest a question to ask about whether it is noise, a real risk, or a tool configuration issue, using only the text. Identify which groups are most often ignored. Do not state that a finding is exploitable or harmless. Suggest how to assign owners. List what you are unsure of.
```

**Scopo: preparare un'esercitazione su un incidente di sicurezza.**

```text
Design a 60-minute tabletop exercise on a suspected data breach in [service].

Scenario basis: [describe, using facts you choose, for example "a laptop with access to production data is reported lost"].
Roles taking part: [list].
Notification duties that apply, with source text from legal or compliance: [paste, or write "not yet confirmed"].

Give a timed plan, prompts for each role (contain, preserve evidence, communicate, decide who is told), a list of decisions that need authority, and a closing step that records gaps with owners. Do not use real data or systems. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [security-testing](../../../../skills/security-testing/SKILL.md): da usare per pianificare i test di sicurezza come parte del ciclo di delivery.
- [risk-register](../../../../skills/risk-register/SKILL.md): da usare per registrare rischi di sicurezza, decisioni e responsabili.
- [key-risk-indicators](../../../../skills/key-risk-indicators/SKILL.md): da usare per scegliere misure di allerta precoce per i rischi di sicurezza.
- [data-governance](../../../../skills/data-governance/SKILL.md): da usare per definire chi possiede i dati e come possono essere usati e condivisi.
- [legal-data-privacy-compliance](../../../../skills/legal-data-privacy-compliance/SKILL.md): da usare per preparare domande per il personale legale o di conformità sugli obblighi di privacy.

## Fonti principali

- **Information security** (Wikipedia): la triade CIA, gestione del rischio, controlli e risposta agli incidenti, con un lungo elenco di standard e leggi correlati.
- **ISO/IEC 27001** (Wikipedia, e lo standard stesso da ISO): i requisiti per un sistema di gestione della sicurezza delle informazioni, con i controlli dell'Annex A e il processo di certificazione.
- **Computer security incident management** (Wikipedia): contesto sulla risposta agli eventi di sicurezza.
- **Defense in depth** (Wikipedia): contesto sui controlli stratificati.

## Riferimenti

1. Information security — Wikipedia — https://en.wikipedia.org/wiki/Information_security
2. ISO/IEC 27001 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_27001
3. ISO/IEC 27002 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_27002
4. Computer security incident management — Wikipedia — https://en.wikipedia.org/wiki/Computer_security_incident_management
5. Defense in depth (computing) — Wikipedia — https://en.wikipedia.org/wiki/Defense_in_depth_(computing)
6. Risk management — Wikipedia — https://en.wikipedia.org/wiki/Risk_management
7. Principle of least privilege — Wikipedia — https://en.wikipedia.org/wiki/Principle_of_least_privilege
8. Continuous delivery — DORA, dora.dev — https://dora.dev/capabilities/continuous-delivery/
9. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
