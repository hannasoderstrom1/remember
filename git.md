## git

`$ git clone (https)` hämta repositoriet som man vill jobba i 

`$ git pull` ta ner nåt från git/kolla så att min lokala repository är up to date med remote repository

`$ git mv` flytta något eller döpa om något men att git har koll på förändringen

`$ git log` kolla vad som har hänt (--oneline = komprimerat)

`$ git commit (vad som ska commitas) -m "meddelande"` commit

`$ git commit -m "meddelande, fixes #2"` commit, fixes #2 = löser issue 2/stänger issue 2

`$ git add` lägga till sånt som ska committas

`$ git add folder/*` lägga till allt som finns i folder

`$ git push` push committade local changes till remote repository

`$ echo "test/" > .gitignore` lägger till mappen test i gitignore-filen (två >> för att appenda när man inte gör det första gången)

`$ git log --oneline` se vilka commits man har gjort och vad de har för "commit hash"

`$ git diff commithashb commithasha` se skillnaden mellan olika commits

`$ git commit -p` committa bara en del av det du har gjort

`$ git diff kodb koda` se skillnaden mellan olika commits

`$ git diff --staged` diffen på det som är i "staging area"

`$ git diff kodb koda` se skillnaden mellan olika commits

`$ git reset` unstage staged files

`$ git checkout [file]` gå tillbaka till senaste versionen

`$ git revert [commithash]` ta bort det man gjorde i denna commit

`$ git log --all --graph --decorate --oneline` se en graf över commits och i vilka branches

workflows: https://www.atlassian.com/git/tutorials/comparing-workflows

branches: https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow
