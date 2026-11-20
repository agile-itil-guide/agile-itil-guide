# Sviluppo software lean

**Lo sviluppo software lean applica al lavoro sul software le idee lean di eliminare gli sprechi, imparare in fretta e ottimizzare l'intero sistema, e offre ai team di servizio un modo condiviso di vedere dove tempo e fatica si disperdono lungo il flusso dalla richiesta al valore.**

## Perché è importante

I metodi agili dicono di consegnare a piccoli passi e di imparare. Lean pone una domanda più netta: dove va a finire il tempo? Nella maggior parte delle organizzazioni di servizio, il tempo di lavoro effettivo su una richiesta è una piccola parte del tempo trascorso. Il resto è attesa di approvazioni, passaggi tra team, rilavorazioni dovute a difetti e lavoro che nessuno voleva in primo luogo. Lean ti dà parole e strumenti per vedere quegli sprechi e rimuoverli.

Lean pone anche l'accento sull'intero sistema. Un team che accelera la propria parte mentre la coda prima o dopo di essa cresce non ha migliorato nulla per il cliente. Questa visione si addice bene alla gestione dei servizi. Un servizio è la somma di molti team, strumenti e fornitori, e un ritardo ovunque è un ritardo per l'utente. Il principio "ottimizza l'intero" è un promemoria permanente a guardare il flusso end-to-end.

Lean è una fonte di gran parte di ciò che compare altrove in questa guida. Kanban attinge alle stesse radici (vedi Argomento 1.5 — Kanban), la gestione del flusso di valore applica la mappatura lean al lavoro digitale (vedi Argomento 5.4 — Gestione del flusso di valore) e il miglioramento continuo riecheggia l'abitudine lean ai piccoli guadagni costanti (vedi Argomento 3.15 — Miglioramento continuo). Questo argomento spiega le idee e come usarle senza ridurle a slogan.

## Concetti fondamentali

### Da dove viene lean

Secondo l'[articolo di Wikipedia sulla lean manufacturing](https://en.wikipedia.org/wiki/Lean_manufacturing), lean è nato dal [sistema di produzione Toyota](https://en.wikipedia.org/wiki/Toyota_Production_System). Dopo la seconda guerra mondiale i produttori giapponesi avevano poca liquidità, poco spazio e poche materie prime, e Taiichi Ohno e Shigeo Shingo riprogettarono il processo della Toyota attorno a piccole fabbriche e basse scorte, basandosi sull'insegnamento di W. Edwards Deming. John Krafcik coniò il termine "lean" in un articolo del 1988, e James Womack e Daniel Jones lo definirono formalmente nel loro libro del 1996 *Lean Thinking*.

Il termine "lean software development" deriva dal libro del 2003 *Lean Software Development: An Agile Toolkit* di Mary e Tom Poppendieck, secondo l'[articolo di Wikipedia sullo sviluppo software lean](https://en.wikipedia.org/wiki/Lean_software_development). Il libro adatta al software i principi della lean manufacturing e confronta gli strumenti lean con le pratiche agili. Gli interventi dei Poppendieck alle conferenze agili contribuirono a portare le idee nella comunità agile.

### Cinque principi del pensiero lean

Womack e Jones enunciarono cinque principi del pensiero lean, come li riporta l'articolo sulla manifattura:

1. **Valore:** definire il valore dal punto di vista del cliente.
2. **Flusso di valore:** individuare l'intera sequenza di passaggi che crea quel valore e mettere in discussione i passaggi che non ne aggiungono.
3. **Flusso:** far scorrere senza interruzioni i passaggi rimanenti.
4. **Pull:** lasciare che la domanda del cliente tiri il lavoro attraverso il sistema, invece di spingerlo.
5. **Perfezione:** continuare a migliorare, così che gli sprechi continuino a essere eliminati.

### Sette principi per il software

L'articolo di Wikipedia sullo sviluppo software lean elenca sette principi per il software:

