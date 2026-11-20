# L'IA nella gestione dei servizi IT

**L'intelligenza artificiale può accelerare il rilevamento, il triage e il lavoro sulla conoscenza nella gestione dei servizi IT, e il suo uso è sicuro solo dove una persona resta responsabile, le risposte sono ancorate al proprio materiale e i rischi di errore, pregiudizio ed esposizione dei dati sono gestiti.**

## Perché è importante

La gestione dei servizi comporta moltissimo linguaggio e riconoscimento di schemi: leggere ticket, riassumere incidenti, cercare nella conoscenza, redigere risposte, individuare segnali insoliti nei dati di monitoraggio. Sono i compiti in cui i recenti sistemi di IA appaiono più capaci, e i fornitori si sono affrettati ad aggiungerli ai service desk e agli strumenti operativi. Ai team verrà chiesto, se non è già successo, se usarli.

L'opportunità è reale, e lo sono anche i pericoli. I sistemi di IA possono affermare falsità con sicurezza, riflettere i pregiudizi presenti nel loro addestramento e nei dati che ricevono, esporre informazioni riservate se alimentati con leggerezza e indurre le persone a fidarsi di un output che non hanno verificato. Diversi casi molto riportati mostrano il costo di una fiducia mal riposta. Un'organizzazione di servizio che adotta l'IA senza riflettere può danneggiare i propri clienti e la propria reputazione.

Entro il 2026 l'IA è entrata anche nel framework. La pagina pubblica delle certificazioni di PeopleCert descrive il nuovo ITIL come "Practical and AI-native by design" ed elenca un modulo ITIL AI Governance (Version 5) che tratta la governance dell'IA "responsibly and at scale" (vedi Argomento 2.2 — ITIL). Questa guida non ha potuto verificare, dalle pubblicazioni del titolare, che cosa dica ITIL 5 sull'IA nel dettaglio, quindi questo argomento non descrive la posizione del framework oltre quelle dichiarazioni. Attinge agli articoli di Wikipedia su AIOps e sull'allucinazione dell'IA, alla pagina del NIST sull'AI Risk Management Framework e a ragionamenti pratici, e segnala come tale ciò che è pratica.

## Concetti fondamentali

### Dove l'IA aiuta nella gestione dei servizi

La maggior parte degli usi rientra in pochi gruppi. La tabella mostra esempi e il tipo di rischio di ciascuno, secondo la lettura di questa guida.

| Uso | Che cosa fa l'IA | Rischi principali |
|---|---|---|
| **Rilevamento e correlazione (AIOps)** | Trova anomalie, raggruppa eventi correlati, suggerisce cause probabili | Falsi allarmi, eventi mancati, ragionamento opaco |
| **Assistenza al service desk** | Suggerisce risposte, riassume ticket, redige risposte, instrada richieste | Risposte sbagliate o inventate, tono, privacy |
| **Lavoro sulla conoscenza** | Redige e migliora articoli, cerca nella conoscenza | Contenuti fabbricati, fonti obsolete |
| **Analisi di incidenti e problemi** | Riassume cronologie, suggerisce ipotesi, redige revisioni | Cause plausibili ma infondate |
| **Supporto a cambiamenti e rilasci** | Rivede cambiamenti, redige note, suggerisce il rischio | Eccessiva sicurezza, contesto mancato |
| **Codice e automazione** | Scrive script e configurazioni | Codice insicuro o errato, dipendenze nascoste |
| **Analisi e reportistica** | Riassume dati, redige report | Calcoli sbagliati, cifre inventate |

### AIOps

L'articolo di Wikipedia descrive l'AIOps come l'uso di IA, apprendimento automatico e analisi dei big data per automatizzare e migliorare la gestione dei data center, con l'obiettivo di rilevare, diagnosticare e risolvere i problemi IT in modo più efficiente dei metodi tradizionali. Dice che Gartner definì per la prima volta l'AIOps nel 2016. L'articolo elenca capacità tra cui correlazione degli eventi, rilevamento di anomalie, analisi delle cause radice, determinazione della causalità, analisi predittiva, gestione degli incidenti, rimedio automatizzato, previsione delle prestazioni, allocazione delle risorse e gestione della capacità. Dice che l'AIOps attinge a dati di osservazione, come log e monitoraggio, e a dati di interazione, come ticket, eventi e registri degli incidenti.

