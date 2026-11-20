# Gestione della continuità del servizio

**La gestione della continuità del servizio prepara un'organizzazione a mantenere in funzione i propri servizi più importanti, o a ripristinarli rapidamente, dopo una grave interruzione, e il suo valore si dimostra solo con le esercitazioni, non con il piano sullo scaffale.**

## Perché è importante

La maggior parte degli incidenti è piccola e locale. Alcuni no: l'incendio di un data center, la caduta di una regione cloud, un attacco ransomware, il crollo di un fornitore, una pandemia, un'alluvione. Questi eventi minacciano la capacità stessa dell'organizzazione di erogare e gestirli richiede una pianificazione che la normale gestione degli incidenti non copre. Un team che ha ragionato in anticipo su che cosa conta di più e su come andrà avanti ha molte più probabilità di cavarsela.

I team agili affrontano questo tema con una sfida particolare. I loro sistemi cambiano ogni settimana, quindi un piano di continuità scritto una volta e archiviato è obsoleto nel giro di pochi mesi. I passaggi di ripristino che dipendevano da un particolare server o script possono non essere più validi. La risposta agile non è rinunciare alla pianificazione ma fare della continuità una parte viva del modo in cui i servizi sono costruiti e gestiti: ripristino progettato fin dall'inizio, testato spesso e tenuto sotto controllo di versione insieme al codice.

L'[articolo di Wikipedia sulla pianificazione della continuità operativa](https://en.wikipedia.org/wiki/Business_continuity_planning) definisce la continuità operativa come la capacità di un'organizzazione di continuare a erogare prodotti o servizi a livelli accettabili dopo un'interruzione e tratta la pianificazione della continuità come un sottoinsieme della gestione del rischio. La pagina "Disaster recovery" della Wikipedia inglese è solo una pagina di disambiguazione, con un avviso che si desidera un articolo completo, quindi questo argomento usa l'articolo sulla continuità operativa per le definizioni e aggiunge indicazioni pratiche dagli altri argomenti della guida, annotando dove si tratta di pratica e non di materiale di fonte riportato.

## Concetti fondamentali

### Continuità, ripristino e resilienza

I termini sono usati con larghezza, quindi usali con cura:

| Termine | Significato, come ampiamente usato | Focus |
|---|---|---|
| **Continuità operativa** | La capacità di continuare a erogare prodotti o servizi a livelli accettabili dopo un'interruzione | Mantenere in funzione l'organizzazione |
| **Pianificazione della continuità operativa** | Creare sistemi di prevenzione e ripristino per le minacce all'organizzazione | I piani e gli accordi |
| **Disaster recovery IT** | Mantenere o ristabilire l'infrastruttura di tecnologia dell'informazione vitale (la descrizione data sulla pagina di disambiguazione di Wikipedia) | La tecnologia |
| **Continuità del servizio (ITSM)** | Assicurare che i servizi IT possano essere ripristinati ai livelli concordati dopo un'interruzione | I servizi IT all'interno del piano più ampio |

L'articolo di Wikipedia dice che il disaster recovery si sovrappone alla pianificazione della continuità operativa, in particolare nella fase di soluzione, e che la continuità è l'esito inteso dall'esecuzione di entrambi. La gestione della continuità del servizio è la visione dei servizi IT dello stesso scopo.

### Analisi dell'impatto sul business

Una **business impact analysis (BIA)** è, secondo l'articolo, un metodo per individuare e valutare come le interruzioni influiscono sulle operazioni e per fissare le priorità di ripristino. I suoi obiettivi includono individuare attività e dipendenze critiche, valutare impatti finanziari, operativi, reputazionali e legali, determinare gli obiettivi di ripristino e informare la valutazione del rischio. Per i servizi IT, la BIA chiede di quali servizi l'organizzazione non può fare a meno, in quale ordine devono tornare e da che cosa dipende ciascuno (vedi Argomento 4.4 — Gestione della configurazione per le dipendenze).

### Obiettivi di ripristino

L'articolo definisce due termini chiave:

- **Recovery time objective (RTO):** il tempo accettabile per ripristinare una funzione.
- **Recovery point objective (RPO):** la quantità accettabile di latenza dei dati, in altre parole quanta perdita di dati è tollerabile.

Elenca anche il periodo massimo tollerabile di interruzione. L'articolo non dà un metodo per scegliere questi valori per una particolare organizzazione, quindi devono venire dal business: chiedi quanto costano un'ora, un giorno e una settimana di interruzione e quali dati il business può permettersi di perdere. Fissarli è una decisione di business con un prezzo, perché il costo di soddisfare un obiettivo più stretto sale (vedi Argomento 3.11 — Disponibilità, capacità e prestazioni).

### Piani

Un piano di continuità o di ripristino descrive chi fa che cosa, in che ordine, per ripristinare i servizi critici dopo un'interruzione. Dovrebbe coprire: come il piano è invocato e da chi, come le persone sono informate e riunite, la sequenza di ripristino dei servizi, dove avverrà il ripristino, da dove vengono i dati, come comunicare con clienti e personale e come tornare alla normalità. I piani per i servizi IT dovrebbero rimandare ai runbook dei singoli sistemi (vedi Argomento 3.9 — Gestione della conoscenza).

### Test ed esercitazioni

L'articolo cita un libro del 2008 della British Standards Institution che descrive tre tipi di esercitazione: una esercitazione **tabletop** in cui un piccolo gruppo discute un aspetto del piano, una esercitazione **media** in cui più team lavorano su più aspetti con sorprese programmate e una esercitazione **complessa** che aggiunge attivazione senza preavviso, evacuazione reale e uso di un sito di disaster recovery. Descrive la manutenzione con un ciclo annuale o biennale, che include il test di soluzioni tecniche e procedure di ripristino, con i risultati che tornano alla fase di analisi. Le esercitazioni sono il posto in cui i piani scoprono di essere sbagliati.

### Livelli di ripristino

L'articolo menziona i sette livelli di disaster recovery di SHARE (1992), poi aggiornati da IBM a otto livelli (da 0 a 7). Le fonti lette qui non ne dettagliano i livelli. Come pratica generale, le organizzazioni classificano i servizi in livelli in base a quanto in fretta devono essere ripristinati e adeguano l'approccio di ripristino e il costo al livello.

### Standard

L'articolo cita ISO 22301:2019, *Security and resilience, Business continuity management systems, Requirements*, che ha sostituito l'edizione 2012 e richiede alle organizzazioni di definire obiettivi di continuità, livelli minimi di servizio accettabili e un periodo massimo tollerabile di interruzione. ISO 22313:2020 dà indicazioni per usarla. Sono standard per un sistema di gestione che un'organizzazione può adottare; non sostituiscono la pianificazione pratica. Controlla direttamente il testo dello standard se i tuoi clienti o le autorità di vigilanza richiedono la conformità.

### Continuità agile

Le pratiche agili e DevOps aiutano la continuità:

- **Infrastruttura e configurazione come codice** permettono di ricostruire gli ambienti dal controllo di versione, il che rende il ripristino più rapido e testabile.
- **Pipeline automatizzate** possono reinstallare i servizi su un sito di ripristino.
- **Rilasci frequenti** tengono il team allenato a installare.
- **Esercitazioni regolari** possono essere trattate come una forma di test nel backlog.

Creano anche rischi: forte dipendenza da un singolo account cloud, un sistema CI che è esso stesso un singolo punto di guasto e segreti conservati dove non si possono raggiungere in un disastro. Pianifica per gli strumenti da cui dipende il ripristino stesso.

### Fattori umani

L'articolo menziona l'epidemia di SARS del 2002–2003 come esempio di team compartimentati e ruotati, un promemoria che la continuità include le persone: competenze chiave distribuite tra gli individui, lavoro da remoto, comunicazione quando i canali normali falliscono e attenzione al personale sotto stress.

### Limiti delle fonti

L'articolo non dà un metodo per fissare gli obiettivi, né indicazioni su quanto spesso testare oltre il ciclo di manutenzione annuale o biennale, né raccomandazioni di strumenti. È un articolo generale di business, non IT. Per i dettagli tecnici di ripristino, usa la documentazione delle tue piattaforme e le competenze della guida sulla pianificazione e sul test del disaster recovery.