| Principio | Che cosa chiede | Nel lavoro sui servizi |
|---|---|---|
| **Eliminare gli sprechi** | Rimuovere tutto ciò che non aggiunge valore per il cliente | Abbandonare approvazioni che non rifiutano mai, report che nessuno legge e funzionalità che nessuno usa |
| **Amplificare l'apprendimento** | Accorciare il ciclo dal provare qualcosa all'imparare com'è andata | Rilasciare piccole modifiche e osservare che cosa fanno gli utenti |
| **Decidere il più tardi possibile** | Ritardare gli impegni finché non hai fatti, mantenendo aperte le opzioni | Non fissare il design dell'intero futuro di un servizio prima di sapere come viene usato |
| **Consegnare il più in fretta possibile** | Ridurre il tempo dall'idea al valore; una consegna rapida permette di vedere e analizzare prima i risultati | Accorciare il percorso per le modifiche piccole e le richieste di routine |
| **Dare potere al team** | Lasciare che le persone che svolgono il lavoro prendano le decisioni su di esso | Dare al service desk l'autorità di risolvere i problemi comuni senza escalation |
| **Incorporare l'integrità** | Costruire la qualità mentre si lavora, invece di ispezionarla dopo | Test automatici, monitoraggio e runbook chiari come parte del lavoro |
| **Ottimizzare l'intero** | Migliorare il flusso end-to-end, non le prestazioni di una parte | Misurare il tempo dalla richiesta alla risoluzione tra i team, non la coda di ciascun team |

L'articolo dice che questi principi hanno successo solo se applicati insieme e con giudizio sano sull'ambiente. Definisce inoltre un mito la convinzione che "la fretta produce sprechi", sostenendo che una consegna rapida aiuta i team a vedere e analizzare prima l'output. Quell'affermazione è un punto di vista, non una legge: la velocità senza qualità incorporata produce sprechi, ed è per questo che "incorporare l'integrità" sta accanto a "consegnare il più in fretta possibile."

### Sprechi nel lavoro sul software e sui servizi

I sette sprechi di lean (chiamati *muda*) derivano dall'elenco di Shingo per la manifattura: scorte, sovrapproduzione, sovralavorazione, trasporto, movimento eccessivo, attesa e difetti. L'articolo sullo sviluppo software lean li mappa sul software così:

| Spreco manifatturiero | Equivalente nel software | Esempio in un team di servizio |
|---|---|---|
| Scorte | Lavoro parzialmente fatto | Un lungo elenco di modifiche iniziate ma non concluse |
| Sovrapproduzione | Funzionalità extra | Un report o un servizio che nessuno ha chiesto |
| Sovralavorazione | Processi extra | Quattro approvazioni su una modifica a basso rischio |
| Trasporto | Cambio di attività | Un ingegnere tirato tra incidenti e lavoro di progetto |
| Attesa | Attesa | Un ticket in attesa nella coda di un altro team |
| Movimento | Passaggi di consegne | Una richiesta che passa per cinque persone |
| Difetti | Difetti | Un bug che causa rilavorazioni e incidenti ripetuti |

I termini giapponesi *mura* (irregolarità) e *muri* (sovraccarico) sono talvolta aggiunti alle discussioni sugli sprechi. Gli articoli di Wikipedia consultati qui elencano solo i sette sprechi, quindi usa i termini aggiuntivi con cautela e definiscili quando lo fai.

### Mappatura del flusso di valore

L'articolo sullo sviluppo software lean indica la mappatura del flusso di valore come la tecnica per trovare gli sprechi, con gli sprechi rimossi in cicli ripetuti. Una mappa mostra ogni passaggio del percorso dalla richiesta al valore consegnato, con il tempo che il lavoro trascorre in lavorazione e quello che trascorre in attesa. Il risultato è spesso uno shock: un percorso che richiede settimane può contenere ore di lavoro effettivo.

### Pull, flusso e kanban

Il principio pull di lean è alla base dei limiti di Kanban al lavoro in corso. L'articolo sul software descrive uno sviluppo just-in-time in cui il cliente indica il risultato necessario e il team organizza da sé i propri compiti, tirando il lavoro quando la capacità lo consente. Le schede kanban sono una forma visibile di quel pull (vedi Argomento 1.5 — Kanban).

### Kaizen: miglioramento piccolo e costante

Kaizen significa miglioramento continuo e incrementale. L'articolo sulla manifattura lo fa risalire ai gruppi di miglioramento alla Toyota nel 1936. In un team di servizio compare come piccole modifiche fatte spesso e dalle persone più vicine al lavoro, come un modello rivisto, un nuovo controllo automatico o un passaggio di consegne più chiaro. Si distingue dai grandi programmi di miglioramento perché non aspetta mai un ciclo di bilancio.

### Limiti di lean

