`$ conda -c bioconda -c conda-forge -p /envs/cnv_r r-base=3.6.3 r-tidyverse` c=channel, typ repositories som man alltid behöver. p=path+vad man vill döpa env till. r-base och r-tidyverse är paket (dependencies) som jag vill ha med i environmentet

men nu behöver jag inte bioconda och conda-forge för de finns i min .condarc så de kommer med automatiskt varje gång 

`$ conda env export --from-history > cnv_r.yaml` för att spara som ett recept för att bygga miljön igen


varje gång man har installerat ett paket måste man gå in i yaml-filen och lägga till det


`$ conda search r-xlsx` leta om paket finns 


`$ conda install r-xlsx=0.6.1` installera paket








