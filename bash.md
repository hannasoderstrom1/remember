# Bash commands


## Permissions

`$ chown user:group target` change ownership

`$ chmod g+w target` change permissions, group + write 

## sudo

`$ sudo !!` sudo + last command 

`$ exit` leave sudo

## copy / move

`$ rsync -P -r` copy + see progress + copy subfolders

`$ rsync -P hanna@pinbot.biomedicine.gu.se:test/FILENAME(OR FOLDER/FILENAME) .` kopiera från en remote server till local (där du är (.))

`$ mv *IDENTIFIER* ~/YourPath/` flytta alla filer som innehåller identifier

## path

relativ sökväg = baserat på vad man står

absolut sökväg = all information för att hitta den

`$ realpath target` absolute path to target

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

## vim/emacs

https://karl-voit.at/unmaintained/vim-emacs-cheatsheet_of_freezing_hell.shtml

## remove

`$ rm -r` remove directory and everything that is in it(remove recursively)

`$ rmdir`remove directory if it's empty

`$ for file in correct_and_filter_umis.sh.o* ; do rm -f $file ; done` remove all these files

`$ rm -f {*.xvg,.*.xvg}` remove including hidden files with this file extension

## tutorial

http://korflab.ucdavis.edu/Unix_and_Perl/current.html#part1

## queue

`$ qstat -f -u "*"` kolla vad som körs på klustret och av vilka users

`$ qsub script.sh` köa in scriptet

`$ qdel {18280..18285}` ta bort alla jobb med id 18280 tom 18285

## textfile 

`$ cls file.txt` se filen på ett "bra" sätt

## alias 

`command alias` ignore alias

## Anders' Today I Learned

https://github.com/pbiology/TIL

## Find

`find ./ -name "*_consensus_reads_filtered.bam" -exec cp {} \;` hittar saker och gör ett kommando (tex cp) på det man hittar

## bashrc

`source ~/.bashrc` om man ändrar något och vill att det ska aktiveras utan att man behöver starta om 

## loops

`$ #!/bin/bash
        for i in $( ls ); do
            echo item: $i
        done`

## space

`$ df -h` se hur mycket plats som finns på medstore/seqstore

`$ du -h --max-depth=1 .` kollar hur mycket space det som finns i mappen du står i och dess undermappar tar upp

## unique files

`$ md5 <filename>` man får en kod för filen och om en fil med samma namn ligger på en annan plats så kan man jämföra koden för att se om det är samma fil

## screen 

`$ screen -S your_session_name` starta en ny screen med valfritt namn

`$ screen -ls` visa vilka screens som finns

## qsub

http://bioinformatics.mdc-berlin.de/intro2UnixandSGE/sun_grid_engine_for_beginners/how_to_submit_a_job_using_qsub.html

## customize bash prompt

https://www.howtogeek.com/307701/how-to-customize-and-colorize-your-bash-prompt/
