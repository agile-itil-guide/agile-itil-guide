# Gestione dei fornitori

**La gestione dei fornitori assicura che le parti esterne da cui un servizio dipende siano scelte con cura, tenute a aspettative chiare e trattate come parte del servizio, perché una promessa ai tuoi clienti è forte quanto le promesse che ci stanno dietro.**

## Perché è importante

Quasi nessun servizio moderno è costruito e gestito da un solo team. Dipende da piattaforme cloud, fornitori di software, processori di pagamento, operatori di rete, collaboratori esterni e partner specializzati. Quando uno di loro si guasta, il cliente non distingue tra il tuo fallimento e il loro. La loro interruzione è la tua, e lo è anche il lavoro di spiegarla.

I team agili usano i fornitori con facilità: una carta di credito, poche righe di configurazione e una nuova capacità è in funzione. Quella velocità è preziosa e crea un divario. Nessuno può aver chiesto che cosa succede se il servizio del fornitore peggiora, cambia le condizioni o chiude. Nessuno può sapere chi possiede la relazione. La gestione dei fornitori è la pratica di colmare quel divario in proporzione al rischio, senza trasformare ogni acquisto in un progetto.

L'[articolo di Wikipedia sulla gestione delle relazioni con i fornitori](https://en.wikipedia.org/wiki/Supplier_relationship_management) descrive la valutazione sistematica, a livello aziendale, di punti di forza, prestazioni e capacità dei fornitori, allineata alla strategia di business, e nota che le sue fonti sono scarse e datate, con diversi riferimenti dal 2009 al 2012. L'[articolo sull'integrazione e gestione dei servizi](https://en.wikipedia.org/wiki/Service_integration_and_management) descrive un approccio per le organizzazioni che usano più fornitori. Questo argomento li combina con gli altri argomenti della guida e con la pratica comune nella gestione dei servizi e dice quando sta facendo quest'ultima.

## Concetti fondamentali

### Gestione delle relazioni con i fornitori

Secondo Wikipedia, la gestione delle relazioni con i fornitori (SRM) coordina le interazioni con i fornitori lungo il ciclo di vita della relazione, con lo scopo di costruire partnership bidirezionali con i fornitori strategici, in modo analogo alla gestione delle relazioni con i clienti. L'articolo fa diversi punti utili per i team di servizio:

- **Segmenta i fornitori.** I fornitori sono segmentati per valore potenziale totale su più dimensioni, non solo per spesa, e per il grado di rischio che influisce su quel valore. L'articolo critica un approccio "one size fits all".
- **Misura le prestazioni in entrambe le direzioni.** Le organizzazioni usano balanced scorecard congiunte e bidirezionali con misure quantitative e qualitative, e alcune usano scorecard a 360 gradi che interpellano anche i fornitori.
- **Collabora.** Le attività congiunte includono vertici con i fornitori, riunioni esecutive, pianificazione di business congiunta, revisioni operative e previsione congiunta della domanda. L'articolo sostiene che la previsione congiunta e la riprogettazione dei processi hanno sbloccato risparmi dal 10 al 30 percento per le organizzazioni leader, ma l'articolo ha etichette di manutenzione per formulazione debole e citazioni mancanti, quindi tratta la cifra come un'affermazione, non un risultato.

### Perché la segmentazione conta

Non puoi gestire da vicino ogni fornitore. Una segmentazione utile pone due domande: quanto il servizio dipende da questo fornitore e quanto sarebbe difficile sostituirlo? Segue una griglia approssimativa.

| Dipendenza e sostituibilità | Esempi | Approccio |
|---|---|---|
| **Critico e difficile da sostituire** | La piattaforma cloud, il processore di pagamento | Relazione stretta: responsabile nominato, revisioni regolari, pianificazione congiunta, piani di uscita e di continuità |
| **Importante ma sostituibile** | Uno strumento di monitoraggio, un servizio di messaggistica | Revisione regolare, livelli di servizio chiari e un piano per cambiare se serve |
| **Di routine e facile da sostituire** | Cancelleria, una libreria minore | Contratto leggero e controllo periodico |

La griglia è un'illustrazione di questa guida, non di una fonte.

### Prestazioni dei fornitori e servizio che prometti

I tuoi livelli di servizio dipendono da quelli dei tuoi fornitori (vedi Argomento 3.7 — Gestione dei livelli di servizio). Se prometti il 99,9% di disponibilità e il tuo unico fornitore cloud ne promette meno, l'aritmetica non torna. La gestione dei fornitori include il confronto tra ciò a cui i fornitori si sono impegnati e ciò che hai promesso e il progettare attorno al divario con ridondanza o adeguando la tua promessa.

Nel vocabolario ITIL, un accordo con un fornitore esterno che sostiene un accordo sul livello di servizio è chiamato underpinning contract, e un accordo tra team interni che lo sostiene è chiamato accordo a livello operativo (operational-level agreement). Le fonti lette per questa guida non li definiscono, quindi controlla le pubblicazioni ITIL per i termini esatti.

### Ambienti multi-fornitore e SIAM

L'articolo sull'integrazione e gestione dei servizi (SIAM) descrive un approccio per gestire più fornitori e integrarli in un unico servizio rivolto al business. Nota che le organizzazioni si procurano sempre più spesso capacità IT da più fornitori esterni, un modello chiamato multisourcing, che può ridurre i costi e incoraggiare la concorrenza ma aggiunge onere di gestione e rende più difficile la gestione dei servizi end-to-end. Un **service integrator** fornisce governance e coordinamento perché i fornitori lavorino insieme.

L'articolo elenca quattro modelli per l'integratore (interno, fornitore principale, esterno e ibrido) e tre livelli: l'organizzazione cliente, il service integrator e i fornitori di servizi. Dice che SIAM è nato intorno al 2005 nel settore pubblico britannico, progettato per la prima volta per il Department for Work and Pensions, ed elenca pietre miliari tra cui un corpo di conoscenze nel 2016 e revisioni nel 2019 per COBIT 2019 e ITIL 4. Nota che ITIL fornisce una base e un linguaggio comune per lavorare con i fornitori ma non affronta in profondità gli ambienti multi-fornitore. Le difficoltà di implementazione che elenca includono SLA non allineati, fornitori che si danno la colpa a vicenda, responsabilità poco chiara delle decisioni sulle cause radice e lacune di comunicazione.

Pochi team agili hanno bisogno di un SIAM formale, ma le lezioni sono utili: quando più parti contribuiscono a un servizio, qualcuno deve possedere l'insieme, concordare come i problemi sono trattati oltre i confini e tenere coerenti tra loro i livelli di servizio dei fornitori.

### Contratti e agilità

I contratti possono aiutare o ostacolare il lavoro agile. I contratti a ambito fisso e prezzo fisso si adattano male all'imparare strada facendo (vedi Argomento 1.1 — Il Manifesto Agile sulla collaborazione con il cliente più della negoziazione dei contratti). Gli accordi che consentono il cambiamento, con modi chiari di adeguare l'ambito e misurare il valore, si adattano meglio. Un contratto deve anche coprire ciò che interessa alla gestione dei servizi: livelli di servizio, orari di supporto, gestione degli incidenti, protezione dei dati, obblighi di sicurezza, diritti di audit, uscita e continuità. I tuoi colleghi dell'ufficio legale e acquisti dovrebbero guidare sui termini legali.

### Rischio

I fornitori portano rischi: guasto, cambiamento di condizioni o prezzo, debolezze di sicurezza, concentrazione in un solo fornitore, lock-in e le dipendenze del fornitore stesso. L'articolo sull'SRM elenca la riduzione del rischio di fallimento come obiettivo senza descrivere metodi. Misure pratiche includono conoscere gli accordi di continuità del fornitore, distribuire le dipendenze critiche, mantenere portabili i dati ed esercitare l'uscita (vedi Argomento 3.12 — Gestione della continuità del servizio e Argomento 3.13 — Gestione della sicurezza delle informazioni).

### Relazione, non solo contratto

L'articolo sull'SRM sottolinea le partnership bidirezionali. I fornitori che comprendono i tuoi piani possono aiutare; i fornitori trattati solo come fonti di fatture no. Condividi le previsioni, coinvolgili nelle revisioni degli incidenti che li riguardano e ascolta il loro feedback sul tuo comportamento, come pagamenti in ritardo o richieste poco chiare.

### Limiti delle fonti

L'articolo sull'SRM non dà criteri di selezione, clausole contrattuali o tempistiche di implementazione. L'articolo sul SIAM non ha una sezione di critiche. Entrambi sono generali. Per i termini legali e finanziari, affidati alle funzioni acquisti e legale e al contratto stesso.

## Buone pratiche

1. **Elenca i tuoi fornitori e ciò per cui dipendi da loro.** Includi cloud, software, rete, pagamenti e collaboratori esterni. Per ciascuno, annota quale servizio supporta e chi nel tuo team possiede la relazione.
2. **Segmenta per dipendenza e sostituibilità.** Decidi quali pochi fornitori sono critici e investi lì la tua attenzione. Mantieni un tocco leggero per il resto.
3. **Nomina un responsabile per ogni fornitore importante.** Una persona dovrebbe conoscere contratto, contatti, prestazioni e piani. Senza un responsabile, le relazioni decadono.
4. **Verifica che gli impegni dei fornitori sostengano le tue promesse.** Confronta ciò a cui ciascun fornitore critico si è impegnato con ciò che hai detto ai clienti. Colma il divario con la progettazione, con la negoziazione o cambiando la tua promessa.
5. **Concorda in anticipo la gestione degli incidenti.** Sappi come segnalare un problema al fornitore, con quale rapidità risponde, chi può fare escalation e come comunicherà. Prova la via prima di averne bisogno.
6. **Includi sicurezza e protezione dei dati.** Chiedi ai fornitori come proteggono le tue informazioni e che cosa ti diranno dopo una violazione. Mettilo nel contratto, con l'ufficio legale.
7. **Pianifica l'uscita e il fallimento.** Per i fornitori critici, mantieni portabili i dati, conosci le alternative e scrivi un breve piano per il fallimento del fornitore o la tua uscita. Esercita la parte che puoi.
8. **Rivedi le prestazioni insieme.** Tieni revisioni regolari con i fornitori critici, condividi i dati in entrambe le direzioni e concorda azioni. Chiedi al fornitore come potresti essere un cliente migliore.
9. **Includi i fornitori nell'apprendimento.** Invitali alle revisioni degli incidenti e alle sessioni di pianificazione che li riguardano. Condividi le lezioni che li aiutano ad aiutarti.
10. **Rendi flessibili i contratti dove si prevede apprendimento.** Per il lavoro di sviluppo, preferisci accordi che permettono di cambiare l'ambito, con chiari punti di revisione, rispetto a promesse a ambito fisso. Mantieni fermi gli obblighi di servizio.
11. **Usa un integratore quando contribuiscono molti fornitori.** Per un servizio che dipende da più fornitori, nomina chi possiede il risultato end-to-end e come sono risolti i problemi tra fornitori. Non lasciarlo al cliente.
12. **Rivedi regolarmente il portafoglio dei fornitori.** Una volta all'anno, verifica quali fornitori servono ancora, quali sono rischi concentrati e quali sono più economici o migliori altrove.

## Domande da discutere con il team

**Quali fornitori potrebbero fermare il nostro servizio se si guastassero, e che cosa faremmo?**

Chiedi a ciascuno di nominare le dipendenze che lo preoccuperebbero di più. Compila l'elenco e segna ciascuna come critica, importante o di routine. Per ogni critica, chiedi che cosa farebbe il team nella prima ora di un guasto. Le risposte tipiche rivelano lacune in contatti, alternative e dati. Scegline una da pianificare.

**Che cosa ci hanno promesso i nostri fornitori, e che cosa abbiamo promesso ai nostri clienti?**

Metti i due elenchi fianco a fianco per un servizio chiave. Dove la promessa del fornitore è più debole, la promessa al cliente è a rischio. Chi facilita può chiedere se qualcuno ha letto di recente i livelli di servizio del fornitore. Concorda un divario da colmare.

**Chi possiede ogni relazione importante con un fornitore?**

Scorri l'elenco e nomina un responsabile per ciascuna. Le lacune sono comuni: la persona che ha firmato il contratto se n'è andata, o uno strumento è stato comprato con una carta e nessuno lo gestisce. Chiedi di che cosa avrebbe bisogno il responsabile per fare il lavoro, come tempo e un contatto. Assegna i responsabili dove mancano.

**Come scopriamo un problema del fornitore, e come lo diciamo ai nostri utenti?**

Ripercorri l'ultima volta in cui un fornitore ha avuto un'interruzione. Chiedi come l'avete saputo, quanto ci è voluto e che cosa avete detto ai clienti. Discuti pagine di stato, contatti e canali concordati. Pianifica un miglioramento, come un abbonamento al feed di stato del fornitore o un contatto di escalation nominato.

**Che cosa servirebbe per lasciare questo fornitore, e vorremmo mai farlo?**

Per un fornitore critico, chiedi di esportazione dei dati, prodotti alternativi e termini contrattuali. I team spesso scoprono un lock-in che non volevano. Discuti come ridurlo dove il rischio giustifica il costo. Registra una breve nota di uscita.

**I nostri fornitori sanno che cosa stiamo pianificando, e noi sappiamo che cosa pianificano loro?**

Chiedi quando ciascun fornitore critico ha sentito parlare dei tuoi piani l'ultima volta e quando tu hai sentito dei suoi. Le sorprese in entrambe le direzioni causano guai. Discuti una conversazione regolare. Concorda un fornitore con cui partire.

## Nella pratica: un esempio di ITIL agile

Un'emittente regionale gestisce un'app di notizie e un sito web con un team di quattordici persone. Il servizio dipende da un fornitore cloud, una rete di distribuzione dei contenuti, un servizio di notifiche push, uno strumento di moderazione dei commenti e una piccola azienda che fornisce un widget di live blog. Quando il servizio del fornitore del live blog si è guastato durante una notte elettorale, l'app ha mostrato errori per due ore e la reputazione dell'emittente ne ha sofferto. Nessuno nel team sapeva dire chi fosse il contatto del fornitore; il widget era stato aggiunto da uno sviluppatore che nel frattempo era passato ad altro.

Il responsabile della piattaforma guida una revisione. Il team elenca tutti i fornitori, ordinandoli per quanto il servizio dipende da loro e per quanto facilmente ciascuno potrebbe essere sostituito. Il fornitore cloud e la rete di distribuzione dei contenuti sono critici, e il servizio di notifiche e il widget sono importanti ma sostituibili. Ciascuno ottiene un responsabile nel team. Per il fornitore del widget, il team ottiene i contatti, legge i termini e scopre che non è promesso alcun livello di servizio. Decidono di tenere il fornitore ma di aggiungere un'alternativa: se il widget non si carica, la pagina mostra un link statico al live blog. Per il fornitore cloud, confrontano i suoi impegni con la disponibilità promessa ai redattori dell'emittente e trovano un divario in una regione, che colmano distribuendo il servizio su due.

Sei mesi dopo, una seconda interruzione al fornitore di notifiche viene rilevata dal monitoraggio in pochi minuti, il responsabile la solleva con il fornitore attraverso la via concordata e l'app continua a funzionare con notifiche ritardate. Restano difficoltà. I redattori vogliono che il widget del live blog faccia di più, ma il fornitore è troppo piccolo per impegnarsi a un livello di servizio e le regole degli acquisti dell'emittente rendono lenta una sostituzione. Il responsabile della piattaforma concorda con gli acquisti di condurre una piccola sperimentazione di un'alternativa e di rivedere l'elenco dei fornitori ogni anno.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery scelgono e integrano molti fornitori. Registra ogni dipendenza quando la aggiungi, nomina un responsabile e chiedi di livelli di servizio e uscita prima di farvi affidamento. Costruisci alternative per i guasti che riesci a immaginare.

### Team di servizio e di operations

I team operativi trattano con i fornitori negli incidenti. Mantieni aggiornati i contatti e le vie di escalation, provali e registra le prestazioni dei fornitori. Porta queste prove alle revisioni e agli acquisti.

### Leadership e governance

Leader e acquisti plasmano i termini e la relazione. Chiedi un elenco dei fornitori critici e dei loro rischi, sostieni contratti flessibili per il lavoro basato sull'apprendimento e assicurati che il contratto copra livelli di servizio, sicurezza e uscita. Chiedi chi possiede il risultato end-to-end quando contribuiscono molti fornitori.

### Clienti e utenti

Clienti e utenti si affidano all'intera catena, non a un singolo anello. Chiedi ai fornitori quali fornitori contano per il servizio che usi e come lo proteggono. Quando qualcosa va storto, aspettati onestà su quale parte ha fallito e che cosa si sta facendo.

## Modalità di fallimento comuni

- **Dipendenze nascoste.** Uno strumento aggiunto da uno sviluppatore diventa critico e nessuno lo possiede. Registra invece ogni dipendenza e nomina un responsabile.
- **Una taglia per tutti.** Ogni fornitore ottiene lo stesso processo pesante, o nessuno ne ottiene. Segmenta invece per dipendenza e sostituibilità.
- **Promesse che non tornano.** La promessa al cliente è più forte di quella del fornitore. Confronta invece gli impegni e colma il divario.
- **Nessuna via testata.** La linea di supporto del fornitore si scopre durante un'interruzione. Concorda e prova invece contatti ed escalation in anticipo.
- **Lock-in per caso.** I dati non possono essere esportati. Verifica invece presto la portabilità e registra una nota di uscita.
- **Solo contratto, nessuna relazione.** Il fornitore è un estraneo quando arrivano i guai. Tieni invece revisioni regolari e condividi i piani.
- **Nessuno possiede l'insieme.** Più fornitori si danno la colpa a vicenda. Nomina invece un integratore per il servizio end-to-end e concorda la gestione tra fornitori.
- **Contratti a ambito fisso per lavoro incerto.** Il contratto combatte l'apprendimento. Usa invece accordi che lasciano cambiare l'ambito entro limiti chiari.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Conoscere i fornitori | I fornitori sono noti ai singoli individui | Alcuni team elencano i propri fornitori | Un elenco condiviso con dipendenza, sostituibilità e responsabili | L'elenco è rivisto rispetto a incidenti e cambiamenti | L'elenco è condiviso tra i team e collegato ai servizi |
| Impegni e servizio | I livelli di servizio dei fornitori sono ignoti | I termini dei fornitori chiave sono letti | Gli impegni dei fornitori sono confrontati con le promesse ai clienti | Le prestazioni dei fornitori sono misurate e riviste | Gli impegni sono allineati lungo la catena con revisione congiunta |
| Incidenti e rischio | I problemi dei fornitori si scoprono per caso | Alcuni contatti sono noti | Le vie di escalation sono concordate e provate; i rischi sono registrati | Incidenti e rischi dei fornitori sono monitorati e se ne tiene conto | Gestione degli incidenti e piani di rischio sono congiunti con i fornitori |
| Relazione e uscita | I fornitori sono transazionali | Alcune riunioni con i fornitori | Revisioni regolari con i fornitori critici e brevi note di uscita | Salute della relazione e prontezza all'uscita sono riviste | I fornitori partecipano a pianificazione e miglioramento |

## Checklist

- [ ] Abbiamo un elenco di fornitori e di ciò che ciascuno supporta.
- [ ] I fornitori sono ordinati per dipendenza e sostituibilità.
- [ ] Ogni fornitore importante ha un responsabile nominato.
- [ ] Abbiamo confrontato gli impegni dei fornitori con le nostre promesse ai clienti per i servizi chiave.
- [ ] Contatti e vie di escalation per i fornitori critici sono noti e provati.
- [ ] Le aspettative su sicurezza e protezione dei dati sono nel contratto o concordate per iscritto.
- [ ] Esiste una breve nota di uscita o di fallimento per ogni fornitore critico.
- [ ] Teniamo revisioni regolari con i fornitori critici.
- [ ] Dove contribuiscono più fornitori, qualcuno possiede il risultato end-to-end.
- [ ] L'elenco dei fornitori è rivisto almeno una volta l'anno.

## Prompt per l'IA

**Scopo: costruire un elenco di fornitori e dipendenze da ciò che sai.**

```text
Help me build a supplier and dependency list for [service].

What the service does and what it is built on: [describe components, cloud services, tools, and contractors].
What I know about each: [for example name, what we use it for, who set it up, contract status].

Produce a table with: supplier, what it supports, who owns the relationship (or "unknown"), how critical it seems (critical, important, routine, with a reason from my text), and one question to ask. Mark guesses. Do not invent suppliers or terms. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: confrontare gli impegni dei fornitori con le tue promesse ai clienti.**

```text
Here are the commitments we have made to customers for [service]: [paste, for example availability and response time].
Here are the commitments our suppliers have made, with the exact wording from their terms: [paste for each supplier].

Compare them. For each customer commitment, list which suppliers it depends on, whether their commitments appear to support ours (using only the pasted text), and what gaps there are. Suggest design or agreement changes as questions to consider. Do not interpret legal terms; flag anything ambiguous for legal review. List what you are unsure of.
```

**Scopo: prepararsi a una riunione di revisione con un fornitore.**

```text
Plan a 45-minute review with [supplier] about [service they provide to us].

Data we have: [incidents involving them, response times, requests, with dates; real data only].
Concerns we want to raise: [list].
Things we want to ask about their plans: [list].
Things they may want from us: [list, or write "unknown"].

Give a timed agenda, a one-page summary of our data, five questions for them, three things we should offer, and a closing step that records actions with owners and dates. Do not invent data. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: redigere una breve nota di uscita per un fornitore critico.**

```text
Help me draft an exit note for [supplier], which provides [service].

What we store with or through them, and how we could export it: [describe].
Alternatives we know of: [list, or write "unknown"].
Contract terms about notice and data return, if known (paste the exact text): [paste, or write "not read"].

Write a one-page note with: what depends on them, what we would need to leave (data, configuration, skills), a rough sequence of steps (leave timing as [to be estimated]), risks, and questions to ask the supplier. Do not interpret the contract. Ask clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [vendor-management](../../../../skills/vendor-management/SKILL.md): da usare per pianificare selezione, revisione e relazione con un fornitore.
- [risk-register](../../../../skills/risk-register/SKILL.md): da usare per registrare i rischi dei fornitori e come sono gestiti.
- [stakeholder-analysis](../../../../skills/stakeholder-analysis/SKILL.md): da usare per capire chi nella tua organizzazione e in quella del fornitore conta per la relazione.
- [service-level-agreement](../../../../skills/service-level-agreement/SKILL.md): da usare per verificare che gli impegni dei fornitori sostengano ciò che prometti.
- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): da usare per chiarire chi possiede ogni relazione con un fornitore e chi è consultato.

## Fonti principali

- **Supplier relationship management** (Wikipedia): una panoramica di segmentazione, scorecard e collaborazione con i fornitori, con etichette di manutenzione che mostrano dove le fonti sono deboli.
- **Service integration and management** (Wikipedia): l'approccio multi-fornitore, con i suoi livelli, modelli e difficoltà di implementazione.
- **Service-level agreement** (Wikipedia): contesto sugli accordi che fornitori e clienti firmano.
- **ITIL** (Wikipedia): contesto su come ITIL tratta i fornitori.

## Riferimenti

1. Supplier relationship management — Wikipedia — https://en.wikipedia.org/wiki/Supplier_relationship_management
2. Service integration and management — Wikipedia — https://en.wikipedia.org/wiki/Service_integration_and_management
3. Service-level agreement — Wikipedia — https://en.wikipedia.org/wiki/Service-level_agreement
4. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
5. Outsourcing — Wikipedia — https://en.wikipedia.org/wiki/Outsourcing
6. Vendor lock-in — Wikipedia — https://en.wikipedia.org/wiki/Vendor_lock-in
7. Balanced scorecard — Wikipedia — https://en.wikipedia.org/wiki/Balanced_scorecard
8. Procurement — Wikipedia — https://en.wikipedia.org/wiki/Procurement
9. Manifesto for Agile Software Development — Beck et al., agilemanifesto.org — https://agilemanifesto.org/
