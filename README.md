## Sommario
1. [Introduzione](README.md#introduzione)
2. [Business Task](README.md#business-task)
3. [Data Sources](README.md#data-sources)
4. [Data Cleaning](README.md#data-cleaning)
5. [Analysis](README.md#analysis)
6. [Conclusioni e Raccomandazioni](README.md#conclusioni)

## Introduzione

Il progetto fa parte del **Corso di certificazione di Google Data Analytics**. Lo scenario prevede l'analisi dei dati di viaggio della società di Bike Sharing Cyclistic.

L'azienda opera a Chicago con circa 6000 biciclette in 700 stazioni.
L'azienda dispone di due modelli per l’utilizzo del servizio: 
* corsa singola "**casual**" 
* abbonamento annuale "**member**". 

Il team esecutivo è alla ricerca di modi per migliorare la crescita e sta valutando strategie di marketing efficaci volte a convertire i ciclisti occasionali in membri abbonati.
Massimizzare il numero di membri annuali sarà la chiave per la crescita futura in quanto garantisce la sostenibilità finanziaria e la fidelizzazione dei clienti.

## Business Task

In qualità di **Junior Data Analyst** nel team di analisi di marketing di Cyclistic, ho avuto il compito di presentare ai dirigenti i miei risultati e le mie raccomandazioni dopo aver esplorato, elaborato e analizzato a fondo tutti i dati rilevanti.

A tal proposito ho cercato di rispondere ad una semplice domanda *“ In che modo i membri annuali e i ciclisti occasionali utilizzano le biciclette Cyclistic in modo diverso? “*

* **Obbiettivo**: Pulire, analizzare e visualizzare i dati per osservare come i ciclisti occasionali utilizzano le biciclette a noleggio in modo diverso dai membri annuali.

> Per questo progetto vista la mole di dati, ho deciso di utilizzare R per quanto concerne la pulizia e l’analisi, ed affiancare successivamente Tableau per  rappresentazioni grafiche più dettagliate con la creazione di una Dashboard con possibilità successiva di sviluppo ed implementazione di processi di automazione per Analisi Live.

## Data Sources

È importante conoscere la provenienza dei nostri dati e capire la veridicità e l’affidabilità di essi, al fine di ottenere un analisi più imparziale possibile senza criticità dovuti ad un inconsistenza o ad altri problemi o BIAS legati ad essi.

Fonte dei dati: [Dati pubblici di Motivate International Inc.](https://divvy-tripdata.s3.amazonaws.com/index.html) (Divvy Bicycle Sharing Service di Chicago) ai sensi della presente [licenza](https://www.divvybikes.com/data-license-agreement) .

Descrizione dati: 
* I dati colpiscono una fascia temporale cha va dal 2013 in poi e sono disponibili in formato `.csv` 
* I dati contengono queste colonne: `ride_id`, `rideable_type`, `started_at`, `ended_at`, `start_station_name`, `start_station_id`, `end_station_name`, `end_station_id`, `start_lat`, `start_lng`, `end_lat`, `end_lng`, `member_casual`
* Ogni file contiene circa 100.000+ record

## Data Cleaning

RStudio - [R Documentation](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Cyclistic-Notebook.Rmd)
1. Download e importazione dei dati in R Studio.
2. Manipolazione dei dati per renderli coerenti tra di loro e quindi consolidarli in un unico data frame.
3. Ricerca ed eliminazione di duplicati o campi nulli
4. Per facilitare l'analisi, sono state:
  - Separate le date per ogni singolo viaggio, aggiungendo delle colonne (`data`,`year`,`month`,`day`,`day_of_week`)
  - Aggiunta colonna `ride_length` per avere la durata di ogni singolo viaggio.
  - Rimozione dei dati cha hanno una durata viaggio uguale o inferiore a 0 sec (dovuti da errori di inserimento)
  - Separazione dei dati relativi ai "TEST" eseguiti per la manutenzione.
5. Analisi con calcolo degli indici di posizione
6. Creazione di grafici a barre, a linea, ad area ecc.


## Analisi


## Conclusioni