## Buone pratiche

1. **Parti da una analisi dell'impatto sul business.** Individua i servizi di cui l'organizzazione non può fare a meno, il costo della loro perdita nel tempo e da che cosa dipendono. Falla con i responsabili di business, non per loro.
2. **Fissa gli obiettivi di ripristino con il business.** Per ogni servizio critico, concorda un tempo di ripristino e un punto di ripristino e registra il costo per rispettarli. Rivedili quando cambiano il business o la tecnologia.
3. **Suddividi i servizi in livelli.** Raggruppa i servizi in base a quanto in fretta devono tornare e applica l'approccio di ripristino adatto a ciascun livello. Non applicare l'approccio più costoso a tutto.
4. **Scrivi un piano breve che le persone possano usare.** Indica come invocare il piano, chi decide, chi fa che cosa, come comunicare e l'ordine di ripristino. Mantienilo a poche pagine con rimandi ai runbook.
5. **Tieni i piani con il codice e l'ambiente.** Conserva script di ripristino, configurazione e runbook sotto controllo di versione e rivedili quando i servizi cambiano. Un piano non aggiornato con il sistema fallirà.
6. **Pianifica per gli strumenti da cui dipende il ripristino.** Assicurati che l'accesso a pipeline, segreti, documentazione e strumenti di comunicazione sopravviva alla perdita dei sistemi che supportano.
7. **Esercitati regolarmente.** Parti da discussioni tabletop, passa a test tecnici di ripristini e failover ed esegui esercitazioni più grandi per i servizi più critici. Programmale come altro lavoro.
8. **Testa i ripristini, non solo i backup.** Un backup si dimostra ripristinandolo. Verifica che i dati tornino, entro il punto di ripristino, e che il servizio funzioni con essi (vedi la competenza sul test del disaster recovery più avanti).
9. **Tratta i risultati come elementi del backlog.** Ogni esercitazione produce lacune. Registrale con responsabili e date e verifica che siano completate prima della successiva.
10. **Pianifica la comunicazione.** Decidi chi dice che cosa a clienti, personale, autorità di vigilanza e pubblico e prepara modelli. Includi modi fuori banda di raggiungere le persone se i canali normali sono fuori uso (vedi la competenza sulla comunicazione di crisi più avanti).
11. **Includi i fornitori.** Chiedi ai fornitori critici dei loro accordi di continuità e includili nelle esercitazioni dove puoi (vedi Argomento 3.14 — Gestione dei fornitori).
12. **Rivedi ogni anno, e dopo qualsiasi incidente grave o cambiamento importante.** Aggiorna l'analisi, gli obiettivi e i piani quando cambiano business o tecnologia, non solo a calendario.

## Domande da discutere con il team

**Quali dei nostri servizi devono tornare per primi, e come lo sappiamo?**

Chiedi a ciascuno di ordinare i servizi per priorità di ripristino. Confronta. Il disaccordo è istruttivo: mostra che l'ordine non è mai stato concordato con il business. Chi facilita può chiedere quanto costerebbe all'organizzazione che ciascuno restasse fermo un'ora, un giorno e una settimana. Porta la domanda ai responsabili di business e concorda un elenco.

**Quanti dati potremmo perdere, e qualcuno ha concordato su questo?**

Chiedi quando è stato fatto l'ultimo backup dei dati chiave e con quale frequenza. Confronta con ciò che il business tollererebbe. Molti team scoprono che la risposta non è quella che presumevano. Discuti quanto costerebbe un punto di ripristino più stretto. Registra la decisione e chi l'ha presa.

**Quando abbiamo ripristinato per l'ultima volta da un backup, e che cosa è successo?**

Chiedi una data reale e un risultato reale. Se la risposta è "mai", è la scoperta più importante. Se è stato fatto, chiedi che cosa è andato storto e che cosa è stato corretto. Pianifica un test di ripristino per un servizio critico nel prossimo mese.

**Che cosa dobbiamo ripristinare che dipende da ciò che si è guastato?**

