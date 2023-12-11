```
git init
```
Transforma diretório local em um repositório git (inicia um repositório git)

```
git clone URL
```
Clona um repositório git remoto para um diretório local

LOCAL ----> REMOTO
```
git init
`````
git **init**ialize
Inicia um repositório local git

```
git remote add origin URL
```
Comando para vincular esse repositório local com um repositório remoto (conectar os dois repositórios)
``origin``: o nome do servidor remoto. Variável, mas é melhor manter esse mesmo

REMOTO ----> LOCAL
```
git clone URL nome-diretorio-local
```
Clona um repositório remoto para um local
o ``nome-diretorio-local`` é opcional, se não especificado fica com o mesmo nome do diretório remoto

Para um repositório com várias branches, é possível selecionar uma em específico para clonar:
```
git clone URL --branch newbranchName --single-branch
```
``newbranchName``: nome da branch, variável
nesse caso, clonará somente a branch newbranchName

```
git clone URL --branch --singlebranch
```
Caso não seja especificada a branch, clonará apenas a principal (main ou master)

````
git status
`````
Mostra o status da Árvore de Trabalho e da Área de Preparação, além do estado dos arquivos

````
git add .
`````
Adiciona/salva todos os arquivos (untracked files) localmente na staging area (área de preparação)

````
git add fileName.txt
`````
Adiciona um arquivo em específico à Área de Preparação

````
git commit -m"commit"
`````
Salva e envia os arquivos para o repositório remoto
``-m"commit"``: mensagem que descreve o commit/a alteração feita.
O nome da mensagem é variável, e.g.:
``-m"novo"``

````
git log
`````
Mostra o histórico de commits (cada um possui uma hash ``#``)

````
git reflog
`````
Histórico detalhado de alterações (log melhorado)

````
echo directoryName > .gitignore
`````
ou
````
echo fileName > .gitignore
`````
Adiciona diretório ou arquivo dentro da pasta ``gitignore``, fazendo o git ignorar esse arquivo ao commitar

````
echo > .gitignore
`````
Remove pasta/arquivo do gitignore, deixando o diretório vazio e o tornando o arquivo novamente pronto para commitar

````
git config --global --list
		   --local
		   --system
`````
Ver/listar configurações do git

````
rm -rf .git
`````
Remove/exclui o diretório git e seu conteúdo
Útil para desfazer quando se dá git init na pasta errada

````
git restore fileName.txt
`````
Descarta todas as alterações feitas no arquivo, restaurando o arquivo da working tree
Retorna para o último estado salvo

````
git commit --amend -m"mensagem"
`````
Altera mensagem do último commit feito, já indicando a mensagem que substituirá a anterior

````
git commit --amend
`````
Abre o editor para alterar a mensagem:
Aperte ``i`` para editar
Para sair: ``Esc`` ``:wq``

````
git reset fileName.txt
`````
Remove o arquivo da área de preparação (depois do git add, mas antes do commit)
O arquivo volta à etapa de untracked file

````
git restore --staged fileName.txt
`````
Mesmo efeito, o arquivo é removido da staging area e volta a ser untracked file

````
git reset --soft
		  --mixed
		  --hard
`````
Desfaz o último commit (retorna ao commit anterior)

``--soft``: adiciona à area de preparação os arquivos que estavam nos commits apagados, deixando apenas o commit indicado (pela hash)
``--mixed`` (comportamento padrão: apenas ``git reset``): adiciona à working tree os arquivos dos commits descartados, deixando o commit indicado (os arquivos voltam ao estágio de untracked files, etapa anterior à área de preparação) 
``--hard`` (WARNING, DANGER): ignora os arquivos dos commits descartados e os desfaz (apaga tudo)

````
git reset --soft hash
`````
``hash``: copiar e colar hash do commit para o qual queremos retornar

````
git push -u origin main
`````
``-u``: upstream
Envia alterações do repositório local para o remoto

````
git pull
`````
"Puxa" alterações feitas no repositório remoto para o repositório local (atualiza o repositório local)
Mescla com o que existe no local

````
git checkout -b branchName
`````
Cria uma branch (a partir da Main) APENAS NO REPOSITÓRIO LOCAL
Switch to a new branch (leva para ela)
A nova branch aponta para o mesmo commit atual da branch main em git log

````
git checkout main
`````
Volta para a branch main

````
git branch
`````
Lista as branches existentes no depositório
O ``*`` (asterisco) sinaliza a branch em que nos encontramos

````
git branch -v
`````
Lista o último commit de cada branch

````
git merge branchName
`````
Mescla a branch main e a branch especificada em ``branchName`` (traz as alterações da branch pra main)

```
git branch -d branchName
```
Exclui uma branch

````
git fetch origin main
`````
Baixar alterações do repositório remoto sem mesclar com o repositório local

````
git diff 
`````
Passa as branches que queremos ver a diferença
``git diff main origin/main``
nesse caso, branch main do repositório local e branch main do repositório remoto (origin)

````
git merge origin/main
`````
Mescla com a branch do repositório remoto e traz as alterações

````
git stash
`````
Arquiva modificações feitas (antes de um commit)
Útil para criar uma nova branch sem carregar junto certas alterações feitas

````
git stash list
`````
Lista as modificações arquivadas

````
git stash pop 
`````
Trazer de volta as modificações para a branch e excluir a alteração mais recente da pilha/lista (stash)

````
git stash apply
`````
Traz de volta as modificações e mantém a modificação na lista para uso posterior
