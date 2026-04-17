# DevStudio — Sito Vetrina

Progetto realizzato come esame finale del corso Git & GitHub.

## Struttura del progetto

- `index.html` — Homepage
- `servizi.html` — Pagina servizi
- `team.html` — Pagina team
- `contatti.html` — Pagina contatti
- `chi-siamo.html` — Pagina chi siamo
- `404.html` — Pagina di errore
- `style.css` — Stili principali
- `typography.css` — Stili tipografici
- `.gitignore` — File ignorati da Git

## Informazioni dal repository

1. Numero totale di commit su main: [22]
2. Hash breve del primo commit in assoluto: [42189b0]
3. Numero di Pull Request aperte durante il progetto: [4]

### Descrizione dei commit - ordine cronologico (da ultimo a primo)
#### Sezione 12 — README e consegna finale
- docs: aggiunto README con riepilogo
&nbsp; Creo un file readme e lo modifico con le informazioni richieste, eseguo lo staging, commit ed ultimo push

#### Sezione 11 — Pulizia branch

&nbsp; Rimuovo tutte le branch con 'git branch -d nome_branch' oppure 'git push origin delete nome_branch'

#### Sezione 10 — Merge squash: pagina chi siamo


- feat: aggiunta sezione chi siamo
&nbsp; Eseguo tutti le modifiche, gli staging e i vari commit. Mi sposto nella branch main ed eseguo 'git merge --squash feature/chi-siamo' per avere tutte le modifiche in un unico commit, eseguo dunque lo staging e commit, concludo con un push.

#### Sezione 9 — Revert: annullare un commit già pushato

- Revert "feat: stili creativi homepage"
&nbsp; Annullo l'ultimo push sfruttando il comando 'git revert id-commit', ed eseguo il push.
 
- feat: stili creativi homepage
&nbsp; Apporto le modifiche ed eseguo staging e push.

#### Sezione 8 — Rebase: allineare una branch con main
 
- feat: aggiunto file tipografia
&nbsp; Eseguo il merge con la branch tipografia.
 
- fix: aggiornamento titolo pagina servizi
&nbsp; Creo la nuova branch, spostandomi in essa. Apporto le modifiche ed eseguo commit e staging, mi sposto nella branch principale ed apporto le modifiche eseguendo poi staging e commit. Mi riporto sull'altra branch e uso 'git rebase main' per aggiornare la branch, mantenendo il commit e le modifiche precedentemente apportate. Verifico la corretta linea dei commit. Eseguo push

#### Sezione 7 — Risoluzione di un conflitto
 
- fix: risolto conflitto colore header, scelta variante A
&nbsp; Dalla branch principale eseguo il pull della prima branch, successivamente eseguo il pull della seconda branch, generando un conflitto, che gestisco tramite GUI di vscode, accettando il current changes. Metto il staging la risoluzione del conflitto ed eseguo il push.
 
- feat: aggiornamento colore header variante B
&nbsp; Creo nuova branch e mi sposto in essa, effettuo le notifiche senza eseguire il push.
 
- feat: aggiornamento colore header variante A
&nbsp; Creo nuova branch e mi sposto in essa, effettuo le modifiche ed eseguo push.

#### Sezione 6 — Reset: commit sulla branch sbagliata
&nbsp; Eseguo il pull delle nuove modifiche
 
- Merge pull request #4 from /feature/404
&nbsp; Gestisco pull requesta da GUI github.
 
- feat: aggiunta pagina 404
&nbsp; Nella branch principale creo il nuovo file, eseguo staging e commit. Utilizzo 'git reset HEAD~1' per annullare il commit precedente. Creo e mi sposto nella branch corretta ed eseguo nuovamente staging e commit. Posso ora eseguire un nuovo push. 

#### Sezione 5 — Amend: commit incompleto
&nbsp; Eseguo il pull sul main del remoto.

- Merge pull request #3 from /feature/contatti

- feat: aggiunta pagina contatti con stili
&nbsp; Procedo a creare una nuova branch, apporto le modifiche, eseguo staging e commit. Successivamente procedo ad apportare le nuove modifiche e modifico commit con 'git commit --amend', e modifico il testo del commit includendo le nuove modifiche. Eseguo push delle branch e gestisco la pull request sul main da GUI github.

#### Sezione 4 — Stash e lavoro urgente: pagina team
 
- Merge pull request #2 from /feature/team
 
- feat: aggiunta pagina team con stili
&nbsp;Mi sposto nella branch corretta rimuovo le modifiche dallo stash con il comando 'git stash apply' verifico con 'git status' le modifiche. Procedo con le modifiche richieste, con lo staging e il commit. Procedo il push con 'git push --set-upstream remote origin feature/branch', ora da gui github eseguo il merge con pull request.

- fix: aggiornamento testi homepage
&nbsp; Dopo aver apportato le modifiche ai file, metto le mofiche in stash, comprese quelle non tracciate, posso farlo tramite comando 'git stash -u', ovvero comprese quelle Untracked. Verifico la corretta presenza dello stash con 'git stash list'; Mi sposto nella branch principale con 'git checkout main' ed apporto le modifiche richieste ai file. Eseguo staging e commit e infine il push. 

#### Sezione 3 — Feature branch e Pull Request: pagina servizi
 
- Merge pull request #1 from /feature/servizi
&nbsp; Tramite GUI gestisco la pull request, inserendo un titolo e una descrizione. Eseguo infine il pull per sincronizzare la repo locale con il remoto.
 
- feat: aggiunta pagina servizi. Utilizzato comando git checkout -b feature/servizi per la creazione e lo spostamento nella branch feature; git add . per mettere in stage le modifiche; git commit -m "" per eseguire il commit delle modifiche
&nbsp; Procedo a creare una nuova branch e a spostarmi automaticamente all'interno di essa tramite comando 'git checkout -b branch', sfrutto i comandi usati precedentemente per eseguire staging, commit e push. Tramite GUI gestisco la pull request, inserendo un titolo e una descrizione.
 
#### Sezione 2 — Prima struttura del sito

- feat: aggiunto foglio di stile
&nbsp;Stesso procedimento per il file style.css; Per controllare le differenze tra le working area e l'ultimo commit posso sfruttare il comando git lg e git status. Infine eseguo il push

- feat: aggiunta homepage
&nbsp; Procedo a creare il file, ed eseguire lo staging e il commit delle modifiche. 
 
#### Sezione 1 — Setup del repository

- chore: aggiunto .gitignore
&nbsp; Creo la cartella in locale e la inizializzo tramite il comando git init, successivamente procedo a creare la repo su github con lo stesso identico nome. Procedo a sincronizzare le due repo, tramite il comando 'git remote add origin url' sfruttando il collegamento ssh del mio dispositivo col mio account github; Tramite linea di comando creo il file gitignore 'touch .gitignore' e apro la repository su vscode tramite comando 'code .'; Preparo il commit mettendo i file in staging con il comando 'git add .' ed eseguo il commit 'git commit -m "" ', concludo la sezione eseguendo il push 'git push --set-upstream remote origin main'
