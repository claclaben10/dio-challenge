Branch = ramo

A branch é uma ramificação do projeto

- É um ponteiro móvel para um commit no histórico do repositório
	- a cada novo commit gerado dentro daquela branch, ela passa a apontar para esse novo commit

Quando se cria uma nova branch a partir de outra existente, a nova se inicia apontando para o mesmo commit da branch que estava quando foi criada

Branch principal = main/master
a partir dela é possível criar novas branches (como universos paralelos do projeto)

a nova ramificação pode servir para testar novos recursos, como adicionar uma funcionalidade nova ao projeto, sem a certeza se manterá essa ideia (teste)

com a branch, o teste pode ser feito de maneira independente, sem afetar a branch principal

a branch test aponta para um novo commit (3)
a branch main continua apontando para o commit anterior (2)

para que a branch main também aponte para o commit 3, ela precisa mesclar com a branch test

- A branch funciona de maneira independente da main (alterações nela não afetam a principal)

- O comando de criação de branch só cria uma branch no repositório LOCAL. Para enviar essa alteração também para o repositório remoto, enviar através do git push normalmente

## Conflitos

#### Conflito de merge
Acontece quando existem alterações concorrentes:
há alteração na mesma linha de código

- Quando uma pessoa tenta enviar, gera um conflito com o que o outro já havia enviado
- O Git não entende qual dessas alterações deve ser mantida e retorna esse erro para que você decida qual alteração manter:
[rejected] error: failed to push some refs to URL
- Existem alterações no repositório remoto que ainda não foram puxadas localmente

Depois de dar o ``git pull``:
CONFLICT (content): Merge conflict in fileName.txt
Automatic merge failed; fix conflicts and then commit the result

- Ao abrir o arquivo com conflito, ele apresenta as duas versões, da branch local (pra onde está apontando) e remota
- Decidimos então qual das alterações deve ser mantida e indicar para o Git:
	- Manter apenas o texto desejado, salvar o arquivo, git add, commit e push (enviar o tratamento do conflito para o repositório remoto)
