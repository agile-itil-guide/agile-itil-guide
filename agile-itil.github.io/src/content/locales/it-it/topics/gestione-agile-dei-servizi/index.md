# Gestione agile dei servizi

**La gestione agile dei servizi applica valori e metodi agili alla progettazione e al miglioramento della gestione dei servizi stessa, trattando ogni processo come un prodotto con un responsabile, un backlog e utenti che possono dire se funziona.**

## Perché è importante

Gran parte di questa guida ha guardato a come i team agili possono usare le pratiche di gestione dei servizi. Questo argomento rovescia la domanda: come si possono costruire e cambiare in modo agile le pratiche di gestione dei servizi? Molte organizzazioni hanno processi per incidenti, cambiamenti e richieste progettati una volta, introdotti in un progetto e lasciati lì. Sono lenti da cambiare, mal sopportati da chi deve seguirli e fuori passo con il modo in cui l'organizzazione ora costruisce il software. È l'opposto di ciò che suggerirebbe il principio del Manifesto di accogliere il cambiamento (vedi Argomento 1.2 — I principi agili).

Il rimedio non è abbandonare il processo ma trattarlo come qualcosa che si progetta con i suoi utenti, si rilascia a piccoli passi e si migliora dalle prove. I principi guida di ITIL 4 dicono lo stesso: partire da dove si è, procedere in modo iterativo con feedback, collaborare e promuovere la visibilità e mantenere semplice e pratico (vedi Argomento 2.4 — I principi guida di ITIL). L'articolo di Wikipedia su ITIL dice che ITIL 4 era allineato ai modi di lavorare agili, DevOps e lean quando fu pubblicato nel 2019. L'articolo su ISO/IEC 20000 elenca parti recenti di quello standard, comprese indicazioni su agile e DevOps, anche se non ne dà il contenuto.

C'è poca ricerca formale sulla gestione agile dei servizi in quanto tale, e gli articoli di Wikipedia consultati per questa guida non la trattano. Questo argomento attinge quindi alla descrizione di ruoli e artefatti della Scrum Guide, ai principi agili e ITIL e al resto di questa guida e offre il proprio approccio come sintesi pratica da provare, non come metodo consolidato.

## Concetti fondamentali

### I processi come prodotti

Un **processo**, in questo senso, è qualsiasi modo ripetibile di lavorare che un'organizzazione di servizio chiede alle persone di seguire: come segnalare un incidente, come richiedere un accesso, come approvare una modifica. Visto come prodotto, un processo ha:

- **Utenti:** le persone che lo seguono e quelle che serve.
- **Uno scopo:** il risultato che esiste per ottenere.
- **Un responsabile:** qualcuno responsabile del suo valore, come la Scrum Guide descrive il Product Owner come l'unica persona responsabile di massimizzare il valore del prodotto e ordinare il suo backlog (vedi Argomento 1.4 — Previsioni di consegna e metriche di pianificazione).
- **Un backlog:** un elenco ordinato di miglioramenti.
- **Rilasci:** modifiche consegnate a piccoli passi, con note.
- **Misure:** prove del fatto che funziona.

Pensare così cambia le domande. Non "abbiamo implementato il processo di cambiamento?" ma "il processo di cambiamento aiuta le persone a fare il loro lavoro, e qual è il prossimo miglioramento?"

### Ruoli

| Ruolo | In un team di prodotto | Per un processo di gestione dei servizi |
|---|---|---|
| **Product owner** | Ordina il backlog ed è responsabile del valore | Il responsabile del processo, che decide che cosa migliorare dopo e perché |
| **Sviluppatori / team** | Costruiscono l'incremento | Le persone che progettano e gestiscono il processo, idealmente inclusi utenti di delivery e operations |
| **Scrum Master o coach** | Aiuta il team ad applicare il framework e rimuove gli impedimenti | Un coach che aiuta il team a praticare la consegna continua di software e a raccogliere feedback |
| **Stakeholder** | Rivedono l'incremento e danno feedback | Team di delivery, service desk, auditor, clienti |