Gli articoli consultati non nominano critiche formali, ma i limiti pratici sono ben noti. Lean nasce dalla manifattura ripetibile, e il lavoro della conoscenza varia molto di più. Contare gli sprechi può ridurre il margine di cui un team ha bisogno per far fronte alle sorprese, quindi un team completamente carico è lento a rispondere a un incidente. Considera lean come una lente che trova gli sprechi e mantieni capacità di riserva dove la variazione è alta (vedi Argomento 3.11 — Disponibilità, capacità e prestazioni).

## Buone pratiche

1. **Definisci il valore dal lato del cliente.** Per ogni servizio, scrivi che cosa l'utente ottiene davvero e quando lo ottiene. Usalo per giudicare ogni passaggio: aggiunge valore per l'utente, o serve solo il nostro processo?
2. **Mappa il flusso di valore per un tipo di richiesta reale.** Scegli una richiesta o una modifica comune e ripercorrila dal primo contatto alla consegna. Registra tempo di lavoro e tempo di attesa a ogni passaggio. Una mappa approssimativa disegnata in un'ora è più utile di una perfetta disegnata in un trimestre.
3. **Dai un nome agli sprechi che trovi.** Usa le sette categorie come checklist: lavoro parzialmente fatto, funzionalità extra, processi extra, cambio di attività, attesa, passaggi di consegne, difetti. Nominarli li rende più facili da discutere senza incolpare gli individui.
4. **Attacca prima l'attesa più lunga.** Il ritardo maggiore nella mappa di solito sta tra i passaggi, non dentro di essi. Ridurlo di solito vale più che rifinire un passaggio già veloce.
5. **Limita il lavoro in corso.** Concludere il lavoro è più rapido che destreggiarsi tra più cose. Fissa un tetto al numero di elementi aperti per team e osserva che cosa succede al tempo che ciascuno richiede.
6. **Incorpora la qualità.** Aggiungi controlli nel momento del lavoro, come test automatici, revisione tra pari e monitoraggio pre-rilascio, così che i difetti siano trovati presto. Ispezionare alla fine è più lento e più costoso.
7. **Ritarda le decisioni che non puoi ancora prendere bene.** Mantieni aperte le opzioni finché non hai fatti, ma fissa una data entro cui deciderai. Questo evita sia l'impegno precoce su un design sbagliato sia l'indecisione infinita.
8. **Dai potere alle persone più vicine al lavoro.** Lascia che analisti del service desk, ingegneri di turno e sviluppatori prendano decisioni entro limiti chiari. Indica i limiti, come soglie di spesa o di rischio, e rivedili dopo gli incidenti.
9. **Guarda l'intero, non la parte.** Misura il tempo end-to-end dalla richiesta alla risoluzione e discutine con tutti i team coinvolti. Una modifica che aiuta un team e ne rallenta un altro non è un miglioramento.
10. **Rendi il miglioramento piccolo, frequente e locale.** Incoraggia ogni team a fare un piccolo miglioramento ogni settimana o due e a condividere ciò che ha imparato. Registra la modifica e il suo risultato.
11. **Tieni margine dove la variazione è alta.** Non riempire ogni ora di un team di reperibilità. Lascia capacità per le sorprese e giudicala da quanto in fretta il team si riprende quando qualcosa va storto.
12. **Usa lean con altre pratiche.** Combina le mappe del flusso di valore con le misure di flusso di Kanban e con la gestione dei problemi per i difetti ricorrenti (vedi Argomento 3.3 — Gestione dei problemi).

## Domande da discutere con il team

**Se seguissimo una richiesta comune dall'inizio alla fine, quanto del tempo trascorso sarebbe lavoro effettivo?**

Scegli una richiesta tipica e raccogli le date di ogni passaggio. Segna il tempo in cui qualcuno ci lavorava e quello in cui è rimasta in una coda. La proporzione è spesso uno shock. Chiedi alle persone dove si aspettavano le attese e dove erano. Chi facilita dovrebbe resistere all'inizio alle soluzioni e chiedere al gruppo di concordare su ciò che la mappa mostra.

**Quale dei sette sprechi vediamo più spesso nel lavoro quotidiano?**

Dai alle persone l'elenco e chiedi un esempio recente per ciascuno. Aspettati che lavoro parzialmente fatto, cambio di attività, attesa e passaggi di consegne emergano spesso. Chiedi quali di essi il team può cambiare da solo e quali richiedono altri team o manager. Concludi scegliendo uno spreco da ridurre questo mese.

