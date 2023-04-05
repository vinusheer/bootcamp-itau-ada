## Bootcamp Itaú | Projeto do módulo [DE-OP-010] PIPELINES DE CI E CD

### Cenário:
Esse repositório possui uma aplicação de Backend e uma de Frontend, ambas precisam ser testadas e suas imagens Docker criadas e enviadas ao GitHub Packages. No nosso cenário, é um problema que isso seja feito manualmente. Sendo assim, cada grupo deverá criar **dois (2)** *workflows* no GitHub Actions, sendo um para a aplicação de Frontend e outro para o Backend.


### Importante lembrar que:
1. Dentro de cada workflow, os steps de teste e build do Docker deverão ser separados;
2. Seus workflows deverão rodar no **Runner self-hosted** que criamos anteriormente;
3. Os workflows obrigatoriamente deverão estar numa pasta chamada .github/workflows;
4. Para mandar sua imagem Docker para o GitHub Packages, você deverá gerar um **P**ersonal **A**ccess **Token** (PAT), aqui você encontra a [documentação](https://docs.github.com/pt/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token);
5. Os worklflows deverão ser disparados quanto a branch **main** for alterada, porém as mudanças deverão via a partir de **Pull Requests**;
6. Os Dockerfile estão dentro da pasta de cada aplicação;

#### Observações sobre a app de Frontend:
- Essa app só requer dois passos: rodar os testes e build da imagem Docker e mandar para o GitHub Packages:
```sh
# as dependencias necessarias sao o npm e a angular-cli
$ apt-get update && apt-get -y install npm
$ npm install -g @angular/cli

# rodar testes
$ ng test
```

#### Observações sobre a app de Backend:
- Essa app requer três passos: rodar os testes, build do java e build da imagem Docker e mandar para o GitHub Packages:
```sh
# a principal dependencia a ser instalada e o maven
$ apt-get update && apt-get -y install maven

# rodar os testes
$ mvn clean test

# build do java
$ mvn clean package
```
#### Links úteis:
- Repositório com alguns exemplos de Actions: https://github.com/andre177/desafio-devops-letscode
- Documentação do Github Actions: https://docs.github.com/pt/actions
- Repositório com Actions prontas: https://github.com/orgs/actions/repositories
---
## Observações gerais do projeto
1. A apresentação pode ser feita por apenas um integrante do grupo, bem como a entrega. Apenas um integrante subirá o link do repo onde o projeto foi feito no Class, lembrando de adicionar na resposta o nome dos outros integrantes do grupo;
2. Dentro do Class, a tarefa do projeto estará na aula 7 - GitHub Actions;
3. A apresentação será feita no dia 10/04, a partir da segunda metade da aula;
4. Não apagar as branches que foram usadas no projeto após finalizar as Pull Requests;
5. Lembrem-se, o objetivo aqui não é testar vocês, e sim botar em prática os conhecimentos que adiquirimos juntos!

### Divirtam-se!!! :hugs:
