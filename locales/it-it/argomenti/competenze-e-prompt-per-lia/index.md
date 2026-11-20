# Competenze e prompt per l'IA

**Un buon prompt dà a un assistente di IA il materiale, il compito e i controlli di cui ha bisogno, e una buona competenza (skill) confeziona quel know-how perché un team possa riusarlo, il che rende i prompt e le competenze per l'IA di questa guida punti di partenza da adattare e verificare.**

## Perché è importante

Ogni argomento di questa guida termina con prompt e competenze. Esistono perché molti compiti della gestione dei servizi si prestano a un assistente in grado di leggere una pila di ticket, redigere un runbook o trasformare appunti in un piano. Esistono anche perché una richiesta vaga a un'IA produce risultati vaghi, a volte sbagliati. La differenza tra una risposta utile e una plausibile ma vuota sta spesso in come la richiesta è stata scritta e in quale materiale l'accompagnava.

Questo argomento spiega come usare i prompt e le competenze della guida, perché sono scritti così e come scriverne di propri per il tuo team. Riguarda più le abitudini che i trucchi: fornire materiale reale, dire che cosa si vuole, chiedere all'assistente di segnalare ciò che non sa e controllare ciò che torna indietro. Si basa sulle cautele dell'argomento precedente, che descrive dove l'IA aiuta e dove può danneggiare (vedi Argomento 6.2 — L'IA nella gestione dei servizi IT).

Le fonti sono pratiche. La competenza `skills/prompt-engineering` della guida descrive la scrittura di prompt come la pratica deliberata di progettare e iterare le istruzioni date a un modello linguistico, trattando un prompt come un piccolo software che si scrive, si prova su casi reali e si rivede. La documentazione di Claude Code descrive come le competenze sono strutturate come directory con un file `SKILL.md`. L'[articolo di Wikipedia sui large language model](https://en.wikipedia.org/wiki/Large_language_model) dà il contesto. Nessuna fonte letta per questa guida offre prove su quali tecniche di prompting funzionino meglio; tratta le tecniche qui riportate come abitudini da provare.

## Concetti fondamentali

### Prompt, competenze e a che cosa servono

Un **prompt** è l'istruzione e il materiale che dai a un assistente di IA per un compito. Una **competenza** (skill), nel formato usato nella cartella `skills/` di questa guida, è un pacchetto riusabile di know-how per un tipo di compito: una directory che contiene un file `SKILL.md` che dice quando usarla e come svolgere il lavoro. Nella documentazione di Claude Code, una competenza è una directory con un file `SKILL.md` obbligatorio il cui frontmatter ha un nome e una descrizione e il cui corpo dà le istruzioni; l'assistente usa la descrizione per decidere quando applicare la competenza e carica il corpo completo solo quando viene usata.

| | Prompt | Competenza |
|---|---|---|
| **Ambito** | Un compito, ora | Un tipo di compito, riusato |
| **Dove vive** | In una chat o in un documento | In una cartella, come `skills/` o la directory delle competenze di un progetto |
| **Modificato da** | Te, ogni volta | Il team, con revisione |
| **Ideale per** | Analisi specifiche del tuo materiale | Metodi ripetibili come condurre una retrospettiva |

### Come sono costruiti i prompt della guida

I prompt di questa guida seguono uno schema semplice, definito nella guida di stile:

1. **Uno scopo in una riga in grassetto** dice a che cosa serve il prompt.
2. **Un blocco delimitato** contiene testo che puoi copiare e incollare.
3. **Segnaposto tra parentesi quadre** indicano ciò che devi fornire, con un suggerimento su che cosa inserire.
4. **Un compito** che nomina l'output desiderato.
5. **Confini**: non inventare numeri, fonti, citazioni o dichiarazioni di conformità; usa solo il materiale incollato.
6. **Una richiesta di chiedere prima** quando mancano informazioni, e di segnalare le ipotesi.
7. **Un controllo finale**: "List what you are unsure of."

Queste parti esistono per ragioni precise. I segnaposto ti obbligano a portare materiale reale. Il confine impedisce all'assistente di riempire i vuoti con l'invenzione. La richiesta di domande di chiarimento trasforma un'ipotesi secca in una breve conversazione. L'ultima riga fa segnalare all'assistente i propri punti deboli, il che ti aiuta a decidere che cosa controllare.

