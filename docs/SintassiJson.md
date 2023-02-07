# Sintassi del file di configurazione
La sintassi di questo file json prevede due nodi:

- *skipCheck* : opzionale
- *whiteList* : mandatorio

il nodo *skipCheck* è di tipo booleano ed indica se inibire tutto il processo di validazione temporale dei certificati. il valore di default è false, pertanto se non presente l'utility effettuerà il controllo di validità. 

il nodo *whiteList* contiene un array di nomi di certificati (estensione inclusa) che non devono essere sottoposti al controllo di validità da parte dell'utility. Sono ammessi certificati con estensione .cer e .der.

Un esempio di contenuto del file di configurazione è il seguente:


    {
       "skipCheck":false,
       "whiteList":[
          "idpInt.cer",
          "idpLeaf.cer",
          "OLD_Intermediate_appRegistry.der",
          "OLD_appRegistry.der"
       ]
    }