L'articolo dichiara benefici, come un miglioramento del 15–20 percento del tempo medio di rilevamento e un calo di oltre il 50 percento degli incidenti critici, ma nota che provengono da un singolo articolo di una società di consulenza e non sono verificati in modo indipendente nel testo. Non cita critiche, casi di fallimento né limiti. Tratta di conseguenza le affermazioni dei fornitori e prova ogni strumento sui tuoi incidenti (vedi Argomento 3.10 — Monitoraggio e gestione degli eventi).

### IA generativa e allucinazione

L'articolo di Wikipedia sull'allucinazione nell'IA la definisce come una risposta che contiene informazioni false o fuorvianti presentate come fatti, e nota che il termine è criticato perché antropomorfizza il software. Ne indica le cause: il pre-addestramento sulla previsione della parola successiva premia l'indovinare quando il modello non ha informazioni, i dataset possono essere incompleti o non rappresentativi e i ricercatori di OpenAI sostengono che addestramento e valutazione premiano l'indovinare rispetto all'ammettere l'incertezza. Gli esempi che riporta includono:

- **Mata v. Avianca (maggio 2023):** un avvocato presentò sei cause false generate da ChatGPT; il giudice impose una multa di 5.000 dollari USA il 23 giugno 2023.
- **Moffatt v. Air Canada (febbraio 2024):** un tribunale vincolò una compagnia aerea a una politica sul lutto che il suo chatbot aveva inventato.
- Rapporti di una società di consulenza che contenevano citazioni false, e uno studio che rilevò che 69 su 178 riferimenti di GPT-3 avevano identificatori errati o inesistenti.

Sono le conseguenze del fidarsi di un output non verificato: responsabilità legale, esposizione finanziaria e fiducia danneggiata. Nella gestione dei servizi, un chatbot che inventa una politica o una procedura crea lo stesso tipo di rischio.

### Mitigazione: ancoraggio e controlli

L'articolo descrive la retrieval-augmented generation (RAG) come ciò che permette al modello di accedere a fonti esterne prima di rispondere. Elenca anche metodi relativi ai dati, metodi relativi al modello e all'inferenza e proposte come software di guardrail e punteggi di confidenza, e nota che nessuna fonte che cita quantifica quanto uno qualsiasi di questi riduca l'allucinazione. Per un team di servizio, le mitigazioni pratiche sono:

- **Ancora le risposte al tuo materiale approvato,** come la base di conoscenza, e mostra la fonte.
- **Tieni una persona nel ciclo** per tutto ciò che riguarda un cliente, un impegno o la produzione.
- **Chiedi che cosa l'IA non sa con certezza,** e tratta le affermazioni non supportate come non verificate.
- **Prova con regolarità** su casi reali, compresi i casi in cui la risposta giusta è "non lo so".

### Framework di gestione del rischio

Il National Institute of Standards and Technology (NIST) ha pubblicato l'AI Risk Management Framework (AI RMF 1.0) il 26 gennaio 2023, che descrive come destinato a un uso volontario, per aiutare a gestire i rischi dell'IA per individui, organizzazioni e società e a migliorare la capacità di incorporare considerazioni di affidabilità nella progettazione, nello sviluppo, nell'uso e nella valutazione di prodotti, servizi e sistemi di IA. La pagina del NIST nomina quattro funzioni, Govern, Map, Measure e Manage, ma non le descrive. Ha anche rilasciato un Generative Artificial Intelligence Profile (NIST-AI-600-1) il 26 luglio 2024 per aiutare le organizzazioni a individuare i rischi specifici dell'IA generativa, e dice che il framework è in revisione. Leggi il framework stesso per i dettagli. Altre regole sull'IA, come leggi e standard, differiscono per paese e settore; chiedi alle funzioni legali e di conformità e procurati il testo (vedi Argomento 5.7 — Governance, rischio e conformità).