**Che cosa facciamo che i nostri clienti non rimpiangerebbero se smettessimo?**

Elenca report, riunioni, moduli e approvazioni. Per ciascuno, chiedi chi lo usa e che cosa succede se si ferma. Alcuni saranno necessari per audit o sicurezza, che è un buon motivo. Altri si riveleranno abitudine. Assegna a qualcuno il compito di verificare ogni elemento dubbio prima di rimuoverlo.

**Dove ispezioniamo la qualità alla fine invece di incorporarla?**

Guarda i tuoi processi di rilascio, modifica e incidente per controlli a fine linea. Chiedi quali difetti trovano quei controlli e quando avrebbero potuto essere trovati prima. Le risposte tipiche includono test dopo la fine dello sviluppo e revisione dei documenti a posteriori. Scegli un controllo da anticipare e descrivi come capirai se ha aiutato.

**Chi può prendere decisioni nel nostro team senza chiedere, e chi dovrebbe?**

Chiedi alle persone di elencare le ultime cinque decisioni che volevano prendere e non hanno potuto, e perché. Cerca schemi, come limiti di spesa, approvazioni di modifiche o scelte di priorità. Chiedi che cosa renderebbe sicuro avvicinare una di quelle decisioni al lavoro, come un guardrail o una revisione a posteriori. Non spingere per un sì; lo scopo è scoprire che cosa le persone ritengono necessario.

**Se tutto ciò che facciamo ora diventasse più veloce, che cosa si romperebbe per primo?**

Questa domanda mette alla prova insieme "consegnare il più in fretta possibile" e "incorporare l'integrità". Chiedi dove un flusso più rapido sovraccaricherebbe un team, uno strumento o una persona. Le risposte tipiche sono test, approvazioni e carico di reperibilità. Considera le risposte come le prossime cose da migliorare. Ricorda che lean valorizza il flusso dell'intero sistema, quindi il collo di bottiglia è dove investire.

## Nella pratica: un esempio di ITIL agile

Il reparto IT di un'agenzia fiscale nazionale gestisce un servizio interno con cui il personale richiede l'accesso a software. Una richiesta tipica richiede circa tre settimane, e il personale si lamenta ad alta voce. Il team di cinque persone che evade le richieste crede di lavorare sodo ed è sorpreso dalla lamentela.

Un manager conduce una sessione di mappatura del flusso di valore con il team, il gruppo sicurezza e due utenti di business. Insieme ripercorrono dieci richieste recenti. Ogni richiesta attraversa otto passaggi: invio del modulo, approvazione del responsabile di linea, approvazione del proprietario dei dati, revisione di sicurezza, verifica della licenza, assegnazione del ticket, installazione e conferma. La mappa mostra che il lavoro effettivo richiede circa un'ora, e quasi tutte le tre settimane sono attesa tra i passaggi, per lo più per le due approvazioni e la revisione di sicurezza. In tre casi su dieci la richiesta è stata restituita all'utente per un campo mancante nel modulo.

Il gruppo concorda tre cambiamenti. Il modulo ottiene campi obbligatori e una breve guida, il che elimina le restituzioni. Le richieste per un breve elenco di applicazioni comuni e a basso rischio ricevono un'unica approvazione dal responsabile di linea, con il proprietario dei dati informato. Il gruppo sicurezza concorda di rivedere ogni settimana un campione di tali richieste, anziché ogni richiesta prima dell'installazione. Dopo due mesi, il tempo tipico scende a circa una settimana. Resta una difficoltà: le richieste per applicazioni sensibili richiedono ancora tre settimane, e il gruppo sicurezza nota che il campionamento ha intercettato due richieste che avrebbero dovuto essere rifiutate. Aggiustano l'elenco delle applicazioni idonee all'approvazione rapida e decidono di rivederlo ogni trimestre.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery possono usare lean per guardare oltre il proprio sprint o la propria lavagna. Mappa il percorso da un'idea alle mani di un utente, compresi test, revisione di sicurezza e approvazioni di rilascio, e trova dove il lavoro aspetta. Tratta il lavoro non concluso come spreco e preferisci concludere a iniziare.

### Team di servizio e di operations

I team operativi vedono gli sprechi ogni giorno: incidenti ripetuti, passaggi tra livelli e richieste che rimbalzano. Usa le mappe per mostrare dove il lavoro aspetta e usa la gestione dei problemi per rimuovere le cause delle ripetizioni. Sostieni la necessità di capacità di riserva mostrando che cosa succede al flusso quando ogni ora è pianificata.

