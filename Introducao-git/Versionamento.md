## O básico

arquivo-base
uma nova versão a cada alteração no código -> versionamento
para organizar melhor e resolver problemas, surgiram:

## Sistemas de Controle de Versão

Softwares que controlam as versões de um arquivo ao longo do tempo

- Registra o histórico de atualizações de um arquivo
- Gerencia quais foram as alterações, a data, autor, etc
- Organização, controle e segurança (quem tem acesso para contribuir)

## Tipos de Sistemas de Controle de Versão:
- VCS Centralizado (CVCS): CVS, Subversion
- apenas um servidor que armazena todos os arquivos de versões
	- se ficar fora de ar, você não consegue salvar/colaborar
	- se algum arquivo for corrompido ou houver perca de dados, sem backup, você perde todo o projeto
- VCS Distribuído (DVCS): Git, Mercurial

- resolve os problemas do anterior
	- cada repositório/banco de versão é duplicado localmente
	- pode editar mesmo se o servidor estiver fora do ar

## DVCS (Distribuído):
- Clona o repositório completo, incluindo o histórico de versões
- Cada clone é como um backup
- Possibilita um fluxo de trabalho flexível
- Possibilidade de trabalhar sem conexão à rede
