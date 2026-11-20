# Gestione della conoscenza

**La gestione della conoscenza rende disponibile ad altri ciò che le persone sanno quando ne hanno bisogno, e l'approccio che funziona per i team agili è catturare la conoscenza come sottoprodotto del lavoro, mantenerla breve e con un responsabile e combinare scrittura e conversazione.**

## Perché è importante

Ogni servizio dipende dalla conoscenza: come funziona, che cosa è andato storto in passato, come si corregge e perché è stato costruito in quel modo. Quando quella conoscenza vive solo in poche teste, il servizio è fragile. Una vacanza, una dimissione o una brutta notte di reperibilità possono trasformare una correzione di dieci minuti in un'interruzione di dieci ore. La gestione della conoscenza è la pratica che assicura che chi ha bisogno di sapere possa scoprirlo.

La tradizione agile propende per la conversazione e per il software funzionante rispetto alla documentazione, e gli autori del Manifesto Agile sono stati criticati per questo (vedi Argomento 1.1 — Il Manifesto Agile). Una lettura corretta è che la documentazione deve guadagnarsi il suo posto. La gestione della conoscenza offre un modo di decidere che cosa se lo guadagna: la conoscenza usata spesso, costosa da riscoprire o detenuta da troppo poche persone. Per il resto, conversazione e coppia possono servire meglio.

L'[articolo di Wikipedia sulla gestione della conoscenza](https://en.wikipedia.org/wiki/Knowledge_management) è ampio e descrive il campo come l'elaborazione della conoscenza per raggiungere obiettivi organizzativi, distinta dalla gestione dei contenuti o dell'informazione. Registra storia, modelli, approcci, fattori abilitanti, barriere e critiche, e non dice nulla di specifico sui servizi IT. Questo argomento usa le idee generali dell'articolo e le applica ai team di servizio, segnalando dove applica e non riferisce.

## Concetti fondamentali

### Che cos'è la gestione della conoscenza

Wikipedia descrive la gestione della conoscenza (KM) come comprensiva di processi per consapevolezza organizzativa, apprendimento, collaborazione e innovazione, che usano e condividono la conoscenza per sostenere gli obiettivi di un'organizzazione. Nota che pratiche come apprendistato, biblioteche aziendali e mentoring precedono di molto il termine. La KM è emersa come disciplina all'inizio degli anni Novanta, con accademici tra cui Ikujiro Nonaka, Hirotaka Takeuchi, Thomas H. Davenport e Baruch Lev che hanno contribuito a svilupparla. L'articolo dice che ISO 9001:2015 ha aggiunto una specifica sulla "conoscenza organizzativa".

### Conoscenza tacita ed esplicita

L'articolo distingue due forme. La **conoscenza tacita** è interiorizzata e spesso non consapevolmente nota. La **conoscenza esplicita** è detenuta consapevolmente e può essere comunicata con facilità. Il modello SECI di Nonaka (socializzazione, esternalizzazione, combinazione, interiorizzazione), che l'articolo attribuisce al libro di Nonaka e Takeuchi del 1995, descrive una spirale tra le due. L'articolo nota anche che ricercatori successivi hanno definito la separazione una semplificazione eccessiva.

Per un team di servizio la distinzione è pratica. Un ingegnere esperto può spesso intuire che un allarme è probabilmente rumore o che un certo rilascio è rischioso, e non sa facilmente scrivere perché. Parte di quell'intuizione può essere trasformata in runbook e controlli; parte può solo essere condivisa lavorando insieme.

### Codificazione e personalizzazione

Seguendo Hansen e colleghi (1999), l'articolo distingue due strategie. La **codificazione** archivia la conoscenza in repository così che altri possano riusarla. La **personalizzazione** condivide la conoscenza attraverso il contatto diretto tra persone. Ciascuna si addice a conoscenze diverse:

| Strategia | Si addice a | Esempi in un team di servizio |
|---|---|---|
| Codificazione | Compiti ripetuti e ben compresi | Runbook, record di errori noti, descrizioni dei servizi, articoli how-to |
| Personalizzazione | Questioni complesse, mutevoli o che richiedono giudizio | Coppia in reperibilità, affiancamento, comunità di pratica, discussioni di progettazione |

La maggior parte dei team ha bisogno di entrambe. Una base di conoscenza di ricette non insegna il giudizio, e la sola conversazione non scala al turno di notte.

### Comunità di pratica

L'articolo elenca le comunità di pratica tra le prospettive sulla KM. In un'organizzazione di servizio possono essere semplici come una riunione informale regolare di persone che lavorano su problemi simili tra i team, come ingegneri di database o analisti del desk. Diffondono conoscenza e norme e danno alle persone un posto in cui chiedere.

### Che cosa catturare

Non tutto merita un record. Candidati utili in un team di servizio includono:

- **Come ripristinare un servizio:** runbook e passaggi di ripristino (vedi Argomento 3.2 — Gestione degli incidenti).
- **Errori noti e workaround:** sintomo, workaround e responsabile (vedi Argomento 3.3 — Gestione dei problemi).
- **Descrizioni dei servizi:** che cosa fa un servizio, chi lo possiede e da che cosa dipende (vedi Argomento 3.8 — Gestione del catalogo dei servizi).
- **Decisioni e loro ragioni:** perché è stato scelto un progetto, così che le modifiche future non lo annullino alla cieca.
- **Lezioni dagli incidenti:** post-mortem che altri possono leggere.
- **Risposte alle domande comuni degli utenti:** brevi articoli per il service desk e per il self-service.

### Fattori abilitanti e barriere

L'articolo nomina persone e cultura, processi e struttura e tecnologia come componenti centrali. Nota che le motivazioni includono innovazione, cicli di sviluppo più brevi e valorizzazione delle competenze e che le organizzazioni usano incentivi come l'invio obbligatorio di contenuti, ma dice che non c'è consenso sul fatto che gli incentivi funzionino. Elenca barriere come la conoscenza che non si trasferisce, l'istruzione insufficiente e la perdita di conoscenza quando i lavoratori esperti se ne vanno. Per i team di servizio, le barriere che contano di più sono la pressione dei tempi, la responsabilità poco chiara dei contenuti, strumenti scomodi da usare e una cultura che premia l'eroismo sulla condivisione.

### Conoscenza nel flusso di lavoro

Un principio pratico, ampiamente usato nei service desk, è catturare la conoscenza come parte del lavoro e non come compito separato. Quando un analista risolve un nuovo problema, la soluzione diventa una bozza di articolo prima che il ticket sia chiuso. Quando un ingegnere corregge un incidente, i passaggi vanno nel runbook. Questo trasforma ogni pezzo di lavoro in un piccolo contributo. Le fonti lette per questa guida non descrivono un metodo specifico per farlo, quindi considera il principio come pratica comune da mettere alla prova e vedi che cosa funziona con i tuoi strumenti.

### Critiche e limiti

L'articolo registra critiche: che la rilevanza pratica della ricerca accademica sulla KM è stata messa in dubbio, che la distinzione tacito-esplicito è stata criticata, che l'efficacia degli incentivi è contestata e che proteggere la conoscenza comporta rischi come iperprotezione e appropriazione indebita. Non riporta prove misurate dell'efficacia o del ritorno sull'investimento della KM. Per un team di servizio la lezione è un'ambizione modesta: parti dalla conoscenza la cui assenza ha fatto male, misura se viene usata e abbandona ciò che non lo è.

### Conoscenza e apprendimento organizzativo

L'articolo dice che la KM è simile all'apprendimento organizzativo ma dà più enfasi alla conoscenza come risorsa strategica e alla condivisione delle informazioni, e che la KM facilita l'apprendimento organizzativo. Questo si collega all'apprendimento agile (vedi Argomento 1.10 — Apprendimento agile) e al miglioramento continuo (vedi Argomento 3.15 — Miglioramento continuo).