L'associazione è di questa guida, non uno standard. I responsabili dei processi in molte organizzazioni mancano di autorità o di tempo, quindi il primo passo è spesso dare loro entrambi.

### Il backlog del processo

Le idee di miglioramento per un processo vengono da molti posti: revisioni degli incidenti, retrospettive, rilievi di audit, reclami degli utenti e metriche (vedi Argomento 3.15 — Miglioramento continuo). Un backlog del processo le raccoglie in un unico elenco ordinato. Le voci sono piccole e descritte dal punto di vista dell'utente: "Come sviluppatore, voglio che le modifiche a basso rischio siano approvate automaticamente così da poter rilasciare quando sono pronto". Il product owner ordina l'elenco per valore e sforzo e il team prende le voci in cicli brevi.

### Consegna continua delle modifiche di processo

Invece di progettare un processo completo e introdurlo, progetta la più piccola versione che potrebbe funzionare, provala con pochi utenti e impara:

| Passaggio | Che cosa avviene |
|---|---|
| **Trova il problema** | Osserva come le persone lavorano davvero e dove faticano |
| **Progetta una piccola modifica** | Un nuovo modulo, una via di approvazione più breve, una checklist |
| **Provala** | Con un team, o un tipo di lavoro, per un breve periodo |
| **Verifica** | Confronta con ciò che ti aspettavi, usando dati e conversazione |
| **Adotta, adegua o abbandona** | Diffondi ciò che ha funzionato; correggi o abbandona ciò che non l'ha fatto |

È il ciclo plan–do–check–act applicato al processo stesso (vedi Argomento 3.15 — Miglioramento continuo).

### Progettare con gli utenti

I progettisti di processo che non usano il processo fanno errori evitabili. Coinvolgi le persone che lo seguono: invita gli ingegneri a progettare il processo di cambiamento, gli analisti del desk a progettare il modulo degli incidenti e i clienti a progettare il catalogo delle richieste. Osserva il lavoro reale. Prova con casi reali. È "la collaborazione col cliente più della negoziazione dei contratti" applicata all'interno dell'organizzazione (vedi Argomento 1.1 — Il Manifesto Agile).

### Processo minimo vitale

Un **processo minimo vitale** (minimum viable process) è il più piccolo insieme di passaggi, record e ruoli che raggiunge lo scopo. Aggiungervi richiede una ragione. Il principio guida "mantenere semplice e pratico" lo sostiene. Un test utile per ogni passaggio è chiedere che cosa succederebbe se fosse rimosso e chi se ne accorgerebbe. I controlli richiesti da legge o contratto sono mantenuti, con la fonte indicata; gli altri sono messi in discussione.

### Rilasci del processo e comunicazione

Quando un processo cambia, le persone devono saperlo. Tratta i cambiamenti come rilasci: una breve nota che descrive che cosa è cambiato, perché e che cosa fare diversamente, con un contatto per le domande. Rilascia a piccoli passi, con un ritmo che le persone possano seguire, ed evita di sorprendere i team con grandi cambiamenti. Tieni una storia visibile dei cambiamenti.

### Standard, audit e agilità

Molte organizzazioni devono soddisfare standard o auditor. ISO/IEC 20000 è uno standard per i sistemi di gestione dei servizi, e Wikipedia elenca una parte recente di esso con indicazioni su agile e DevOps (vedi Argomento 2.7 — Framework e standard ITSM). Un processo costruito a piccoli passi può soddisfare gli audit se i record mostrano come funziona e come cambia: backlog, note di rilascio e misure sono essi stessi prove. Discuti presto con gli auditor di che cosa hanno bisogno e mostra loro il modo in cui lavori.

### Gestione agile dei servizi e DevOps

