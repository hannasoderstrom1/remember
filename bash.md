# Bash commands

relativ sökväg = baserat på vad man står
absolut sökväg = all information för att hitta den

## Permissions

`$ chown user:group target` change ownership

`$ chmod g+w target` change permissions, group + write 

## sudo

`$ sudo !!` sudo + last command 

`$ exit` leave sudo

## copy

`$ rsync -P -r` copy + see progress + copy subfolders

## path

`$ realpath target` absolute path to target

## git

`$ git clone (https)` hämta repositoriet som man vill jobba i 

`$ git pull` ta ner nåt från git/kolla så att min lokala repository är up to date med remote repository

`$ git mv` flytta något eller döpa om något men att git har koll på förändringen

`$ git log` kolla vad som har hänt (--oneline = komprimerat)

`$ git commit (vad som ska commitas) -m "meddelande"` commit

`$ git add` lägga till sånt som ska committas

`$ git push` push committade local changes till remote repository

## vim/emacs

https://karl-voit.at/unmaintained/vim-emacs-cheatsheet_of_freezing_hell.shtml

## remove

`$ rm -r` remove directory (remove recursively)