### Schemi che aiutano

La competenza `prompt-engineering` della guida elenca tecniche, che questa guida riassume con parole proprie:

- **Sii specifico sull'output che vuoi,** come una tabella con colonne nominate o un elenco numerato di al massimo cinque voci, così che l'assistente non debba indovinare la forma.
- **Dai esempi quando le istruzioni sono ambigue,** mostrando in un breve campione lo schema che vuoi.
- **Fornisci il contesto che l'assistente non può conoscere,** come la tua terminologia, i vincoli e il documento in questione, e di' che cosa non dovrebbe presumere.
- **Itera su casi di prova reali,** eseguendo il prompt su una gamma di input reali e rivedendolo dove fallisce, invece di giudicarlo da un solo buon esempio.

Un prompt messo a punto su un input può fallire su altri. La competenza sottolinea che un input breve e formulato in modo strano, o a cui manca un campo, può rompere un prompt che gestiva l'esempio originale.

### Abitudini di verifica

Ogni output va controllato in proporzione al costo di sbagliare. Abitudini che aiutano:

- **Controlla i fatti sulla fonte che hai incollato.** Chiedi all'assistente di citare la parte del tuo materiale che supporta ogni affermazione.
- **Non accettare mai riferimenti che non hai visto.** I casi descritti nell'argomento precedente includono citazioni giudiziarie inventate; non ripeterli.
- **Separa ciò che l'assistente ha visto da ciò che ha presunto.** I prompt della guida lo chiedono.
- **Verifica tu stesso i calcoli,** o chiedi i passaggi e controllali.
- **Usa una seconda occhiata per tutto ciò che esce dal team,** come una risposta a un cliente o una politica.
- **Conserva registrazioni degli usi significativi,** come descritto nell'Argomento 6.2 — L'IA nella gestione dei servizi IT.

### Proteggere i dati

Prima di incollare qualsiasi cosa in un prompt, chiediti che cosa contiene e dove andrà. Rimuovi dati personali, credenziali e dettagli commerciali riservati, a meno che lo strumento e i suoi termini non siano stati approvati per essi (vedi Argomento 3.13 — Gestione della sicurezza delle informazioni). I prompt della guida ti chiedono di anonimizzare, ma la responsabilità è tua. Nel dubbio, descrivi la situazione in termini generali.

### Come appare una competenza

Dalla documentazione di Claude Code e dalle competenze di questa guida, una competenza è una directory come `skills/runbook/` che contiene `SKILL.md`. Il file inizia con un frontmatter YAML tra marcatori `---`, contenente almeno un `name` e una `description`. La documentazione dice che la descrizione dice all'assistente che cosa fa la competenza e quando usarla, e raccomanda di mettere per primo il caso d'uso principale. Il corpo dà il metodo in markdown. Altri file, come documenti di riferimento o script, possono stare accanto ed essere caricati quando servono; la documentazione consiglia di tenere breve `SKILL.md` stesso, sotto le 500 righe.

Le competenze copiate in questa guida seguono la stessa forma. Le loro descrizioni iniziano con "Use when asked to…", il che chiarisce quando ciascuna si applica.

### Dove vivono le competenze

La documentazione descrive competenze personali nella directory delle competenze della home di un utente, competenze di progetto nella directory delle competenze di un repository, che può essere sottoposta a commit e condivisa con un team, e altre posizioni come i plugin. Per un team, una cartella di progetto sotto controllo di versione è il luogo naturale: le competenze sono riviste, modificate con lo stesso processo del resto del lavoro e disponibili a tutti.

### Scrivere le proprie competenze di team

Una competenza di team cattura una pratica che il team ripete e vuole svolta in modo coerente. Esempi per la gestione dei servizi: come scrivere un postmortem nello stile della casa, come fare il triage di un certo tipo di ticket, come preparare una richiesta di cambiamento, come condurre la tua revisione del venerdì. Per scriverne una:

