Tab (botão do teclado)
Completa automaticamente o nome da pasta ou comando no terminal

Ctrl + L
ou
````
$ clear
`````
Limpar terminal (limpar a tela de todos os comandos anteriores)

```
$ cd
```
**c**hange **d**irectory
Mudar de pasta/diretório no terminal:
``$ cd ~/Directory/subdirectory``

- When `cd` is executed without a directory, it puts the user in their home directory:
   `cd` = `cd ~`

```
$ cd ..
```
Voltar uma pasta no terminal

- If the current working directory is `/home/username/dir/subdir`:
  `$ cd ..` will get us to `/home/username/dir

```
$ mkdir
```
**m**ake **d**irectory
Criar novo diretório/pasta no diretório em que se encontra o terminal:
``$ mkdir DirectoryName``
ou criar dentro de outro diretório específico:
``$ mkdir ~/DirectoryName/newdirectory

```
$ mkdir -p
```
Criar um novo diretório com um ou mais subdiretórios:
``$ mkdir -p directoryName/subdirectory``

```
$ ls
```
**l**i**s**t
Listar arquivos e diretórios dentro de uma pasta

```
$ ls -a
```
**l**i**s**t **al**l (flag ``-a``)
Exibir todos os arquivos e diretórios, incluindo ocultos (``.``)

```
$ ls -l
```
**l**i**s**t **l**ong (flag ``-l``)
Mostrar o tamanho, última data e hora de alteração, autores e permissões de arquivos e diretórios (info detalhada dos itens)

```
$ ls -al
```
combinação das flags ``-a`` e ``-l``
Mostrar todos os arquivos e diretórios, incluindo os ocultos, além de informações detalhadas de cada um

````
$ touch
`````
Criar um arquivo em branco (vazio) de qualquer extensão no diretório atual:
``$ touch newfile.txt``
ou em outro diretório específico:
``$ touch ~/DirectoryName/newfile.docx

````
$ nano
`````
Editar arquivo dentro do terminal (editing mode):
``$ nano fileName.txt``
- to Exit: Ctrl + X
- salvar: S
- Enter

````
$ echo
`````
Criar um arquivo com texto dentro:
``$ echo "text" > newfile.txt``

```
$ cat
```
**c**onc**a**tena**t**e
Exibir conteúdo do arquivo (ler dados de um arquivo especificado e imprimir seu output):
``$ cat fileName.txt``

Podemos também exibir o conteúdo de múltiplos arquivos:
``$ cat file1.txt file2.txt file3.txt``

````
$ cat -n
`````
Imprime o número de cada linha do arquivo:
``$ cat -n fileName.txt``

````
$ pwd
````
**p**rint **w**orking **d**irectory
Imprimir na tela o caminho completo para o diretório atual

````
$ rm -rf
`````
Remover diretório não vazio, junto com seus subdiretórios e arquivos:
``$ rm -rf DirectoryName``
Warning: IRREVERSIBLE !!!!
o diretório não vai para a Lixeira, não pode ser restaurado, é excluído definitivamente!!!

````
$ mv
`````
**m**o**v**e directory/file
Mover diretório ou arquivo de um lugar para outro:
``$ mv ~/DirectoryName/file.txt ~/DirectoryName/subdirectory/file.txt``

````
$ cp
`````
**c**o**p**y file
Criar cópia do arquivo:
``$ cp ~/DirectoryName/pic.png ~/AnotherDirectory/pic.png``

Também podemos criar uma cópia do arquivo com um novo nome, na mesma pasta:
``$ cp ~/DirectoryName/pic.png pin.png``
ou dentro de outra pasta:
``$ cp ~/DirectoryName/pic.png ~/AnotherDirectory/pin.png``

````
$ cp -r
`````
Criar cópia do diretório com todos seus subdiretórios e arquivos:
``$ cp -r ~/DirectoryName/subdirectory ~/AnotherDirectory/subdirectory

````
$ find
`````
Procurar arquivos no sistema:
``$ find / -name 'fileName.txt'``

Mostra exatamente em que pasta reside o arquivo em questão
Podemos também especificar o ``/`` path:
``$ find ~/DirectoryName/ -name 'fileName.txt'``
Sem especificação, o ``/`` corresponde ao diretório principal, onde o ``find`` vai começar a procurar

``$ find / -name '*.csv'``
Podemos especificar por wildcards para encontrar todos os arquivos de determinada extensão, como arquivos CSV, txt, PNG

````
$ rmdir
`````
**r**e**m**ove **dir**ectory
Remover diretório vazio:
``$ rmdir DirectoryName``

Se o diretório não estiver vazio, retorna o erro:
``rmdir: failed to remove 'DirectoryName': Directory not empty``

````
$ less
`````
Coloca o conteúdo de um arquivo especificado uma tela por vez (terminal pager):
``$ less 2023-11-02.log``

Útil para inspecionar o conteúdo de arquivos grandes, como logs

````
$ sudo
`````
user privileges set to administrator privileges
pede senha do usuário
fórmula: ``$ sudo 'command'``
Exemplo:
``$ sudo rm -R DirectoryName``

````
$ whatis
`````
Oferece uma descrição curta de um comando e o que ele faz:
fórmula: ``$ whatis 'command'``
Exemplo:
``$ whatis mv``

````
$ exit
`````
Fechar sessão atual do Terminal

While you can simply close the window, that may not be possible when you’re using SSH through Terminal to access a remote machine. In this instance, you’ll want to use exit to hang up that remote connection before closing the window.
