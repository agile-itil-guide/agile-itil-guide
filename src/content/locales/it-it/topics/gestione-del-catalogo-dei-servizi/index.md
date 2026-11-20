# Gestione del catalogo dei servizi

**Un catalogo dei servizi (ITIL lo scrive "service catalogue") è un elenco curato di ciò che un'organizzazione offre, con un responsabile e una descrizione semplice per ogni servizio, e il suo valore dipende dal fatto che gli utenti lo trovino utile e che i responsabili lo mantengano veritiero.**

## Perché è importante

Chiedi a un utente che cosa offre l'IT e spesso otterrai una risposta vaga. Chiedilo al team IT e otterrai un elenco di sistemi. I due elenchi raramente coincidono, e il divario causa malintesi: gli utenti chiedono cose che non esistono, i team supportano servizi che nessuno usa e nessuno sa dire chi è responsabile di che cosa. Un catalogo dei servizi colma quel divario dichiarando, in un solo posto e in termini semplici, che cosa viene offerto e chi risponde.

Per i team agili, il catalogo è anche un modo di rendere visibile la responsabilità. Un team che costruisce e gestisce un servizio dovrebbe poter dire: "questo è ciò che offriamo, questa è la persona a cui chiedere, questo è ciò che puoi aspettarti". Senza di esso, le richieste arrivano al posto sbagliato, gli incidenti rimbalzano tra i team e i nuovi arrivati non trovano aiuto.

L'[articolo di Wikipedia sui cataloghi dei servizi](https://en.wikipedia.org/wiki/Service_catalog) descrive un catalogo dei servizi come una raccolta organizzata e curata di servizi di business e di tecnologia dell'informazione all'interno di un'impresa, che serve da strumento di gestione della conoscenza e designa esperti della materia per ogni servizio elencato. Nota che il volume Service Design di ITIL definisce un catalogo dei servizi IT come un elenco esaustivo di servizi solo IT e l'unica parte del portafoglio dei servizi pubblicata ai clienti, senza specificare l'edizione di ITIL. Questo argomento si basa su quella descrizione e sugli altri argomenti della guida e mantiene il catalogo pratico e leggero.

## Concetti fondamentali

### Che cosa c'è in un catalogo

Secondo Wikipedia, ogni voce di un catalogo dei servizi include tipicamente un responsabile nominato, una descrizione, una categoria, tipi di richiesta correlati, servizi sottostanti, diritti d'uso, costi, come il servizio è richiesto ed evaso e contatti di escalation. Le categorie comuni includono IT, operations ed evasione. Non ti servono tutti per ogni servizio. Un buon catalogo parte dai pochi di cui utenti e personale di supporto hanno davvero bisogno.