### Protezione dei dati e privacy

Tutto ciò che si dà a un servizio di IA può essere conservato, usato per l'addestramento o esposto, a seconda del servizio e dei termini. Ticket, log e trascrizioni di chat contengono spesso dati personali, credenziali e informazioni aziendali riservate. Prima di usare qualunque strumento di IA con dati reali, scopri dove vanno i dati, chi può vederli, per quanto tempo sono conservati e se sono usati per addestrare modelli, e applica la tua politica di sicurezza delle informazioni (vedi Argomento 3.13 — Gestione della sicurezza delle informazioni). Rimuovi o sostituisci i dati personali e segreti prima di incollarli in uno strumento che non hai approvato.

### Responsabilità e trasparenza

Una persona o un team deve restare responsabile delle decisioni a cui l'IA contribuisce. Quando l'IA redige una risposta, è responsabile chi la invia. Quando l'IA suggerisce una causa radice, è responsabile chi indaga di verificarla. Di' ai clienti quando parlano con un sistema automatico, dove la legge, un contratto o l'equità lo richiedono, e offri una via per arrivare a una persona. Conserva registrazioni di ciò che è stato chiesto all'IA e di ciò che ha prodotto per le decisioni significative, come faresti per altri strumenti (vedi Argomento 5.1 — Gestione agile dei servizi per le evidenze).

### Pregiudizio ed equità

I sistemi di IA imparano da dati che riflettono decisioni e lacune del passato. Un assistente di triage addestrato su ticket storici può trattare alcuni gruppi di utenti o alcuni tipi di problemi come meno prioritari. Verifica gli output tra i gruppi, coinvolgi persone con prospettive diverse nei test e osserva gli schemi. Le fonti lette per questa guida non approfondiscono il pregiudizio, quindi questa è una cautela generale, non un risultato.

### Misurare l'IA

Misura la qualità e l'effetto di ogni passaggio di IA, non solo il suo volume: quanto spesso gli esseri umani lo scavalcano, quanto spesso sbaglia, quanto tempo richiedono i compiti con e senza di esso e che cosa dicono gli utenti (vedi Argomento 5.6 — Metriche e misurazione). Sii cauto con le cifre dei fornitori; le dichiarazioni di beneficio dell'articolo sull'AIOps poggiano su una sola fonte.

### Competenze e prompt

La competenza pratica di lavorare con l'IA comprende scrivere istruzioni chiare, fornire il materiale giusto, chiedere l'incertezza e verificare l'output. L'Argomento 6.3 — Competenze e prompt per l'IA lo tratta in dettaglio.

### Limiti delle fonti

L'articolo sull'AIOps non contiene critiche e le sue cifre sui benefici vengono da una sola fonte; l'articolo sull'allucinazione è segnalato come bisognoso di aggiornamento ed è stato letto in parte; la pagina del NIST non descrive le funzioni del framework; e la pagina di PeopleCert non spiega che cosa dica ITIL 5 sull'IA. Questo argomento offre quindi un resoconto prudente e lascia i dettagli alle fonti primarie.

## Buone pratiche

