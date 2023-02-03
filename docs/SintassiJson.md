# Sintassi del json
Questo file json contiene la lista dei certificati da escludere dalla valutazione da parte dell'utility. La sintassi di questo file prevede la presenza di un nodo mandatorio:

 - *whiteList* 

che contiene un array. Ogni elemento dell'array è il nome del certificato da skippare, comprensivo dell'estensione (.cer o .der). Es:


    {
       "whiteList":[
          "idpInt.cer",
          "idpLeaf.cer",
          "OLD_Intermediate_appRegistry.der",
          "OLD_appRegistry.der"
       ]
    }

