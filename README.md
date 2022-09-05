## Sommario
1. [Introduzione](README.md#introduzione)
2. [Business Task](README.md#task)
3. [Data](README.md#data)
4. [Elaborazione e Pulizia](README.md#elaborazione-e-pulizia)
5. [Analisi](README.md#analisi)
6. [Conclusioni e Raccomandazioni](README.md#conclusioni)

## Introduzione

Il progetto fa parte del **Corso di certificazione di Google Data Analytics**. Lo scenario prevede l'analisi dei dati di viaggio della società di Bike Sharing Cyclistic.

L'azienda opera a Chicago con circa 6000 biciclette in 700 stazioni.
L'azienda dispone di due modelli per l’utilizzo del servizio: corsa singola chiamata "**casual**" e abbonamenti annuali chiamati "**member**". 

Il team esecutivo è alla ricerca di modi per migliorare la crescita e sta valutando una strategia di marketing.
Massimizzare il numero di membri annuali sarà la chiave per la crescita futura in quanto garantisce la sostenibilità finanziaria e la fidelizzazione dei clienti.
Le analisi permettono di aiutare a elaborare strategie di marketing efficaci volte a convertire i ciclisti occasionali in membri abbonati.

## Business Task

In qualità di **Junior Data Analyst** nel team di analisi di marketing di Cyclistic, ho avuto il compito di presentare ai dirigenti i miei risultati e le mie raccomandazioni dopo aver esplorato, elaborato e analizzato a fondo tutti i dati rilevanti.

A tal proposito ho cercato di rispondere ad una semplice domanda “ In che modo i membri annuali e i ciclisti occasionali utilizzano le biciclette Cyclistic in modo diverso? “

Obbiettivo: Pulire, analizzare e visualizzare i dati per osservare come i ciclisti occasionali utilizzano le biciclette a noleggio in modo diverso dai ciclisti membri annuali.

Per questo progetto vista la mole di dati ho deciso di utilizzare sia R quanto concerne la pulizia e l’analisi, per affiancare successivamente Tableau delle rappresentazioni grafiche più dettagliate con la creazione di una Dashboard con possibilità successiva di sviluppo ed implementazione di processi di automazione per Analisi Live.

## Data
È importante conoscere la provenienza dei nostri dati e capire la veridicità e l’affidabilità di essi, al fine di ottenere un analisi più imparziale possibile senza criticità dovuti ad un inconsistenza dei dati o ad altri problemi o BIAS legati ad essi.

Fonte dei dati: [Dati pubblici di Motivate International Inc.](https://divvy-tripdata.s3.amazonaws.com/index.html) (Divvy Bicycle Sharing Service di Chicago) ai sensi della presente [licenza](https://www.divvybikes.com/data-license-agreement) .

Data Frame: I dati colpiscono una fascia temporale cha va dal 2013 in poi e sono disponibili in formato `.csv`

## Elaborazione e Pulizia
* Dati scaricati per la manipolazione e l'analisi tramite R.
* Manipolazione dei dati per renderli coerenti tra di loro e quindi consolidarli in un unico data frame.
* Verifica presenza di duplicati
* Ricerca ed eliminazione dei rows nulli o inconsistenti 

Per facilitare l'analisi, sono state 
* Separate le date per ogni singolo viaggio, creando delle colonne (data,year,month,day,day_of_week)
* Aggiunta colonna ride_length per avere la durata di ogni singolo viaggio.
* Rimoviamo dei dati cha hanno una durata inferiore e uguale 0 secondi.

## Analisi


## Conclusioni