1. **Inizia con un uso a basso rischio e una domanda chiara.** Scegli un compito in cui gli errori costano poco e sono facili da intercettare, come redigere un riassunto per uso interno, e definisci che cosa significa successo.
2. **Mantieni una persona responsabile.** Nomina chi è responsabile di ciò a cui l'IA contribuisce e richiedi una revisione per tutto ciò che raggiunge un cliente, cambia la produzione o assume un impegno.
3. **Ancora le risposte al materiale approvato.** Dove usi l'IA per le risposte, collegala alla tua base di conoscenza e mostra la fonte. Fai in modo che dica "non lo so" quando non ne ha una.
4. **Proteggi i dati.** Decidi quali dati possono andare a quale strumento, rimuovi i dati personali e segreti e usa strumenti approvati con termini che hai letto. Coinvolgi presto il personale di sicurezza e legale.
5. **Prova con casi reali.** Raccogli un insieme di ticket e incidenti reali con risposte note, esegui l'IA su di essi e registra dove fallisce. Ripeti dopo qualsiasi cambio di strumento o impostazioni.
6. **Verifica affermazioni e riferimenti.** Controlla nomi, numeri, citazioni e procedure sulle fonti, come mostrano i casi delle citazioni giudiziarie inventate. Non accettare mai riferimenti che non hai visto.
7. **Sii onesto con i clienti.** Di' quando risponde un sistema automatico, dove conta, e offri una via facile per arrivare a una persona.
8. **Fai attenzione al pregiudizio.** Rivedi gli output tra gruppi di utenti e tipi di problemi e coinvolgi persone in grado di individuare le lacune. Adegua o interrompi l'uso dove compare un danno.
9. **Misura qualità ed effetto.** Monitora tassi di scavalcamento, tassi di errore, tempo risparmiato e opinioni degli utenti. Confronta con il processo senza IA e sii scettico verso le cifre dei fornitori.
10. **Conserva le registrazioni.** Per le decisioni significative, conserva ciò che è stato chiesto e prodotto, chi lo ha rivisto e che cosa è stato deciso. Sostiene la responsabilità e l'audit.
11. **Usa un framework di rischio.** Adotta un approccio riconosciuto, come l'AI RMF del NIST o una politica organizzativa sull'IA, per strutturare le decisioni su dove l'IA è consentita. Trattalo come una guida al ragionamento.
12. **Forma le persone.** Insegna al personale come funzionano gli strumenti, dove falliscono e che cosa è consentito. Aggiorna la formazione al cambiare di strumenti e regole.

## Domande da discutere con il team

**Dove stiamo già usando l'IA, ufficialmente o no?**

Chiedilo con onestà. Il personale usa spesso strumenti pubblici con ticket reali. Lo scopo non è punire ma capire. Elenca gli usi e i dati coinvolti. Discuti quali sono accettabili e quali richiedono una via più sicura. Concorda una breve politica.

**Con quale compito vorremmo più aiuto, e che cosa succede se l'IA sbaglia?**

Scegli un compito e percorri il caso di fallimento. Se la conseguenza è un'e-mail di scuse, il rischio è piccolo; se è un'istruzione sbagliata a un cliente, il rischio è maggiore. Aiuta a ordinare gli usi per rischio. Scegli un primo pilota con danno limitato.

**Come sapremmo che una risposta dell'IA è sbagliata?**

Chiedi chi controlla le risposte e come. Risposte comuni: nessuno, o la persona che ha chiesto. Discuti fonti, test e seconde revisioni. Concorda un controllo minimo per ogni tipo di uso.

**Quali dati ci sentiamo a nostro agio nel mettere in uno strumento di IA, e quali no?**

Raccogli i tipi: ticket, log, nomi di clienti, credenziali, contratti. Segna ciascuno come accettabile, accettabile dopo la rimozione delle parti sensibili, o mai. Verifica con sicurezza e ufficio legale. Scrivilo come guida di una pagina.

**Chi è responsabile quando una decisione assistita dall'IA va male?**

Usa un esempio passato di decisione assistita da uno strumento. Chiedi chi ha risposto. Concorda che una persona nominata resti responsabile e quali evidenze dovrebbe conservare. Annota ogni lacuna in cui nessuno lo sarebbe.

**Che cosa ci convincerebbe che vale la pena tenere uno strumento?**

Chiedi al team di descrivere le evidenze che accetterebbe: tempo risparmiato con qualità uguale o migliore, meno errori, soddisfazione degli utenti. Discuti come raccoglierle in una prova. Concorda una data di revisione.

