## Criando localmente
```
$ git init
$ git branch -M "main/master" 
$ git remote add origin https://github.com/Cazotti/git-test.git
$ git pull -u origin main
```

## Realizando Commit's
```
$ git status
$ git add (*, all, README.txt, *.txt)
$ git commit -m "Comentário aqui."
```

## Subindo para o Repositório
```
$ git push
```

## Clonando Repositório
```
$ git clone https://github.com/Cazotti/git-test.git
```

## Criação e Manuseio de Branch's
```
git branch --> Lista todas as Branch's.
git branch "name-branch" --> Cria uma Branch.
git checkout "name-branch" --> Altera para a Branch informada.
git merge "name-branch" --> Mescla duas Branch's.
git branch -d "name-branch" --> Remove a Branch.
git push origin "name-branch" --> Sobe a Branch local para o repositório.
```

## Rebase
```
git rebase (--continue | --abort | --skip)
```

> Rebase Simple
```
git checkout "main/master"
git fetch
git rebase "name.branch"
```

> Rebase Simple^2
```
git checkout "name.branch"
git rebase "main/master"
git checkout "main/master"
git merge "name.branch"
```
## Interactive Rebase
> Rebase Simple^3 (Trocar ordem de commits)
```
git rebase -i HEAD~4
git rebase --continue
```
> Rebase Simple^4 (Alterar mensagem do commit)
```
git rebase -i HEAD~4
(trocar pick por reword)
git rebase --continue
```
> Rebase Simple^4 (Transformar 1 commit em dois ou mais)
```
git rebase -i HEAD~4
(trocar pick por edit)
git reset HEAD^
Realizar commit separados
git rebase --continue
```
> Rebase Simple^5 (Transformar 2 commits em um)
```
git rebase -i HEAD~4
(trocar pick por squash no ultimo)
git rebase --continue
```

## Stashing
```
git stash save --> Salva os arquivos que ainda não foram concluidos em uma área temporária.
git stash apply --> Aplica o stash posicionado no topo da fila.
git stash apply [stash@[1]]--> Aplica o stash que foi passado. 

git stash drop --> Exclui o stach no topo da fila. 
git stash clear --> Limpa toda a lista de staches.

git stash list --> Mostra a lista de stashes sendo utilizados.
git stash show [stash@[1]]--> Mostra os dados do stash passado.
```

# Purging History
```
git filter-branch --tree-filter <command> -- --all --> Percorre todo o repositório, incluindo as branches executando o comando especificado.
git filter-branch --tree-filter 'rm -f passwords.txt' --prune-empty -- --all

git filter-branch -f --prune-empty -- --all --> Limpa os commits vazios.
```

# Submodules
```
git submodule add git@example.com:css.git --> Adiciona um submodulo ao repositório.
git submodule init
git submodule update
```
#Reflog
```
git reflog
```
