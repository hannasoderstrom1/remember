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

`$ qlogin -q batch.q -pe mpi 40` (köra typ ett qsub-jobb utan att göra ett qsub-script. om man är i en screen, exit för att gå ut)

## textfile 

`$ cls file.txt` se filen på ett "bra" sätt

## alias 

`$ command alias` ignore alias

## Anders' Today I Learned

https://github.com/pbiology/TIL

## Find

`$ find ./ -name "*_consensus_reads_filtered.bam" -exec cp {} \;` hittar saker och gör ett kommando (tex cp) på det man hittar

`$ grep "some string" . -R` find string in file

`$ ls -lrt` mappar listade med nya längst ner

## bashrc

`$ source ~/.bashrc` om man ändrar något och vill att det ska aktiveras utan att man behöver starta om 

## loops

`$ #!/bin/bash
        for i in $( ls ); do
            echo item: $i
        done`

## space

`$ df -h` se hur mycket plats som finns på medstore/seqstore

`$ du -h --max-depth=1 .` kollar hur mycket space det som finns i mappen du står i och dess undermappar tar upp

## unique files

`$ md5sum <filename>` man får en kod för filen och om en fil med samma namn ligger på en annan plats så kan man jämföra koden för att se om det är samma fil

## screen 

`$ screen -S your_session_name` starta en ny screen med valfritt namn

`$ screen -ls` visa vilka screens som finns

`$ screen -X -S [session # you want to kill] quit` ta bort en screen

## incrontab

`$ sudo less /var/log/cron | grep incron` kolla i loggen om den har försökt köra nåt

## petasuite

`$ petasuite -d DNA.fasterq` gör om till ej komprimerad

## run something in the background

1. ctrl+z (lägger det i bakgrunden)

2. `$ bg 1` (bakgrundsjobb 1)

3. `$ disown -h` (avsäger mig ägandet)


## qsub / qlogin

http://bioinformatics.mdc-berlin.de/intro2UnixandSGE/sun_grid_engine_for_beginners/how_to_submit_a_job_using_qsub.html

`$ qlogin -q batch.q -l excl=1 -pe mpi 40` 

## customize bash prompt

https://www.howtogeek.com/307701/how-to-customize-and-colorize-your-bash-prompt/

## symlink

`$ ln -s <path to the file/folder to be linked> <the path of the link to be created>`

## awk

`$ awk 'NR == 1 {print; next} {$4=$4+1 ; print ;}' oldfile.txt > newfile.txt` hoppar över headern och gör +1 på kolumn 4