### Leadership e governance

I leader plasmano il sistema che crea la maggior parte degli sprechi: regole di approvazione, cicli di finanziamento e reporting. Chiedi ai tuoi team dove quelle regole costano più tempo e da quale rischio protegge ciascuna. Sii pronto a sostituire un controllo con un controllo più leggero che soddisfi lo stesso scopo.

### Clienti e utenti

I clienti definiscono il valore nel pensiero lean, e avvertono gli sprechi come ritardo. Aspettati che ti si chieda di che cosa hai davvero bisogno e con quale urgenza. Di' al team quale parte di un servizio conta di più per te, perché ciò guida dove va lo sforzo. In cambio puoi aspettarti attese più brevi e prevedibili.

## Modalità di fallimento comuni

- **Tagliare la capacità in nome degli sprechi.** I team funzionano a pieno carico e non sanno rispondere alle sorprese. Mantieni invece margine dove la variazione è alta e giudica da quanto in fretta il team si riprende.
- **Mappare senza agire.** La mappa del flusso di valore finisce su una parete e nulla cambia. Scegli invece l'attesa maggiore e concorda un cambiamento con un responsabile prima della fine della sessione.
- **Ottimizzare un solo team.** Un guadagno locale sposta la coda altrove. Misura invece il tempo end-to-end e concorda i cambiamenti con tutti i team del flusso.
- **Rimuovere controlli senza comprenderli.** Un passaggio che sembrava spreco proteggeva da un rischio reale. Chiedi invece che cosa protegge ciascun passaggio e sostituiscilo con un controllo più leggero dove puoi.
- **Usare le parole lean come slogan.** Le persone dicono "spreco" per liquidare il lavoro dei colleghi. Usa invece i termini per descrivere il flusso e tieni la conversazione sul sistema.
- **Spingere la velocità a scapito della qualità.** Una consegna più veloce produce più difetti e rilavorazioni. Tratta invece "incorporare l'integrità" come precondizione della velocità.
- **Applicare numeri della manifattura al lavoro della conoscenza.** Gli obiettivi di una fabbrica non si adattano al lavoro variabile. Usa invece lean come modo di vedere e di chiedere e fissa le misure dai tuoi dati.
- **Trattare lean come un progetto una tantum.** I guadagni svaniscono quando l'attenzione si sposta. Rendi invece i piccoli miglioramenti parte della routine di ogni team.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Vedere gli sprechi | Gli sprechi sono avvertiti ma non descritti | Alcuni team mappano il proprio lavoro | I team usano categorie di spreco e mappe del flusso di valore condivise | Attese e rilavorazioni sono misurate lungo il flusso di valore | Mappe e misure attraversano team e fornitori |
| Flusso e pull | Il lavoro è spinto e avviato in blocco | Alcuni team limitano il lavoro in corso | Regole pull e limiti sono standard | Le misure di flusso guidano le modifiche a limiti e regole | Il flusso è coordinato lungo l'intero flusso di valore |
| Incorporare la qualità | La qualità è ispezionata alla fine | Alcuni team testano presto e rivedono il lavoro | Controlli automatici e revisioni integrate sono standard | I tassi di difetti sfuggiti sono monitorati e ridotti | Le pratiche di qualità sono condivise e migliorate tra i team |
| Miglioramento continuo | Il miglioramento segue le crisi | Alcuni team fanno piccole modifiche regolari | Ogni team ha una routine di miglioramento regolare | I miglioramenti sono monitorati e il loro effetto verificato | I miglioramenti si diffondono abitualmente tra team e fornitori |

## Checklist

- [ ] Abbiamo definito che cosa significa valore per almeno un servizio dal lato dell'utente.
- [ ] Abbiamo mappato il flusso di valore per un tipo di richiesta comune, con tempo di lavoro e tempo di attesa.
- [ ] Il team sa nominare i sette sprechi e dare un esempio recente di ciascuno.
- [ ] Il lavoro in corso è limitato e il lavoro non concluso è visibile.
- [ ] I controlli di qualità avvengono durante il lavoro oltre che alla fine.
- [ ] Abbiamo scelto almeno un'attesa da ridurre, con un responsabile e una data.
- [ ] Il team ha limiti chiari per le decisioni che può prendere senza chiedere.
- [ ] Misuriamo il tempo end-to-end per almeno un flusso tra più team.
- [ ] Teniamo capacità di riserva per le sorprese dove la domanda varia.
- [ ] Ogni team fa e registra un piccolo miglioramento a un ritmo regolare.

