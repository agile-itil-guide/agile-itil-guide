# Gestione delle richieste di servizio

**La gestione delle richieste di servizio tratta le cose di routine che gli utenti chiedono, come accessi, attrezzature e informazioni, e l'obiettivo agile è rendere ogni richiesta comune rapida, prevedibile e in gran parte automatica, così che le persone competenti dedichino il loro tempo ai problemi.**

## Perché è importante

Gran parte del lavoro che arriva a un service desk non è affatto un guasto. È un utente che chiede qualcosa che il servizio è pensato per fornire: un nuovo account, l'accesso a una cartella, un portatile, una licenza, il reset di una password. Queste richieste sono prevedibili e ripetitive. Gestite bene, sono rapide e nessuno se ne accorge. Gestite male, sono la fonte di lunghe attese, domande ripetute e silenziosa frustrazione che danneggia la reputazione di un team più di qualsiasi singola interruzione.

La gestione delle richieste è anche il luogo in cui automazione e self-service rendono di più. Una richiesta che segue ogni volta gli stessi passaggi può essere progettata una volta, testata e in gran parte automatizzata. L'[articolo di Wikipedia sulla gestione dei servizi IT](https://en.wikipedia.org/wiki/IT_service_management) definisce una richiesta di servizio come una richiesta di routine per un servizio ed elenca l'automazione dei processi IT, che sostituisce i passaggi manuali di routine con passaggi automatizzati così che il personale possa concentrarsi sul lavoro a priorità più alta. È lo scopo di questa pratica in una frase.

L'articolo dice poco di più sulle richieste. Questo argomento combina quindi quella definizione con indicazioni pratiche tratte dalla pratica di gestione dei servizi di uso comune, offerte come tali, e con gli altri argomenti della guida su service desk, catalogo dei servizi e conoscenza. Dove qualcosa è una pratica comune e non un risultato di una fonte, il testo lo dice.

## Concetti fondamentali

### Che cos'è una richiesta di servizio

Una **richiesta di servizio** è una richiesta di routine per qualcosa che un servizio normalmente fornisce. Si differenzia da un **incidente**, che è un'interruzione o potenziale interruzione di un servizio, e da un **cambiamento**, che modifica un servizio (vedi Argomento 3.2 — Gestione degli incidenti e Argomento 3.4 — Abilitazione dei cambiamenti). Il confine può sfumare: "ho bisogno di accedere al sistema finanziario" è una richiesta; "ho accesso ma il sistema mostra un errore" è un incidente; "aggiungere un nuovo campo al sistema finanziario" è probabilmente un cambiamento.

Un test pratico: se il lavoro segue una procedura nota, ha un costo e un rischio noti e la risposta a "è consentito?" è già decisa in anticipo, è una richiesta. Tutto ciò che richiede un nuovo giudizio sul rischio è più probabilmente un cambiamento o un progetto.

### Perché la distinzione conta

Mescolare richieste e incidenti distorce entrambi. I conteggi dei "ticket" confondono due tipi diversi di domanda. Le priorità entrano in conflitto, perché un incidente che ferma il lavoro dovrebbe venire prima di una richiesta che può aspettare. Le misure di risposta ingannano: un lungo tempo medio di chiusura può nascondere che le richieste aspettano le approvazioni mentre gli incidenti vengono risolti in fretta. Tenere separati i due permette di fissare obiettivi adatti e di vedere dove sta il ritardo (vedi Argomento 2.1 — Gestione dei servizi IT).

### Modelli di richiesta

Un **modello di richiesta** è uno schema ripetibile per un tipo di richiesta: quali informazioni servono, chi deve approvare, quali passaggi sono svolti da chi o dall'automazione e qual è il tempo atteso. I modelli di richiesta sono un'idea ampiamente usata nella gestione dei servizi. Danno a un team un modo di progettare una volta le richieste comuni e di eseguirle molte volte. Un catalogo dei servizi elenca le richieste disponibili (vedi Argomento 3.8 — Gestione del catalogo dei servizi).

Un modello per "portatile per nuovo assunto" potrebbe specificare: le informazioni necessarie dal responsabile, l'approvazione (nessuna, se il ruolo è in un elenco standard), i passaggi (ordinare, configurare, spedire) e il tempo atteso. Un modello per "accesso a un sistema riservato" includerà un'approvazione del responsabile del sistema e un record per l'audit.

### Approvazione

