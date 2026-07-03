# Analisi degli incidenti stradali nei comuni italiani



### Progetto Capstone finale per Boolean Academy - corso di Data Analytics



##### La domanda di business



Un'azienda che si occupa di sicurezza stradale vuole capire dove conviene investire in Italia per ridurre gli incidenti, individuando i comuni a maggior rischio. L'analisi parte dai dati ufficiali ISTAT (2001 - 2023) e arriva a una raccomandazione geografica concreta.



##### Cosa contiene il repository



* Final Project Nicola Vessio.ipynb: notebook di preparazione dei dati, download automatico, pulizia, unione delle fonti e calcolo delle metriche.
* Final Project Nicola Vessio pt 2.ipynb: notebook di analisi, esplorazione, clustering per profili di rischio, test statistico e analisi geografica con la mappa finale.
* Report Final Assignment Nicola Vessio.pbix: dashboard Power BI interattiva a 5 pagine, che racconta il problema e la risposta di business.
* Deck Capstone Nicola Vessio.pdf: deck di presentazione (max 5 slide) sul processo e gli strumenti usati.
* df\_finale\_pulito.csv: dataset pulito e arricchito, una riga per comune e anno.
* metriche\_geo.csv: tabella per comune con metriche, gruppi di rischio e coordinate, usata per la mappa.
* main.csv e cartella CSV Situas: dati grezzi di supporto (coordinate e territorio).



##### Le fonti dei dati



Incidenti stradali: ISTAT, API SDMX ufficiale, endpoint https://esploradati.istat.it/SDMXWS/rest/data/41\_983, scaricati automaticamente dal notebook.

Popolazione e superficie dei comuni: ISTAT, banca dati SITUAS (https://situas.istat.it).

Coordinate geografiche dei comuni: dataset pubblico OpenDataSicilia (https://github.com/opendatasicilia/comuni-italiani).



##### Il metodo



* Pulizia e unione: i dati ISTAT sono stati puliti, aggregati per comune sui 23 anni e uniti a popolazione, superficie e coordinate.
* Metriche: per ogni comune sono state calcolate la densità di incidenti (per km²) e il dato pro capite (incidenti ogni 1000 abitanti), che misurano aspetti diversi del rischio.
* Profili di rischio: i comuni sono stati divisi in quattro gruppi con una matrice 2x2, incrociando le due metriche rispetto ai loro valori mediani.
* Scelta metodologica: sono stati esclusi i grandi centri urbani, per concentrare l'analisi sui comuni medio-piccoli aggredibili, che erano il vero bersaglio.
* Analisi geografica: i comuni a rischio sono stati mappati per individuare dove si concentrano. Il risultato indica la Lombardia, e in particolare la fascia Milano-Brescia-Bergamo, come area prioritaria.



##### Strumenti e tecnologie



Python: pandas e numpy per l'elaborazione, requests per il download, matplotlib e seaborn per i grafici.

Power BI: dashboard interattiva.

Git e GitHub: versionamento e pubblicazione del progetto.



##### Come riprodurre l'analisi



I notebook sono eseguibili dall'alto in basso (Restart \& Run All). Il primo notebook scarica e prepara i dati, generando df\_finale\_pulito.csv e metriche\_geo.csv; il secondo li analizza. Serve un ambiente Python (almeno versione 3.12.12) con le librerie sopra elencate.





*Nicola Vessio, Luglio 2026*