## Prompt per l'IA

**Scopo: analizzare un flusso di valore dai tempi che fornisci.**

```text
Help me analyze a value stream for [type of request, e.g. "software access requests"].

Here are the steps in order, with who does each step, how long work was actually done on it, and how long the item waited before and after it. Use real numbers from a few recent cases: [paste as a table, with one row per step and one column per case].

Calculate, using only my numbers, the total elapsed time, the total working time, and the share of time spent waiting. Identify the three longest waits. For each wait, ask what the step protects against, and suggest one lighter alternative. Do not invent data. If numbers are missing, ask me first, mark assumptions, and list what you are unsure of.
```

**Scopo: classificare esempi di spreco dal lavoro del tuo team.**

```text
Here is a list of things that frustrate our team or customers: [paste 8-12 short, factual examples].

Classify each one under the seven wastes of lean software development: partially done work, extra features, extra process, task switching, waiting, handoffs, and defects. If an item does not fit any, say so. Give one sentence of reasoning per item based only on what I wrote. Then say which two categories seem most common in this list and suggest two questions the team should discuss. Mark assumptions, and list what you are unsure of.
```

**Scopo: verificare se rimuovere un controllo è sicuro.**

```text
We are considering removing or simplifying this control: [describe the approval, report, or step].

What we believe it is for: [describe the purpose, or write "unknown"].
Who uses its output: [list people or teams, or write "unknown"].
Rules we know apply (audit, security, legal), with the actual text if you have it: [paste text, or write "none known"].

List the questions we should answer before changing it. Describe two lighter ways to meet its purpose, and a way to check after the change that nothing worse happened. Do not claim any law or standard applies unless I pasted its text. Mark assumptions, and list what you are unsure of.
```

**Scopo: pianificare un workshop di mappatura del flusso di valore.**

```text
Plan a 90-minute value stream mapping workshop for [number] people from [teams or roles]. We want to examine [request type or service].

Include: a timed agenda, who must attend, what data to bring (use only data we really have), how to draw the map step by step, how to mark working time and waiting time, and a closing step that records one agreed change with an owner and a date. Keep it free of any particular tool. Ask clarifying questions first if information is missing, and list what you are unsure of.
```

## Competenze per l'IA

- [value-stream-map](../../../../skills/value-stream-map/SKILL.md): da usare per mappare passaggi, tempo di lavoro e tempo di attesa di una richiesta dall'inizio alla fine.
- [kaizen](../../../../skills/kaizen/SKILL.md): da usare per pianificare miglioramenti piccoli e continui una volta trovati gli sprechi.
- [workflow-analysis](../../../../skills/workflow-analysis/SKILL.md): da usare per analizzare come il lavoro si muove tra i ruoli e trovare passaggi di consegne e ritardi.
- [kanban](../../../../skills/kanban/SKILL.md): da usare per applicare pull e limiti al lavoro in corso al flusso che hai mappato.
- [six-sigma](../../../../skills/six-sigma/SKILL.md): da usare quando difetti e variazione, non solo l'attesa, sono il problema principale e serve un metodo basato sui dati per ridurli.

## Fonti principali

- **Lean software development** (Wikipedia): i sette principi, la mappatura degli sprechi e rimandi a ulteriori letture.
- **Lean manufacturing** (Wikipedia): la storia di lean alla Toyota, gli sprechi e i cinque principi del pensiero lean.
- **Lean Software Development: An Agile Toolkit** (Mary e Tom Poppendieck, 2003): il libro che portò le idee lean nella comunità agile.
- **Lean Thinking** (James Womack e Daniel Jones, 1996): l'enunciazione formale dei cinque principi di lean.

## Riferimenti

1. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
2. Lean manufacturing — Wikipedia — https://en.wikipedia.org/wiki/Lean_manufacturing
3. Toyota Production System — Wikipedia — https://en.wikipedia.org/wiki/Toyota_Production_System
4. Kaizen — Wikipedia — https://en.wikipedia.org/wiki/Kaizen
5. Value-stream mapping — Wikipedia — https://en.wikipedia.org/wiki/Value-stream_mapping
6. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
7. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
8. Muda (Japanese term) — Wikipedia — https://en.wikipedia.org/wiki/Muda_(Japanese_term)
