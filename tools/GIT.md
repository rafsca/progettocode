# Cosa è Git?
Git è uno strumento che traccia le modifiche apportate ai file nel tempo. 
Piuttosto che salvare solo le ultime **versioni** dei file, Git tiene traccia delle modifiche apportate nel tempo, 
consentendo di visualizzare e ripristinare versioni precedenti dei file.

# Come utilizzarlo:

## Installazione di Git:
Puoi trovarlo sul sito ufficiale di Git [Sito Ufficiale](https://git-scm.com/), è disponibile per **Windows**, **macOS** e **Linux**.

## Configurazione iniziale:
Apeena dopo l'avvio è importante configurare il nome utente e l'email in Git, è possibile farlo grazie a dei semplici comandi da eseguire nel terminale.

```
git config --global user.name "IlTuoNome"
```

```
git config --global user.email "tua@email.com"
```

## Inizializzazione di un repository
Per iniziare a utilizzare Git bisogna creare un nuovo **repository** o **clonando** uno gia esistente.
- Per iniziare un nuovo repository bisogna eseguire un comando nella directory del progetto:

```
git init
```

- Per clonare un repository gia esistente bisogna invece conoscere **l'URL** del repository remoto, aprire il terminale (come per esempio **PowerShell** o su Windows il prompt di comandi,
per aprirlo bisogna premere il tasto Windows e digitare **cmd** e infine inviare), digitare il comando di clonazione:

```
git clone URL_del_repository
```

## Aggiunta di file al repository:
Dopo aver inizializzato il repository, puoi aggiungere i file che desideri tracciare utilizzando il seguente comando:

```
git add nome_file
```

## Commit delle modifiche:
Una volta aggiunti i file, devi confermare le modifiche eseguite. Fai ciò tramite il comando:

```
git commit -m "Descrizione delle modifiche"
```

## Gestione dei rami:
Git consente di creare **rami** secondari in modo di apportare modifiche senza influenzare il ramo principale, chiamato **mater** o **main** , 
- Puoi creare un nuovo ramo eeguendo il comando:

```
git branch nome_del_ramo
```


- Quindi puoi pasare al ramo che piu ti interessa utilizzando il comando:

```
git checkout nome_del_ramo
```

- Oppure puoi creare e spostarti direttamente in un nuovo ramo utilizzando il comando:

```
git checkout -b nome_del_ramo
```

## Push e Pull da repository remoto:
Se stai collaborando a un progetto su un repository remoto come u **GitHub**, **GitLab** o **Bitbucket** puoi scaricare e inviare le modifiche con due comandi:
- Per scaricare le modifica fatte da altri utenti devi eseguire il comando:

```
git pull origin nome_del_ramo
```

- Per inviare le tue modifiche invece devi eseguire:

```
git push origin nome_del_ramo
```
## Storico
Per vedere lo storico
```
git log
```
## Tornare a una verisone precedente
per tornare a una versione precedente

```
git reset codice del commit
```
## scartare le modifiche
Per scartare le modifiche
```
git checkout nome del file
```

# GIT flow
Git Flow è un modello di branching e versioning per Git che fornisce una serie di linee guida su come organizzare i rami del repository Git per facilitare lo sviluppo software in team.

Il Git Flow prevede l'utilizzo di diversi tipi di rami per gestire le diverse fasi del ciclo di vita dello sviluppo software. I rami principali in questo modello sono:

1. **Master o Main**: Il ramo master rappresenta il flusso di produzione del software. Ogni commit su questo ramo dovrebbe rappresentare una nuova versione stabile e pronta per il rilascio.

2. **Develop**: Il ramo develop è il punto centrale dello sviluppo. È da questo ramo che vengono creati i rami per le nuove funzionalità e le correzioni di bug. Tutte le modifiche pianificate per il prossimo rilascio sono integrate in questo ramo.

Inoltre, il Git Flow prevede l'uso di altri tipi di rami, tra cui:

1. **Feature branches**: Ramo utilizzato per sviluppare nuove funzionalità. I branch di funzionalità sono creati da e fusi con il ramo develop.

2. **Release branches**: Ramo utilizzato per preparare un nuovo rilascio di software. In questo ramo vengono eseguite attività come il controllo della qualità, la risoluzione di bug e la preparazione della documentazione. Una volta che il rilascio è pronto, viene fuso sia nel ramo master che nel ramo develop.

3. **Hotfix branches**: Ramo utilizzato per correggere bug critici che sono stati scoperti nella produzione. I fix urgenti sono effettuati in un hotfix branch, che è creato dal ramo master e fuso sia nel master che nel ramo develop.

Questo modello fornisce una struttura chiara per lo sviluppo software, facilitando il lavoro in team e la gestione del ciclo di vita del software. Tuttavia, è importante notare che il Git Flow non è l'unico modello di branching e versioning disponibile per Git, e alcune organizzazioni possono adottare varianti o approcci diversi in base alle proprie esigenze.





---

Questi sono solo i fondamenti di Git. Ci sono molte altre funzionalità e concetti più avanzati, ma questi ti daranno una buona base per iniziare.