Ripercorri uno scenario come la perdita di un account cloud o di un data center. Chiedi dove stanno runbook, segreti e pipeline. Le dipendenze dal sistema guasto sono comuni, come un runbook conservato su un server che è fermo. Elencale e pianifica di spostare o copiare ciascuna.

**Chi ha l'autorità di dichiarare un disastro e avviare il piano?**

Chiedi alle persone chi deciderebbe e se lo sanno. Il ritardo nell'invocare un piano costa tempo. Discuti una regola chiara e un sostituto. Verifica come la persona sarà raggiunta se i canali abituali sono fuori uso.

**Che cosa faremmo se le persone che sanno di più non fossero disponibili?**

Immagina il personale chiave irraggiungibile. Chiedi chi altro potrebbe eseguire il ripristino e di che cosa avrebbe bisogno. Questa domanda collega la continuità alla gestione della conoscenza. Pianifica un modo di diffondere la conoscenza critica.

## Nella pratica: un esempio di ITIL agile

Il catasto di un governo provinciale gestisce un servizio online in cui avvocati e geometri depositano le transazioni immobiliari. Un team di dodici persone lo costruisce e lo gestisce, usando una singola regione di un fornitore cloud. Una revisione della continuità operativa scopre che il servizio è classificato come critico dal ministero, con l'aspettativa che possa essere ripristinato entro quattro ore, e che nessuno ha mai testato se ciò sia possibile.

Il team parte con un'esercitazione tabletop. Lo scenario: la regione cloud è indisponibile per un giorno. Scoprono che i runbook sono conservati in una wiki ospitata nella stessa regione, che il codice dell'infrastruttura copre solo una parte dell'ambiente e che i backup del database sono copiati nella stessa regione. L'aspettativa di quattro ore del ministero risulta essere stata scritta anni fa da un dirigente e mai quantificata nel costo. Il team e il responsabile di business del ministero si incontrano. Il responsabile spiega che cosa significherebbe per le scadenze dei depositi un'interruzione di un giorno e concorda che servono quattro ore nei giorni di deposito di fine mese ma che otto ore sono accettabili negli altri periodi.

Il team copia runbook e backup in una seconda regione, completa il codice dell'infrastruttura e ricostruisce l'ambiente dal codice in una regione di prova in un'esercitazione di una giornata. Il primo tentativo richiede undici ore, soprattutto per passaggi manuali e un segreto mancante. Dopo le correzioni, un secondo tentativo ne richiede cinque. Restano alcuni problemi. L'obiettivo di quattro ore di fine mese è ancora fuori portata, il provider di identità che il personale usa per accedere non ha un proprio accordo di ripristino e il team si rende conto di dipendere da un fornitore di cui non ha mai visto il piano di continuità. Il team mette nel backlog il provider di identità e la questione del fornitore e il ministero concorda un tempo di ripristino più lungo per i periodi non di punta mentre il lavoro continua.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery rendono possibile o impossibile il ripristino attraverso la progettazione. Costruisci servizi che possano essere ricostruiti dal codice, tieni replicati i dati e scrivi i passaggi di ripristino come parte del fatto. Partecipa alle esercitazioni e correggi le lacune che trovano.

### Team di servizio e di operations

I team operativi detengono i piani e conducono le esercitazioni. Mantieni i piani brevi e legati ai runbook, testa ripristini e failover e rendi visibili le dipendenze del ripristino. Monitora i risultati di ogni esercitazione finché non sono chiusi.

### Leadership e governance

I leader fissano gli obiettivi e li pagano. Chiedi l'analisi dell'impatto sul business e gli obiettivi di ripristino, capisci quanto costano e partecipa a un'esercitazione. Accetta che alcuni servizi richiederanno più tempo per essere ripristinati e prendi la decisione di proposito.

### Clienti e utenti

Clienti e utenti dipendono dal fatto che il servizio continui o ritorni. Di' al fornitore per quanto tempo puoi stare senza di esso e quali dati non puoi perdere. Chiedi dei loro accordi di continuità e di che cosa dovresti fare in un disastro, come un modo alternativo di inviare lavoro urgente.