1. **Scegli un compito che ripeti** e per cui esiste un buon modo noto di svolgerlo.
2. **Scrivi prima la descrizione,** iniziando con "Use when…" e il caso d'uso principale, così che l'assistente e i colleghi sappiano quando si applica.
3. **Scrivi il metodo** in passi brevi, con il formato dell'output, i controlli e le cose da evitare.
4. **Aggiungi esempi** di un buon risultato, con i dettagli sensibili rimossi.
5. **Di' che cosa non deve fare,** come inventare cifre o inviare qualcosa senza revisione.
6. **Provala su casi reali** e rivedila.
7. **Dalle un responsabile e una data di revisione,** come a qualsiasi altro documento condiviso.

### Le competenze in questa guida

La cartella `skills/` di questo repository contiene copie di competenze dalla raccolta skills-on-ai, elencate in `skills/README.md`, e due competenze scritte per questa guida: una per i lettori e una per i manutentori. Ogni argomento rimanda alle competenze più utili per il suo tema, con una frase su quando usare ciascuna. Le competenze copiate sono generiche, non specifiche del contenuto di questa guida, quindi usale come punti di partenza e adatta il loro output al tuo contesto.

### Limiti

Nessuna fonte letta per questa guida misura quanto bene funzioni una qualsiasi tecnica di prompting, e gli strumenti di IA cambiano in fretta. La documentazione di Claude Code letta era lunga ed è stata letta solo in parte. Ciò che segue è consiglio pratico che ha retto nell'uso generale, offerto come abitudini da provare e non come garanzie.

## Buone pratiche

1. **Parti da un compito reale e da materiale reale.** Scegli qualcosa che ti serve fare e incolla i fatti effettivi, non una loro descrizione. Compila ogni segnaposto con dettagli specifici.
2. **Enuncia lo scopo in una riga.** Di' a che cosa serve l'output e chi lo userà. Aiuta l'assistente a scegliere il giusto livello di dettaglio.
3. **Specifica l'output.** Nomina il formato, la lunghezza e la struttura che vuoi. Chiedi una tabella quando vuoi confrontare, un elenco quando vuoi dei passi.
4. **Fissa dei confini.** Di' che cosa l'assistente non deve fare: inventare numeri, fonti o citazioni; presumere fatti non dati; affermare che una regola si applica senza il testo.
5. **Chiedi prima domande di chiarimento.** Di' all'assistente di chiedere ciò di cui ha bisogno prima di rispondere. Rispondi brevemente e poi chiedigli di procedere.
6. **Chiedigli di separare i fatti dalle ipotesi.** Fagli segnare ciò che ha preso dal tuo materiale e ciò che ha supposto. I prompt di questa guida terminano con "List what you are unsure of."
7. **Richiedi evidenze.** Chiedi citazioni dal tuo materiale che supportino ogni affermazione, così da poter controllare in fretta.
8. **Itera.** Tratta la prima risposta come una bozza. Di' che cosa non va e chiedi una revisione, oppure cambia il prompt e riprova.
9. **Prova i prompt su più casi.** Prima di fare affidamento su un prompt, eseguilo su tre o quattro input reali, compreso uno insolito. Annota dove fallisce.
10. **Proteggi i dati.** Rimuovi i dettagli personali e riservati prima di incollare. Usa strumenti approvati. Segui la politica della tua organizzazione.
11. **Controlla prima di usare.** Verifica fatti, numeri e riferimenti. Fai rivedere da una persona tutto ciò che va ai clienti o cambia un sistema.
12. **Condividi ciò che funziona.** Metti i prompt che si rivelano utili, con le loro note, in una competenza di team o in un documento sotto controllo di versione, con un responsabile.

## Domande da discutere con il team

**Quali compiti ripetiamo che un assistente potrebbe aiutare a svolgere, e che cosa dovremmo controllare?**

Chiedi a ciascuno di elencare compiti e di segnare il rischio se l'output fosse sbagliato. Raggruppali in rischio basso, medio e alto. Inizia con uno a basso rischio. Chi facilita può chiedere quale sarebbe il passaggio di controllo. Scegli un compito per una prova.

**Che cosa incolliamo oggi negli strumenti di IA, e dovremmo?**