## Buone pratiche

1. **Parti dalla conoscenza la cui assenza ha fatto male.** Elenca gli ultimi incidenti o ritardi causati da conoscenza mancante. Parti da quegli argomenti, non da un tentativo di documentare tutto.
2. **Cattura la conoscenza nel momento del lavoro.** Fai della scrittura di una breve nota parte della chiusura di un incidente, una richiesta o una modifica. Una nota grezza scritta ora vale più di un articolo rifinito pianificato per dopo.
3. **Mantieni gli articoli brevi e strutturati.** Usa una forma coerente: sintomo, causa se nota, passaggi, quando fare escalation, responsabile, data dell'ultima revisione. Le persone sotto pressione leggono i titoli e i passaggi numerati.
4. **Dai a ogni articolo un responsabile e una data di revisione.** Il contenuto senza responsabile si degrada. Mostra la data di revisione sull'articolo così che i lettori possano giudicare l'affidabilità.
5. **Elimina e unisci.** Ritira gli articoli che nessuno usa e unisci i duplicati. Una base più piccola e aggiornata è meglio di una grande e obsoleta.
6. **Rendila facile da trovare.** Metti la conoscenza dove le persone già lavorano, verifica la ricerca con query reali e collega gli articoli da ticket, catalogo dei servizi e runbook.
7. **Verifica i runbook usandoli.** Chiedi alla persona che userà un runbook di seguirlo su un caso di prova. Correggi ciò che non è chiaro. Questo trasforma un documento in conoscenza operativa.
8. **Usa coppia e affiancamento per il tacito.** Fai lavorare le persone meno esperte con quelle esperte su incidenti e modifiche reali. Pianifica l'affiancamento, perché non avverrà quando tutti sono occupati.
9. **Sostieni le comunità di pratica.** Dai alle persone tempo e luogo per incontrarsi tra i team. Lascia che gli argomenti vengano dai membri.
10. **Registra decisioni e ragioni.** Tieni un breve record delle decisioni significative di progettazione e di processo e del perché sono state prese. Previene la riscoperta e aiuta i nuovi arrivati.
11. **Condividi le lezioni.** Pubblica ampiamente post-mortem e riassunti di problemi, in linguaggio semplice, e chiedi agli altri team che cosa si applica a loro (vedi Argomento 3.2 — Gestione degli incidenti).
12. **Sorveglia il rischio di conoscenza.** Una volta a trimestre, elenca le competenze e i sistemi che dipendono da una sola persona e pianifica come diffonderli. Tratta le partenze come stimolo per una revisione.

## Domande da discutere con il team

**Che cosa non potremmo fare se una persona nominata fosse assente per un mese?**

Chiedi al team di nominare le persone la cui assenza farebbe male e perché. Elenca i compiti che dipendono da loro. Di solito è un lungo elenco, e scomodo per le persone nominate. Presentalo come un rischio per il servizio, non un giudizio. Chi facilita può chiedere quale compito è più urgente condividere e come. Scegline uno da cui partire.

**Che cosa scriviamo, e qualcuno lo legge?**

Chiedi gli ultimi tre documenti che le persone hanno usato e gli ultimi tre che hanno scritto. Confronta. Il divario mostra dove lo sforzo di documentazione è fuori posto. Chiedi che aspetto avrebbe una versione utile dei documenti non letti, o se dovrebbero essere eliminati. Concorda di ritirarne o correggerne uno.

**Quando correggiamo qualcosa di nuovo, dove va a finire la conoscenza?**

Ripercorri l'ultimo nuovo problema: chi l'ha corretto, chi sa come e dove è stato registrato. Se la risposta è "in un ticket" o "nella mia testa", discuti che aspetto avrebbe una via migliore. Spesso una piccola abitudine, come un modello alla chiusura, fa la differenza. Provane una per un mese.

**Quale conoscenza si condivide meglio lavorando insieme, non scrivendo?**