## Modalità di fallimento comuni

- **Un piano che nessuno ha testato.** Il primo test è il disastro. Parti invece dalle esercitazioni tabletop e procedi verso ripristini tecnici.
- **Obiettivi che nessuno ha concordato.** Il tempo di ripristino è stato scritto da qualcuno che se n'è andato. Fissa invece tempo e punto di ripristino con i responsabili di business e registra il costo.
- **Backup mai ripristinati.** I backup esistono ma il ripristino fallisce. Testa invece i ripristini a scadenza fissa e misura il tempo.
- **Il ripristino dipende da ciò che si è guastato.** Runbook, segreti e strumenti stanno nel sistema guasto. Mappa invece le dipendenze del ripristino e tieni copie altrove.
- **Un solo livello per tutto.** Tutti i servizi ottengono il trattamento più costoso, o nessuno. Suddividi invece i servizi in livelli in base al bisogno.
- **Piani obsoleti.** I sistemi cambiano e i piani no. Tieni invece i piani con il codice e rivedili quando i servizi cambiano.
- **Ignorare le persone.** I piani presumono che il personale abituale sia disponibile. Pianifica invece per l'assenza e per la comunicazione quando i canali sono fuori uso.
- **Ignorare i fornitori.** Le dipendenze critiche non hanno accordi di continuità. Chiedi invece ai fornitori e includili nelle esercitazioni.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Analisi dell'impatto e obiettivi | I servizi critici sono presunti | Alcuni servizi hanno obiettivi di ripristino approssimativi | I servizi critici hanno tempo e punto di ripristino concordati, con i costi | Gli obiettivi sono rivisti rispetto ai risultati delle esercitazioni e al cambiamento del business | Gli obiettivi sono allineati con clienti, fornitori e autorità di vigilanza |
| Piani e progettazione del ripristino | Il ripristino è improvvisato | Alcuni servizi hanno note di ripristino | Piani e codice di ripristino esistono per i servizi critici e sono tenuti con il sistema | Aggiornamento dei piani e tempo di ripristino sono misurati e migliorati | Il ripristino è coordinato tra servizi, team e fornitori |
| Esercitazioni e test | Pochi o nessun test | Alcuni ripristini sono testati | Test tabletop e tecnici avvengono a scadenza fissa | I risultati sono tracciati fino alla chiusura e i test calibrati sul rischio | Le esercitazioni includono i fornitori e attraversano le organizzazioni |
| Comunicazione e persone | La comunicazione è estemporanea | Esistono alcuni elenchi di contatti | I piani coprono chi informa chi, con vie fuori banda e sostituti | Le lacune di comunicazione e di personale sono misurate e colmate | La comunicazione è provata con clienti, fornitori e autorità di vigilanza |

## Checklist

- [ ] Abbiamo individuato i nostri servizi critici con i responsabili di business.
- [ ] Ogni servizio critico ha un tempo di ripristino e un punto di ripristino concordati, con il costo noto.
- [ ] I servizi sono raggruppati in livelli che corrispondono alle loro esigenze di ripristino.
- [ ] Esiste un breve piano di ripristino, con chi può invocarlo e come raggiungerlo.
- [ ] Codice di ripristino, configurazione e runbook sono sotto controllo di versione e rivisti con le modifiche.
- [ ] Runbook, segreti e strumenti necessari al ripristino sopravvivono alla perdita dell'ambiente primario.
- [ ] Un ripristino da backup è stato testato per ogni servizio critico nell'ultimo anno.
- [ ] Un'esercitazione tabletop è stata tenuta nell'ultimo anno e i risultati sono tracciati.
- [ ] Esistono modelli di comunicazione e vie fuori banda.
- [ ] Ai fornitori critici sono stati chiesti i loro accordi di continuità.

## Prompt per l'IA

**Scopo: redigere le domande per un'analisi dell'impatto sul business.**