Sii onesto e senza giudizio. Elenca esempi. Confronta con la politica sui dati e con gli strumenti approvati. Concorda un controllo rapido che le persone possano applicare prima di incollare: "questo contiene dati personali, segreti o dettagli riservati?"

**Quali prompt di questa guida proveremmo per primi, e con quale materiale reale?**

Sfogliate insieme i prompt e sceglietene uno. Individuate il materiale reale da incollare, rimuovete i dettagli sensibili ed eseguitelo. Confrontate i risultati e discutete che cosa cambiare nel prompt. È un modo rapido di imparare lo schema.

**Come sapremmo che un prompt funziona?**

Chiedi un insieme di prova: alcuni input reali con output buoni noti. Discuti come valutare le risposte e chi decide. Un prompt senza un insieme di prova è una speranza. Concorda un piccolo insieme per un prompt.

**Quale pratica ripetiamo che merita di diventare una competenza di team?**

Elenca i candidati: un formato di revisione, una routine di triage, un modello per i report. Sceglierne uno e redigete insieme descrizione e passi. Decidete chi ne è responsabile e quando sarà rivisto.

**Che cosa non vorremmo mai che un'IA facesse da sola?**

Elenca le azioni: inviare ai clienti, cambiare la produzione, approvare accessi, decidere una priorità. Discuti perché. Le risposte sono i confini da scrivere nei vostri prompt e nelle vostre competenze. Concorda un breve elenco.

## Nella pratica: un esempio di ITIL agile

Il service desk IT di un ospedale regionale ha quattordici analisti. La responsabile del desk ha notato che i colleghi usano un assistente di IA in modi diversi: uno incolla ticket interi, compresi i nomi dei pazienti, in un chatbot pubblico; un altro scrive prompt elaborati e ottiene riassunti utili; la maggior parte non lo usa affatto. Un recente articolo di conoscenza, redatto da un assistente, conteneva un passaggio di procedura che non esisteva.

La responsabile tiene una sessione di un'ora usando l'approccio di questa guida. Parte dai dati: il gruppo concorda una regola per cui nessun dettaglio di pazienti né credenziale va in alcuno strumento, e che l'assistente approvato, che l'ospedale ha in licenza con termini adeguati, è l'unico usato con il testo dei ticket. Sceglie un compito, redigere un articolo di conoscenza da un ticket risolto, e usa lo schema dei prompt di questa guida: uno scopo in una riga, un segnaposto per il ticket anonimizzato, istruzioni di usare solo il contenuto del ticket, di segnare con un'etichetta ogni passaggio dedotto e di elencare ciò di cui non è sicuro. Due analisti eseguono il prompt su cinque ticket passati e il gruppo legge insieme i risultati. In un caso il prompt inventa un passaggio; aggiungono una riga che chiede una citazione dal ticket per ogni passaggio.

La responsabile scrive il prompt migliorato come competenza di team nella cartella condivisa del desk, con una descrizione che inizia con "Use when…", un responsabile e una data di revisione, e aggiunge una regola per cui ogni articolo redatto è controllato da un secondo analista prima della pubblicazione. Dopo due mesi, il numero di articoli redatti a settimana è raddoppiato e i revisori trovano meno errori di prima. Restano alcuni problemi. Due analisti incollano ancora dettagli in uno strumento pubblico quando sono sotto pressione, la competenza produce una formulazione troppo formale che gli analisti riscrivono e un revisore ammette di scorrere in fretta. La responsabile ripete la regola sui dati a ogni riunione di team, aggiunge un esempio di stile alla competenza e chiede ai revisori di spuntare una breve checklist.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery usano gli assistenti per codice, test e documentazione. Applica le stesse abitudini: materiale reale, confini chiari, verifica e revisione. Tieni i segreti fuori dai prompt e conserva i prompt e le competenze utili insieme al codice.

### Team di servizio e di operations

I team operativi possono usare i prompt per analizzare ticket, redigere runbook e preparare revisioni. Tieni fuori i dati personali, controlla gli output su log e registrazioni e scrivi competenze per le routine che il team ripete, come postmortem e passaggi di consegne di turno.

### Leadership e governance

