# Bash commands


## Permissions

`$ chown user:group target` change ownership

`$ chmod g+w target` change permissions, group + write 

## sudo

`$ sudo !!` sudo + last command 

`$ exit` leave sudo

## copy

`$ rsync -P -r` copy + see progress + copy subfolders

`rsync -avx hanna@pinbot.biomedicine.gu.se:test/FILENAME(OR FOLDER/FILENAME) .` kopiera från en remote server till local (där du är (.))

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

`$ git push` push committade local changes till remote repository

## vim/emacs

https://karl-voit.at/unmaintained/vim-emacs-cheatsheet_of_freezing_hell.shtml

## remove

`$ rm -r` remove directory and everything that is in it(remove recursively)

`$ rmdir`remove directory if it's empty

## tutorial

http://korflab.ucdavis.edu/Unix_and_Perl/current.html#part1

# qstat

`$ qstat -f -u "*"` kolla vad som körs på klustret och av vilka users

# textfile 

`$ cls file.txt` se filen på ett "bra" sätt





