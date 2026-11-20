# Framework e standard ITSM

**La gestione dei servizi IT ha molti framework e standard che si sovrappongono, e la competenza utile è sapere a che cosa serve ciascuno: una guida da cui imparare, uno standard rispetto al quale si può essere certificati o un modello di governance che dice che cosa controllare.**

## Perché è importante

Chiedi a cinque persone che cosa significhi "seguiamo le migliori pratiche ITSM" e potresti ottenere cinque risposte: ITIL, ISO/IEC 20000, COBIT, FitSM o "qualunque cosa faccia lo strumento del fornitore". I termini sono usati con larghezza, e le differenze contano. Un cliente che chiede la certificazione ISO/IEC 20000 non può essere soddisfatto dalla formazione ITIL. Un auditor che chiede dei controlli COBIT non sarà aiutato da una mappa dei processi del service desk.

Per i team agili la domanda è pratica: con quali di questi dobbiamo fare i conti, e quali possiamo trattare come fonte di idee? Molti team restano sorpresi nello scoprire che ITIL, il più noto, è una guida in cui le persone si certificano e non uno standard per le organizzazioni. Altri restano sorpresi che il principale standard ITSM abbia aggiunto di recente indicazioni sui modi di lavorare agili e DevOps.

Questo argomento confronta i principali framework e standard, usando gli articoli di Wikipedia su [IT service management](https://en.wikipedia.org/wiki/IT_service_management), [ISO/IEC 20000](https://en.wikipedia.org/wiki/ISO/IEC_20000), [COBIT](https://en.wikipedia.org/wiki/COBIT) e [FitSM](https://en.wikipedia.org/wiki/FitSM). Quegli articoli sono di qualità variabile e diversi portano avvisi di manutenzione. Dove sono deboli, questo argomento lo dice. Controlla le pubblicazioni dei proprietari prima di fare affidamento su un dettaglio per un contratto o un audit.

## Concetti fondamentali

### Tre tipi di cosa

I nomi di questo argomento cadono in tre gruppi. Tenerli distinti evita molte conversazioni confuse.

| Tipo | Che cosa ti dà | Esempi nominati nell'articolo di Wikipedia sull'ITSM |
|---|---|---|
| **Guida (un framework o una libreria)** | Idee e pratiche descritte da adattare | ITIL, Microsoft Operations Framework, Application Services Library, Business Information Services Library |
| **Uno standard certificabile** | Requisiti rispetto ai quali un'organizzazione può essere sottoposta ad audit e certificata | ISO/IEC 20000 |
| **Un modello di governance o di capacità** | Un modo di dirigere, controllare o valutare l'IT | COBIT, CMMI, TOGAF |

FitSM sta tra i primi due, come descritto sotto.

### ITIL

ITIL è una guida sull'ITSM e sulla gestione degli asset IT. La certificazione è per le persone, e non esiste una valutazione indipendente della conformità di un'organizzazione a ITIL (vedi Argomento 2.2 — ITIL). È la fonte di vocabolario più diffusa.

### ISO/IEC 20000

ISO/IEC 20000 è uno standard internazionale per la gestione dei servizi IT. Secondo Wikipedia, la Parte 1 fissa i requisiti per un sistema di gestione dei servizi che copre pianificazione, erogazione e miglioramento dei servizi. È stato sviluppato a partire da BS 15000, creato da BSI Group, ed è stato pubblicato per la prima volta nel dicembre 2005. Sono seguiti aggiornamenti: la Parte 1 nel giugno 2011 e una seconda revisione, ISO/IEC 20000-1:2018, pubblicata il 15 luglio 2018, dopo la quale le organizzazioni certificate hanno avuto un periodo di transizione di tre anni. L'edizione 2018 ha dieci clausole che seguono la struttura di alto livello ISO.

Lo standard ha molte parti. L'articolo elenca, tra le altre: indicazioni sull'applicazione di un sistema di gestione dei servizi (Parte 2); indicazioni su ambito e applicabilità (Parte 3); indicazioni di implementazione (Parte 5); requisiti per gli organismi di certificazione (Parte 6); concetti e vocabolario (Parte 10); e una specifica tecnica sul rapporto con ITIL 4 (Parte 11). Elenca anche parti pubblicate di recente, dal 2023 al 2025, con indicazioni su service integration and management (SIAM), agile e DevOps e sostenibilità. Wikipedia non dice quale numero di parte copra quale argomento, quindi controlla il catalogo ISO prima di citarne una.

Le organizzazioni possono essere certificate, e le persone possono ottenere qualifiche da enti come APMG-International, EXIN e PECB. L'articolo riferisce che l'indagine ISO 2024 ha contato 27.332 certificati, di cui 24.056 in Cina. Ciò mostra quanto la certificazione sia distribuita in modo disomogeneo tra i paesi, quindi non dare per scontato che un cliente altrove la chieda.

Wikipedia dice che lo standard fu originariamente sviluppato per riflettere le migliori pratiche ITIL, ma segna l'affermazione "citation needed". Considera il rapporto come stretto ma non identico. L'articolo dice anche che lo standard supporta altri framework come Microsoft Operations Framework e parti di COBIT.

### COBIT

COBIT, secondo Wikipedia, è un framework creato da ISACA per la gestione e la governance dell'IT. Collega gli obiettivi di business agli obiettivi IT e definisce le responsabilità dei team di business e IT. L'articolo descrive cinque aree di processo: Evaluate, Direct and Monitor; Align, Plan and Organize; Build, Acquire and Implement; Deliver, Service and Support; e Monitor, Evaluate and Assess. Fornisce queste date: pubblicato per la prima volta nel 1996, versione 5 nel 2012, e dice che ISACA offre certificazione su COBIT 2019 e COBIT 5. L'articolo collega COBIT a ITIL, ISO 27000, CMMI, TOGAF e alla PMBOK Guide del Project Management Institute.

L'articolo stesso porta avvisi di manutenzione su fonti primarie e citazioni mancanti, e un'affermazione, secondo cui il framework aiuterebbe le aziende a rispettare la legge e a essere più agili, poggia su una sola fonte. Usa le pubblicazioni di COBIT stesse come autorità.

### FitSM

FitSM è una famiglia di standard leggeri. Wikipedia dice che è nato da FedSM, un progetto finanziato dall'UE per migliorare la gestione dei servizi nelle e-infrastrutture federate, e che i deliverable rivisti furono pubblicati con il nome FitSM dal maggio 2013. FitSM-1 contiene circa 85 requisiti verificabili che coprono i requisiti generali e 14 processi, ed è molto più breve della Parte 1 di ISO/IEC 20000 pur essendo simile per ambito e stile. Tutte le parti sono pubblicate con licenze Creative Commons. Le organizzazioni non possono essere certificate come conformi a FitSM, anche se la conformità può essere verificata, e uno schema di certificazione del personale è iniziato nel 2013.

FitSM è utile per piccoli team che vogliono un breve insieme di requisiti. L'articolo non indica la versione corrente né lo stato del suo gruppo di manutenzione, quindi verificali prima di farvi affidamento.

### Altri nomi

L'articolo sull'ITSM elenca anche i seguenti. Questa guida non li tratta oltre.

- **CMMI:** un modello per stabilire, gestire e migliorare servizi e processi.
- **TOGAF:** un framework che collega gli obiettivi di business agli obiettivi architetturali.
- **Microsoft Operations Framework:** indicazioni di gestione dei servizi basate sulle tecnologie Microsoft.
- **Application Services Library e Business Information Services Library:** framework per la gestione delle applicazioni e per la gestione delle informazioni.
- **USM:** un sistema basato su principi adottato dal governo olandese.

L'articolo aggiunge che i framework ITSM hanno attinto a ISO 9000, ISO/IEC 27000 e CMMI. La gestione della sicurezza ha una propria famiglia di standard (vedi Argomento 3.13 — Gestione della sicurezza delle informazioni).

### Agile e DevOps negli standard

L'articolo su ISO/IEC 20000 elenca una parte recente dello standard con indicazioni su agile e DevOps. È notevole perché mostra che l'ente di normazione tratta i modi di lavorare agili come qualcosa che un sistema di gestione dei servizi deve accogliere. L'articolo non dà dettagli sul suo contenuto, quindi leggi lo standard stesso se ti serve. Nel frattempo, ITIL 4 si descrive come allineato ad agile, DevOps e lean (vedi Argomento 2.2 — ITIL), e l'articolo di Wikipedia sull'ITSM non menziona affatto l'agile. Le fonti differiscono in quanto si sono aggiornate.

### Scegliere

Non esiste un unico framework giusto. Un modo sensato di scegliere è chiedersi di che cosa hai bisogno:

| Se ti serve… | Considera… |
|---|---|
| Un vocabolario condiviso e idee per le pratiche | ITIL |
| La certificazione del tuo sistema di gestione dei servizi per clienti o gare | ISO/IEC 20000 |
| Un breve insieme verificabile di requisiti per un piccolo team | FitSM |
| Governance e controllo dell'IT nell'impresa, collegati agli obiettivi di business | COBIT |
| Valutazione della capacità dei processi | CMMI |

Questa tabella è il riassunto della guida, non una raccomandazione di alcun proprietario di framework.

## Buone pratiche

1. **Parti dalla domanda a cui devi rispondere.** Scrivi di che cosa hai bisogno: vocabolario, certificazione, controllo o valutazione. Scegli il framework che risponde, e non quello con il miglior marketing.
2. **Impara la differenza tra guide e standard.** Insegna al team che la certificazione ITIL è per le persone, la certificazione ISO/IEC 20000 è per le organizzazioni e COBIT è un modello di governance. Molte confusioni su contratti e audit iniziano qui.
3. **Scopri che cosa richiedono davvero clienti e autorità di vigilanza.** Chiedi la clausola o il requisito esatti. Spesso la richiesta è per un "framework riconosciuto", e una breve e onesta descrizione della tua pratica basta.
4. **Usa il testo dello standard, non i riassunti, per la conformità.** Quando dichiari la conformità, lavora a partire dallo standard ISO o dalla pubblicazione del proprietario del framework. I riassunti, compreso questo, servono solo per l'orientamento.
5. **Mappa la tua pratica una volta, non quattro.** Se devi soddisfare più di un framework, costruisci una descrizione unica della tua pratica e mappala su ciascuno, invece di scrivere documenti separati.
6. **Mantieni il sistema il più piccolo possibile.** ISO/IEC 20000 richiede un sistema di gestione dei servizi e record. Soddisfa ogni requisito con l'approccio più leggero che funziona e automatizza le prove dai tuoi strumenti.
7. **Presta attenzione all'ambito.** Un certificato copre un ambito dichiarato. Scegli un ambito che rifletta servizi e team reali e non escludere le parti che rendono difficile il certificato.
8. **Controlla le indicazioni su agile e DevOps negli standard che usi.** Dove uno standard ha indicazioni su agile e DevOps, leggile prima di discutere con un auditor su come un team agile possa soddisfare un requisito.
9. **Considera opzioni più leggere per i piccoli team.** FitSM o un sottoinsieme di ITIL possono adattarsi a un piccolo team meglio di un sistema completo certificato. Annota a che cosa rinunci, come la certificazione esterna.
10. **Mantieni allineate sicurezza e gestione dei servizi.** Se usi ISO/IEC 27001 per la sicurezza delle informazioni, condividi record e revisioni con il tuo sistema di gestione dei servizi per evitare lavoro duplicato (vedi Argomento 3.13 — Gestione della sicurezza delle informazioni).
11. **Documenta il tuo adattamento.** Registra quali parti di un framework usi, quali no e perché. Ti protegge negli audit e aiuta i nuovi arrivati.
12. **Rivedi ogni anno.** Standard e framework cambiano. Assegna a qualcuno il compito di seguire gli aggiornamenti e riferire ciò che conta per il tuo team (vedi Argomento 6.4 — Percorsi di apprendimento e certificazione).

## Domande da discutere con il team

**Quali di questi framework o standard siamo tenuti a usare, e quali usiamo per abitudine?**

Elenca ciò che clienti, contratti, autorità di vigilanza e manager richiedono davvero, con il documento che lo dice. Poi elenca ciò che il team usa senza un requisito. I due elenchi spesso differiscono più del previsto. Chi facilita può chiedere chi ha introdotto ciascuno per primo e perché. Prosegui trovando la formulazione esatta di qualsiasi requisito che guida il lavoro.

**Se un cliente chiedesse se siamo "certificati ITIL", che cosa risponderemmo?**

Esercitati a una risposta onesta: le persone possono essere certificate, le organizzazioni no, ed ecco che cosa facciamo. Confronta le risposte. Alcune esagereranno. Discuti di che cosa il cliente ha probabilmente bisogno e quali prove potrebbero soddisfarlo, come la certificazione ISO/IEC 20000 o una descrizione della pratica. Concorda una frase che tutti possano usare.

**Quanto ci costerebbe essere certificati ISO/IEC 20000, e che cosa guadagneremmo?**

Chiedi quali clienti o mercati la apprezzerebbero e che cosa il team dovrebbe cambiare. Non indovinare i costi; raccogli preventivi reali o chiedi a un collega che l'ha fatto. Elenca i benefici che sai descrivere: un'etichetta riconosciuta, un sistema disciplinato, accesso alle gare. Decidi se approfondire.

**Da dove vengono i nostri record per l'audit, e i nostri strumenti potrebbero produrli automaticamente?**

Elenca i record che gli auditor chiedono e da dove viene ciascuno. Molti possono venire da controllo di versione, strumenti di ticket e monitoraggio se configurati con questo in mente. Chiedi quali record sono prodotti a mano e perché. Scegline uno da automatizzare.

**Come si adattano le nostre pratiche agili a ciò che gli standard si aspettano, e dov'è il divario?**

Prendi un requisito a cui il tuo auditor tiene, come l'autorizzazione dei cambiamenti, e descrivi come un team agile lo soddisfa. Dove lo standard ha indicazioni su agile e DevOps, leggete insieme il testo pertinente. Annota le lacune nelle prove, non nell'intento.

**Chi segue per noi i cambiamenti in questi framework?**

Chiedi chi legge gli annunci dei proprietari dei framework e degli enti di normazione. Una risposta frequente è "nessuno". Decidi chi lo farà, come riferirà e quando. Chi facilita può suggerire una breve nota ogni trimestre che elenchi ciò che è cambiato e se conta.

## Nella pratica: un esempio di ITIL agile

Un'azienda di software di 120 persone vende a ospedali e università un prodotto di pianificazione in hosting. La gara di un grande cliente universitario richiede "un sistema di gestione dei servizi IT certificato". I fondatori avevano ipotizzato che bastasse il responsabile del supporto formato su ITIL. Il responsabile del supporto spiega che la certificazione ITIL si applica alle persone, e che la gara molto probabilmente intende ISO/IEC 20000.

La responsabile delle operations indaga. Legge la formulazione della gara, che nomina ISO/IEC 20000-1, e chiede al cliente quale ambito si aspetta. Legge l'indice dello standard e confronta le sue dieci clausole con i record esistenti dell'azienda, che vengono per lo più dallo strumento di ticket, dalla cronologia delle modifiche e dalle revisioni degli incidenti. Scopre che molte prove esistono già, ma che mancano politiche documentate di gestione dei servizi, revisioni formali dei fornitori e un riesame della direzione. Scopre anche che lo standard ora ha una parte con indicazioni su agile e DevOps, il che la aiuta a spiegare i rilasci settimanali dell'azienda a un futuro auditor.

L'azienda decide di perseguire la certificazione solo per il prodotto in hosting, con un modesto insieme di documenti e un riesame trimestrale della direzione. Prevede circa un anno di lavoro. Non tutto va liscio. Due ingegneri resistono ai record aggiuntivi e un fornitore rifiuta di fornire rapporti formali di revisione del servizio. La responsabile delle operations sostituisce alcuni record manuali con esportazioni dagli strumenti dell'azienda e negozia con il fornitore un accordo di revisione più leggero. L'azienda vince la gara e decide di verificare al prossimo audit di sorveglianza se il sistema aiuta o ostacola i rilasci settimanali.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery incontrano questi framework come requisiti di clienti e auditor. Scopri quale requisito si applica e chiedi quali prove sono accettabili. Molti requisiti possono essere soddisfatti con gli strumenti che già usi. Offri di spiegare il tuo processo di rilascio nel linguaggio dello standard.

### Team di servizio e di operations

I team operativi di solito portano il sistema di gestione. Mantieni utili i record, con uno scopo dichiarato per ciascuno. Fai attenzione ai requisiti che si duplicano tra i framework e mappali una volta. Condividi il piano con i team di delivery così che i record siano un sottoprodotto del lavoro e non un compito separato.

### Leadership e governance

I leader decidono quali framework adottare e quanto investire nella certificazione. Chiedi qual è il business case e che cosa richiedono davvero i clienti. Diffida dall'acquistare la certificazione come etichetta. Assicurati che il sistema aiuti l'organizzazione a migliorare e che qualcuno lo possieda.

### Clienti e utenti

I clienti che chiedono la certificazione spesso vogliono garanzie. Chiedi ai fornitori quale standard e quale ambito copre il loro certificato e che cosa ne è fuori. Un certificato è prova di un sistema di gestione, non una garanzia di un singolo risultato.

## Modalità di fallimento comuni

- **Confondere certificazione individuale e organizzativa.** I team dichiarano "certificato ITIL" per un'azienda. Indica invece esattamente che cosa è certificato e da chi.
- **Inseguire la certificazione come etichetta.** Il sistema esiste per l'audit, non per il miglioramento. Rendi invece prima utili i record per il team.
- **Duplicare documenti tra framework.** Ogni standard ottiene il proprio raccoglitore. Descrivi invece la tua pratica una volta e mappala.
- **Restringere l'ambito per evitare le parti difficili.** Il certificato esclude i servizi a cui i clienti tengono. Scegli invece un ambito che rifletta i servizi reali.
- **Affidarsi ai riassunti.** Le dichiarazioni di conformità si basano su post di blog. Lavora invece sul testo dello standard o del proprietario del framework.
- **Ignorare le indicazioni agili.** I team discutono con gli auditor senza leggere la parte dello standard che tratta agile e DevOps. Leggila invece e prepara esempi.
- **Documentare troppo.** Il sistema produce più record di quanti ne legga qualcuno. Collega invece ogni record a uno scopo e automatizza le prove.
- **Dimenticare i cambiamenti.** Lo standard va avanti e il team non se ne accorge. Nomina invece qualcuno che segua gli aggiornamenti.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Comprensione dei framework | I nomi sono usati con larghezza | Alcune persone sanno dire a che cosa serve ciascun framework | I team condividono una descrizione breve e accurata dei framework in uso | L'uso dei framework è rivisto rispetto a requisiti e risultati | Team, clienti e fornitori condividono una comprensione accurata |
| Requisiti e ambito | I requisiti sono presunti | Alcuni requisiti sono ricondotti a documenti | Requisiti e ambito sono documentati | Conformità e ambito sono rivisti e le lacune monitorate | I requisiti sono allineati con partner e clienti |
| Prove | Le prove sono assemblate a mano per ogni richiesta | Alcuni record sono prodotti dagli strumenti | Le prove vengono per lo più dagli strumenti e sono descritte in modo coerente | La qualità delle prove è misurata e migliorata | Le prove sono condivise automaticamente con auditor e partner |
| Aggiornamento | I cambiamenti dei framework passano inosservati | Alcune persone seguono gli annunci | Una persona nominata riferisce i cambiamenti a intervalli fissi | I cambiamenti sono valutati e se ne tiene conto | I cambiamenti sono anticipati e affrontati con i partner |

## Checklist

- [ ] Sappiamo indicare quali framework e standard clienti, contratti o autorità di vigilanza richiedono davvero.
- [ ] Sappiamo quali sono guide, quali standard certificabili e quali modelli di governance.
- [ ] Le nostre dichiarazioni sulla certificazione sono accurate e specificano l'ambito.
- [ ] Per ogni dichiarazione di conformità lavoriamo sul testo dello standard o del proprietario.
- [ ] La nostra pratica è descritta una volta e mappata su ogni framework che dobbiamo soddisfare.
- [ ] Le prove per gli audit vengono per lo più dai nostri strumenti.
- [ ] Abbiamo letto le indicazioni su agile e DevOps negli standard che ci riguardano.
- [ ] Qualcuno è nominato per seguire gli aggiornamenti e riferirli.
- [ ] Le nostre decisioni di adattamento sono scritte.
- [ ] Abbiamo verificato se il nostro ambito corrisponde ai servizi reali.

## Prompt per l'IA

**Scopo: associare un requisito del cliente al testo del framework che lo sostiene.**

```text
A customer or auditor has made this requirement: [paste the exact wording and where it appeared, for example a tender clause].

Here is the text of the relevant standard or framework, which I have copied from the owner's publication: [paste only text you are entitled to use; keep it short].

Using only the pasted text, say what the requirement appears to ask for, what is unclear, and what questions I should put to the customer. Do not describe the contents of any standard that I have not pasted. Do not say whether we comply. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: descrivere la tua pratica una volta in modo da poterla mappare su più framework.**

```text
Help me write a single plain-language description of how we handle [practice, e.g. "changes to production"].

How it works today, in steps, with the tools and records involved: [paste].
Frameworks we need to map it to: [list names; I will paste the relevant requirement text for each].

Produce a description in short numbered steps, then a table with one row per step and one column per framework showing which pasted requirement the step seems to address (only from my pasted text). Mark gaps as questions, not conclusions. Do not claim conformance. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: prepararsi a rispondere onestamente a "siete certificati ITIL?".**

```text
Write a short, honest reply to a customer who asks whether our company is "ITIL certified."

Facts I have verified from official sources: [paste, for example that certification in ITIL applies to individuals; and list the certifications our staff hold].
What we actually do: [describe our practice in a few sentences].
Other certifications we hold or are considering: [list].

The reply should be polite, accurate, under 150 words, and avoid overclaiming. Offer evidence we could share. Use only the facts I gave. Ask clarifying questions first if anything is missing, and list what you are unsure of.
```

**Scopo: pianificare le prove che un audit di gestione dei servizi potrebbe richiedere.**

```text
We expect an audit of our service management against [standard name and edition].

The records we produce today, and the tool each comes from: [list].
The requirement areas I know of, with the wording I have from the standard: [paste, or write "not yet read"].

Create a table of likely evidence by requirement area (from my pasted text only), the record we already have, the gap, and whether the record could come from a tool automatically. Do not invent requirements. Ask clarifying questions first, mark assumptions, and list what you are unsure of.
```

## Competenze per l'IA

- [enterprise-architecture](../../../../skills/enterprise-architecture/SKILL.md): da usare per collocare i framework di gestione dei servizi nel quadro più ampio di architettura aziendale e governance.
- [legal-compliance-audit](../../../../skills/legal-compliance-audit/SKILL.md): da usare per pianificare come prepararsi a un audit rispetto a uno standard o a un requisito contrattuale.
- [compliance-testing](../../../../skills/compliance-testing/SKILL.md): da usare per progettare controlli che producano automaticamente prove di conformità.
- [vendor-management](../../../../skills/vendor-management/SKILL.md): da usare quando l'ambito di una certificazione dipende dai fornitori e devi pianificare le revisioni dei fornitori.
- [project-management-body-of-knowledge](../../../../skills/project-management-body-of-knowledge/SKILL.md): da usare quando framework come COBIT o la PMBOK Guide incontrano il tuo ufficio di progetto.

## Fonti principali

- **ISO/IEC 20000-1** (International Organization for Standardization): lo standard stesso; leggi ambito e titoli delle clausole nel catalogo ISO prima di fare dichiarazioni.
- **ISO/IEC 20000** (Wikipedia): storia, parti e panorama della certificazione dello standard, con citazioni.
- **COBIT** (ISACA e Wikipedia): le pubblicazioni di ISACA sono autorevoli; l'articolo di Wikipedia dà storia e struttura ma ha fonti deboli.
- **FitSM** (Wikipedia e progetto FitSM): un'alternativa breve e con licenza libera; controlla le pagine del progetto per la versione corrente.

## Riferimenti

1. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
2. ISO/IEC 20000 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_20000
3. COBIT — Wikipedia — https://en.wikipedia.org/wiki/COBIT
4. FitSM — Wikipedia — https://en.wikipedia.org/wiki/FitSM
5. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
6. CMMI — Wikipedia — https://en.wikipedia.org/wiki/CMMI
7. TOGAF — Wikipedia — https://en.wikipedia.org/wiki/TOGAF
8. ISACA — Wikipedia — https://en.wikipedia.org/wiki/ISACA
9. ISO/IEC 27001 — Wikipedia — https://en.wikipedia.org/wiki/ISO/IEC_27001
10. Microsoft Operations Framework — Wikipedia — https://en.wikipedia.org/wiki/Microsoft_Operations_Framework