```text
Help me prepare a business impact analysis for these services: [list services].

About the organization: [describe sector and who relies on the services].
Peak periods or deadlines: [list, or write "unknown"].
Rules or contracts that set recovery requirements, with source text: [paste, or write "none known"].

Write, for each service, a short set of questions to put to business owners about the impact of an outage after one hour, one day, and one week (financial, operational, reputational, legal), what data loss would be tolerable, what the service depends on, and what workarounds exist. Do not invent impacts or numbers. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: pianificare un'esercitazione tabletop.**

```text
Design a 90-minute tabletop exercise for [number] people from [teams] on this scenario: [describe, for example "our cloud region is unavailable for 24 hours"].

Services in scope: [list].
Existing plans and runbooks: [describe, or write "none"].

Give a timed plan with: the scenario released in three stages, prompts for each role, questions on dependencies of recovery (where runbooks, secrets, and tools live), decisions that must be made and who makes them, and a closing step that records gaps with owners and dates. Do not use real production access. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

**Scopo: trasformare le note di un'esercitazione in un elenco di lacune.**

```text
Below are the notes from a continuity exercise: [paste what happened, what went wrong, what people said].

List the gaps found, grouped as: plan (what was missing or unclear), technology (what failed or was slow), people (who was missing or unsure), and dependencies (what recovery depended on that was itself unavailable). For each gap, suggest a backlog item title and a question about priority. Use only the notes. Do not invent causes. List what you are unsure of.
```

**Scopo: scrivere uno schema breve di piano di ripristino per un servizio.**

```text
Help me outline a recovery plan for [service].

What it does and who depends on it: [describe].
Agreed recovery time and recovery point, if any: [paste, or write "not agreed"].
Where it runs, where data and backups are kept: [describe].
Dependencies (other services, suppliers, identity, networks): [list].
People who can recover it: [roles].

Write a plan outline of no more than two pages: how it is invoked, who decides, communication, order of recovery steps (with links to runbooks as [LINK]), testing evidence needed, and how to return to normal. Mark each item that is an assumption. Do not invent recovery times. Ask clarifying questions first, and list what you are unsure of.
```

## Competenze per l'IA

- [business-continuity-plan](../../../../skills/business-continuity-plan/SKILL.md): da usare per scrivere il piano a livello di organizzazione per mantenere in funzione le funzioni critiche.
- [disaster-recovery-plan](../../../../skills/disaster-recovery-plan/SKILL.md): da usare per pianificare il ripristino tecnico dei servizi IT.
- [disaster-recovery-testing](../../../../skills/disaster-recovery-testing/SKILL.md): da usare per progettare test di ripristino e di failover.
- [crisis-communication-plan](../../../../skills/crisis-communication-plan/SKILL.md): da usare per pianificare che cosa dire a clienti, personale e pubblico durante un'interruzione.
- [risk-register](../../../../skills/risk-register/SKILL.md): da usare per registrare i rischi di continuità e come sono gestiti.

## Fonti principali

- **Business continuity planning** (Wikipedia): definizioni di continuità, analisi dell'impatto sul business, obiettivi di ripristino, esercitazioni e standard.
- **ISO 22301** (International Organization for Standardization): lo standard dei requisiti per i sistemi di gestione della continuità operativa; leggi lo standard per le dichiarazioni di conformità.
- **Incident management** (Wikipedia): la panoramica multi-settore che colloca la continuità accanto alla risposta agli incidenti.
- **Embracing Risk** (*Site Reliability Engineering*, Google, sre.google): l'economia dell'affidabilità che inquadra gli obiettivi di ripristino.

## Riferimenti

1. Business continuity planning — Wikipedia — https://en.wikipedia.org/wiki/Business_continuity_planning
2. Disaster recovery — Wikipedia (disambiguation page) — https://en.wikipedia.org/wiki/Disaster_recovery
3. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
4. Embracing Risk — Google SRE book, sre.google — https://sre.google/sre-book/embracing-risk/
5. ISO 22301 — Wikipedia — https://en.wikipedia.org/wiki/ISO_22301
6. Risk management — Wikipedia — https://en.wikipedia.org/wiki/Risk_management
7. Backup — Wikipedia — https://en.wikipedia.org/wiki/Backup
8. Infrastructure as code — Wikipedia — https://en.wikipedia.org/wiki/Infrastructure_as_code
