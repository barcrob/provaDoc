# DOCUMENTAZIONE

# Introduzione
L'utility oggetto della presente documentazione è un command line tool che serve a verificare la validità temporale dei certificati.

## Utilizzo
Il comando prende in ingresso tre argomenti:

 - il path della directory in cui si trovano i certificati 
 - il path del file json di configurazione dell'utility
 - un flag opzionale "FORCE_CHECK_ENABLED" che, se presente, rende obbligatoria la presenza di almeno un certificato nella cartella dei certificati da validare. 
 
 tali parametri possono essere configurati direttamente nello schema di lancio del progetto XCode contenuto nel repository dell'utility. Di seguito uno screenshot di esempio:
 
 ![configurazioneArgomenti](docs/images/configurazioneArgomenti.png)
 
Nella root directory del repository è inoltre presente la cartella "CertificateCheckInputFiles". Tale cartella costituisce un esempio di alberatura di file da fornire in ingresso all'utility. Pertanto l'utente può copiare questa cartella nella propria HOME directory e lanciare l'utility.


[Sintassi del file di configurazione](docs/SintassiJson.md)

[Integrazione con un progetto XCode](docs/IntegrazioneConIlProgetto.md)
