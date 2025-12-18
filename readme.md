# GIT / GIT HUB - Comandos gerais / General commands

## 🔹Configuração Inicial (Executar uma vez) / Initial Setup (Run once)

⚙️ PT - É sempre um pouco dificil lembrar de codigos do git e do github principalmente para pessoas que estão iniciando. Na tentativa de ajudar compilei abaixo uma lista completa de codigos e claro aceito sugestões.

⚙️ EN - It's always a little difficult to remember Git and GitHub codes, especially for beginners. In an attempt to help, I've compiled a complete list of codes below, and of course, I welcome suggestions.

```python
git config --global user.name "user.name"
```

_Define seu nome para todos os projetos no PC._  
_Set your name for all projects on your PC._

```python
git config --global user.email "user.email"
```

_Define seu email para todos os projetos no PC._  
_Set your email address for all projects on your PC._

```python
git config user.name "user.name"
```

_Define seu nome para projeto especifico._  
_Define your name for a specific project._

```python
git config user.email "user.email"
```

_Define seu email para projeto especifico._  
_Define your email for a specific project._

```python
git config user.name
```

_Verifica qual nome está configurado no projeto atual._  
_Check which name is configured in the current project._

```python
git config user.email
```

_Verifica qual email está configurado no projeto atual._  
_Check which email address is configured in the current project._

```python
git config --global --list
```

_Lista todas as configurações globais._  
_Lists all global settings._

```python
git --version
```

_Verifica versão do git instalada_  
_Check the installed git version._

```python
ls -al ~/.ssh
```

_Verifica se existe chave ssh cadastrada no computador_  
_Checks if an SSH key is registered on the computer._

```python
ssh-keygen -t ed25519 -C "user.email" -f ~/.ssh/id_ed25519_"nome"
```

_Gerar uma nova chave SSH com descrição especifica_  
_Generate a new SSH key with a specific description._

## 🔹Comandos de Navegação (Bash/Terminal) / Navigation Commands (Bash/Terminal)

```python
pwd
```

_Mostra o caminho da pasta onde você está agora._  
_Shows the path to the folder you are currently in._

```python
ls
```

_Lista os arquivos (visíveis) da pasta atual._  
_Lists the (visible) files in the current folder._

```python
ls -a
```

_Lista todos os arquivos (incluindo ocultos, como .git)._  
_Lists all files (including hidden files, such as .git)._

```python
cd "nome.pasta"
```

_Entra na pasta._  
_Enter the folder._

```python
cd ..
```

_Sai da pasta atual (volta um nível)._  
_Exit the current folder (go back one level)._

```python
mkdir "nome.pasta"
```

_Cria uma nova pasta vazia._  
_Creates a new empty folder._

```python
touch "nome_arquivo.ext"
```

_Cria um arquivo vazio._  
_Creates an empty file._

```python
ctrl + l
```

_Limpa a tela do terminal (visual)._  
_Clears the terminal screen (visually)._

```python
cat "nome_arquivo.ext"
```

_Mostra o conteúdo do arquivo._  
_Shows the contents of the file._

## 🔹O Ciclo Básico (Dia a Dia) / The Basic Cycle (Day by Day)

```python
git init

```
_Transforma a pasta atual em um repositório Git._  
_Transforms the current folder into a Git repository._

```python
git status
```

_O comando mais importante. Mostra o que mudou, o que está no stage, etc._  
_The most important command. It shows what has changed, what's on the stage, etc._

```python
git add "nome_arquivo.ext"
```

_Prepara um arquivo específico para o próximo commit (Stage)._  
_Prepares a specific file for the next commit (Stage)._

```python
git add .
```

_Prepara todos os arquivos alterados/novos para o commit._  
_Prepares all changed/new files for commit._

```python
git commit -m "mensagem"
```

_Grava o "snapshot" (foto) dos arquivos que estão no Stage._  
_Records a "snapshot" (photo) of the files that are on the Stage._

```python
git show
```

_mostra os detalhes (diferenças) do último commit._  
_shows the details (differences) of the last commit._

```python
git log
```

_Mostra o histórico de commits (autor, data, hash)._  
_Displays the commit history (author, date, hash)._

```python
git log --oneline
```

_Mostra o histórico resumido (útil para leitura rápida)._  
_Shows a summary of the history (useful for quick reading)._

```python
git diff
```

_Mostra as diferenças entre a árvore de trabalho e a área de staging._  
_Shows the differences between the work tree and the staging area._

```python
git tag
```

_Cria uma tag/versão._  
_Creates a tag/version._

