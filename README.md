## Criando localmente
```
git init
git branch -M "main/master" 
git remote add origin https://github.com/Cazotti/git-test.git
git pull -u origin main
```

## Realizando Commit's
```
git status
git add (*, all, README.txt, *.txt)
git commit -m "Comentário aqui."
```

## Subindo para o Repositório
```
git push
```

## Clonando Repositório
```
git clone https://github.com/Cazotti/git-test.git
```

## Criação e Manuseio de Branch's
```
git branch --> Lista todas as Branch's.
git log-graph --> Lista todas as Branch's graficamente.
git branch "name-branch" --> Cria uma Branch.
git checkout "name-branch" --> Altera para a Branch informada.
git merge "name-branch" --> Mescla duas Branch's.
git branch -d "name-branch" --> Remove a Branch.
git push origin "name-branch" --> Sobe a Branch local para o repositório.
```

## Stashing
```
git stash save --> Salva os arquivos que ainda não foram concluidos em uma área temporária.
git stash apply --> Aplica o stash posicionado no topo da fila.
git stash apply [stash@[1]]--> Aplica o stash que foi passado. 

git stash drop --> Exclui o stach no topo da fila. 
git stash list --> Limpa toda a lista de staches.

git stash list --> Mostra a lista de stashes sendo utilizados.
git stash show [stash@[1]]--> Mostra os dados do stash passado.
```
