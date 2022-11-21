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
È stato analizzato il set di dati finale contenente i dati di viaggio di circa 3,4 milioni di corse. 
Le visualizzazioni sono state sviluppate per osservare le tendenze diverse tra l'utilizzo da parte dei ciclisti occasionali e dei soci annuali.  

### Total numbers of rides by day
![chart-2](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Chart/Chart-2.png)
#### **Insights**
* I membri casual utilizzano maggiormente il servizio nel week-end.
* I menbri abbonati utilizzano il servizio con una media costante durante tutta la settimana.
* I membri abbonati costituiscono la maggior parte del business aziendale e massimizzare questo numero dovrebbe essere l'obiettivo a lungo termine.

### Density of ride times for User 
![chart-3](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Chart/Chart-3.png)
![chart-4](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Chart/Chart-4.png)
#### **Insights**
* I menbri abbonati utilizzano maggiormente il servizio con una durata del viaggio inferiore ai 15 minuti, prediligendo quindi tratte brevi.
* I membri casual utilizzano il servizio con tratte più lunghe ed una durata del viaggio prolungata ma una densità molto minore.

### Total number of ride by Month
![chart-5](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Chart/Chart-5.png)
![chart-7](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Chart/Chart-7.png)
#### **Insights**
* Il servizio viene usato maggiormente nel periodo estivo dell'anno, cioè nei mesi più caldi.
* La stagionalità del servizio nell'arco dell'anno è pressoché identica ad eccezione degli ultimi 3 mesi.
* I membri abbonati utilizzano il servizio negli ultimi 3 mesi dell'anno in modo estremamente maggiore rispetto ai membri casual.
* La durata del viaggio rimane sempre di lunga durata per i membri casual e di breve durata per gli abbonati.

### Total number of ride by Hour
![chart-8](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Chart/Chart-8.png)
![chart-9](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Chart/Chart-9.png)
#### **Insights**
* Il servizio viene usato maggiormente nelle ore di entrata ed uscita dal lavoro.
* Il servizio va calando man mano che l'termina la giornata, per poi riprende la mattina seguente.
* I membri abbonati continuano ad avere un durata del viaggio media sotto i 1000 secondi per viaggio.
* I membri casual effettuano viaggi di lunga percorrenza anche in orari notturni, presumibilmente per far ritorno a casa.

### Total number of ride by Ride type
![chart-10](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Chart/Chart-10.png)
#### **Insights**
* I membri abbonati utilizzano tutte le tipologie di bici senza particolari evidenze.
* I membri casual prediliggono utilizzo delle "classic bike".

### Top 10 Station
![chart-11](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Chart/Chart-11.png)
![chart-1](https://github.com/ManuelGaliotta/Cyclistic-Case-Study-Data-Analytics-Project/blob/main/Chart/Chart-1.png)
#### **Insights**
* La stazione "Streeter Dr & Grand Ave" è quella maggiormente utilizzata per far partire e terminare le corse con quasi 12000 corse.
* Subito dopo troviamo "Clark St & Elm St" con circa 7000 corse, che si posiziona poco sopra la media rispetto alle altre stazioni.

## Conclusioni