```python
git blame "nome_arquivo.ext"
```

_Mostra quem alterou cada linha do arquivo._  
_Shows who modified each line of the file._

## 🔹Ramificação (Branches) / Branches

```python
git branch
```

_Lista as branches locais. O asterisco (*) indica a atual._  
_Lists the local branches. The asterisk (*) indicates the current branch._

```python
git branch "nome_branch"
```

_Apenas cria uma branch, mas não muda para ela._  
_It only creates a branch, but doesn't switch to it._

```python
git switch "nome_branch"
```

_Troca para a branch especificada. (Antigo: git checkout)._  
_Switch to the specified branch. (Old: git checkout)._

```python
git switch -c "nome_branch"
```

_Cria e já troca para a nova branch. (Antigo: git checkout -b)._  
_Creates and switches to the new branch. (Old method: git checkout -b)._

```python
git push -u origin "nome_branch"
```

_Cria a branch também no github para permissão de commits._  
_Also create the branch on GitHub to allow commits._

```python
git merge "nome_branch"
```

_Funde a branch especificada na branch atual._  
_Merge the specified branch into the current branch._

```python
git branch -d "nome_branch"
```

_Deleta uma branch (se já foi mergeada)._  
_Deletes a branch (if it has already been merged)._

```python
git branch -D "nome_branch"
```

_Força a deleção de uma branch (mesmo sem merge)._  
_Forces the deletion of a branch (even without a merge)._

## 🔹Sincronização com GitHub (Remoto) / Synchronization with GitHub (Remote)

```python
git clone "url"
```

_Baixa um repositório completo do GitHub para seu PC._  
_Download a complete GitHub repository to your PC._

```python
git remote add origin "URL"
```

_Conecta seu repositório local a um repositório vazio no GitHub._  
_Connects your local repository to an empty repository on GitHub._

```python
git remote remove origin
```

_Remove o remoto URL._  
_Remove the remote URL._

```python
git remote -v
```

_Ver o endereço remoto atual utilizado._  
_View the currently used remote address._

```python
git remote set-url origin "URL"
```

_Altere o endereço remoto para o repositório correto._  
_Change the remote address to the correct repository._

```python
git push -u origin main
```

_Envia seus commits locais para o GitHub (primeira vez)._  
_Send your local commits to GitHub (first time)._

```python
git push
```

_Envia seus commits para o GitHub (após configurado)._  
_Send your commits to GitHub (after configuration)._

```python
git pull
```

_Traz alterações do GitHub para seu PC e faz merge automático._  
_Brings changes from GitHub to your PC and performs automatic merges._

```python
git fetch
```

_Baixa informações do GitHub mas não altera seus arquivos (seguro)._  
_Downloads information from GitHub but does not modify your files (safe)._

## 🔹Desfazendo Coisas (Cinto de Segurança) / Taking Things Apart (Seat Belt)

```python
git restore "nome_arquivo.ext"
```

_Descarta alterações no arquivo (volta como estava no último commit)._  
_Discards changes to the file (reverts it to its state in the last commit)._

```python
git reset "nome_arquivo.ext"
```

_Tira o arquivo do Stage (mas mantem as alterações no arquivo)._  
_Remove the file from the Stage (but keep the changes in the file)._

```python
git commit --amend -m "txt"
```

_Corrige a mensagem do último commit (se não foi enviado ainda)._  
_Corrects the message from the last commit (if it hasn't been sent yet)._

```python
git stash
```

_Guarda mudanças temporariamente num "bolso" para limpar a área de trabalho._  
_Temporarily store spare change in a "pocket" to clear your workspace._

```python
git stash pop
```

_Recupera as mudanças guardadas no "bolso"._  
_Retrieve the changes kept in your "pocket"._

```python
git checkout "codigo_do_ultimo_commit" "nome_arquivo.ext"
```

_Restaura arquivo deletado a partir do ultimo commit._  
_Restores deleted files starting from the last commit._

## 🔺Apagando arquivos, (Perigo) / Deleting files (Danger)

```python
rm nome_"nome_arquivo.ext"
```

_Deletar um arquivo específico do repositório local._  
_Delete a specific file from the local repository._

```python
rm -i "nome_arquivo.ext"
```

_Deletar um arquivo pedindo confirmação (mais seguro)._  
_Deleting a file and requesting confirmation (more secure)._

```python
rmdir "nome_pasta"
```

_Deletar uma pasta vazia._  
_Delete an empty folder._

```python
rm -r "nome_pasta"
```

_Deletar uma pasta com conteúdo._  
_Delete a folder containing content._