Alcune richieste hanno bisogno di approvazione prima di procedere: spesa, accesso a dati sensibili o uso di risorse scarse. La domanda per la progettazione è se l'approvazione aggiunge un controllo reale. Un'approvazione che dice sempre sì è un ritardo. Dove le approvazioni servono, rendile rapide e visibili, di' all'approvatore esattamente che cosa gli viene chiesto e prevedi un'alternativa se non risponde. Dove l'approvazione dipende da un ruolo, come un responsabile che approva la richiesta di un membro del team, considera di preapprovare gli elementi standard per il ruolo.

### Evasione e automazione

L'evasione è il lavoro di consegnare la richiesta. L'articolo sull'ITSM descrive l'automazione dei processi IT come l'automazione dei compiti di routine così che il personale possa concentrarsi sul lavoro a priorità più alta. I candidati all'automazione sono le richieste frequenti, che seguono una procedura stabile e comportano basso rischio: reset di password, appartenenza a gruppi, installazioni standard di software. L'automazione dovrebbe essere costruita con la stessa cura di qualsiasi modifica, con test e un modo di vedere che cosa ha fatto.

### Self-service

Molte organizzazioni offrono un portale in cui gli utenti possono trovare il servizio di cui hanno bisogno, vedere quali informazioni servono e inviare una richiesta senza parlare con nessuno. Un buon self-service dipende da un elenco chiaro dei servizi scritto con le parole degli utenti e da moduli chiari. Un portale che rispecchia l'organigramma e chiede informazioni che l'utente non ha spingerà le persone verso e-mail e telefono.

### Enterprise service management

L'articolo sull'ITSM nota che l'enterprise service management applica strumenti e idee ITSM ad altre aree aziendali come le risorse umane o i servizi generali. La gestione delle richieste è il posto più facile da cui iniziare, perché molte funzioni ricevono richieste di routine: inserimento, viaggi, attrezzature, traslochi d'ufficio. Una piattaforma di richieste condivisa può servire più funzioni, ciascuna con i propri modelli di richiesta e responsabili.

### Misure

Le misure comuni includono quanto tempo richiedono le richieste dall'invio all'evasione, quanto spesso il richiedente deve tornare con domande, quante richieste sono evase senza sforzo umano e la soddisfazione dei richiedenti. Come per ogni misura, evita obiettivi che premiano la chiusura anticipata delle richieste. Cerca il tempo di attesa, perché la maggior parte del tempo trascorso di una richiesta è di solito attesa di approvazione o informazioni, non lavoro (vedi Argomento 1.7 — Sviluppo software lean e Argomento 5.6 — Metriche e misurazione).

### Sicurezza e conformità

Le richieste spesso controllano accessi e spese, quindi hanno implicazioni di sicurezza e di audit. I record dovrebbero mostrare chi ha chiesto, chi ha approvato, che cosa è stato fatto e quando. Rimuovi l'accesso quando non serve più, come parte di un modello di richiesta per chi lascia l'organizzazione, non come ripensamento (vedi Argomento 3.13 — Gestione della sicurezza delle informazioni).

## Buone pratiche

1. **Parti dalle richieste più comuni.** Elenca le prime dieci richieste per volume dai tuoi record. Progetta prima queste. Pochi modelli ben progettati coprono gran parte della domanda.
2. **Definisci un modello di richiesta per ciascuna.** Scrivi quali informazioni servono, chi approva, i passaggi, chi svolge ciascuno e il tempo atteso. Mantieni ogni modello a una pagina.
3. **Usa le parole dell'utente.** Dai alle richieste i nomi che userebbero gli utenti ("Ottenere un nuovo portatile", non "Richiesta di provisioning hardware tipo 2"). Verifica i nomi con gli utenti.
4. **Chiedi solo ciò che serve.** Ogni campo di un modulo dovrebbe avere uno scopo. Recupera ciò che puoi dai sistemi che già hai, come il reparto dell'utente, invece di chiederlo all'utente.
5. **Preapprova ciò che è di routine.** Concorda con gli approvatori un elenco standard di elementi e ruoli che non richiedono approvazione caso per caso. Rivedi l'elenco periodicamente.
6. **Rendi facili e rapide le approvazioni reali.** Mostra all'approvatore che cosa gli viene chiesto e perché, consenti l'approvazione da telefono o e-mail e imposta un promemoria automatico e un delegato per le assenze.
7. **Automatizza ciò che è stabile e frequente.** Scegli richieste che seguono gli stessi passaggi ogni volta e comportano basso rischio. Testa l'automazione e registra che cosa ha fatto.
8. **Mantieni una via umana.** Consenti agli utenti di chiedere aiuto quando un modulo non si adatta alle loro esigenze. Tratta quei casi come feedback sul modello.
9. **Separa le richieste da incidenti e cambiamenti.** Dai a ciascuno la propria categoria, coda e misure. Insegna al desk a riclassificare quando una richiesta si rivela un guasto o un cambiamento.
10. **Osserva le attese.** Misura il tempo speso ad aspettare approvazione o informazioni, non solo il tempo totale. Scegli per prima l'attesa più lunga da ridurre.
11. **Chiudi il cerchio con il richiedente.** Conferma il completamento, chiedi se ha funzionato e offri un modo di dire se non ha funzionato. Una richiesta segnata come fatta ma non consegnata è peggio di una ancora aperta.
12. **Rivedi regolarmente il catalogo delle richieste.** Ritira le richieste che nessuno fa, unisci i quasi-duplicati e aggiungine di nuove sulla base di prove (vedi Argomento 3.8 — Gestione del catalogo dei servizi).