I leader stabiliscono le regole su che cosa si può usare, con quali dati e chi è responsabile. Chiedi un inventario, una politica sui dati ed evidenze dai piloti. Sostieni il tempo che i team dedicano a scrivere e provare prompt e competenze e assicurati che le competenze condivise abbiano responsabili.

### Clienti e utenti

Clienti e utenti possono vedere i risultati di prompt e competenze in risposte, articoli e riassunti. Aspettati che i fornitori li controllino e che ti dicano quando usano strumenti automatici, dove conta. Segnala gli errori, che aiutano a migliorare il materiale sottostante.

## Modalità di fallimento comuni

- **Richieste vaghe.** L'assistente indovina. Fornisci invece il materiale, lo scopo e l'output che vuoi.
- **Incollare dati sensibili.** Dettagli personali o riservati lasciano l'organizzazione. Rimuovili invece e usa strumenti approvati.
- **Accettare contenuti inventati.** Si usano passaggi, numeri o riferimenti fabbricati. Fissa invece dei confini, chiedi citazioni e verifica.
- **Messa a punto su un solo esempio.** Un prompt funziona una volta e fallisce altrove. Prova invece su più input reali.
- **Competenze senza responsabili.** I prompt condivisi diventano obsoleti. Assegna invece un responsabile e una data di revisione e tienili sotto controllo di versione.
- **Eccessiva fiducia nei prompt copiati.** Un prompt preso da internet o da questa guida è usato senza modifiche. Adattalo invece al tuo contesto e controlla i risultati.
- **Nessuna seconda occhiata.** L'output dell'IA va direttamente ai clienti. Fai invece rivedere da una persona tutto ciò che esce dal team.
- **Trattare l'assistente come un'autorità.** La sua sicurezza è presa per correttezza. Chiedi invece di che cosa non è sicuro e controlla.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Pratica dei prompt | Le persone scrivono prompt ad hoc | Alcune persone condividono prompt | I team usano uno schema comune con scopo, materiale, confini e controlli | La qualità dei prompt è provata su insiemi di casi reali | I prompt sono migliorati tra i team a partire dai risultati di prova condivisi |
| Competenze | Nessuna competenza condivisa | Esistono alcune competenze personali | Competenze di team con responsabili e date di revisione vivono sotto controllo di versione | Uso e risultati delle competenze sono rivisti | Le competenze sono condivise e mantenute tra team e partner |
| Verifica e dati | L'output è considerato affidabile; i dati sono incollati liberamente | Alcuni controlli e regole sui dati | Abitudini di verifica e una politica sui dati sono routine | Errori e incidenti sui dati sono monitorati e se ne tiene conto | Verifica e pratica sui dati sono coordinate nell'organizzazione |
| Apprendimento | L'apprendimento è individuale | Alcuni suggerimenti sono condivisi | I team tengono sessioni regolari per migliorare prompt e competenze | I miglioramenti sono monitorati e misurati | L'apprendimento si diffonde continuamente tra i team |

## Checklist

- [ ] Il team ha una breve regola su quali dati possono andare in quali strumenti di IA.
- [ ] I prompt su cui facciamo affidamento hanno uno scopo dichiarato, materiale reale, confini e una richiesta di ciò di cui l'assistente non è sicuro.
- [ ] Ogni prompt su cui facciamo affidamento è stato provato su almeno tre input reali.
- [ ] L'output che esce dal team è rivisto da una persona.
- [ ] Riferimenti e numeri dell'output dell'IA sono controllati sulle fonti.
- [ ] I prompt utili sono salvati con note in un luogo condiviso sotto controllo di versione.
- [ ] Le competenze di team hanno una chiara descrizione "Use when…", un responsabile e una data di revisione.
- [ ] Il team ha elencato le azioni che l'IA non deve mai compiere da sola.
- [ ] Il personale sa quali strumenti sono approvati.
- [ ] Rivediamo i nostri prompt e le nostre competenze almeno due volte l'anno.

## Prompt per l'IA

**Scopo: migliorare un prompt che già usi.**