## Nella pratica: un esempio di ITIL agile

Il service desk IT di un'agenzia fiscale nazionale gestisce circa 1.200 contatti a settimana dal personale, molti su domande di routine. Il responsabile del desk propone un assistente di IA che suggerisca risposte dalla base di conoscenza e rediga risposte. Il responsabile della sicurezza dell'agenzia è preoccupato per i dati personali nei ticket e per le risposte sbagliate che raggiungerebbero il personale.

Concordano un pilota limitato. L'assistente lavora solo da articoli di conoscenza approvati, mostra da quale articolo viene ogni suggerimento e dice quando non trova nulla di pertinente. Gli analisti rivedono ogni risposta suggerita prima di inviarla e lo strumento non può inviare da solo. I ticket sono scansionati alla ricerca di dati personali e credenziali, che vengono rimossi prima che l'assistente li veda. Prima del pilota si usa un insieme di prova di 200 ticket passati con risposte note e il team registra dove l'assistente fallisce. Il responsabile del desk e il responsabile della sicurezza concordano le misure: quanto spesso gli analisti modificano o rifiutano i suggerimenti, il tempo alla prima risposta e una breve domanda di soddisfazione per il personale. Il pilota dura tre mesi e il responsabile riferisce a una revisione congiunta che include un analista e un rappresentante del personale.

Alla fine gli analisti accettano la maggior parte dei suggerimenti per le domande comuni e il tempo di risposta per queste scende. L'insieme di prova mostra che l'assistente dà una risposta sicura ma sbagliata alle domande su una politica cambiata di recente, perché l'articolo di conoscenza era obsoleto. Restano alcuni problemi. Due analisti hanno cominciato a inviare i suggerimenti con pochi controlli quando erano occupati, un membro del personale con una domanda fuori dall'ordinario ha ricevuto una risposta banale che mancava il punto e i termini del fornitore sulla conservazione dei dati erano poco chiari. Il responsabile aggiunge una regola secondo cui i cambiamenti di politica devono aggiornare l'articolo di conoscenza prima di entrare in vigore, usa un controllo a campione delle risposte inviate da parte di un analista senior e chiede agli acquisti e al responsabile della sicurezza di chiarire i termini prima di estendere il pilota.

## Quattro prospettive

### Team di prodotto e di delivery

I team di delivery possono aggiungere funzionalità di IA ai prodotti e usare l'IA per scrivere codice e test. Verifica la correttezza e la sicurezza del codice generato, tieni i segreti fuori dai prompt e sii chiaro con gli utenti quando è coinvolta l'IA. Costruisci nel tuo servizio un monitoraggio del comportamento dell'IA.

### Team di servizio e di operations

I team operativi incontreranno l'IA nel monitoraggio, negli strumenti del desk e nell'analisi. Tratta i suggerimenti dell'IA come ipotesi, provali e conserva le registrazioni. Aiuta a definire quali dati possono essere usati e dai riscontri per migliorare il materiale di ancoraggio.

### Leadership e governance

I leader stabiliscono politica, propensione al rischio e responsabilità per l'IA. Chiedi un inventario degli usi, un framework di rischio ed evidenze dai piloti, non dichiarazioni dei fornitori. Assicurati che il personale legale, di sicurezza e di privacy sia coinvolto fin dall'inizio.

### Clienti e utenti

Clienti e utenti dovrebbero essere informati quando hanno a che fare con un sistema automatico, dove conta, e avere una via per arrivare a una persona. Segnala risposte sbagliate o strane, perché sono evidenze. Chiedi ai fornitori come proteggono i tuoi dati e come verificano l'output dell'IA.

## Modalità di fallimento comuni