Le pratiche DevOps, come automazione e pipeline, sono strumenti per implementare i processi (vedi Argomento 5.2 — DevOps). Dove un passaggio del processo può essere automatizzato, come registrare una modifica da una pipeline, fallo e tratta l'automazione come parte del processo. La gestione agile dei servizi e DevOps condividono l'interesse per i cicli brevi e il feedback rapido.

### Limiti

L'approccio presuppone che le persone abbiano tempo e mandato per migliorare il processo, il che non è sempre vero. Può fallire quando la responsabilità del processo è nominale, quando gli stakeholder pretendono un progetto finito prima di provare qualsiasi cosa o quando ogni modifica richiede una lunga approvazione. Rischia anche un continuo rimescolamento se i cambiamenti sono troppo frequenti perché le persone li assorbano. Bilancia la consegna continua del cambiamento con la stabilità: cambia con un ritmo prevedibile.

## Buone pratiche

1. **Nomina un responsabile per ogni processo.** Scegli qualcuno con l'autorità di cambiarlo e il tempo per farlo. Rendi chiaro il suo ruolo: risponde di quanto bene il processo serve il suo scopo.
2. **Scrivi uno scopo in una frase.** Indica a che cosa serve il processo e chi serve. Se non puoi, il processo potrebbe essere candidato alla rimozione.
3. **Tieni un backlog del processo.** Raccogli idee da revisioni, audit, feedback e dati in un unico elenco ordinato. Mostralo a chi segue il processo.
4. **Coinvolgi gli utenti nella progettazione.** Includi ingegneri, analisti del desk e clienti in workshop e prove. Osserva il lavoro reale prima di cambiarlo.
5. **Parti da un processo minimo vitale.** Progetta la più piccola versione che soddisfa lo scopo e le esigenze legali. Aggiungi passaggi solo quando un problema lo giustifica.
6. **Prova prima di estendere.** Sperimenta con un team o un tipo di lavoro per un periodo breve e definito. Concorda che cosa guarderai prima di iniziare.
7. **Rilascia le modifiche a piccoli passi con un ritmo.** Pubblica una breve nota per ogni rilascio del processo, con un contatto. Evita cambiamenti grandi e a sorpresa.
8. **Misura il processo.** Scegli poche misure del fatto che funziona, come tempo impiegato, rilavorazioni e soddisfazione degli utenti (vedi Argomento 5.6 — Metriche e misurazione). Rivedile con gli utenti.
9. **Automatizza dove aiuta.** Cattura i record dagli strumenti, non dai moduli; fai in modo che la via facile sia quella giusta. Verifica che l'automazione non nasconda un giudizio che le persone dovrebbero esprimere.
10. **Conserva le prove per gli auditor.** Conserva backlog, decisioni, note di rilascio e misure dove gli auditor possano vederli. Invitali a una revisione di come cambia il processo.
11. **Ritira il processo.** Rimuovi passaggi, moduli e record che non servono più il loro scopo. Tratta l'eliminazione come un miglioramento.
12. **Rivedi ogni anno la responsabilità dei processi.** Verifica che ogni processo abbia ancora un responsabile attivo, un backlog aggiornato e utenti che possano raggiungerlo.

## Domande da discutere con il team

**Chi possiede ciascuno dei nostri processi, e quale autorità ha di cambiarlo?**

Elenca i processi principali e nomina il responsabile di ciascuno. Chiedi che cosa il responsabile può cambiare senza chiedere a nessuno. Spesso la risposta è "molto poco". Chi facilita può chiedere che cosa servirebbe perché il responsabile faccia piccole modifiche rapidamente. Concorda un processo da cui partire.

**A che cosa serve il nostro processo di cambiamento? Sappiamo dirlo in una frase?**

Chiedi a ciascuno di scrivere uno scopo. Confronta. Le differenze mostrano confusione su perché il processo esiste. Usa la dichiarazione condivisa per giudicare ogni passaggio. Rimuovi o metti in discussione i passaggi che non la servono.

