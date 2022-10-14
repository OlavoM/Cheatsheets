# Git

## Configuração Inicial
- `git config --global user.name "<usuario>"`
- `git config --global user.email "<email>"`

<br>

## Primeiro Commit
- na pasta desejada use `git init` => Cria o subdiretório .git
- `git add *` => Adiciona todos os arquivos para o modo staged/tracked (adiciona para o próximo commit)
- `git commit -m "initial project version"` => Faz o primeiro commit (pode ser qualquer mensagem)
- `git status` => Verifica o status dos arquivos

<br>

## Principais Comandos
- `git add <file>` => Adiciona um arquivo específico para o modo staged/tracked
- `git commit` => Novo commit, abre editor de texto para escrita da mensagem de commit
- `git commit -m "mensagem"` => Usa como mensagem de commit o que for passado por parâmetro
- `git commit -a` => Já executa o git add * e faz o commit automaticamente (pode colocar com outros parâmetros adicionais)
- `git rm <file>` => Remove arquivo do modo staged, ao commitar ele é deletado automaticamente (se ainda estiver lá)
- `git rm --cached <file>` => Remove só do git mas deixa no hd (bom para quando se esquece do git ignore)
- `git log` => Exibe o histórico dos commits (mais recente primeiro)
- `git log -p` => Histórico com as diferenças introduzidas em cada commit
- `git log --stat` => Histórico com resumo das diferenças
- `git log -<number>` => Histórico com ultimos n commits
- `git log --pretty=<oneline, short, full, fuller>` => Outro tipo de formatação de saída do histórico (tem como parametro avançado o format)(--graph desenha um grafo da arvore)
- `git commit --amend` => Para quando se esquece de algum add ou para reescrever a mensagem de commit
- `git reset HEAD <file>` => Tira do modo staged
- `git checkout -- <file>` => Descarta mudanças realizadas após o último commit

<br>

## Git Ignore
- Pode ser criado no vscode por exemplo, com nome ".gitignore"
- Cada linha ignora um item no comit, exemplo:
    - .gitignore => Ignora o próprio arquivo
    - exemploIgnorar.txt
    - executavel.exe

<br>

## Git Pull & Push com repositório remoto criado primeiro
- Primeiro cria-se o repositório remoto ou pushable
- `git clone <local do respositório remoto> <OutroNomeProDiretório(opcional)>`
- Faz o que precisa, add e commit
- `git remote` => Consulta o nome do repositório remoto (o padrão é origin)
- `git push origin main` => Faz o push pro remoto, se for os valores padrão (orign e <branch atual>), só precisa de `git push`
- `git pull origin main` => Faz o pull (traz arquivos) do remoto, se for os valores padrão (orign e <branch atual>), só precisa de `git pull`
- `git fecth origin <branch-name(opcional para FETCH_HEAD)>` => Traz arquivos do remoto para uma branch, sem fazer o merge com a main

<br>

## Clonar Repositório
- `git clone <url>` => Clona o repositório remoto para dentro do repositório atual
- `git remote add <shortname> <url>` => Clona explicitamente, o shortname substitui a url como alias
- `git fetch <remote-name>` => Pega os dados (se atualiza) do repositório remoto

<br>

## Push para o GitHub
- Este método é muito mais simples para criar repositórios, e é o que eu utilizo na maioria das vezes
- Cria-se um novo repositório no GitHub prefencialmente sem nada além da licença e do README (ou clona antes do primeiro commit)
- Copiar URL do repositório do GitHub no botão específico
- `git clone <url>`
- Faz o que precisa, add e commit
- `git push` => Envia os commits locais para o GitHub
- `git pull` => Obtém os commits do repositório remoto

<br>

## Branches
- `git branch <branch-name>` => Cria branch com o nome especificado
- `git checkout <branch-name>` => Muda o working directory para a branch
- `git checkout -b <branch-name>` => Cria a branch e muda pra ela
- `git merge <branch-name>` => [Dentro do destino, tipo a main] faz o merge (passa pra atual o conteúdo da branch especificada)
- `git branch` => Lista todas as branches existentes no repositório
- `git branch -a` => Lista todas as branches incluindo as que estão no repositório remoto
- `git branch -d <branch-name>` => Deleta a branch local
- `git branch -D <branch-name>` => força o delete da branch local
- conflitos são resolvidos no próprio código com conflito

<br>

## Git Stash
- `git stash` => Salva as alterações não comittadas no stash
- `git stash pop` => Pega as alterações do stash de volta

<br>

## Git Tag
git tag -a v1.0 -m "Versão 1.0" -> cria tag anotada(-a que registra criador, etc) e com mensagem (-m)
git tag -a v0.0 <sha1 do commit antigo, ou o começo dele> -m "Versao 0.0" -> criaa tag para commit antigos
git show <tag> -> exibe as informações da tag
git checkout <tag> -> retorna para o estado daquela tag
git checkout main -> retorna para a main
git tag -d v0.0 -> deleta a tag

<br>

## Outros Comandos
git diff -> mostra diferenças específicas em arquivos alterados
git diff --staged -> mostra as diferenças que estão no modo staged
git mv <file_from> <file_to> -> move arquivos no git, renomeia se git mv <file_name> <new_file_name>
gitk -> abre uma GUI de relatório dos comitts no git bash
git init --bare -> cria repositório pushable

<br>

## Git Bash
inicia na pasta desejada ao alterar essa opção em "propriedades" do ícone (volta pro padrão se estiver escrito --cd-to-home no destino)
- Realmente não recomendo o uso dessa ferramenta, no Windows a experiência com o powershell é muito mais agradável

<br>

## GitLab
cria ssh no windows (powershell) com:
ssh-keygen -t ed25519 -C "<email>" -> ED25519 keys are more secure and performant than RSA keys
armazena a chave no local padrão
coloca senha (qualquer coisa as chaves podem ser reescritas repetindo o procedimento)
visualiza a chave pública com:
cat ~/.ssh/id_ed25519.pub -> powershell
cat ~/.ssh/id_ed25519.pub | clip -> gitbash, copia pra área de transferência
git config --global http.sslVerify false -> desativa essa verificação pra intranet

<br>

## Submodules
git submodule update --init
git submodule update --init --rebase
git submodule update --init --force