- **Fidarsi di un output non verificato.** Fatti fabbricati raggiungono i clienti. Ancora invece le risposte al materiale approvato e verifica prima di inviare.
- **IA ombra.** Il personale incolla dati reali in strumenti pubblici. Fornisci invece strumenti approvati e una politica chiara sui dati.
- **Nessuna persona responsabile.** Nessuno risponde delle decisioni assistite dall'IA. Nomina invece un responsabile e richiedi la revisione.
- **Credere alle cifre dei fornitori.** Le dichiarazioni di beneficio non sono verificate. Prova invece sui tuoi casi e misura.
- **Ancoraggio obsoleto.** La base di conoscenza è sbagliata e l'IA la ripete. Mantieni invece gli articoli aggiornati e con un responsabile.
- **Pregiudizio nascosto.** Alcuni utenti o problemi sono trattati peggio. Prova invece tra i gruppi e rivedi gli output.
- **Automatizzare prima di capire.** L'IA agisce sulla produzione senza controlli. Inizia invece con suggerimento e revisione e passa all'azione solo con solide salvaguardie.
- **Nessuna registrazione.** Le decisioni non possono essere sottoposte ad audit. Conserva invece log di ciò che è stato chiesto, prodotto e deciso.

## Modello di maturità

| Dimensione | Avvio | Sviluppo | Standardizzazione | Gestione | Orchestrazione |
|---|---|---|---|---|---|
| Politica e responsabilità | L'uso è ad hoc e non registrato | Alcuni team hanno regole | Una politica scritta, un inventario degli usi e responsabili nominati | La conformità alla politica e gli incidenti sono rivisti | La politica è allineata tra team, fornitori e regolatori |
| Qualità e ancoraggio | L'output è considerato affidabile per impostazione predefinita | Alcuni controlli sugli usi importanti | Le risposte sono ancorate a fonti approvate e provate su casi reali | Tassi di errore e di scavalcamento sono misurati e se ne tiene conto | Ancoraggio e test sono condivisi e migliorati tra i team |
| Protezione dei dati ed equità | I dati sono incollati liberamente | Esistono alcune regole sui dati | Regole di gestione dei dati e controlli sul pregiudizio sono routine | Incidenti sui dati e risultanze sull'equità sono monitorati e corretti | Pratiche sui dati e sull'equità sono coordinate nell'organizzazione e con i fornitori |
| Valore e apprendimento | Il valore è presunto | Si eseguono alcune prove | I piloti hanno misure e decisioni concordate | Benefici e costi sono misurati rispetto a riferimenti di base | L'apprendimento dall'uso dell'IA si diffonde continuamente tra i servizi |

## Checklist

- [ ] Abbiamo un inventario di dove l'IA è usata nei nostri servizi o attorno ad essi, compreso l'uso non ufficiale.
- [ ] Una persona nominata è responsabile di ogni uso assistito dall'IA.
- [ ] Una politica scritta dice quali dati possono andare in quali strumenti.
- [ ] I dati personali e i segreti sono rimossi o mascherati prima dell'uso con strumenti non approvati per essi.
- [ ] Le risposte mostrate ai clienti o usate nelle decisioni sono ancorate a materiale approvato e riviste.
- [ ] Abbiamo un insieme di prova di casi reali e lo rieseguiamo dopo i cambiamenti.
- [ ] I clienti sono informati quando risponde un sistema automatico, dove conta, e hanno una via per arrivare a una persona.
- [ ] Misuriamo tasso di scavalcamento, tasso di errore, tempo risparmiato e opinioni degli utenti.
- [ ] Si conservano registrazioni per le decisioni significative assistite dall'IA.
- [ ] Il personale legale, di sicurezza e di privacy ha rivisto il nostro uso e i termini dello strumento.

## Prompt per l'IA

**Scopo: redigere un inventario dell'uso dell'IA a partire da ciò che le persone ti dicono.**

```text
Help me structure an inventory of AI use in our service organization.

What people have told us they use AI for (paste notes; remove names): [paste].
Tools mentioned: [list].
Types of data involved, as far as we know: [list].

Produce a table with: use, tool, data involved, who is accountable (use "unknown" if not given), risk if wrong (low, medium, high with a one-sentence reason from my notes), and one question to ask. Do not guess about tools or terms I did not mention. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: progettare un insieme di prova per un assistente di IA.**

```text
Design a test set for an AI assistant that suggests answers to service desk questions.