## Domande da discutere con il team

**Quali richieste gestiamo più spesso, e quanto richiede ciascuna dall'inizio alla fine?**

Estrai le prime dieci dell'ultimo trimestre e ripercorri il tempo trascorso per ciascuna. Segna dove ogni richiesta aspetta. La sorpresa è di solito che la maggior parte del tempo è attesa, non lavoro. Chiedi chi aspetta chi. Chi facilita può chiedere quale richiesta sarebbe più facile da migliorare per prima.

**Quali approvazioni nelle nostre richieste non hanno mai detto di no?**

Rivedi un campione di approvazioni e conta i rifiuti. Un'approvazione che non rifiuta mai può essere un ritardo senza beneficio. Chiedi a che cosa serve l'approvazione e chi ne beneficia. Alcune approvazioni esistono per audit o responsabilità, che è uno scopo legittimo che si può soddisfare in modo più leggero, come notificare l'approvatore a posteriori. Scegline una da semplificare.

**Che cosa devono dirci gli utenti che già sappiamo?**

Guarda un modulo di richiesta e segna i campi le cui risposte esistono in un altro sistema. Ogni campo del genere è sforzo per l'utente e fonte di errore. Chiedi che cosa servirebbe per precompilarli. Scegli un campo da rimuovere o precompilare.

**Quali delle nostre richieste potrebbero essere evase senza che una persona le tocchi?**

Elenca le richieste che seguono una procedura fissa. Per ciascuna, chiedi che cosa impedisce l'automazione: strumenti, accessi, paura di errori. Discuti le salvaguardie che renderebbero accettabile l'automazione, come limiti e log. Scegline una da automatizzare come esperimento.

**Come scoprono gli utenti che cosa possono chiedere?**

Chiedi a qualche utente come richiederebbe qualcosa di insolito. Se la risposta è "chiedo a qualcuno che conosco", l'elenco dei servizi non funziona. Discuti come è presentato l'elenco e se i nomi hanno senso per gli utenti. Verifica una bozza con due o tre utenti.

**Quando una richiesta si rivela qualcos'altro, che cosa succede?**

Raccogli esempi di richieste che erano in realtà incidenti o cambiamenti. Chiedi quanto è costata la classificazione errata. Discuti come il desk riconosce e riclassifica e se il modulo aiuta gli utenti a scegliere correttamente. Concorda un semplice passaggio di riclassificazione.

## Nella pratica: un esempio di ITIL agile

Un istituto nazionale di statistica ha 3.000 dipendenti e un reparto IT di 80 persone. I nuovi assunti aspettano di routine dieci giorni per un portatile funzionante e gli account, e i responsabili si lamentano che i nuovi assunti restano inattivi. Il service desk gestisce le richieste di inserimento come ticket individuali, con ciascuno di cinque team che svolge un passaggio e passa il ticket.

Una responsabile del miglioramento mappa una richiesta di inserimento. Scopre che il lavoro effettivo richiede circa tre ore e il resto è attesa: che il responsabile fornisca i dettagli, per un'approvazione di budget su un portatile standard e che ciascun team si accorga del ticket. Il team progetta un modello di richiesta per i nuovi assunti. Il responsabile compila un breve modulo tre settimane prima della data di inizio, con la maggior parte dei campi riempiti dal sistema delle risorse umane. Portatili standard e account per il ruolo sono preapprovati. Uno script crea account e gruppi; l'hardware è ordinato automaticamente da un elenco di magazzino; il desk riceve un unico elenco di attività. Il responsabile del nuovo assunto riceve aggiornamenti e una conferma.