**Quando abbiamo cambiato per l'ultima volta un processo perché gli utenti l'hanno chiesto, e come l'abbiamo scoperto?**

Chiedi esempi. Se non ce ne sono, chiedi dove vanno i reclami. Discuti come il feedback potrebbe raggiungere il responsabile: un canale, una revisione regolare, una breve indagine. Scegli una via da provare.

**Che aspetto avrebbe una sperimentazione di un mese di un processo più semplice?**

Scegli un processo con attrito noto. Descrivi una versione più leggera, chi la proverebbe, che cosa misureresti e che cosa ti farebbe fermare. Questo trasforma una discussione in un esperimento. Concorda i dettagli e la data.

**Quali prove accetterebbero i nostri auditor da un processo di consegna continua di software?**

Chiedilo a un auditor o a un collega della conformità. Elenca che cosa produce il processo: un backlog, note di rilascio, misure, record. Discuti le lacune. I team spesso restano sorpresi da quanto gli auditor siano disposti ad accettare prove chiare di un cambiamento controllato.

**Come scoprono le persone che un processo è cambiato?**

Ripercorri l'ultimo cambiamento. Molte persone l'hanno appreso da un collega o imbattendosi in esso. Discuti note di rilascio e un registro visibile dei cambiamenti. Concorda un modo semplice di annunciare i cambiamenti e dove vivono.

## Nella pratica: un esempio di ITIL agile

Un'agenzia nazionale per la sicurezza stradale ha un reparto IT di 90 persone che supportano un'applicazione usata da polizia e tribunali. Il processo degli incidenti del reparto fu scritto otto anni fa: un modulo di 14 campi, tre approvazioni per chiudere un incidente ad alta priorità e un rapporto mensile che nessuno legge. I team di delivery saltano il modulo durante le interruzioni e lo compilano dopo, quindi i suoi record sono scadenti. Un rilievo di audit dice che i record degli incidenti sono incompleti.

La responsabile della gestione dei servizi si nomina responsabile del processo degli incidenti e forma un piccolo gruppo di lavoro: due analisti del service desk, un ingegnere da ciascuno di due team di delivery e un addetto qualità dall'unità di governance dell'agenzia. Scrive uno scopo per il processo: ripristinare rapidamente il servizio e imparare da ciò che è successo. Il gruppo osserva tre incidenti reali. Scoprono che il modulo viene compilato dopo l'evento, per lo più con gli stessi pochi valori, e che le approvazioni aggiungono ritardo senza mai cambiare un esito. Costruiscono un backlog e partono dalle modifiche più piccole. Una sperimentazione con due team riduce il modulo a sei campi compilati automaticamente dallo strumento di monitoraggio dove possibile, elimina due delle tre approvazioni e aggiunge una breve revisione senza colpe per ogni incidente ad alta priorità.

Dopo sei settimane, i team della sperimentazione registrano gli incidenti durante l'interruzione anziché dopo e l'addetto qualità trova i record più completi di prima. Il gruppo pubblica una nota di rilascio di una pagina, estende la modifica a tutti i team e mostra all'auditor il backlog, i risultati della sperimentazione e le misure. Restano alcune difficoltà. Un team di delivery non ha mai partecipato alla sperimentazione e usa ancora il vecchio modulo, il contratto di un fornitore richiede un campo che il nuovo modulo omette e l'addetto qualità teme che l'eliminazione delle approvazioni sarà messa in discussione al prossimo audit. La responsabile della gestione dei servizi aggiunge un campo per il caso del fornitore, chiede al team rimasto di unirsi al ciclo successivo e concorda con l'auditor di rivedere i record degli incidenti alla prossima riunione trimestrale.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery sono gli utenti di molti processi di gestione dei servizi. Partecipa alla progettazione di quelli che ti riguardano, offri dati su come funzionano nella pratica e prova le sperimentazioni. Dove un passaggio del processo può essere automatizzato nella tua pipeline, offriti di costruirlo.

