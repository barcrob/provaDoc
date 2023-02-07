# Integrazione con il progetto
L'integrazione con un progetto XCode può avvenire inserenso il seguente Script in una delle Build Phase prima del processo di compilazione.

    xcrun --sdk macosx swiftc -parse-as-library $SCRIPT_INPUT_FILE_0 \
        $SCRIPT_INPUT_FILE_1 \
        $SCRIPT_INPUT_FILE_2 \
        $SCRIPT_INPUT_FILE_3 \
        $SCRIPT_INPUT_FILE_4 \
        $SCRIPT_INPUT_FILE_5 \
        $SCRIPT_INPUT_FILE_6   -o CompiledScript
        ./CompiledScript "ClientConfigurations/${SCHEME_NAME_CONFIG}-configuration.json" "${PROJECT}/"
        rm -f ./CompiledScript
        
    status=$?

    if [ $status -eq 0 ]
    then
        echo "SCRIPT COMPILATION SUCCESS!!!"
        exit 0
    else
        echo "SCRIPT COMPILATION FAILED!!!"
        exit 1  
    fi 

Dove la lista di file di input sono definiti tramite interfaccia di XCode:

 ![InputFilesList](images/InputFilesList.png) 
 
 Come si può vedere lo script prende in ingresso la lista dei file swift della compilation utility, li compila per piattaforma macos e lancia l'eseguibile così ottenuto con gli opportuni argomenti. 
 
 I file del codice della compilation utility possono essere inseriti nell'alberatura della directory del progetto principale tramite un git submodule, piuttosto che trovarsi nello stesso repository del progetto client. Inoltre tale submodule deve puntare al branch di release (attualmente "release_0_1_0").