Dopo due mesi, il tempo mediano dalla richiesta al portatile pronto scende a tre giorni quando il modulo è inviato in tempo. Restano alcune difficoltà. Circa un terzo dei responsabili invia ancora il modulo in ritardo, quindi i nuovi assunti aspettano ancora, e lo script fallisce quando il record delle risorse umane non ha il codice del reparto, producendo lavoro di riparazione manuale. Il team aggiunge un promemoria alla checklist di inserimento delle risorse umane, imposta un allarme per gli script falliti e inizia a parlare con le risorse umane del miglioramento dei dati. Mantengono anche una via umana per i ruoli che non rientrano nell'elenco standard.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery spesso ricevono richieste che sono in realtà cambiamenti: un nuovo campo, un nuovo report. Aiuta il desk a riconoscerli e a instradarli al tuo backlog. Dove le richieste per il tuo servizio sono frequenti, come gli accessi, costruisci una via self-service con limiti chiari e log.

### Team di servizio e di operations

Operations e desk possiedono la maggior parte dei modelli di richiesta. Progetta prima i più comuni, elimina le attese e automatizza dove sicuro. Proteggi il tempo per costruire e rivedere i modelli, perché il lavoro sulle richieste soffoca facilmente il lavoro di miglioramento. Condividi i dati sulle attese con approvatori e manager.

### Leadership e governance

Leader e approvatori determinano gran parte dell'attesa. Chiedi quali approvazioni aggiungono controllo e quali aggiungono ritardo e accetta la preapprovazione dove il rischio è basso. Sostieni una piattaforma di richieste condivisa tra funzioni e chiedi misure del tempo di attesa anziché conteggi di ticket.

### Clienti e utenti

Gli utenti traggono vantaggio da nomi chiari, moduli brevi e stime oneste. Fornisci informazioni complete quando chiedi e di' quando è urgente e perché. Di' al team quando una richiesta non ha consegnato ciò di cui avevi bisogno, perché ciò migliora il modello per la persona successiva.

## Modalità di fallimento comuni

- **Trattare le richieste come incidenti o viceversa.** Priorità e report sono distorti. Separali invece e insegna la riclassificazione.
- **Moduli che chiedono troppo.** Gli utenti abbandonano il portale. Chiedi invece solo ciò che serve e precompila il resto.
- **Approvazioni come rituale.** Ogni richiesta aspetta una firma che non rifiuta mai. Preapprova invece gli elementi di routine e mantieni rapide le approvazioni reali.
- **Automazione senza salvaguardie.** Uno script fa la modifica sbagliata su larga scala. Testa, limita e registra invece l'automazione e monitora i fallimenti.
- **Nomi interni.** Gli utenti non trovano ciò che serve. Dai invece alle richieste nomi nelle parole degli utenti e verificali.
- **Nessuna via umana.** Le esigenze insolite cadono nel vuoto. Offri invece aiuto e tratta le richieste strane come feedback.
- **Contare solo la velocità.** Le richieste sono chiuse presto. Conferma invece con il richiedente e osserva le richieste ripetute.
- **Non ritirare mai le richieste.** L'elenco diventa obsoleto. Rivedi invece regolarmente l'uso e rimuovi ciò che nessuno chiede.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Modelli di richiesta | Ogni richiesta è gestita in modo estemporaneo | Esistono modelli per alcune richieste frequenti | Esistono modelli per le richieste principali con responsabili e tempi attesi | Le prestazioni dei modelli sono misurate e regolate | I modelli sono condivisi tra funzioni e fornitori |
| Approvazione | L'approvazione è informale o per abitudine | Alcuni elementi di routine sono preapprovati | Elenchi di preapprovazione e vie di approvazione rapide sono standard | Esiti e attese delle approvazioni sono rivisti | Le regole di approvazione sono allineate tra le funzioni in base ai dati sul rischio |
| Automazione e self-service | Le richieste sono gestite manualmente per e-mail | Alcune richieste sono disponibili in un portale o automatizzate | Le richieste frequenti a basso rischio sono automatizzate e il self-service è standard | Successo dell'automazione e sforzo degli utenti sono misurati | Automazione e self-service coprono IT, risorse umane e servizi generali |
| Apprendimento e miglioramento | Le richieste non sono analizzate | Si raccolgono alcuni conteggi | Attese e richieste ripetute sono riviste regolarmente | I miglioramenti sono pianificati dai dati e gli effetti verificati | Le idee di miglioramento vengono da utenti e team in tutta l'organizzazione |

## Checklist

