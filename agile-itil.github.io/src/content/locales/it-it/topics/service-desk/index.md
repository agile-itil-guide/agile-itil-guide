# Service desk

**Il service desk è il luogo in cui utenti e fornitore del servizio si incontrano, e in un'organizzazione agile il suo prodotto più prezioso non sono i ticket chiusi ma ciò che impara su come gli utenti vivono il servizio.**

## Perché è importante

Per la maggior parte degli utenti, il service desk è il servizio. Raramente vedono gli ingegneri, l'architettura o la pipeline; vedono la persona che risponde quando qualcosa va storto. Come va quella conversazione plasma la loro fiducia in tutto ciò che sta dietro. Un desk cordiale e competente può attenuare una brutta interruzione, e uno sprezzante può guastare un buon servizio.

Il desk è anche il miglior sensore che un'organizzazione abbia. Ogni contatto è un piccolo indizio su ciò che gli utenti trovano confuso, su ciò che si rompe e su ciò che vorrebbero che il servizio facesse. I team agili che rilasciano spesso hanno bisogno di quelle prove in fretta. Un desk isolato dai team di delivery produce ticket, e un desk collegato produce miglioramenti.

L'[articolo di Wikipedia sulla gestione dei servizi IT](https://en.wikipedia.org/wiki/IT_service_management) descrive il service desk come un unico punto di contatto tra fornitori e utenti o clienti, che gestisce incidenti e richieste di servizio. L'[articolo di Wikipedia sugli help desk](https://en.wikipedia.org/wiki/Help_desk) è breve: copre la definizione, la gestione delle code e l'instradamento delle chiamate e non dice nulla su storia, livelli di supporto, metriche o differenza tra help desk e service desk. Questo argomento attinge quindi a quei due articoli per le definizioni, e il resto è una guida pratica offerta come tale, non come risultati consolidati.

## Concetti fondamentali

### Che cos'è un service desk

Un **help desk**, secondo Wikipedia, è un reparto o una persona che dà assistenza e informazioni, di solito per problemi elettronici o informatici. Un **service desk**, nell'uso ITSM, è più ampio: l'unico punto di contatto per utenti e clienti, che gestisce sia incidenti (interruzioni o potenziali interruzioni di un servizio) sia richieste di servizio (richieste di routine per qualcosa che il servizio normalmente fornisce). L'articolo sull'help desk elenca "service desk" solo come argomento correlato, quindi il confine esatto tra i due termini non è dato lì. Molte organizzazioni usano le parole in modo intercambiabile; ciò che conta è che cosa ci si aspetta dal tuo desk.

### Utenti e clienti

L'articolo sull'ITSM distingue gli utenti, che usano il servizio, dai clienti, che lo pagano o lo commissionano. Un desk sente soprattutto gli utenti. Dovrebbe anche sapere chi sono i clienti, perché decidono priorità e finanziamenti. Un buon desk sa parlare a entrambi.

### Code e instradamento

Wikipedia dice che i grandi help desk hanno una persona o un team che gestisce le richieste in arrivo, spesso chiamati queue manager o queue supervisor, che assegnano ogni problema a un team specializzato per tipo. Alcuni desk usano sistemi telefonici con distribuzione automatica delle chiamate che instradano le chiamate su argomenti specifici ad analisti con l'esperienza giusta. L'instradamento è lo strumento principale del desk per far corrispondere il problema alla persona che può risolverlo.

### Livelli di supporto

Molti desk organizzano il supporto in livelli, spesso chiamati tier. Le fonti lette per questa guida non descrivono i tier, quindi quanto segue è una pratica comune descritta in termini generali, non un'affermazione di una fonte:

| Livello | Ruolo tipico |
|---|---|
| Primo livello | Riceve i contatti, li registra, risolve i problemi comuni usando conoscenza documentata e instrada il resto |
| Secondo livello | Gestisce i problemi più difficili che richiedono competenze tecniche più profonde |
| Terzo livello | Specialisti, spesso gli ingegneri che costruiscono il servizio, che correggono i guasti di fondo |

Il modello ha una debolezza nota: può rendere ogni livello un luogo in cui il lavoro aspetta. I team agili spesso cercano di accorciare il percorso in modo che un analista del desk possa raggiungere direttamente un ingegnere (vedi Argomento 3.2 — Gestione degli incidenti).

### Canali

I contatti arrivano per telefono, e-mail, chat, portale web o di persona. Ogni canale si adatta a utenti e problemi diversi. Un portale può rendere le richieste strutturate e rapide. Una linea telefonica si addice a un'interruzione urgente. Offrire più canali è un bene, purché tutti alimentino lo stesso record, così che la domanda sia visibile in un unico posto (vedi Argomento 2.1 — Gestione dei servizi IT sull'unica porta d'ingresso).

### Self-service e conoscenza

Molti desk offrono il self-service: un portale in cui gli utenti possono trovare risposte e fare richieste di routine senza parlare con nessuno. Le fonti lette non descrivono il self-service, ma si collega a due pratiche di questa guida: una buona base di conoscenza (vedi Argomento 3.9 — Gestione della conoscenza) e un elenco chiaro dei servizi (vedi Argomento 3.8 — Gestione del catalogo dei servizi).

### Il desk come fonte di prove

Ciò che un desk registra può essere prezioso per l'intera organizzazione: le domande più comuni, i guasti più comuni, quanto tempo richiedono le cose e che cosa dicono gli utenti. Queste prove aiutano i team di delivery a decidere che cosa correggere, aiutano la gestione dei problemi a trovare le cause (vedi Argomento 3.3 — Gestione dei problemi) e aiutano la gestione dei livelli di servizio a concordare obiettivi realistici (vedi Argomento 3.7 — Gestione dei livelli di servizio). Un desk che registra solo quanto basta a chiudere i ticket lo spreca.

### Misure

I desk sono spesso giudicati dai conteggi: contatti gestiti, tempo di risposta, tempo di chiusura. I conteggi sono facili da raccogliere e facili da usare male. Il tempo di chiusura si può manipolare chiudendo presto i ticket, e i conteggi dei contatti possono premiare la gestione dei problemi ripetuti invece della loro eliminazione. Misure migliori includono la soddisfazione degli utenti, quanto spesso un contatto è risolto al primo tocco e se i contatti ripetuti sullo stesso problema calano nel tempo. Tratta qualsiasi misura come stimolo per una domanda e concorda che cosa ne farai (vedi Argomento 5.6 — Metriche e misurazione).

### Critiche e limiti

Gli articoli di Wikipedia letti per questa guida non nominano critiche agli help desk o ai service desk. I professionisti sollevano comunemente alcune preoccupazioni note: che i desk siano trattati come un costo da minimizzare, che i copioni sostituiscano il giudizio, che chi risponde non abbia il potere di correggere nulla e che il turnover sia alto. Sono ampiamente discusse ma sono presentate qui come preoccupazioni comuni, non come risultati delle fonti.

## Buone pratiche

1. **Dai al desk uno scopo chiaro.** Scrivi a che cosa serve il desk: chi serve, che cosa gestisce e che cosa passa ad altri. Un desk senza uno scopo dichiarato scivola nel gestire qualunque cosa arrivi.
2. **Offri pochi buoni canali che alimentano un unico record.** Scegli i canali che i tuoi utenti preferiscono e assicurati che ciascuno crei un record nello stesso posto. I canali nascosti, come i messaggi personali agli ingegneri, nascondono la domanda.
3. **Separa incidenti, richieste e domande.** Usa categorie semplici ed esempi, così che gli analisti classifichino in modo coerente. La separazione conta per la priorità e per il reporting (vedi Argomento 3.6 — Gestione delle richieste di servizio).
4. **Metti la conoscenza davanti all'analista.** Fornisci indicazioni brevi e ricercabili per i problemi più comuni e aggiornale quando la risposta cambia. Chiedi agli analisti quali articoli usano e quali sono sbagliati.
5. **Lascia che il desk risolva ciò che può.** Dove è sicuro, dai agli analisti autorità e strumenti per risolvere i problemi comuni, come il reset delle password e la concessione degli accessi. Ogni escalation non necessaria costa tempo all'utente.
6. **Crea una linea diretta con gli ingegneri.** Rendi facile per gli analisti chiedere a un team di delivery di un nuovo guasto e per il team informare il desk di un rilascio. Un canale condiviso e un referente nominato bastano per iniziare.
7. **Informa il desk dei cambiamenti prima che gli utenti li sentano.** Condividi in anticipo con il desk le note di rilascio e i problemi noti (vedi Argomento 3.5 — Gestione di rilasci e deployment). Le sorprese fanno sembrare il desk disinformato.
8. **Registra abbastanza per imparare, e non di più.** Cattura la categoria, il servizio interessato, che cosa è successo e come è stato risolto. Rivedi regolarmente i campi e rimuovi quelli che nessuno usa.
9. **Rivedi i contatti per temi.** Una volta al mese, raggruppa i contatti recenti per causa e guarda i primi. Condividi i temi con i team di delivery e la gestione dei problemi.
10. **Chiedi agli utenti com'è andata.** Usa una breve domanda dopo un contatto, per esempio se il problema è stato risolto. Leggi i commenti. Combina con altre prove, perché un punteggio di soddisfazione da solo è facile da fraintendere.
11. **Prenditi cura delle persone.** Offri formazione, varietà e un percorso verso altri ruoli. Un desk è buono quanto le persone che lo gestiscono, e un alto turnover è un costo che non compare nei conteggi dei ticket.
12. **Tratta il desk come parte della delivery.** Includi un rappresentante del desk nelle sprint review e nella pianificazione e tratta il feedback del desk come input per il backlog (vedi Argomento 5.1 — Gestione agile dei servizi).

## Domande da discutere con il team

**Che cosa vive un utente quando ci contatta, dal primo momento alla risposta?**

Ripercorri un contatto tipico dal punto di vista dell'utente. Annota come trova il desk, che cosa gli viene chiesto, quanto aspetta e che cosa sente. Se possibile, chiedi a qualche utente. Lo scopo è vedere il servizio dall'esterno. Chi facilita può chiedere dove l'utente ha più probabilità di sentirsi ignorato. Prosegui scegliendo un passaggio da migliorare.

**Che cosa sentiamo più spesso, e che cosa è stato fatto al riguardo?**

Elenca i cinque motivi di contatto più comuni dell'ultimo mese. Accanto a ciascuno, scrivi che cosa, se qualcosa, è stato fatto per ridurlo. Un divario mostra dove le prove del desk non raggiungono nessuno che possa agire. Chiedi chi dovrebbe ricevere l'elenco e con quale frequenza. Concorda di inviare il primo questo mese.

**Dove un analista non può risolvere qualcosa che potrebbe con lo strumento, l'accesso o la conoscenza giusti?**

Chiedi agli analisti esempi di escalation che sono sembrate inutili. Le risposte tipiche includono accessi che non hanno, conoscenza superata e paura di sbagliare. Tratta le risposte come un elenco di miglioramenti. Chiedi quali si possono fare ora in sicurezza e quali garanzie aiuterebbero per il resto.

**Come veniamo a sapere dei cambiamenti che riguardano gli utenti, e con quanto anticipo?**

Guarda gli ultimi rilasci o interruzioni e chiedi quando il desk l'ha saputo. Le informazioni tardive sono comuni. Chiedi quale canale funzionerebbe: un feed condiviso, un breve briefing, un referente nominato. I team di delivery dovrebbero essere nella stanza. Concorda una regola semplice, come nessun rilascio senza una nota al desk.

**Quali delle nostre misure ci aiutano a migliorare, e quali ci limitiamo a riferire?**

Elenca le misure che il desk produce e chiedi chi usa ciascuna. Le misure che nessuno usa sono candidate alla rimozione. Chiedi quale misura le persone temono e perché. Se gli analisti manipolano una misura, deve cambiare. Scegli una misura da sostituire o aggiungere che mostri se gli utenti stanno meglio.

**Come manteniamo le persone che lavorano qui, e che cosa dicono di aver bisogno?**

Chiedi agli analisti che cosa renderebbe migliore il lavoro e che cosa li farebbe andare via. Le risposte comuni sono varietà, formazione, riconoscimento e un modo di crescere. Non promettere ciò che non puoi mantenere; impegnati però a un cambiamento visibile. Chi facilita dovrebbe trattare il turnover come un rischio per il servizio e non solo come una questione di personale.

## Nella pratica: un esempio di ITIL agile

Il service desk IT interno di un'agenzia fiscale nazionale supporta circa 9.000 dipendenti con un team di 25 analisti. I contatti arrivano per telefono, e-mail e portale. Il personale si lamenta di dover spiegare più volte il proprio problema, e i team di delivery si lamentano di sentire parlare dei guasti solo quando un dirigente arrabbiato telefona.

Il responsabile del desk incontra i responsabili di tre team di delivery e propone tre cambiamenti. Primo, un canale chat condiviso collega analisti e team di delivery, con la regola che la prima risposta è attesa entro un'ora lavorativa. Secondo, ogni rilascio ottiene una breve nota al desk prima del deployment, scritta dal team di delivery con un modello di una pagina. Terzo, il desk produce un elenco mensile dei dieci motivi di contatto più comuni e lo condivide con tutti i team di delivery, che si impegnano a guardare i primi tre.

Dopo tre mesi, desk e team di delivery riferiscono che diversi guasti ripetuti sono stati corretti, e gli analisti dicono di sentirsi meglio informati. Restano alcune difficoltà. Il canale condiviso è diventato rumoroso e alcuni analisti lo ignorano, le note di rilascio sono in ritardo nei giorni intensi e un team di delivery non ha risposto affatto all'elenco mensile. Il responsabile del desk chiede ai team di delivery di nominare una persona che sorvegli il canale, sposta le note di rilascio tardive nella checklist del rilascio e solleva il silenzio del team che non risponde con il responsabile IT, che chiede al responsabile del team di partecipare alla prossima revisione mensile.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery dovrebbero trattare il service desk come un collega e come un cliente. Di' al desk che cosa sta cambiando e che cosa aspettarsi. Leggi i suoi temi mensili e porta i principali nel backlog. Invita un analista alle revisioni, così che le persone che sentono gli utenti ogni giorno informino i passi successivi.

### Team di servizio e di operations

I team operativi gestiscono il desk o lavorano a stretto contatto con esso. Dai agli analisti la conoscenza e l'autorità per risolvere i problemi comuni e rendi l'escalation rapida e rispettosa. Usa le prove del desk nella gestione dei problemi e nella pianificazione della capacità e proteggi le persone dall'essere trattate come una fabbrica di ticket.

### Leadership e governance

I leader decidono se il desk è un costo da minimizzare o una fonte di conoscenza. Chiedi temi e risultati, non solo volumi. Proteggi formazione e percorsi di carriera. Sii cauto con obiettivi che premiano la chiusura rapida o il dirottamento dei contatti, che abbassano la qualità migliorando i numeri.

### Clienti e utenti

Clienti e utenti traggono vantaggio da un desk facile da raggiungere, che capisce il problema e li tiene informati. Descrivi chiaramente il problema, di' che cosa stavi facendo e comunica al desk quale risultato ti serve. Dai un feedback dopo un contatto, perché è uno dei pochi segnali che raggiungono il team.

## Modalità di fallimento comuni

- **Trattare il desk solo come centro di costo.** Il desk ha personale minimo ed è valutato sul volume. Misura invece i risultati e investi nelle competenze e negli strumenti del desk.
- **Canali nascosti.** Gli utenti aggirano il desk scrivendo agli ingegneri. Rendi invece facili i canali ufficiali e instrada le richieste informali nel record.
- **Escalation per impostazione predefinita.** Gli analisti passano tutto ad altri per evitare colpe. Forma, equipaggia e fidati invece degli analisti per risolvere ciò che possono.
- **Conoscenza obsoleta.** Gli articoli descrivono sistemi cambiati. Assegna invece responsabili e date di revisione e chiedi agli analisti quali articoli li deludono.
- **Il desk lo scopre per ultimo.** Rilasci e interruzioni lo sorprendono. Rendi invece il briefing al desk parte della checklist del rilascio.
- **Metriche che invitano alla manipolazione.** Il tempo di chiusura spinge a chiudere presto. Abbina invece una misura di velocità a una di qualità e osserva gli schemi.
- **Nessun feedback alla delivery.** Le prove del desk non vanno da nessuna parte. Condividi invece i temi mensili e aspettati una risposta.
- **Ignorare le persone.** Alto turnover e basso morale sono accettati. Offri invece formazione, varietà e percorsi verso altri ruoli.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Gestione dei contatti | I contatti arrivano per molte vie informali | Esiste un desk con alcuni canali condivisi | Un'unica porta d'ingresso con categorie e instradamento concordati | Gestione e risultati sono misurati e rivisti | La gestione dei contatti è coordinata tra team e fornitori |
| Conoscenza e strumenti | Le risposte vivono nella testa delle persone | Esistono alcune indicazioni | Conoscenza mantenuta e strumenti comuni sostengono la risoluzione al primo livello | Uso e accuratezza della conoscenza sono monitorati | Conoscenza e strumenti sono condivisi con utenti, team di delivery e fornitori |
| Legame con la delivery | Il desk apprende dei cambiamenti dagli utenti | Alcuni team di delivery informano il desk | I rilasci includono una nota al desk e un referente nominato | Il flusso di informazioni è misurato e le lacune colmate | Desk e team di delivery pianificano e rivedono insieme |
| Imparare dai contatti | I contatti sono chiusi e dimenticati | Si notano alcuni temi | I temi mensili sono condivisi e tracciati | I temi portano a correzioni pianificate il cui effetto è verificato | I temi alimentano la pianificazione tra servizi e con i clienti |

## Checklist

- [ ] Il desk ha uno scopo scritto che dice chi serve e che cosa gestisce.
- [ ] Tutti i canali creano un record in un unico posto.
- [ ] Incidenti, richieste e domande sono classificati in modo coerente.
- [ ] Gli analisti hanno indicazioni ricercabili per i problemi più comuni, con responsabili e date di revisione.
- [ ] Gli analisti possono risolvere i problemi comuni senza escalation.
- [ ] Esiste una via diretta tra analisti e team di delivery.
- [ ] Il desk è informato dei rilasci e dei problemi noti prima che gli utenti li sentano.
- [ ] I temi mensili sono condivisi con i team di delivery e la gestione dei problemi.
- [ ] Agli utenti viene chiesto brevemente com'è andato un contatto.
- [ ] Esistono formazione e percorsi di carriera per il personale del desk.

## Prompt per l'IA

**Scopo: trovare temi in un mese di contatti.**

```text
Below is a list of contacts to our service desk from the last [period]: [paste short, anonymized descriptions, one per line; remove names and personal data first].

Group them into themes based only on what is written. For each theme, give a name, the number of contacts in my list, one example, and one question that delivery teams or problem management could ask. Highlight the top three themes by count from my list. Mark contacts you could not classify. Do not invent categories beyond the text or estimate counts for contacts I did not provide. List what you are unsure of.
```

**Scopo: scrivere una nota di rilascio di una pagina per il service desk.**

```text
Help me write a one-page release note for a service desk about this change.

What changed (plain words): [describe].
Who is affected and when: [describe].
What users might ask or report: [list, or write "unknown"].
Known issues and workarounds: [list, or write "none known"].
How to roll back or who to call: [describe].

Write the note in short sections: what changed, what users will notice, what to tell users, what to do if it goes wrong, and who to contact. Use only my information. Mark assumptions as such, ask clarifying questions first if information is missing, and list what you are unsure of.
```

**Scopo: migliorare un articolo di conoscenza usato dagli analisti.**

```text
Here is a knowledge article that service desk analysts use: [paste it].
Here is what analysts say is wrong or missing: [paste their comments, or write "none yet"].

Rewrite it so that a first-line analyst can follow it in under two minutes: a one-line symptom, steps to check, the fix, when to escalate and to whom, and the date and owner of the article. Do not add technical facts that are not in the article or the comments. Mark any step you are unsure of with [CHECK], and list what you are unsure of.
```

**Scopo: pianificare una conversazione tra il service desk e un team di delivery.**

```text
Plan a 45-minute conversation between a service desk of [number] analysts and a delivery team of [number] people.

Recent frictions: [describe in a few sentences].
What each side says it needs: [describe, or write "unknown"].

Give a timed agenda, five questions for each side, and a closing step that records one agreed change with an owner and a date. Keep it free of any particular tool. Ask clarifying questions first if information is missing, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [service-catalog](../../../../skills/service-catalog/SKILL.md): da usare per dare al desk un elenco chiaro dei servizi che supporta e delle richieste che gestisce.
- [runbook](../../../../skills/runbook/SKILL.md): da usare per trasformare le correzioni comuni in procedure brevi che gli analisti di primo livello possano seguire.
- [getting-feedback](../../../../skills/getting-feedback/SKILL.md): da usare per progettare come il desk chiede feedback agli utenti.
- [survey-design](../../../../skills/survey-design/SKILL.md): da usare per progettare una breve indagine di soddisfazione che produca risposte utilizzabili.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): da usare per capire volume e tipi di contatti e pianificare il personale.

## Fonti principali

- **IT service management** (Wikipedia): la definizione del service desk come unico punto di contatto, con incidenti e richieste di servizio.
- **Help desk** (Wikipedia): una breve panoramica della definizione di help desk, della gestione delle code e dell'instradamento delle chiamate.
- **Technical support** (Wikipedia): contesto sul campo più ampio del supporto a cui appartengono gli help desk.
- **ITIL** (Wikipedia): contesto su come la pratica del service desk si colloca in ITIL.

## Riferimenti

1. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
2. Help desk — Wikipedia — https://en.wikipedia.org/wiki/Help_desk
3. Technical support — Wikipedia — https://en.wikipedia.org/wiki/Technical_support
4. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
5. Customer service — Wikipedia — https://en.wikipedia.org/wiki/Customer_service
6. Issue tracking system — Wikipedia — https://en.wikipedia.org/wiki/Issue_tracking_system
7. Knowledge base — Wikipedia — https://en.wikipedia.org/wiki/Knowledge_base
8. Call centre — Wikipedia — https://en.wikipedia.org/wiki/Call_centre
