# Miglioramento continuo

**Il miglioramento continuo è l'abitudine di rendere servizi e modi di lavorare un po' migliori ancora e ancora, e diventa reale solo quando il lavoro di miglioramento è visibile, ha un responsabile, è programmato e verificato come qualsiasi altro lavoro.**

## Perché è importante

Ogni pratica di questa guida finisce nello stesso posto: imparare da ciò che è successo e cambiare qualcosa. Gli incidenti portano ai problemi, i problemi alle correzioni, le retrospettive agli esperimenti e le revisioni dei livelli di servizio a nuovi obiettivi. Il miglioramento continuo è la pratica che li collega e li tiene in movimento. Senza di essa, ogni pratica produce intuizioni su cui nessuno agisce.

In molte organizzazioni, il miglioramento è la prima cosa a essere schiacciata. La pressione della consegna riempie ogni giorno e le idee di miglioramento si accumulano in un documento che nessuno apre. I team agili partono avvantaggiati, perché le retrospettive sono incorporate, ma le retrospettive che non producono cambiamenti sono comuni. Il test di una pratica di miglioramento continuo è semplice: sai nominare tre cose che sono migliori in questo trimestre grazie ad essa?

L'[articolo di Wikipedia sul processo di miglioramento continuo](https://en.wikipedia.org/wiki/Continual_improvement_process) lo descrive come uno sforzo costante per migliorare prodotti, servizi o processi, incrementale o dirompente, con feedback, efficienza ed evoluzione attraverso piccoli passi come caratteristiche chiave. L'[articolo sul PDCA](https://en.wikipedia.org/wiki/PDCA) descrive il ciclo plan–do–check–act alla base di molti metodi di miglioramento. Entrambi sono generali. ITIL tratta il miglioramento continuo come componente del sistema di valore del servizio (vedi Argomento 2.3 — Il sistema di valore del servizio ITIL) e come pratica, ma il testo del proprietario del framework non era disponibile per questa guida, quindi questo argomento non descrive in dettaglio il modello di miglioramento di ITIL.

## Concetti fondamentali

### Che cos'è

Secondo Wikipedia, un processo di miglioramento continuo (CIP), detto anche continuous improvement, è uno sforzo costante per migliorare prodotti, servizi o processi. L'articolo lo descrive come un meta-processo per sistemi di gestione come qualità, gestione dei progetti e dei programmi, con tre caratteristiche chiave: feedback, efficienza ed evoluzione attraverso piccoli passi incrementali. Attribuisce a W. Edwards Deming il ruolo di pioniere, che vedeva il CIP come parte di un sistema che valuta il processo e il feedback dei clienti rispetto agli obiettivi organizzativi.

### Continual o continuous

L'articolo nota una questione terminologica: alla fine degli anni Novanta gli sviluppatori di ISO 9001:2000 cambiarono "continuous" in "continual", a quanto pare perché il comitato preferiva un miglioramento a passi e pensava che "continuous" potesse implicare cambiamenti minuto per minuto. ITIL usa "continual". Nella pratica i termini sono usati in modo intercambiabile. Ciò che conta è il miglioramento regolare e ripetuto.

### Kaizen

**Kaizen** è un termine giapponese che significa all'incirca "cambiare in meglio". Secondo l'articolo, il libro di Masaaki Imai del 1986 *Kaizen: The Key to Japan's Competitive Success* lo ha reso popolare, e le sue caratteristiche includono molti piccoli cambiamenti, idee dai lavoratori esistenti, basso costo e responsabilità dei dipendenti. Si adatta ai team agili, in cui chi svolge il lavoro è nella posizione migliore per vedere che cosa migliorare (vedi Argomento 1.7 — Sviluppo software lean).

### Il ciclo PDCA

Il PDCA (plan, do, check, act) è, nelle parole di Wikipedia, un metodo iterativo per controllare e migliorare continuamente processi e prodotti. È detto anche ciclo di Shewhart, da Walter Shewhart ai Bell Telephone Laboratories negli anni Venti; W. Edwards Deming lo modificò negli anni Quaranta e lo applicò alla gestione in Giappone negli anni Cinquanta. I passaggi:

| Passaggio | Che cosa fai |
|---|---|
| **Plan (pianificare)** | Stabilire gli obiettivi e i processi necessari per ottenere i risultati voluti |
| **Do (fare)** | Eseguire il piano, preferibilmente su piccola scala |
| **Check (verificare)** | Confrontare i dati raccolti con gli esiti attesi e cercare tendenze |
| **Act (agire)** | Indagare le cause radice dei problemi, adeguare il processo e iniziare il ciclo successivo |

L'articolo lega il PDCA al metodo scientifico e al suo schema ipotesi, esperimento, valutazione. Una variante, il PDSA, sostituisce "check" con "study", che Deming preferiva. L'articolo dice che l'iterazione è centrale: ogni ciclo affina la conoscenza. I team che chiamano una modifica "esperimento" con un'aspettativa dichiarata e una verifica usano questo schema.

### Da dove viene il miglioramento

Le idee di miglioramento vengono da molti posti in un'organizzazione di servizio:

| Fonte | Esempio | Dove è trattato |
|---|---|---|
| Incidenti e post-mortem | Un guasto mostra un allarme mancante | Argomento 3.2 — Gestione degli incidenti |
| Indagine sui problemi | Interruzioni ripetute mostrano un difetto di progetto | Argomento 3.3 — Gestione dei problemi |
| Temi del service desk | La stessa domanda ricorre ogni settimana | Argomento 3.1 — Service desk |
| Retrospettive | Il team trova lento il proprio passaggio di consegne | Argomento 1.4 — Previsioni di consegna e metriche di pianificazione |
| Dati di flusso | Una coda cresce in un passaggio | Argomento 1.5 — Kanban |
| Feedback dei clienti | Gli utenti trovano confuso un modulo | Argomento 3.6 — Gestione delle richieste di servizio |
| Revisioni dei livelli di servizio | Un obiettivo è mancato ripetutamente | Argomento 3.7 — Gestione dei livelli di servizio |
| Audit e revisioni dei rischi | Un controllo risulta debole | Argomento 5.7 — Governance, rischio e conformità |

La pratica del miglioramento continuo li raccoglie in un unico elenco visibile, sceglie che cosa fare e verifica i risultati.

### Il miglioramento come lavoro

La disciplina centrale è trattare il miglioramento come lavoro: elementi in un backlog con responsabili, benefici attesi e date. Senza di essa, il miglioramento dipende da entusiasmo e tempo libero. Significa anche affrontare apertamente il compromesso con il lavoro di consegna, così che la capacità sia protetta deliberatamente. Un accordo comune è riservare una quota di ogni ciclo al miglioramento, o condurre brevi cicli di miglioramento accanto alla consegna.

### Misurare il miglioramento

Per sapere che qualcosa è migliorato, serve un prima e un dopo. Scegli una misura legata al cambiamento, come tempo di ripristino del servizio, incidenti ripetuti o tempo di attesa, e guardala prima e dopo. Evita misure facili da spostare senza migliorare nulla. Usane diverse e discuti che cosa significano i numeri (vedi Argomento 5.6 — Metriche e misurazione). Gli articoli consultati non danno prove sull'efficacia dei programmi di miglioramento, quindi i risultati dei team stessi sono la prova.

### Metodi

Molti metodi sostengono il miglioramento: analisi delle cause radice, Six Sigma e DMAIC per la riduzione dei difetti basata sui dati, mappatura del flusso di valore ed eventi kaizen. L'articolo di Wikipedia sul miglioramento continuo non menziona Six Sigma, DMAIC o il modello di miglioramento di ITIL, quindi questa guida non glieli attribuisce. Scegli i metodi adatti alla dimensione del problema: un'azione di retrospettiva per un piccolo attrito, un progetto basato sui dati per un difetto persistente.

### Limiti

L'articolo non registra critiche al miglioramento continuo, e alcune delle sue fonti sono deboli o datate. I rischi pratici sono ben noti: affaticamento da miglioramento quando arrivano troppi cambiamenti, teatro del miglioramento in cui gli elenchi crescono e nulla cambia e ottimizzazione locale in cui un team migliora la propria parte e peggiora l'insieme. Proteggiti con un elenco breve e visibile e una verifica regolare dei risultati.

## Buone pratiche

1. **Tieni un unico elenco di miglioramenti visibile.** Raccogli in un posto le idee da incidenti, retrospettive, feedback e revisioni. Dai a ogni voce un responsabile, il problema che affronta e il beneficio atteso.
2. **Tratta i miglioramenti come lavoro.** Mettili nel backlog accanto agli elementi di consegna e decidi in pianificazione quanta capacità ottengono. Proteggi quella quota quando la pressione sale.
3. **Scegli pochi e portali a termine.** Lavora sulle una-tre voci più preziose alla volta. Un lungo elenco di voci iniziate è segno di teatro del miglioramento.
4. **Usa il ciclo.** Per ogni modifica, indica il piano e il risultato atteso, fai la modifica su piccola scala, verifica i dati e decidi se adottare, adeguare o abbandonare. Scrivi la decisione.
5. **Definisci il successo prima di iniziare.** Scegli la misura e che cosa ti aspetti di vedere prima della modifica. Questo evita di spiegare qualsiasi risultato come un successo a posteriori.
6. **Parti in piccolo e in locale.** Lascia che i team migliorino il proprio lavoro senza attendere permessi, entro limiti chiari. Riserva i programmi più grandi ai problemi che attraversano i team.
7. **Condividi ciò che impari.** Pubblica brevi note su che cosa è cambiato e che cosa è accaduto, compresi i fallimenti. Altri team possono riusarli o evitarli.
8. **Guarda l'intero sistema.** Prima di adottare un miglioramento, chiedi chi riguarda. Un guadagno locale che aggiunge lavoro a un altro team non è un miglioramento complessivo (vedi Argomento 2.4 — I principi guida di ITIL sul pensare in modo olistico).
9. **Rivedi regolarmente l'elenco.** Una volta al mese, guarda l'elenco con il team e il responsabile del servizio: che cosa è fatto, che cosa è bloccato, che cosa va abbandonato. Rimuovi le voci che hanno perso il senso.
10. **Celebra i risultati, non l'attività.** Riconosci i miglioramenti che hanno reso le cose migliori per utenti o personale, con prove. Non premiare il numero di idee o riunioni.
11. **Abbina il metodo al problema.** Usa esperimenti rapidi per i piccoli problemi, metodi basati sui dati per i difetti persistenti e chiedi aiuto specialistico per quelli complessi.
12. **Coinvolgi utenti e fornitori.** Chiedi loro che cosa migliorare e invitali a rivedere i risultati dove sono interessati (vedi Argomento 3.14 — Gestione dei fornitori).

## Domande da discutere con il team

**Che cosa è migliorato nell'ultimo trimestre grazie a qualcosa che abbiamo deciso di cambiare?**

Chiedi esempi specifici con prove. Se le persone fanno fatica, quello è il risultato. Se ci sono esempi, chiedi che cosa li ha fatti funzionare: un responsabile, tempo, una misura chiara. Confronta con i miglioramenti che si sono bloccati. Chi facilita può chiedere quale schema è più comune nel tuo team.

**Dove vanno a finire le nostre idee di miglioramento?**

Ripercorri diverse idee recenti: da una revisione di incidente, da una retrospettiva, da un commento di un cliente. Scopri dove è finita ciascuna. Spesso sono sparse in documenti e ticket. Discuti un elenco unico, chi lo mantiene e come viene rivisto. Crea la prima versione durante la sessione.

**Quanta della nostra capacità va al miglioramento, e chi l'ha deciso?**

Guarda gli ultimi cicli e stima la quota. Spesso è molto più piccola di quanto le persone credano, e nessuno l'ha scelta. Chiedi che cosa pensano team e manager che dovrebbe essere. Concorda una quota di partenza e un modo di proteggerla.

**Quali delle nostre modifiche abbiamo verificato dopo?**

Chiedi delle ultime tre modifiche e quali prove hanno mostrato che funzionavano. Molte non sono mai state verificate. Discuti una semplice abitudine: prima della modifica, di' che cosa ti aspetti di vedere e quando guarderai. Scegli una modifica in corso a cui applicarla.

**Quale miglioramento ha aiutato noi e danneggiato qualcun altro?**

Raccogli esempi di miglioramenti locali che hanno spostato un problema altrove. Spesso vengono da modifiche a passaggi di consegne o approvazioni. Discuti come chiedere prima alle persone interessate. Lo scopo è una semplice domanda da porre prima di una modifica.

**Qual è la voce più vecchia del nostro elenco di miglioramenti, e perché è ancora lì?**

Scegli la voce più vecchia e ricostruiscine la storia. Le ragioni includono nessun responsabile, nessun tempo, disaccordo o essere stata superata dagli eventi. Decidi di farla, programmarla o abbandonarla apertamente. Abbandonare una voce di proposito è segno di un elenco sano.

## Nella pratica: un esempio di ITIL agile

Un'azienda idrica regionale ha una piattaforma di fatturazione ai clienti e di lettura dei contatori gestita da un team di undici persone. Le retrospettive si tengono ogni due settimane e producono elenchi di azioni, ma poche vengono completate. Gli incidenti sono rivisti e le azioni di tali revisioni sono archiviate in un sistema separato. L'autorità di regolazione dell'azienda ha chiesto prove di come l'azienda impara dai guasti del servizio.

La responsabile del servizio e il responsabile del team decidono di rendere visibile il miglioramento. Creano un unico elenco di miglioramenti che raccoglie azioni da retrospettive, revisioni degli incidenti e feedback dei clienti. Ogni voce ha un responsabile, un'enunciazione del problema, il beneficio atteso e una misura. Riservano il 15 percento di ogni ciclo di due settimane alle voci di miglioramento e limitano a tre il numero in corso. Per ciascuna seguono plan, do, check e act: scrivono che cosa si aspettano di vedere, provano la modifica su un sottoinsieme, guardano i numeri dopo un periodo fisso e registrano la decisione. Una revisione mensile con la responsabile del servizio e un rappresentante del servizio clienti guarda che cosa è stato fatto e che cosa è stato imparato.

Dopo sei mesi, il team ha completato nove voci, tra cui una correzione per un guasto ripetuto nell'importazione dei dati dei contatori che ha portato a quasi zero gli incidenti ripetuti per quella causa, e una spiegazione più chiara della bolletta che ha ridotto le chiamate sull'argomento. Ha anche le prove per l'autorità di regolazione sotto forma dell'elenco e delle verifiche. Restano alcune difficoltà. Due voci sono state completate senza essere verificate perché il ciclo è andato avanti, e un miglioramento al processo di importazione ha reso più lento il lavoro di un team di reportistica a valle, cosa venuta alla luce solo un mese dopo. Il team aggiunge al modello dell'elenco una domanda "chi altro è interessato" e un promemoria in calendario per ogni verifica.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery possiedono gran parte dell'elenco di miglioramenti. Porta in un unico posto le idee da retrospettive e incidenti, porta a termine ciò che inizi e verifica i risultati. Sii disposto a spendere capacità in miglioramento e non solo in nuove funzionalità.

### Team di servizio e di operations

I team operativi vedono per primi l'attrito. Alimenta l'elenco con i temi degli incidenti, i contatti del desk e i dati di flusso e partecipa alla verifica dei risultati. Sostieni i miglioramenti che riducono il lavoro ripetitivo (toil) e gli incidenti ripetuti.

### Leadership e governance

I leader proteggono la capacità per il miglioramento e chiedono dei risultati. Chiedi che cosa è migliorato e come è stato verificato, non quante idee ci sono. Rimuovi gli ostacoli che i team nominano e mostra di averlo fatto. Sostieni i miglioramenti che attraversano i confini dei team.

### Clienti e utenti

Clienti e utenti forniscono alcune delle idee migliori. Di' al team che cosa ti frustra e chiedi di sapere che cosa è cambiato di conseguenza. Partecipa alle revisioni in cui il tuo servizio è coinvolto. Il tuo feedback sul fatto che una modifica abbia aiutato è la verifica più diretta che esista.

## Modalità di fallimento comuni

- **Idee senza responsabili.** L'elenco cresce e nulla viene fatto. Richiedi invece un responsabile e un beneficio atteso per ogni voce.
- **Miglioramento come tempo libero.** La consegna lo scalza. Riserva invece capacità e proteggila.
- **Troppi insieme.** Tutto è avviato e poco concluso. Limita invece il lavoro in corso per le voci di miglioramento.
- **Nessuna verifica.** Le modifiche sono adottate perché pianificate. Indica invece in anticipo il risultato atteso e guarda i dati.
- **Ottimizzazione locale.** Un team migliora e un altro soffre. Chiedi invece chi altro è interessato prima e dopo.
- **Teatro del miglioramento.** Workshop e poster sostituiscono i risultati. Conta invece i miglioramenti completati e verificati.
- **Misure manipolabili.** Il numero si muove e nulla migliora. Usa invece più misure e guarda il lavoro sottostante.
- **Dimenticare di condividere.** Le lezioni restano al team. Pubblica invece brevi note e invita altri a riusarle.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Raccolta e prioritizzazione | Le idee sono sparse e non prioritizzate | Alcuni team tengono elenchi | Un elenco visibile per team con responsabili e benefici attesi | Le priorità usano dati su impatto e sforzo | Gli elenchi di miglioramento sono allineati tra team e con i clienti |
| Capacità e flusso | Il miglioramento si fa nel tempo libero | Una parte di capacità è riservata | Una quota protetta di capacità e limiti al lavoro in corso | Capacità e throughput del miglioramento sono rivisti | La capacità è condivisa tra team per miglioramenti trasversali |
| Verifica dei risultati | I risultati non sono verificati | Alcune modifiche sono riviste | Ogni modifica ha un'aspettativa dichiarata e una verifica | I risultati sono misurati e legati alle decisioni | Le prove sono condivise tra team e usate per guidare l'organizzazione |
| Apprendimento e diffusione | Le lezioni restano locali | Alcune note sono condivise | Le lezioni sono pubblicate e riviste | Il riuso dei miglioramenti è monitorato | I miglioramenti si diffondono abitualmente tra team e fornitori |

## Checklist

- [ ] Abbiamo un unico elenco di miglioramenti visibile con responsabili e benefici attesi.
- [ ] Idee da retrospettive, revisioni degli incidenti, temi del desk e feedback lo alimentano tutte.
- [ ] Una quota protetta di ogni ciclo va alle voci di miglioramento.
- [ ] Limitiamo il numero di voci di miglioramento in corso.
- [ ] Ogni modifica indica un risultato atteso e un momento per verificarlo.
- [ ] Verifichiamo i risultati e registriamo la decisione di adottare, adeguare o abbandonare.
- [ ] Chiediamo chi altro è interessato prima di fare una modifica.
- [ ] L'elenco è rivisto almeno ogni mese.
- [ ] Condividiamo brevi note su che cosa è cambiato e che cosa abbiamo imparato.
- [ ] Sappiamo nominare tre cose che sono migliori in questo trimestre grazie al lavoro di miglioramento.

## Prompt per l'IA

**Scopo: consolidare le idee di miglioramento in un unico elenco prioritizzato.**

```text
Here are improvement ideas from several sources over the last [period]: [paste items from retrospectives, incident reviews, desk themes, and feedback, one per line, with their source].

Merge duplicates, group related items, and produce a list with: a one-line problem statement for each, the source, what benefit it might bring (use only what the text implies, otherwise write "unknown"), and a question about effort. Do not rank by guesswork; instead propose a way to rank (for example by repeat count and user impact) and apply it only to data I gave. List what you are unsure of.
```

**Scopo: trasformare un'idea di miglioramento in un piccolo esperimento.**

```text
Help me turn this improvement idea into a small experiment using plan, do, check, act.

The idea: [describe].
The problem it addresses, with evidence: [paste facts].
Who is affected: [list teams and users].
Measures we already have: [list].

Write: a hypothesis in one sentence, the smallest change that could test it, how long to run it, what we will measure before and after (leave targets as [to be agreed]), who else to ask before we start, and what decision rule we will use at the end. Do not invent baseline data. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: rivedere lo stato di un elenco di miglioramenti.**

```text
Here is our improvement list with status, owner, age, and expected benefit: [paste].

Using only this text, identify: items with no owner; items older than [period] with no progress; items whose expected benefit is unclear; and items that look related and could be combined. For each, suggest a question to ask at the monthly review. Do not decide for us what to drop. List what you are unsure of.
```

**Scopo: verificare se un miglioramento ha funzionato.**

```text
We made this change: [describe] on [date].

Measure before the change, with dates and values: [paste real data].
Measure after, with dates and values: [paste real data].
What else changed in the same period: [list, or write "unknown"].

Describe in plain words what the data shows, without claiming the change caused it if other changes could explain it. Suggest additional checks, and say whether the data is enough to decide to adopt, adjust, or drop. Do not invent numbers or statistics. List what you are unsure of.
```

## Competenze per l'IA

- [kaizen](../../../../skills/kaizen/SKILL.md): da usare per pianificare e rivedere miglioramenti piccoli e continui.
- [agile-reflection](../../../../skills/agile-reflection/SKILL.md): da usare per condurre retrospettive che producono azioni con responsabile.
- [dmaic](../../../../skills/dmaic/SKILL.md): da usare per il miglioramento basato sui dati dei difetti persistenti, attraverso define, measure, analyze, improve e control.
- [six-sigma](../../../../skills/six-sigma/SKILL.md): da usare quando variazione e difetti sono il problema principale e serve un approccio statistico.
- [futurespective](../../../../skills/futurespective/SKILL.md): da usare per guardare avanti insieme e concordare i miglioramenti per il periodo successivo.

## Fonti principali

- **Continual improvement process** (Wikipedia): la definizione, il kaizen, il PDCA e la terminologia continual contro continuous.
- **PDCA** (Wikipedia): il ciclo plan–do–check–act, le sue origini e varianti come il PDSA.
- **Kaizen** (Wikipedia): contesto sul miglioramento piccolo e continuo e sulle sue origini nell'industria giapponese.
- **Lean software development** (Wikipedia): le idee lean dietro il miglioramento continuo nel lavoro sul software.

## Riferimenti

1. Continual improvement process — Wikipedia — https://en.wikipedia.org/wiki/Continual_improvement_process
2. PDCA — Wikipedia — https://en.wikipedia.org/wiki/PDCA
3. Kaizen — Wikipedia — https://en.wikipedia.org/wiki/Kaizen
4. W. Edwards Deming — Wikipedia — https://en.wikipedia.org/wiki/W._Edwards_Deming
5. Walter A. Shewhart — Wikipedia — https://en.wikipedia.org/wiki/Walter_A._Shewhart
6. Lean software development — Wikipedia — https://en.wikipedia.org/wiki/Lean_software_development
7. Six Sigma — Wikipedia — https://en.wikipedia.org/wiki/Six_Sigma
8. Root cause analysis — Wikipedia — https://en.wikipedia.org/wiki/Root_cause_analysis
9. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
