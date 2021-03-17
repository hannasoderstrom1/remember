`$ conda -c bioconda -c conda-forge -p /envs/cnv_r r-base=3.6.3 r-tidyverse` c=channel, typ repositories som man alltid behöver. p=path+vad man vill döpa env till. r-base och r-tidyverse är paket (dependencies) som jag vill ha med i environmentet

men nu behöver jag inte bioconda och conda-forge för de finns i min .condarc så de kommer med automatiskt varje gång 

`$ conda env export --from-history > cnv_r.yaml` för att spara som ett recept för att bygga miljön igen


varje gång man har installerat ett paket måste man gå in i yaml-filen och lägga till det


`$ conda search r-xlsx` leta om paket finns 


`$ conda install r-xlsx=0.6.1` installera paket


`$ conda remove r-xlsx` ta bort paket


`$ conda list` se vilka paket som finns i miljön


`$ conda deactivate` deactivate den miljön du är i 


`$ conda env list` se vilka environments som finns


`$ conda env create -f cnv_r_copy.yaml` skapa en miljö från en yaml-fil


`$ conda env update -f local.yaml --prune` uppdatera ett environment baserat på yml-filen. prune gör att paket som tagits bort från yaml-filen avinstalleras


`$ conda env update -f local.yaml --prune` uppdatera ett environment baserat på yml-filen. prune gör att paket som tagits bort från yaml-filen avinstalleras


`$ conda env remove -n ENV_NAME` ta bort ett environment


`$ conda env export > environment.yaml` spara miljön som den ser ut just nu i en yaml