Chiedi dove conta il giudizio: leggere un grafico, decidere quando fare escalation, conoscere un cliente. Discuti come i nuovi arrivati le imparano oggi. Le risposte tipiche sono fortuna e tempo. Pianifica un'organizzazione deliberata, come l'affiancamento in reperibilità. Concorda chi lavorerà in coppia con chi.

**Come sappiamo se un articolo di conoscenza è ancora vero?**

Scegli un articolo e mettilo alla prova. Verifica il responsabile, la data di revisione e se i passaggi funzionano. Molti non superano il test. Chiedi quale ciclo di revisione è realistico e chi può ritirare gli articoli. Lo scopo è un segno visibile di affidabilità su ogni articolo.

**Che cosa ci impedisce di condividere ciò che sappiamo?**

Raccogli risposte oneste: nessun tempo, paura di sembrare sciocchi, nessun posto ovvio, nessun riconoscimento. L'articolo di Wikipedia nota che l'efficacia degli incentivi è contestata, quindi evita risposte facili. Chiedi quale ostacolo il team potrebbe cambiare e quale richiede la direzione. Impegnati a un cambiamento visibile.

## Nella pratica: un esempio di ITIL agile

Il team di informazione ai passeggeri di una ferrovia nazionale, di quattordici persone, gestisce i sistemi dietro i display delle stazioni e l'app degli orari. L'ingegnere più esperto, che ha costruito il controller dei display, annuncia il proprio pensionamento tra sei mesi. Nessun altro capisce come il controller gestisce i guasti, e la documentazione è un documento di progetto di 200 pagine scritto dieci anni fa.

Il responsabile del team elenca ciò che l'ingegnere sa e gli altri no. Ottiene tre gruppi: come ripristinare il controller dopo un guasto (esplicito e ripetibile), perché esistono certi comportamenti strani (in parte scritto, in parte nella memoria) e come giudicare quando un guasto è grave (tacito). Per il primo, il team scrive runbook con l'ingegnere e verifica ciascuno facendolo seguire a un collega su un'unità di prova. Per il secondo, una coppia di ingegneri lo intervista ogni settimana e scrive brevi note di decisione in una cartella condivisa, ciascuna con un responsabile. Per il terzo, un ingegnere meno esperto lo affianca in ogni incidente di reperibilità per sei mesi e prende la guida in alcuni mentre lui osserva.

Alla fine dei sei mesi, tre ingegneri sanno gestire i guasti del controller, il documento di 200 pagine è sostituito da undici brevi runbook e venti note di decisione e il team ha una sessione mensile in cui una persona spiega qualcosa che sa. Restano problemi. Due runbook sono falliti quando provati su una diversa versione hardware e hanno dovuto essere riscritti, e il giudizio tacito è stato trasferito solo in parte: l'ingegnere che affiancava dice che alcune decisioni gli sembrano ancora tirate a indovinare. Il team pianifica un secondo ciclo di affiancamento con il successore dell'ingegnere che va in pensione e concorda di rivedere i runbook ogni trimestre.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery detengono gran parte della conoscenza di come i servizi sono costruiti. Scrivi brevi runbook e note di decisione come parte della tua definition of done e verificali con le persone che li useranno. Condividi con le operations le ragioni di progettazione così che le modifiche non le annullino.

### Team di servizio e di operations

I team operativi generano e usano gran parte della conoscenza quotidiana. Cattura le soluzioni quando chiudi i ticket, tieni aggiornati gli errori noti e chiedi ai team di delivery ciò di cui hai bisogno. Rendi gli articoli facili da trovare per il desk e per il self-service.

### Leadership e governance

I leader determinano se la condivisione è premiata o scoraggiata. L'articolo di Wikipedia dice che gli incentivi sono contestati, quindi concentrati sulla rimozione degli ostacoli: dai tempo, rendi facili gli strumenti e premia chi aiuta gli altri. Monitora il rischio di conoscenza, come i punti singoli di competenza, come gli altri rischi del servizio.

### Clienti e utenti

