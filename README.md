# 🎓 Progetto di Tesi in Calcolo Numerico: Analisi di Reti Sociali e Commerciali

**Autore:** Lovreglio Francesco Pio  
**Relatrice:** Dott.ssa Falini Antonella  

Questo repository contiene i materiali di supporto, i codici sorgente, i dataset e i risultati sperimentali relativi al mio Progetto di Tesi in Calcolo Numerico. L'obiettivo della ricerca è analizzare e confrontare l'efficacia degli algoritmi di ranking **PageRank**, **HITS** e di un approccio di ottimizzazione algebrica ai **Minimi Quadrati**, applicati a topologie di rete complesse formalizzate attraverso la teoria dei grafi.

Per garantire la privacy e aggirare i vincoli legati ai dati reali, i dataset analizzati sono stati interamente simulati e generati tramite tecniche avanzate di *prompting* su modelli LLM (Intelligenza Artificiale).

---

## 🔍 I Casi di Studio

Il progetto si articola in due domini di applicazione principali:

### 1. Influencer Marketing (Network Analysis)
Modellazione di una community social come grafo orientato, dove i **nodi** rappresentano gli utenti e gli **archi** le interazioni (es. *follow*, menzioni).
* L'algoritmo **PageRank** è stato applicato per superare le metriche quantitative superficiali (il mero numero di follower) e calcolare la *reale autorevolezza* degli utenti.
* L'algoritmo **HITS** è stato utilizzato per distinguere tematicamente la rete in **Hub** (utenti che raccolgono e ricondividono contenuti) e **Authority** (esperti e punti di riferimento che creano contenuti originali).
* La formulazione ai **Minimi Quadrati** è stata introdotta per ricalibrare matematicamente le gerarchie, dimostrando una sensibilità leggermente maggiore rispetto all'algoritmo PageRank nella valutazione delle community locali.

### 2. E-commerce e Cross-Selling
In questo caso di studio la topologia cambia: i **nodi** diventano i singoli prodotti del catalogo e gli **archi** le loro correlazioni di acquisto o visualizzazione.
* L'algoritmo **PageRank** identifica i prodotti centrali o *best-seller* all'interno di specifici cluster di articoli affini.
* L'algoritmo **HITS** categorizza le dinamiche di acquisto, individuando come **Hub** i prodotti base/civetta (es. uno smartphone) che generano percorsi logici verso molteplici accessori, i quali assumono il ruolo di **Authority**.
* L'approccio ai **Minimi Quadrati** interviene per validare la stabilità gerarchica e ottimizzare il punteggio dei prodotti, confermando o smentendo il posizionamento all'interno delle categorie merceologiche bilanciate.

---

## 🌐 Scalabilità e Dimensioni delle Reti

Per testare a fondo la robustezza e le performance degli algoritmi, le simulazioni sono state condotte su due differenti scale di grandezza per ogni scenario:

* **Reti a scala ridotta (100 nodi):** Ambienti fittizi e controllati. Sono stati utilizzati per la validazione teorica, per generare le visualizzazioni spaziali dei grafi e per osservare in modo granulare il comportamento matematico dei singoli nodi (es. l'individuazione di specifici Micro-Hub).
* **Reti su larga scala (1.000.000 di nodi):** Ambienti che simulano scenari realistici e volumi di traffico paragonabili a quelli di veri social network o grandi piattaforme e-commerce. Sono stati utilizzati per testare la complessità computazionale, la convergenza asintotica e la scalabilità effettiva dei modelli numerici.

---

## 📂 Struttura del Repository

Tutto il materiale prodotto per la sperimentazione è liberamente scaricabile e consultabile, organizzato in apposite cartelle divise per caso di studio. Nello specifico, il repository contiene:

* 💻 **Codici Sorgente (Python):** Gli script e i notebook (`.ipynb`) sviluppati per il calcolo degli algoritmi (PageRank, HITS, Minimi Quadrati) e per la generazione delle visualizzazioni dei grafi tramite librerie dedicate.
* 🗄️ **Dataset di Input:** Le matrici sparse in formato `.csv` generate tramite LLM per i vari scenari di test (sia per i grafi da 100 nodi che per quelli da 1.000.000 di nodi).
* 📊 **Risultati:** I risultati finali ottenuti testando i dataset generati con ogni algoritmo