### Team di servizio e di operations

I team operativi spesso possiedono i processi. Tratta ciascuno come un prodotto: scrivi uno scopo, tieni un backlog, chiedi agli utenti e rilascia piccole modifiche. Ritaglia tempo per il miglioramento dei processi e difendilo, perché il lavoro di delivery lo soffocherà.

### Leadership e governance

I leader danno ai responsabili dei processi autorità e tempo e fissano l'aspettativa che i processi cambino sulla base delle prove. Chiedi scopo e misure di ogni processo e il backlog. Sostieni le sperimentazioni e sii disposto ad accettare prove in forme nuove.

### Clienti e utenti

Clienti e utenti dei servizi seguono anch'essi processi, come richieste e approvazioni. Di' al responsabile che cosa è confuso o lento. Offriti di partecipare a una sperimentazione. Aspettati che i cambiamenti siano annunciati e spiegati.

## Modalità di fallimento comuni

- **Processo senza responsabile.** Nessuno può cambiarlo. Nomina invece un responsabile con autorità e tempo.
- **Riprogettazione big-bang.** Un intero nuovo processo è introdotto in una volta e respinto. Cambia invece a piccoli passi e sperimenta.
- **Progettazione a comitato lontano dagli utenti.** Il processo si addice ai progettisti. Includi invece le persone che lo seguono e osserva il lavoro reale.
- **Rimescolamento costante.** I cambiamenti arrivano troppo spesso per essere assorbiti. Rilascia invece con un ritmo prevedibile.
- **Dimenticare i requisiti legali.** Un controllo necessario viene eliminato. Verifica invece a che cosa serve ogni passaggio e indica la fonte.
- **Cambiamenti non annunciati.** Le persone li scoprono per caso. Pubblica invece brevi note di rilascio.
- **Prove non conservate.** L'audit non può vedere come il processo è cambiato. Conserva invece backlog, decisioni e misure.
- **Nessuna rimozione.** I passaggi si accumulano. Tratta invece l'eliminazione come un miglioramento.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Responsabilità e scopo | I processi non hanno un responsabile o uno scopo chiari | Alcuni processi hanno responsabili | Ogni processo ha un responsabile con autorità e uno scopo scritto | I responsabili sono rivisti per efficacia e sostenuti | I responsabili lavorano insieme tra i team per allineare i processi end-to-end |
| Backlog e cambiamento | I cambiamenti sono progetti, rari e grandi | Alcuni responsabili tengono elenchi di idee | Ogni processo ha un backlog ordinato e rilascia i cambiamenti a piccoli passi | Flusso del backlog ed effetti dei rilasci sono misurati | I cambiamenti di processo sono coordinati tra i processi e con i fornitori |
| Coinvolgere gli utenti | I progettisti consultano raramente gli utenti | Alcune sperimentazioni sono condotte con gli utenti | Gli utenti partecipano a progettazione e sperimentazioni come standard | Feedback e soddisfazione degli utenti sono misurati e trattati | Clienti e fornitori partecipano alla progettazione dei processi |
| Prove e audit | I record sono scadenti e i cambiamenti non registrati | Alcuni cambiamenti di processo sono registrati | Backlog, note di rilascio e misure servono come prove di audit | Gli auditor rivedono regolarmente il registro dei cambiamenti | Le prove sono condivise con auditor e partner in modo continuo |

## Checklist

- [ ] Ogni processo principale ha un responsabile nominato con autorità e tempo.
- [ ] Ogni processo ha uno scopo in una frase e un insieme definito di utenti.
- [ ] Ogni processo ha un backlog di miglioramenti visibile e ordinato.
- [ ] Gli utenti di delivery e operations partecipano a progettazione e sperimentazioni.
- [ ] I cambiamenti sono sperimentati prima dell'estensione, con una verifica definita.
- [ ] I cambiamenti di processo sono rilasciati con un ritmo e brevi note.
- [ ] Poche misure mostrano se ogni processo funziona.
- [ ] I controlli legali e contrattuali sono individuati con le loro fonti.
- [ ] Gli auditor hanno visto backlog, note di rilascio e misure.
- [ ] I passaggi che non servono più uno scopo sono rimossi.

