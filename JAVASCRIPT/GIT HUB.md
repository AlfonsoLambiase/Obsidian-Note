Creare una repository visual studio code:

- apri il terminare usando Ctrl + ò
- mkdir nome progetto (crea nuova cartella)
- cd nome progetto ( mi sposto nella cartella appena creata )
- git init (inizializza repository git)
- echo “# nome progetto” >> [README.](http://README.MD)md ( aggiungi un file readme)
- git add .
- git commit -m ( aggiungi e conferma i tuoi file) (inizializza la repository)
- a questo punto crea una nuova repository su github e copia l’url
- git remote add origin URL REPOSITORY (aggiungi remote)
- Git push -u origin master (invia i file a github)

###### **CONFIGURARE GIT**

Esistono tre livelli di configurazione: Local, Global e System.

Local: si riferisce solo al repository sul quale ci troviamo. Global: fa riferimento all’intero utente del sistema operativo. System: fa riferimento a tutti gli utenti del sistema operativo.

Per controllare l’intera configurazione possiamo usare il comando git config -l.

- **NAVIGA NELLA CARTELLA DEL TUO PROGETTO GIT.**
==cd /percorso/del/tuo/progetto==

- **CONFIGURA IL TUO USERNAME E LA TUA EMAIL LOCALMENTE**
==git config [user.name](http://user.name/) "IlTuoNome" git config user.email "[iltuomail@example.com](mailto:iltuomail@example.com)"==

- **VERIFICA LA CONFIGURAZIONE LOCALE**
==git config --list==


- **CONFIGURAZIONE GLOBALE**

Configura il tuo username e la tua email:
==git config --global [user.name](http://user.name/) "IlTuoNome" git config --global user.email "[iltuomail@example.com](mailto:iltuomail@example.com)"==

Verifica la configurazione globale:
==git config --global --list==

**COPIA REPOSITORY GIT**
Clona l’intero contenuto repository remoto
==git clone \filegithub\ls -li = controllare all’interno delle cartelle==

**COME CREARE UNA COMMIT IN GIT**
aprire il terminale e usare CD per navigare nei file, aggiungere il file alla tua stanging aerea.

- per aggiungere un singolo file:
==git add nomefile.txt==

- per aggiungere tutti i file modificati
==git add .==

- Crea la tua commit
dopo aver aggiunto i file, crea la commit con un messaggio descrittivo. è importante fornire un messaggio chiaro delle modifiche apportate.
==git commit -m “messaggio della commit”==

- Verifica la tua commit
puoi controllare lo stato della tua commit utilizzando il comando:
==git log==


**ESEMPIO COMPLETO**
- git add .
- git commit -m "Aggiunta nuove funzionalità"
- git log


###### **COS’E’ E COME CREARE UNA BRANCH IN GIT**

Un branch in Git è una linea di sviluppo indipendente che permette di lavorare su diverse funzionalità o correzioni senza influenzare il ramo principale (solitamente chiamato "master" o "main"). Ecco alcuni punti chiave sui branch in Git:

- I branch permettono di creare una copia del codice su cui lavorare separatamente, senza influenzare il ramo principale
- Per visualizzare i branch esistenti, si usa il comando: `git branch`
- Per creare un nuovo branch, si usa: `git branch nome_del_branch`
- Per passare a un branch specifico, si usa: `git checkout nome_del_branch`
- Il branch attivo è evidenziato con un asterisco quando si usa il comando `git branch`

I branch sono utili per sviluppare nuove funzionalità, correggere bug o sperimentare senza rischiare di compromettere il codice principale. Una volta completato il lavoro su un branch, è possibile unirlo (merge) al ramo principale per integrare le modifiche.

- Innanzitutto visualizza i branch esistenti utilizzando il comando: git branch
- per creare un nuovo branch usa: git branch _stile(nome branch)_
- dopo aver creato il branch puoi passarci usando git checkout _stile_
- verifica utilizzando di nuovo git branch (il branch è evidenziato con un asterisco)

###### **CREARE UNA CARTELLA CSS IN BRANCH**

- Si può creare la cartella utilizzando il testo o il codice, dal terminale si crea utilizzando il comando touch: touch style.css, una volta creato apri il codice e scrivi il tuo css.
- aggiungi il file alla tua stanging aerea con: git add style.css
- crea una commit: git commit -m “aggiunto file CSS style.css”
    

###### **IMPORTA FILE CSS IN INDEX.HTML**

- Per aggiungere le modifiche: git add index.html
- crea commit per registrare le modifiche: git commit -m “importo style.css in index.html”

###### **SALVARE CAMBIAMENTI IN GIT**

- Dopo aver apportato le modifiche, si deve aggiungere il file da salvare alla stanging aerea, si utilizza il comando: git add index.html, se voglio aggiungere tutti i file modificati si utilizza git add .
- crea una commit per registrare le modifiche: git commit -m “messaggio descrittivo delle modifiche”
- git status per controllare lo stato
- git log per vedere tutte le modifiche apportate alla commit

###### **UNIRE I BRANCH**

1. assicurarsi di aver salvato tutte le modifiche poi passa al branch master con: git checkout master
2. facoltativo; git pull origin: master per aggiornare
3. una volta che ti trovi nel branch master puoi unire il branch stile utilizzando il comando git merge :stile.

**Riepilogo:**

- git add . git commit -m "Commit delle modifiche nel branch stile"
- git checkout master
- git pull origin master
- git merge stile
- git log

# **Merge**

- faccio il commit nel mio branch
- passo sul branch principale (master)
- git pull origin master per prendere le modifiche
- git merge (nome-branch)
- git log(facoltativo)