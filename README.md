# Documentação sobre Git Workflow 

Este repositório tem como propósito principal armazenar documentações elaboradas durante outros projetos que requeriam um fluxo de trabalho colaborativo com Git.

Além disso, este repositório busca explicar de forma abrangente o conceito de workflow Git, suas diferentes abordagens, importância e benefícios, com o auxílio de imagens para facilitar a compreensão.

Com o objetivo de aprender através da prática, foi utilizado o workflow `Git Flow` no desenvolvimento deste repositório.

## Sumário

[Instalação](#instalação) • [Git](#git) • [Git Workflow](#git-workflow) • [Git Flow](#git-flow)

## Instalação
<details>
<summary>Clique aqui!</summary>
<p>

### Pré-requisitos para instalação!

![Git](https://img.shields.io/badge/Git-E34F26?style=for-the-badge&logo=git&logoColor=white)
--------------------------------------------------------------------------------------------

Para começar, clone o repositório do projeto em seu ambiente local. Siga a etapa abaixo:

* Abra o terminal na pasta onde deseja clonar o repositório.

* Clone o repositório para o seu ambiente local usando o seguinte comando:

```git
git clone https://github.com/JoaoLucasAssis/Git_Workflow.git
```

> :warning: obs: Certifique-se de ter o git instalado antes de executar o comando no terminal

* Execute o comando a seguir para buscar todas as branches do repositório remoto:

```git
git fetch --all
```

> :bulb: obs: Para listar todas as branches, execute o comando:
>
> git branch -a

* Crie uma branch local baseada na branch remota `develop` com o seguinte comando:

```git
git checkout develop
```

Agora você está pronto para começar a trabalhar em sua nova branch!
</p>
</details>

## Git

O Git é um sistema de controle de versão que nos permite controlar as diferentes versões de nossos arquivos ao longo do tempo, permitindo acompanhar todas as mudanças que fazemos em nossos arquivos e até mesmo voltar a versões anteriores se necessário.
> :bulb: obs: Para aprender mais sobre git e alguns comandos [clique aqui](https://github.com/JoaoLucasAssis/Git_GitHub)

Sendo um sistema distribuído de controle de versão, o git permite que cada usuário tenha uma cópia completa do repositório em seu próprio computador, fornecendo redundância e a capacidade de restaurar o projeto em caso de falha do servidor central.

<p align="center"><img  src="https://git-scm.com/book/en/v2/images/distributed.png" alt="imagem controle de versão distribuído" width="450px" height="450px"/></p>

Com o Git, podemos criar "ramificações" do nosso projeto, podendo trabalhar em diferentes partes do projeto ao mesmo tempo sem interferir no trabalho de outras pessoas. 

Cada alteração nos arquivos é "confirmada" por meio de um commit, sendo como pequenos pacotes de mudanças que são registrados em um histórico, para que possamos ver exatamente o que foi alterado e por quem.
> :bulb: obs: Para aprender mais sobre boas práticas de commits [clique aqui](https://github.com/JoaoLucasAssis/Git_Workflow/blob/develop/commits.md)

Para facilitar o gerenciamento eficiente de projetos de software colaborativos, usa-se um workflow Git. Esse workflow define as diretrizes e práticas para coordenar o desenvolvimento, revisão, teste e implantação de código em equipe.

## Git Workflow

É um conjunto de práticas e processos utilizados para gerenciar o fluxo de trabalho de desenvolvimento de software usando o sistema de controle de versão git.

Ele define como as alterações são propostas, revisadas, testadas e mescladas durante o ciclo de vida do desenvolvimento de um projeto.

Há vários Git Workflows que podem ser uma boa opção para sua equipe. Neste repositório iremos abordar os seguintes:

[
Eu não tenho certeza de nada que está marcado nessa tabela
_
CONFIRMAR ANTES DE MUDAR A VISIBILIDADE DO REPOSITÓRIO
_
]: #

|Workflows     |Integração Contínua (CI)|Entrega Contínua (CD)|Branch Única|Reversão Simples de Alterações|Suporte a Ambientes de Produção|Automação de Testes|Facilidade de Uso|Flexibiliade|Estabilidade|Automatização|Simplicidade|Agilidade|
|:------------:|:----------------------:|:-------------------:|:----------:|:----------------------------:|:-----------------------------:|:-----------------:|:---------------:|:----------:|:----------:|:-----------:|:----------:|:-------:|
|GitFlow       |                        |                     |            |                              |:heavy_check_mark:             |:heavy_check_mark: |                 |            |:heavy_check_mark:|:heavy_check_mark:|            |         |
|Github Flow   |                        |:heavy_check_mark:   |:heavy_check_mark:|:heavy_check_mark:      |                               |:heavy_check_mark: |:heavy_check_mark:|:heavy_check_mark:|            |:heavy_check_mark:|:heavy_check_mark:|         |
|GitLab        |:heavy_check_mark:      |:heavy_check_mark:   |:heavy_check_mark:|                        |:heavy_check_mark:             |:heavy_check_mark: |                 |            |:heavy_check_mark:|:heavy_check_mark:|            |         |
|Trunk-based Development|               |:heavy_check_mark:   |:heavy_check_mark:|                        |                               |                   |                 |            |            |             |:heavy_check_mark:|:heavy_check_mark:|

## Git Flow

Consiste no uso de ramificações de recursos e várias ramificações primárias.

Utiliza duas branches principais, `main` e a `develop`, que são permanentes e sempre estarão presentes, e três branches de suporte temporárias: `feature`, `release` e `hotfix`.

O Gitflow tem mais ramificações de vida longa e commits maiores, retardando o merge com a main até que o recurso esteja completo.

> :warning: obs: Este é apenas um resumo sobre Git Flow. Para mais detalhes [clique aqui](https://github.com/JoaoLucasAssis/Git_Workflow/blob/feature/git-flow/gitflow.md)

### Branches Principais

`main`

A branch principal que armazena o código estável e oficial do projeto.

`develop`

A branch de desenvolvimento, onde novas branches são criadas e novos recursos e funcionalidades são adicionados.

### Branches de Suporte

`feature`

Criadas para o desenvolvimento de funcionalidades específicas.

Elas devem ter o nome iniciado por **"feature/"** seguido por uma **descrição**.

Essas branches são criadas a partir da branch **develop** e, após finalizadas, são removidas após serem mescladas com a branch **develop**.

`release`

Criadas para fazer o lançamento de novas funcionalidades da branch **develop** para a branch **main**.

Elas devem ter o nome iniciado por **"release/"** seguido por uma **versão**.

Essas branches são criadas a partir da branch **develop** e, após finalizadas, são removidas após serem mescladas com a branch **main**.

`hotfix`

Criadas para fazer correções com rapidez no código base na branch **main**.

Elas devem ter o nome iniciado por **"hotfix/"** seguido por uma **versão**.

Essas branches são criadas a partir da branch **main** e, após finalizadas, são removidas após serem mescladas com a branch **main** e **develop**.

`bugfix`

Criadas para fazer para correções encontradas no momento da validação na branch **release**.

Elas devem ter o nome iniciado por **"bugfix/"** seguido por uma **descrição**.

Essas branches são criadas a partir da branch **release** e, após finalizadas, são removidas após serem mescladas com a branch **release**.

> :warning: obs: Este é apenas um resumo sobre Git Flow. Para mais detalhes [clique aqui](https://github.com/JoaoLucasAssis/Git_Workflow/blob/feature/git-flow/gitflow.md)
