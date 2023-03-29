## Conhecendo alguns eventos do Git

### Realizar os seguintes passos:

1. Crie um *fork* desse repositório para a sua conta pessoal do GitHub;
2. Faça *merge* da branch `feature/frontend` na branch `main` via *Pull Request*;
3. Agora o *merge* será da branch `task/docker` na branch `main` via *Pull Request*, resolvendo todos os possíveis conflitos, dando prioridade para as mudanças que estão na branch de **origem**;
4. Após todas as mudanças constarem na branch *main*, crie uma a tag **1.0.0** a partir dessa branch;
---
### Comandos básicos do Git
```sh
# clonar o repositório
$ git clone <url-do-repositorio>

# puxar as mudanças mais recentes do repositório
$ git pull

# adicionar um novo arquivo ao repositório
$ git add exemplo.txt

# fazer um commit
$ git commit -m 'descricao do commit' exemplo.txt

# enviar mudanças para o repositório
$ git push

# criar tag
$ git tag -m 'descricao da tag' 0.0.1

# dar push na tag
$ git push --tags

# listar tags criadas no repositório
$ git tag -l

# criar nova branch localmente
$ git checkout -b nome-da-branch

# primeiro push numa branch nova local
$ git push --set-upstream origin nome-da-branch

# saber em qual branch estou no momento
$ git branch

# mudar de branch
$ git checkout branch-que-desejo-ir
```