| Campo | Perché aiuta | Chi lo usa |
|---|---|---|
| **Nome e descrizione in parole semplici** | Gli utenti riconoscono ciò che viene offerto | Utenti, service desk |
| **Responsabile** | Qualcuno risponde del servizio | Tutti |
| **Chi può usarlo (diritto d'uso)** | Evita richieste sprecate | Utenti, service desk |
| **Come richiedere o ottenere aiuto** | Porta gli utenti al posto giusto | Utenti, service desk |
| **Da che cosa dipende (servizi sottostanti)** | Mostra che cos'altro deve funzionare | Operations, team di delivery |
| **Costo, se addebitato** | Sostiene decisioni e budget | Clienti, finanza |
| **Livello di servizio o aspettativa** | Fissa le aspettative | Utenti, clienti (vedi Argomento 3.7 — Gestione dei livelli di servizio) |
| **Contatto di escalation** | Accelera l'aiuto durante i problemi | Service desk, operations |

### Catalogo e portafoglio

L'articolo di Wikipedia colloca il catalogo dei servizi IT come sottoinsieme del catalogo aziendale più ampio. Nel vocabolario ITIL, il portafoglio dei servizi è l'insieme completo dei servizi, compresi quelli in sviluppo e quelli in dismissione, e il catalogo è la parte pubblicata ai clienti. Le fonti lette qui non definiscono il portafoglio in dettaglio: l'articolo sulla gestione del portafoglio dei servizi rimanda alla gestione del portafoglio IT, che dice solo che ITIL v3 richiede una pratica di gestione del portafoglio dei servizi che appare funzionalmente equivalente alla gestione del portafoglio IT. Considera l'idea di portafoglio così: il catalogo è ciò che offri ora, e il portafoglio è anche ciò che stai costruendo e ritirando (vedi Argomento 5.7 — Governance, rischio e conformità per le scelte di portafoglio).

### Cataloghi aziendali e IT

Un catalogo dei servizi aziendale copre i servizi di più funzioni, come risorse umane, servizi generali e IT. Un catalogo dei servizi IT è un sottoinsieme. L'articolo cita i benefici di un catalogo: centralizzare i servizi in imprese distribuite, individuare lacune e ridondanze nei servizi, tracciare l'allocazione delle risorse e misurare domanda, offerta, tempi di approvazione, tempi di consegna e finanze del servizio. Per i servizi cloud cita l'auto-provisioning e le definizioni standardizzate che aiutano la pianificazione della capacità e le previsioni d'acquisto. Sono affermazioni dell'articolo, basate sulle sue fonti citate.

### Vista di business e vista tecnica

Molte organizzazioni distinguono ciò che i clienti vedono da ciò di cui il fornitore ha bisogno internamente. Le fonti lette qui non fanno la distinzione, quindi consideralo pratica comune. La **vista rivolta al cliente** elenca i servizi nei termini dell'utente ("E-mail e calendario"). La **vista tecnica** elenca i componenti e i team dietro di essi ("Server di posta, filtro antispam, servizio di directory"). La vista del cliente aiuta gli utenti a scegliere. La vista tecnica aiuta le operations a capire le dipendenze (vedi Argomento 4.4 — Gestione della configurazione). Mantieni le due collegate ma separate, così che gli utenti non si trovino davanti nomi di componenti.

### Il catalogo come strumento di conoscenza

L'articolo di Wikipedia sottolinea che il catalogo designa esperti della materia per ogni servizio. Questo ne fa una mappa di chi sa che cosa. Un catalogo mantenuto aggiornato aiuta il service desk a instradare i contatti, aiuta i nuovi arrivati a trovare aiuto e aiuta chi risponde agli incidenti a raggiungere la persona giusta (vedi Argomento 3.9 — Gestione della conoscenza).

### Catalogo e richieste

Il catalogo di solito include le richieste che gli utenti possono fare per ogni servizio, come "richiedere l'accesso" o "segnalare un guasto". Un modello di richiesta descrive come ciascuna viene evasa (vedi Argomento 3.6 — Gestione delle richieste di servizio). Non ogni servizio ha bisogno di richieste, e non ogni richiesta ha bisogno di una voce di catalogo, ma le richieste frequenti dovrebbero essere facili da trovare.

### Mantenerlo veritiero

Un catalogo diventa rapidamente obsoleto se nessuno lo possiede. I servizi cambiano, i team si riorganizzano e le descrizioni si allontanano dalla realtà. La disciplina più utile è un ciclo di revisione: ogni responsabile conferma le proprie voci a scadenza fissa e i servizi inutilizzati vengono ritirati. L'articolo di Wikipedia non discute critiche o limiti, ma l'esperienza pratica è coerente: un catalogo sbagliato è peggio di nessun catalogo, perché manda le persone al posto sbagliato con sicurezza.

### Cataloghi e team agili

I team agili spesso resistono ai cataloghi pesanti perché si aspettano burocrazia. Un catalogo leggero è compatibile con i modi di lavorare agili. Può essere un documento o una pagina condivisa, mantenuta dai responsabili stessi, con pochi campi per servizio. Il test è l'uso: utenti e desk lo consultano davvero?

## Buone pratiche

1. **Elenca i servizi con le parole degli utenti.** Parti chiedendo a utenti e service desk come chiamerebbero ogni cosa. Dai ai servizi il nome di ciò che gli utenti fanno ("Partecipare a una videoriunione") e non della tecnologia ("Piattaforma di conferenza").
2. **Dai a ogni servizio un responsabile nominato.** Una persona dovrebbe rispondere di ogni servizio. Dove un servizio ha più parti, nomina un responsabile dell'insieme ed elenca i contributori.
3. **Parti in piccolo.** Inizia con i 10-20 servizi di cui gli utenti chiedono più spesso. Aggiungi altro man mano che impari che cosa è utile. Un elenco breve e accurato è meglio di uno lungo e obsoleto.
4. **Includi solo ciò che le persone usano.** Per ogni campo, chiedi chi lo usa e per che cosa. Rimuovi i campi che nessuno usa. Aggiungi un campo solo quando qualcuno ne ha bisogno.
5. **Collega a richieste e aiuto.** Per ogni servizio, mostra come chiedere qualcosa, segnalare un guasto e trovare aiuto. Collega alla base di conoscenza (vedi Argomento 3.9 — Gestione della conoscenza).
6. **Mostra le aspettative di servizio.** Indica in termini semplici che cosa gli utenti possono aspettarsi, come orari di supporto e risposta tipica. Collega all'accordo formale dove ce n'è uno.
7. **Registra le dipendenze.** Per ogni servizio, annota i principali servizi e fornitori da cui dipende. Aiuta la risposta agli incidenti e la pianificazione dei cambiamenti.
8. **Separa la vista del cliente dalla vista tecnica.** Mantieni le descrizioni rivolte agli utenti libere da gergo. Collegale ai record tecnici dove esistono.
9. **Rivedi a scadenza fissa.** Chiedi a ogni responsabile di confermare le proprie voci almeno due volte l'anno e ritira i servizi che nessuno usa. Mostra su ogni voce la data dell'ultima revisione.
10. **Rendilo facile da trovare e da usare.** Metti il catalogo dove gli utenti già guardano, come l'intranet o il portale. Verifica la ricerca con query reali.
11. **Usa il catalogo per trovare lacune e sovrapposizioni.** Cerca servizi che nessuno possiede, servizi che si duplicano e richieste senza un servizio corrispondente. Porta i risultati alla pianificazione (vedi Argomento 5.5 — Responsabilità di prodotto e di servizio).
12. **Tratta le modifiche del catalogo come modifiche del servizio.** Quando aggiungi, cambi o ritiri un servizio, annuncialo al desk e agli utenti interessati, come faresti con un rilascio.

## Domande da discutere con il team

**Se un nuovo collega chiedesse che cosa offriamo, che cosa risponderemmo, e diremmo tutti la stessa cosa?**

Chiedi a ciascuno di elencare i servizi in due minuti, poi confronta. Le differenze mostrano quanto siano sfumati i confini. Chi facilita può chiedere quali voci gli utenti non riconoscerebbero. Usa l'elenco combinato come bozza di catalogo e segna le voci su cui c'è disaccordo.

**Quali servizi non hanno un responsabile chiaro?**

Scorri l'elenco e segna quelli per cui nessuno sa dire chi ne risponde. I servizi senza responsabile spesso causano i ritardi più lunghi in incidenti e richieste. Chiedi che cosa impedisce a una persona di assumersi la responsabilità: tempo, autorità o confini poco chiari. Concorda un responsabile o una decisione di ritiro per ciascuno.

**Che cosa chiedono gli utenti che non elenchiamo, e che cosa elenchiamo che nessuno chiede?**

Confronta i dati delle richieste con l'elenco. Le richieste senza un servizio corrispondente rivelano lacune; i servizi elencati senza richieste rivelano candidati al ritiro. Sii cauto: alcuni servizi sono usati in silenzio. Chiedi agli utenti prima di rimuovere. Scegli una lacuna e un candidato da esaminare.

**Che cosa dovrebbe vedere un utente per scegliere il servizio giusto senza chiamarci?**

Prendi una scelta comune, come quale strumento usare per condividere file. Chiedi quali informazioni aiuterebbero: una breve descrizione, a chi è rivolto, un confronto. Redigi una voce di un paragrafo e verificala con due utenti. Lo scopo è un catalogo che evita le chiamate essendo chiaro.

**Come scopriamo quando un servizio è cambiato e il catalogo è obsoleto?**

Chiedi quando c'è stata l'ultima revisione e chi l'ha fatta. Discuti gli inneschi, come una riorganizzazione o un rilascio importante, e un ciclo regolare. Una data "ultima revisione" visibile su ogni voce aiuta. Concorda la data della prima revisione e chi ne è responsabile.

**Da che cosa dipendiamo che non è nel catalogo?**

Elenca le piattaforme e i fornitori dietro i tuoi servizi. Chiedi quali sono elencati e chi li possiede. Le dipendenze senza responsabile sono rischi. Scegline una da aggiungere alla vista tecnica.

## Nella pratica: un esempio di ITIL agile

Un consiglio regionale ha 120 persone nel suo reparto IT al servizio di 2.500 dipendenti del consiglio e di diversi servizi rivolti al pubblico. Il personale si lamenta di non sapere a chi chiedere aiuto e il service desk spende gran parte del tempo a reindirizzare le chiamate. Il consiglio una volta costruì un catalogo dei servizi con 300 voci, ma è usato raramente ed è per lo più obsoleto.

La responsabile della delivery dei servizi decide di ricominciare, in piccolo. Chiede al service desk i 30 motivi più comuni per cui le persone lo contattano e li raggruppa in 15 servizi con parole degli utenti: "E-mail e calendario", "File e condivisione", "Portatili e dispositivi", "Sito web del consiglio", "Sistema finanziario" e così via. Per ciascuno, un responsabile nominato scrive quattro cose: una descrizione di due frasi, a chi è rivolto, come ottenere aiuto e che cosa aspettarsi. Le dipendenze sono registrate in un elenco tecnico separato per le operations. Il catalogo è una singola pagina web sull'intranet del consiglio, e ogni voce mostra la data dell'ultima conferma da parte del suo responsabile.

Dopo tre mesi, le chiamate al desk su a chi rivolgersi calano e i responsabili notano lacune: nessuno possedeva il sistema di prenotazione delle sale riunioni e due servizi si sovrapponevano. Vengono assegnati e fusi. Restano problemi. Tre responsabili non hanno confermato le loro voci e parte del personale chiama ancora il desk per abitudine. La responsabile della delivery dei servizi imposta un ciclo di promemoria e fa in modo che il desk indirizzi i chiamanti al catalogo mentre gestisce la richiesta. Scopre anche che alcune voci sono scritte in linguaggio tecnico e chiede a un addetto alla comunicazione di rivederle.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery dovrebbero essere nominati responsabili dei servizi che costruiscono e gestiscono e dovrebbero mantenere aggiornate le loro voci. Quando lanci o ritiri un servizio, aggiorna il catalogo e informa il service desk. Usa il catalogo per trovare con chi parlare di una dipendenza.

### Team di servizio e di operations

Operations e service desk sono i maggiori utilizzatori. Di' ai responsabili che cosa è sbagliato o manca nelle voci e usa il catalogo per instradamento ed escalation. Mantieni la vista tecnica collegata alla vista del cliente, così che chi risponde agli incidenti possa vedere che cosa dipende da che cosa.

### Leadership e governance

I leader possono usare il catalogo per vedere che cosa l'organizzazione offre, che cosa si sovrappone e che cosa è orfano. Chiedi che lacune e duplicati siano affrontati e che siano nominati i responsabili. Non richiedere ogni campo per ogni servizio; chiedi ciò che sostiene le decisioni.

### Clienti e utenti

Clienti e utenti ottengono una visione chiara di ciò che possono chiedere e di che cosa aspettarsi. Usa il catalogo per trovare il servizio giusto e di' ai responsabili quando una voce è sbagliata o poco chiara. Se non trovi ciò di cui hai bisogno, dillo, perché è prova di una lacuna.

## Modalità di fallimento comuni

- **Troppo grande, troppo presto.** Si creano centinaia di voci e non si mantengono. Parti invece dai servizi più usati e cresci.
- **Scritto nel linguaggio del fornitore.** Gli utenti non trovano ciò che serve. Dai invece ai servizi il nome di ciò che gli utenti fanno e verifica con gli utenti.
- **Nessun responsabile.** Nessuno mantiene veritiere le voci. Nomina invece un responsabile per ogni voce e mostra le date di revisione.
- **Un catalogo che nessuno usa.** Sta su un sito che gli utenti non visitano. Mettilo invece dove le persone già guardano e fai in modo che il desk vi rimandi.
- **Mescolare le viste del cliente e tecnica.** Gli utenti si trovano davanti nomi di componenti. Mantieni invece una vista del cliente chiara e collega una tecnica per le operations.
- **Nessun ritiro.** I servizi morti restano elencati. Rivedi invece l'uso e ritira ciò di cui nessuno ha bisogno.
- **Trattarlo come un progetto una tantum.** Il catalogo diventa obsoleto dopo il lancio. Fissa invece un ciclo di revisione e rendilo parte dei cambiamenti.
- **Troppi campi obbligatori.** I responsabili compilano i campi per soddisfare il modello. Richiedi invece solo ciò che qualcuno usa.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Copertura e chiarezza | I servizi sono noti in modo informale | Esiste un elenco di alcuni servizi | Un catalogo dei servizi principali con parole degli utenti e responsabili | Uso e lacune sono misurati e il catalogo è regolato | Il catalogo copre funzioni e partner ed è plasmato con gli utenti |
| Responsabilità e aggiornamento | Nessuno possiede l'elenco | Alcuni responsabili confermano le voci occasionalmente | Ogni voce ha un responsabile e una data di revisione | Le revisioni in ritardo sono monitorate e risolte | Responsabilità e revisione sono routine in tutta l'organizzazione |
| Legame con richieste e aiuto | Le richieste vanno per e-mail o telefono | Alcune voci rimandano a moduli o aiuto | Le voci rimandano a richieste, conoscenza e vie di supporto | Click-through e deviazione sono misurati | Richieste, conoscenza e supporto sono integrati tra le funzioni |
| Dipendenze e decisioni | Le dipendenze sono conoscenza tribale | Alcune dipendenze sono elencate | Le dipendenze sono registrate e usate nel lavoro su incidenti e cambiamenti | I dati sulle dipendenze sostengono pianificazione e revisione dei rischi | Le dipendenze sono condivise con i fornitori e usate per pianificare insieme |

## Checklist

- [ ] Abbiamo un elenco di servizi con le parole degli utenti, partendo dai più usati.
- [ ] Ogni servizio ha un responsabile nominato.
- [ ] Ogni voce dice a chi è rivolta, come ottenere aiuto e che cosa aspettarsi.
- [ ] Il catalogo è dove utenti e service desk già guardano.
- [ ] Le voci mostrano la data dell'ultima conferma.
- [ ] I responsabili rivedono le proprie voci almeno due volte l'anno.
- [ ] Le dipendenze principali sono registrate in una vista tecnica.
- [ ] I servizi inutilizzati sono rivisti per il ritiro.
- [ ] Aggiungere, cambiare o ritirare un servizio è annunciato a desk e utenti.
- [ ] Abbiamo verificato il catalogo con query reali degli utenti.

## Prompt per l'IA

**Scopo: trasformare i dati dei contatti in una bozza di elenco di servizi con le parole degli utenti.**

```text
Below are the reasons people contacted our service desk in the last [period]: [paste short, anonymized descriptions or category counts].

Group them into 10 to 20 candidate services, each named in plain words that a non-technical user would recognize, such as "Email and calendar." For each, give a two-sentence description based only on the contacts, the contacts that fit under it, and a question to ask its owner. List contacts that do not fit. Do not invent services or systems that do not appear in the data. Ask clarifying questions first if the data is thin, and list what you are unsure of.
```

**Scopo: scrivere una voce di catalogo chiara.**

```text
Help me write a service catalog entry for [service].

What it does, in my own words: [describe].
Who may use it: [describe].
How users get help or make requests: [describe].
Support hours and what users can expect: [describe, or write "unknown"].
Main things it depends on: [list].
Owner: [role].

Write a short entry for users (no jargon, under 80 words) and a separate technical note for operations. Mark anything you added as an assumption. Do not invent service levels or contacts. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: rivedere un catalogo per lacune, sovrapposizioni e orfani.**

```text
Here is our service catalog (names, owners, descriptions, and last review dates): [paste].
Here is data on what users request or report: [paste counts by topic, or write "none"].

Using only this text, list: services with no owner or an overdue review; pairs of services that seem to overlap; request topics with no matching service; and services with no requests in the data. For each, suggest a question for the owner or the desk rather than a conclusion. Do not guess about services not listed. List what you are unsure of.
```

**Scopo: pianificare una revisione del catalogo con i responsabili.**

```text
Plan a 60-minute review of our service catalog with [number] service owners.

State of the catalog: [describe, such as number of entries and how old they are].
Problems we know of: [list].

Give a timed agenda that has each owner confirm or correct their entries, look at overlaps and gaps, decide what to retire, and agree a review date. Include a one-page template for owners to prepare. Keep it free of any particular tool. Ask clarifying questions first if information is missing, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [service-catalog](../../../../skills/service-catalog/SKILL.md): da usare per redigere voci e strutturare un catalogo dei servizi.
- [stakeholder-analysis](../../../../skills/stakeholder-analysis/SKILL.md): da usare per capire chi usa ogni servizio e di che cosa ha bisogno.
- [demand-analysis](../../../../skills/demand-analysis/SKILL.md): da usare per trovare quali richieste e servizi sono più usati.
- [raci-matrix](../../../../skills/raci-matrix/SKILL.md): da usare per registrare chi possiede, supporta e viene consultato su ogni servizio.
- [product-roadmap](../../../../skills/product-roadmap/SKILL.md): da usare per pianificare come i servizi saranno aggiunti, cambiati o ritirati nel tempo.

## Fonti principali

- **Service catalog** (Wikipedia): una breve descrizione di contenuti, benefici e definizione ITIL di un catalogo dei servizi IT.
- **IT portfolio management** (Wikipedia): contesto sui concetti di portafoglio, compresa la nota che la gestione del portafoglio dei servizi di ITIL v3 appare funzionalmente equivalente.
- **ITIL** (Wikipedia): contesto sulle versioni di ITIL e su da dove vengono le idee di catalogo e portafoglio.
- **Knowledge management** (Wikipedia): contesto su come i cataloghi agiscono come strumenti di conoscenza.

## Riferimenti

1. Service catalog — Wikipedia — https://en.wikipedia.org/wiki/Service_catalog
2. IT portfolio management — Wikipedia — https://en.wikipedia.org/wiki/IT_portfolio_management
3. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
4. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
5. Knowledge management — Wikipedia — https://en.wikipedia.org/wiki/Knowledge_management
6. Enterprise service management — Wikipedia — https://en.wikipedia.org/wiki/Enterprise_service_management
7. Help desk — Wikipedia — https://en.wikipedia.org/wiki/Help_desk
8. Service-level agreement — Wikipedia — https://en.wikipedia.org/wiki/Service-level_agreement