Clienti e utenti traggono vantaggio da risposte chiare e articoli di self-service. Di' al team quando un articolo è sbagliato o manca. Chiedi ai fornitori come imparano dagli incidenti e come condividono con te ciò che imparano.

## Modalità di fallimento comuni

- **Documentare tutto.** La base diventa grande e obsoleta. Parti invece dalla conoscenza la cui assenza ha fatto male e aggiungi secondo necessità.
- **Scrittura separata dal lavoro.** La cattura è una seccatura a posteriori. Rendi invece una breve nota parte della chiusura del lavoro.
- **Nessun responsabile.** Nessuno aggiorna gli articoli. Nomina invece un responsabile e una data di revisione per ciascuno.
- **Ricerca scadente.** Le persone non trovano ciò che esiste e quindi scrivono duplicati. Verifica invece la ricerca con query reali e collega gli articoli da dove le persone lavorano.
- **Ignorare il tacito.** Si presume che tutto sia scrivibile. Pianifica invece coppia, affiancamento e comunità di pratica.
- **Runbook non verificati.** I passaggi falliscono quando servono. Fai invece seguire ogni runbook a un utente su un caso di prova.
- **Accumulare come status.** Le persone proteggono la conoscenza per proteggere la propria posizione. Riconosci invece la condivisione e distribuisci la dipendenza.
- **Imporre i contenuti.** Gli obiettivi di quantità producono articoli sottili. Concentrati invece su uso e qualità e ricorda che l'effetto degli incentivi è contestato.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Catturare la conoscenza | La conoscenza vive nelle teste e nella chat | Alcuni team tengono note e runbook | Catturare una nota fa parte della chiusura del lavoro | Tassi di cattura e utilità sono rivisti | La cattura della conoscenza è condivisa tra team e fornitori |
| Qualità e responsabilità | Nessun responsabile; il contenuto si degrada | Alcuni articoli hanno responsabili | Ogni articolo ha un responsabile e una data di revisione | Accuratezza e uso sono misurati; il contenuto obsoleto è rimosso | Le pratiche di qualità sono condivise e migliorate in tutta l'organizzazione |
| Reperibilità e uso | La ricerca è scadente; le persone si chiedono a vicenda | Alcuni contenuti sono collegati dai ticket | La conoscenza è collegata da ticket, catalogo e runbook | Uso e fallimenti della ricerca sono misurati e corretti | La conoscenza è disponibile a utenti, fornitori e partner come appropriato |
| Condividere il tacito | La condivisione è casuale | Avvengono alcune sessioni di coppia e affiancamento | Coppia, affiancamento e comunità di pratica sono pianificati | Il rischio di conoscenza è monitorato e ridotto | Comunità e rotazione spostano abitualmente la conoscenza tra i team |

## Checklist

- [ ] Abbiamo elencato la conoscenza la cui assenza ci ha fatto male e siamo partiti da lì.
- [ ] Chiudere un incidente, una richiesta o una modifica include una breve nota quando qualcosa era nuovo.
- [ ] Gli articoli seguono una breve struttura comune con un responsabile e una data di revisione.
- [ ] I runbook sono stati verificati da qualcuno che non li ha scritti.
- [ ] La ricerca funziona per query reali e gli articoli sono collegati da ticket e catalogo dei servizi.
- [ ] Gli articoli inutilizzati e duplicati sono ritirati.
- [ ] Abbiamo un piano per diffondere la conoscenza detenuta da una sola persona.
- [ ] Coppia o affiancamento sono pianificati per il lavoro che richiede giudizio.
- [ ] Le lezioni dagli incidenti sono condivise oltre il team.
- [ ] Rivediamo il rischio di conoscenza almeno ogni trimestre.

## Prompt per l'IA

**Scopo: trasformare un ticket risolto in una bozza di articolo di conoscenza.**