- [ ] Conosciamo le nostre dieci richieste più comuni e quanto richiede ciascuna.
- [ ] Ognuna ha un modello di richiesta: informazioni necessarie, approvatore, passaggi, responsabile, tempo atteso.
- [ ] Le richieste hanno nomi nelle parole degli utenti.
- [ ] I moduli chiedono solo le informazioni necessarie e precompilano ciò che sappiamo.
- [ ] Gli elementi di routine sono preapprovati e le approvazioni reali hanno una via rapida e un delegato.
- [ ] Le richieste frequenti a basso rischio sono automatizzate con test e log.
- [ ] Richieste, incidenti e cambiamenti sono separati con un passaggio di riclassificazione.
- [ ] Misuriamo il tempo di attesa oltre al tempo totale.
- [ ] Ai richiedenti viene chiesto di confermare il completamento.
- [ ] L'elenco delle richieste è rivisto almeno due volte l'anno.

## Prompt per l'IA

**Scopo: trovare le richieste più comuni e le attese più lunghe.**

```text
Here is data on service requests from the last [period]: [paste a table with request type, date submitted, date approved if any, date fulfilled, and any notes; remove personal data].

Using only my data, list the ten most common request types with counts, the typical elapsed time for each (give the middle value and the range), and how much of that time was waiting for approval, if the data shows it. Highlight the three requests with the longest waits. Suggest questions to ask the owners. Do not invent numbers or causes. If the data is too thin, tell me what to collect. List what you are unsure of.
```

**Scopo: scrivere un modello di richiesta per una richiesta.**

```text
Help me write a request model for [request, e.g. "access to a shared team folder"].

How it is handled today, step by step, with who does each: [paste].
Information the requester must provide today: [list].
Approvals today and who gives them: [list].
Rules we must follow, with source text if available: [paste, or write "none known"].

Produce a one-page model: purpose, who may request, information needed (mark what could be prefilled from existing systems), approval (and a suggestion for pre-approval where low risk), steps with who or what does each, expected time marked as [to be agreed], and how completion is confirmed. Mark assumptions. Do not invent rules. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: riscrivere un modulo di richiesta perché sia più breve e più chiaro.**

```text
Here is a request form we use: [paste the fields and instructions].
Here is what we already know about the requester from other systems: [list, such as name, department, manager].

For each field, say whether it is needed, could be prefilled, or could be removed, and give a reason from the text. Rewrite the form with clear labels in plain language. Do not remove any field that I have marked as required by a rule: [list, or write "none known"]. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: decidere che cosa automatizzare per primo.**

```text
Here is a list of our requests with volume per month, steps, and how risky each step is (my judgment): [paste].
Tools we can automate with: [list, or write "unknown"].
Safeguards we can put in place: [list, such as logs, limits, approvals for exceptions].

Rank the requests as automation candidates, using only my data, and explain each ranking in one sentence. For the top two, list what could go wrong and a safeguard for each. Do not invent volumes. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [service-catalog](../../../../skills/service-catalog/SKILL.md): da usare per elencare le richieste che gli utenti possono fare, con le loro parole, con i responsabili.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): da usare per trovare le richieste più comuni e i loro volumi.
- [workflow-analysis](../../../../skills/workflow-analysis/SKILL.md): da usare per analizzare i passaggi e le attese di una richiesta.
- [user-story](../../../../skills/user-story/SKILL.md): da usare per descrivere una richiesta dal punto di vista dell'utente con criteri di accettazione.
- [runbook](../../../../skills/runbook/SKILL.md): da usare per documentare i passaggi delle richieste che restano manuali.

## Fonti principali

- **IT service management** (Wikipedia): definisce una richiesta di servizio, l'enterprise service management e l'automazione dei processi IT.
- **Help desk** (Wikipedia): contesto sulla gestione delle code e sull'instradamento per le richieste che arrivano a un desk.
- **Business process automation** (Wikipedia): contesto generale sull'automazione del lavoro di routine.
- **ITIL** (Wikipedia): il contesto della gestione delle richieste di servizio in ITIL.

## Riferimenti

1. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
2. Help desk — Wikipedia — https://en.wikipedia.org/wiki/Help_desk
3. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
4. Enterprise service management — Wikipedia — https://en.wikipedia.org/wiki/Enterprise_service_management
5. Business process automation — Wikipedia — https://en.wikipedia.org/wiki/Business_process_automation
6. Self-service software — Wikipedia — https://en.wikipedia.org/wiki/Self-service_software
7. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
8. Access control — Wikipedia — https://en.wikipedia.org/wiki/Access_control