The knowledge sources it will use: [describe].
Types of question we get: [list with rough share if you know].
Cases where the right answer is "not in the knowledge base" or "escalate": [describe].

Propose a structure for 100-200 test cases (categories, how to choose real examples, how to record the correct answer and its source), how to score answers (correct, partly correct, wrong, confidently wrong, correctly declined), and how to repeat after changes. Do not invent test content; tell me what to collect. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: scrivere una politica di una pagina sull'uso dell'IA per un team.**

```text
Draft a one-page AI use policy for [team].

Tools approved: [list, or write "none yet"].
Data we handle (types and sensitivity): [list].
Rules we must follow, with source text from legal, security, or contracts: [paste, or write "none known"].
Roles: [list].

Write plain-language sections: what AI may be used for, what data may and may not be put into tools, what must be checked by a person before use, who is accountable, how to record significant uses, how to report problems. Mark every item that is an assumption. Do not state that any law requires something unless I pasted its text. Ask clarifying questions first, and list what you are unsure of.
```

**Scopo: rivedere una risposta generata dall'IA prima che vada a un utente.**

```text
Here is a draft answer that an AI tool produced for a user question.

The user's question: [paste, with personal data removed].
The knowledge article(s) the answer should be based on: [paste].
The draft answer: [paste].

Check the draft against the article only. List statements that are supported by the article (quote the part), statements that are not supported, anything missing that the user would need, and the tone. Suggest a corrected version that uses only the article. Do not add facts. List what you are unsure of.
```

## Competenze per l'IA

- [prompt-engineering](../../../../skills/prompt-engineering/SKILL.md): da usare per scrivere prompt chiari che forniscano il materiale giusto e chiedano l'incertezza.
- [machine-learning-model-card](../../../../skills/machine-learning-model-card/SKILL.md): da usare per documentare a che cosa serve un modello, come è stato provato e i suoi limiti.
- [data-governance](../../../../skills/data-governance/SKILL.md): da usare per decidere quali dati possono essere usati con quali strumenti.
- [legal-data-privacy-compliance](../../../../skills/legal-data-privacy-compliance/SKILL.md): da usare per preparare domande per il personale legale e di privacy sull'uso dell'IA.
- [risk-register](../../../../skills/risk-register/SKILL.md): da usare per registrare i rischi legati all'IA, i responsabili e i trattamenti.

## Fonti principali

- **AIOps** (Wikipedia): una breve descrizione dell'IA per le operazioni IT, delle sue capacità e dei benefici dichiarati, senza critiche.
- **Hallucination (artificial intelligence)** (Wikipedia): cause, esempi e idee di mitigazione per l'output falso.
- **AI Risk Management Framework** (NIST): il framework volontario e il suo profilo per l'IA generativa; leggi il framework stesso per i dettagli.
- **ITIL certifications** (PeopleCert): le dichiarazioni pubbliche del titolare sul nuovo ITIL e sul suo modulo di governance dell'IA.

## Riferimenti

1. AIOps — Wikipedia — https://en.wikipedia.org/wiki/AIOps
2. Hallucination (artificial intelligence) — Wikipedia — https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)
3. AI Risk Management Framework — NIST — https://www.nist.gov/itl/ai-risk-management-framework
4. ITIL certifications — PeopleCert — https://www.peoplecert.org/browse-certifications/it-governance-and-service-management/ITIL-1
5. Retrieval-augmented generation — Wikipedia — https://en.wikipedia.org/wiki/Retrieval-augmented_generation
6. Artificial intelligence — Wikipedia — https://en.wikipedia.org/wiki/Artificial_intelligence
7. Large language model — Wikipedia — https://en.wikipedia.org/wiki/Large_language_model
8. Algorithmic bias — Wikipedia — https://en.wikipedia.org/wiki/Algorithmic_bias
9. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