```text
Here is a prompt I use: [paste it].
Here is an example of an input I give it, with sensitive details removed: [paste].
Here is what I got: [paste].
Here is what I wanted: [describe].

Diagnose why the output fell short, using only the text above. Suggest a revised prompt that: states the purpose, names the output format, sets boundaries (no invented facts, numbers, or sources), asks for clarifying questions first, requests quotes from the supplied material as evidence, and ends by asking you to list what you are unsure of. Keep placeholders in [square brackets]. Do not change the task. List what you are unsure of.
```

**Scopo: trasformare un compito ripetuto in una bozza di competenza di team.**

```text
Help me draft a team skill in SKILL.md format for this task: [name and describe the task].

How we do it today, step by step: [paste].
What a good result looks like (an example with sensitive details removed): [paste].
What must never happen (for example inventing figures or sending without review): [list].

Write a SKILL.md with YAML frontmatter containing a name and a description that starts with "Use when" and puts the key use case first, then a body with the purpose, short method steps, output format, checks, and things to avoid. Keep it under 150 lines. Mark every item you added as an assumption. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: costruire un piccolo insieme di prova per un prompt.**

```text
I have a prompt that [describe what it does]: [paste it].

Help me design a test set of 5 to 10 inputs: typical cases, an unusual case, a case with a missing field, and a case where the right answer is "not enough information." Tell me what to collect from real examples (with sensitive details removed), how to record the expected output, and how to score results (correct, partly correct, wrong, confidently wrong, correctly declined). Do not invent test content; give me the categories and what to look for. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: controllare una bozza scritta da un'IA rispetto alla sua fonte.**

```text
Here is the source material: [paste].
Here is a draft produced by an AI tool from that material: [paste].

List every statement in the draft, say whether the source supports it (quote the supporting text), contradicts it, or does not mention it, and suggest edits to remove unsupported statements. Do not add facts of your own. Give a short summary of how reliable the draft is. List what you are unsure of.
```

## Competenze per l'IA

- [prompt-engineering](../../../../skills/prompt-engineering/SKILL.md): da usare per scrivere, provare e migliorare prompt in modo che diano risultati affidabili.
- [machine-learning-model-card](../../../../skills/machine-learning-model-card/SKILL.md): da usare per documentare a che cosa serve un modello e quali sono i suoi limiti quando il tuo team ne usa uno.
- [agile-coaching](../../../../skills/agile-coaching/SKILL.md): da usare per aiutare un team a costruire nel tempo abitudini attorno a prompt e competenze.
- [agile-itil-guide-skill](../../../../skills/agile-itil-guide-skill/SKILL.md): da usare per trovare argomenti in questa guida, condurre una conversazione di team a partire dalle sue domande o adattare uno dei suoi prompt.
- [agile-itil-guide-maintainer-skill](../../../../skills/agile-itil-guide-maintainer-skill/SKILL.md): da usare per scrivere o controllare un argomento, un prompt o un link a una competenza per questa guida.

## Fonti principali

- **Claude Code skills documentation** (code.claude.com): la descrizione di come le competenze sono strutturate come directory con un file `SKILL.md`.
- **Prompt engineering** (la `skills/prompt-engineering/SKILL.md` di questa guida): una breve esposizione delle tecniche e le ragioni per provare i prompt su input reali.
- **Large language model** (Wikipedia): contesto su come sono costruiti questi sistemi e dove possono fallire.
- **AI Risk Management Framework** (NIST): il framework volontario per gestire i rischi dell'IA, utile per la politica di team.

## Riferimenti

1. Skills (Claude Code documentation) — Anthropic — https://code.claude.com/docs/en/skills
2. Large language model — Wikipedia — https://en.wikipedia.org/wiki/Large_language_model
3. Prompt engineering — Wikipedia — https://en.wikipedia.org/wiki/Prompt_engineering
4. AI Risk Management Framework — NIST — https://www.nist.gov/itl/ai-risk-management-framework
5. Hallucination (artificial intelligence) — Wikipedia — https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)
6. Retrieval-augmented generation — Wikipedia — https://en.wikipedia.org/wiki/Retrieval-augmented_generation
7. Artificial intelligence — Wikipedia — https://en.wikipedia.org/wiki/Artificial_intelligence
8. Version control — Wikipedia — https://en.wikipedia.org/wiki/Version_control
9. Information security — Wikipedia — https://en.wikipedia.org/wiki/Information_security
