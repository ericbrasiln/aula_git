# Workshop de Git e GitHub

Eric Brasil (IHLM/UNILAB)

<img src="img/octolab.png" alt="octolabhd" height="500">

## O que é git e github?

Tem diferença? É a mesma coisa? Por que usar?

### Git

-*Version Control System*
	- Distribuído
	- Repositório Local
	- Livre e gratuito
- Vantagens:
	- Controle de histórico
	- Trabalho em equipe
	- Ramificações (Branches)
	- Segurança
	- Organização

### GitHub

- Plataforma de hospedagem de códigos e arquivos
- Possui controle de versões utilizando Git;
- Rede Social;
- Vantagens:
	- repositórios ilimitados
	- Forks
	- Colaboração e trabalho com equipes grandes
	- gestão de projetos
	- automação de tarefas
	- GitHub Pages

## Git

### Instalação

Site oficial: [git-scm.com](http://git-scm.com/)

### Configurando

- `git config --global user.name` => configura nome do usuário na máquina
- `git config --global user.email` => configura email
- `git config --list` => lista as configurações atuais

### Criar um diretório git

- `git init`

Esse comando cria a estrutura do git, como pode ser visto no diretório .git

### Mudanças

Os arquivos no seu diretório git podem estar em 3 estágios:

1. `Modified`: Um arquivo alterado sem ter sido preparado ou gravado no git está na
condição de "modificado" (`modified`).

2. `Staged`: preparado para entrar no histórico.
	- `git add [arquivo]`: prepara o arquivo ou arquivos para serem enviados
	- Os arquivos passam para a condição de preparados (`staged`)
3. `Commited`: gravados no histórico do git
	- `git commit`: grava as alterações no histórico
	- `git commit -m "mensagem do commit"`
	- `git commit -a -m "mensagem do commit"`

Lembrando que um commit armazena um snapshot de tudo que você incluiu sua
'staging area'.

É possível consultar o status dos arquivos no diretório:

- `git status` 
	
É possível acessar as diferenças entre os arquivos

- `git diff`

Remover um arquivo do diretório de trabalho e também do histórico:

- `git remove [arquivo]`

Remover apenas o registro do arquivo do histórico, mas manter o arquivo
no diretório de trabalho:

- `git rm --cached [arquivo]`

Renomear arquivos

-`git mv [atual] [novo]`

Ver os registros das ações:

-`git log`

### Desfazendo coisas

Corrigir o último commit:

- `git commit --amend`

Desfazer preparação de arquivos:

- `git restore --staged [arquivo]`

### Clonando e lidando com Remotes

Para clonar um diretório de algum servidor online:

- `git clone [url]`

Todo conteúdo do repositório será clonado localmente. 

O repositório online é chamado de `origin`

Fetch:

- `git fetch [remote-name]`

Push

- `git push [remote-name] [branch name]`

Ex:`git push origin main`

Pull

- `git pull`

### Branches

Criar um novo branch

- `git branch [name]`

HEAD => aponta para qual branch você está

Mudar de branch

- `git checkout [branch name]`

Merge

- `git merge [branch name]`

Deletar branch

- `git branch -d [branch name]`