```text
Turn this resolved ticket into a draft knowledge article for service desk analysts.

The ticket (symptom, steps taken, resolution; remove personal data): [paste].

Write a short article with: a one-line symptom, likely cause (mark as "suspected" if the ticket does not say), numbered steps to check and fix, when to escalate and to whom (use [ROLE] if unknown), and a place for owner and review date. Use only what the ticket says. Mark any step that you inferred with [CHECK]. Ask clarifying questions first if information is missing, and list what you are unsure of.
```

**Scopo: trovare il rischio di conoscenza nel tuo team.**

```text
Here is a list of the systems and tasks our team handles and who can do each: [paste as a table, one row per system or task, with the names or roles of people who can do it].

Using only this list, identify those that only one person can do, and those with two. Rank by how critical the task is, if I have marked it, otherwise leave unranked. For each single-person item, suggest one low-effort way to spread the knowledge (for example pairing or a tested runbook). Do not invent tasks or people. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: rivedere un runbook per chiarezza prima di verificarlo.**

```text
Here is a runbook: [paste].

Act as a tired on-call engineer who has not seen this system before. List every place where you would be unsure what to do, every term or tool not explained, and every step that assumes knowledge. Suggest clearer wording for each. Do not add technical steps that are not in the runbook; mark questions for the author as [ASK AUTHOR]. List what you are unsure of.
```

**Scopo: pianificare un passaggio di conoscenza per chi se ne va.**

```text
Help me plan a knowledge handover for [role] who leaves in [time].

What they own or do that others do not: [list].
Where it is written down now: [list, or write "nowhere"].
Who will take over, and their current experience: [describe].

Sort the items into: repeatable tasks to turn into tested runbooks, reasons and decisions to record as short notes, and judgment to share by shadowing or pairing. Propose a week-by-week plan, including testing each runbook with the successor. Do not invent items. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [runbook](../../../../skills/runbook/SKILL.md): da usare per scrivere procedure passo per passo che qualcun altro possa seguire sotto pressione.
- [postmortem](../../../../skills/postmortem/SKILL.md): da usare per registrare le lezioni degli incidenti in una forma che altri possano leggere.
- [architecture-decision-record](../../../../skills/architecture-decision-record/SKILL.md): da usare per registrare perché è stata presa una decisione di progettazione.
- [decision-records](../../../../skills/decision-records/SKILL.md): da usare per tenere un breve record di decisioni importanti non architetturali.
- [training-needs-analysis](../../../../skills/training-needs-analysis/SKILL.md): da usare per trovare le lacune di competenze che la condivisione della conoscenza dovrebbe affrontare.

## Fonti principali

- **Knowledge management** (Wikipedia): una panoramica ampia di storia, modelli, approcci e critiche del campo.
- **Postmortem Culture: Learning from Failure** (*Site Reliability Engineering*, Google, sre.google): come un'organizzazione condivide le lezioni degli incidenti.
- **Tacit knowledge** (Wikipedia): contesto sulla conoscenza difficile da mettere per iscritto.
- **Community of practice** (Wikipedia): contesto sui gruppi tra team che condividono conoscenza.

## Riferimenti

1. Knowledge management — Wikipedia — https://en.wikipedia.org/wiki/Knowledge_management
2. Postmortem Culture: Learning from Failure — Google SRE book, sre.google — https://sre.google/sre-book/postmortem-culture/
3. Tacit knowledge — Wikipedia — https://en.wikipedia.org/wiki/Tacit_knowledge
4. Community of practice — Wikipedia — https://en.wikipedia.org/wiki/Community_of_practice
5. SECI model of knowledge dimensions — Wikipedia — https://en.wikipedia.org/wiki/SECI_model_of_knowledge_dimensions
6. Organizational learning — Wikipedia — https://en.wikipedia.org/wiki/Organizational_learning
7. Knowledge base — Wikipedia — https://en.wikipedia.org/wiki/Knowledge_base
8. Ikujiro Nonaka — Wikipedia — https://en.wikipedia.org/wiki/Ikujiro_Nonaka
9. Manifesto for Agile Software Development — Beck et al., agilemanifesto.org — https://agilemanifesto.org/