## Prompt per l'IA

**Scopo: redigere una dichiarazione di scopo e un elenco di utenti per un processo.**

```text
Help me write a purpose statement for this process: [name and brief description].

Who follows it: [roles].
Who it serves: [roles].
What goes wrong today: [examples].
Rules or contracts that require parts of it, with source text: [paste, or write "none known"].

Write three alternative one-sentence purpose statements, each focused on an outcome and not on the steps. Then list questions for the users to test which is closest. Do not invent rules. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: trasformare feedback e revisioni degli incidenti in un backlog del processo.**

```text
Here are comments, complaints, audit findings, and review actions about [process]: [paste one per line, with source].

Group related items. For each group, write a backlog item in the form "As a [role], I want [change] so that [outcome]," using only what the text says. Add a note on who is affected and a question about evidence. Leave priority blank. List items that look like requirements from law or contract, quoting the text, and items that conflict. List what you are unsure of.
```

**Scopo: progettare una sperimentazione di un mese di un processo più leggero.**

```text
Design a one-month trial of a lighter version of [process].

Current steps and where people struggle: [describe].
Proposed change: [describe].
Teams that could take part: [list].
Controls that must stay, with source: [list, or write "none known"].

Give: the trial scope, what we expect to see, what to measure before and during (leave targets as [to be agreed]), how to gather user feedback, conditions to stop, and what evidence to keep for auditors. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: scrivere una nota di rilascio per un cambiamento di processo.**

```text
Write a short release note for a change to [process].

What changed: [describe].
Why: [describe].
Who is affected and from what date: [describe].
What people should do differently: [describe].
Where to ask questions: [contact].

Write under 150 words in plain language, with a heading, a short list of changes, and what to do. Use only my information. Ask clarifying questions first if anything is missing, and list what you are unsure of.
```

## Competenze per l'IA

- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): da usare per chiarire chi possiede ogni processo e chi è consultato.
- [user-story](../../../../skills/user-story/SKILL.md): da usare per scrivere le voci del backlog del processo dal punto di vista dell'utente.
- [workflow-analysis](../../../../skills/workflow-analysis/SKILL.md): da usare per studiare come un processo gira davvero e dove fatica.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): da usare per rivedere con gli utenti come sta funzionando un processo.
- [kaizen](../../../../skills/kaizen/SKILL.md): da usare per pianificare miglioramenti piccoli e continui a un processo.

## Fonti principali

- **The Scrum Guide** (Ken Schwaber e Jeff Sutherland, scrumguides.org): la fonte dei ruoli e degli artefatti usati qui come analogia per la responsabilità dei processi e i backlog.
- **Principles behind the Agile Manifesto** (agilemanifesto.org): il lato agile dell'approccio di progettazione.
- **ITIL** (Wikipedia): la storia dell'allineamento di ITIL 4 ai modi di lavorare agili, DevOps e lean.
- **ISO/IEC 20000** (Wikipedia): l'elenco delle parti, comprese le indicazioni recenti su agile e DevOps.

## Riferimenti

1. The Scrum Guide (November 2020) — Ken Schwaber and Jeff Sutherland, scrumguides.org — https://scrumguides.org/scrum-guide.html
2. Principles behind the Agile Manifesto — Beck et al., agilemanifesto.org — https://agilemanifesto.org/principles.html
3. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
4. ISO/IEC 20000 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_20000
5. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
6. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
7. PDCA — Wikipedia — https://en.wikipedia.org/wiki/PDCA
8. Business process management — Wikipedia — https://en.wikipedia.org/wiki/Business_process_management
9. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
