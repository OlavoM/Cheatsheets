# Git

## Configuração Inicial
- `git config --global user.name "<usuario>"`
- `git config --global user.email "<email>"`

## Primeiro Commit
- na pasta desejada use `git init` => cria o subdiretório .git
- `git add *` => adiciona todos os arquivos para o modo staged/tracked (adiciona para o próximo commit)
- `git commit -m "initial project version"` => faz o primeiro commit (pode ser qualquer mensagem)
- `git status` => verifica o status dos arquivos

**PRINCIPAIS COMANDOS**
git add <file> -> adiciona um arquivo específico para o modo staged/tracked
git commit -> novo commit, abre editor de texto para escrita da mensagem de commit
git commit -m "mensagem" -> usa como mensagem de commit o que foi passado por parâmetro
git commit -a -> já executa o git add * e faz o commit automaticamente (pode colocar com outros parâmetros adicionais)
git rm <file> -> remove arquivo do modo staged, ao commitar ele é deletado automaticamente (se ainda estiver lá)
git rm --cached <file> -> remove só do git mas deixa no hd (bom quando se esquece do git ignore)
git log -> exibe o histórico dos commits (mais recente primeiro)
git log -p -> histórico com as diferenças introduzidas em cada commit
git log --stat -> histórico com resumo das diferenças
git log -<number> ->histórico com ultimos n commits
git log --pretty=<oneline, short, full, fuller> ->outro tipo de formatação de saída do histórico (tem como parametro avançado o format)(--graph desenha um grafo da arvore)
git commit --amend ->pra quando se esquece de algum add ou para reescrever a mensagem de commit
git reset HEAD <file> -> tira do modo staged
git checkout -- <file> -> descarta mudanças realizadas após o último commit

**GIT IGNORE**
pode ser criado no vscode por exemplo, com nome ".gitignore"
cada linha ignora um item no comit, exemplo:
.gitignore -> ignora o próprio arquivo
exemploIgnorar.txt
executavel.exe

**GIT PULL & PUSH COM REPOSITÓRIO REMOTO CRIADO PRIMEIRO**
- Este método é muito mais simples para criar repositórios
[após criar o repositório remoto ou pushable]
git clone <local do respositório remoto> <OutroNomeProDiretório(opcional)>
[faz o que precisa, add e commit]
git remote -> consulta o nome do repositório remoto (o padrão é origin)
git push origin master -> faz o push pro remoto
git pull origin master -> faz o pull (traz arquivos) do remoto
git fecth origin <branch-name(opcional para FETCH_HEAD)> -> traz arquivos do remoto para uma branch, sem fazer o merge com a master


**CLONAR RESPOSITÓRIO**
git clone <url> -> clona o repositório remoto para dentro do repositório atual
git remote add <shortname> <url> -> clona explicitamente, o shortname substitui a url como alias
git fetch <remote-name> -> pega os dados do repositório remoto

**PUSH PRO GITHUB**
[cria-se um novo repositório no GitHub prefencialmente sem nada (ou clona antes do primeiro commit)]
[garante-se que está tudo commitado]
copiar URL do repositório do GitHub
git remote add origin <URL>
git push -u origin master
depois o uso de somente git push é possivel -> envia todos os branches correspondentes que têm os mesmos nomes de branches remote
git pull origin -> pull do repositório remoto

**BRANCHES**
git branch <branch-name> -> cria branch com o nome especificado
git checkout <branch-name> -> muda o working directory para a branch
git checkout -b <branch-name> -> cria a branch e muda pra ela
git merge <branch-name> -> [dentro do destino, tipo a master] faz o merge (passa pra atual o conteúdo da branch especificada)
git branch -> lista todas as branches existentes no repositório
git branch -d <branch-name> -> deleta a branch local
git branch -D <branch-name> -> força o delete da branch local
conflitos são resolvidos no próprio código com conflito

**GIT STASH**
git stash -> salva as alterações não comittadas no stash
git stash pop -> pega as alterações do stash de volta

**GIT TAG**
git tag -a v1.0 -m "Versão 1.0" -> cria tag anotada(-a que registra criador, etc) e com mensagem (-m)
git tag -a v0.0 <sha1 do commit antigo, ou o começo dele> -m "Versao 0.0" -> criaa tag para commit antigos
git show <tag> -> exibe as informações da tag
git checkout <tag> -> retorna para o estado daquela tag
git checkout master -> retorna para a master
git tag -d v0.0 -> deleta a tag


**OUTROS COMANDOS**
git diff -> mostra diferenças específicas em arquivos alterados
git diff --staged -> mostra as diferenças que estão no modo staged
git mv <file_from> <file_to> -> move arquivos no git, renomeia se git mv <file_name> <new_file_name>
gitk -> abre uma GUI de relatório dos comitts no git bash
git init --bare -> cria repositório pushable

**GIT BASH**
inicia na pasta desejada ao alterar essa opção em "propriedades" do ícone (volta pro padrão se estiver escrito --cd-to-home no destino)

**GITLAB**
cria ssh no windows (powershell) com:
ssh-keygen -t ed25519 -C "<email>" -> ED25519 keys are more secure and performant than RSA keys
armazena a chave no local padrão
coloca senha (qualquer coisa as chaves podem ser reescritas repetindo o procedimento)
visualiza a chave pública com:
cat ~/.ssh/id_ed25519.pub -> powershell
cat ~/.ssh/id_ed25519.pub | clip -> gitbash, copia pra área de transferência
git config --global http.sslVerify false -> desativa essa verificação pra intranet

**SUBMODULES**
git submodule update --init
git submodule update --init --rebase
git submodule update --init --force
