# Documentação sobre Git Workflow

Este repositório tem como propósito principal armazenar documentações elaboradas durante outros projetos que requeriam um fluxo de trabalho colaborativo com Git.

Além disso, este repositório busca explicar de forma abrangente o conceito de workflow Git, suas diferentes abordagens, importância e benefícios, com o auxílio de imagens para facilitar a compreensão.

Com o objetivo de aprender através da prática, foi utilizado o workflow `Git Flow` no desenvolvimento deste repositório.

## Sumário

[Instalação](#instalação) • [Git](#git) • [Git Workflow](#git-workflow)

## Instalação
<details>
<summary>Clique aqui!</summary>
<p>
Para começar, clone o repositório do projeto em seu ambiente local. Siga a etapa abaixo:

* Abra o terminal na pasta onde deseja clonar o repositório.

* Clone o repositório para o seu ambiente local usando o seguinte comando:

```git
git clone https://github.com/JoaoLucasAssis/Git_Workflow.git
```

> obs: Certifique-se de ter o git instalado antes de executar o comando no terminal

* Execute o comando a seguir para buscar todas as branches do repositório remoto:

```git
git fetch --all
```

> obs: Para listar todas as branches, execute o comando:
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
> obs: Para aprender mais sobre git e alguns comandos [clique aqui](https://github.com/JoaoLucasAssis/Git_GitHub)

Sendo um sistema distribuído de controle de versão, o git permite que cada usuário tenha uma cópia completa do repositório em seu próprio computador, fornecendo redundância e a capacidade de restaurar o projeto em caso de falha do servidor central.

<p align="center"><img  src="https://git-scm.com/book/en/v2/images/distributed.png" alt="imagem controle de versão distribuído" width="420px" height="420px"/></p>

Com o Git, podemos criar "ramificações" do nosso projeto, podendo trabalhar em diferentes partes do projeto ao mesmo tempo sem interferir no trabalho de outras pessoas. 

Cada alteração nos arquivos é "confirmada" por meio de um commit, sendo como pequenos pacotes de mudanças que são registrados em um histórico, para que possamos ver exatamente o que foi alterado e por quem.
> obs: Para aprender mais sobre boas práticas de commits [clique aqui](https://github.com/JoaoLucasAssis/Git_Workflow/blob/develop/commits.md)

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

## Issues

- [ ] Git Workflow

- [ ] Git Flow

- [ ] Github Flow

- [ ] Gitlab Flow

- [ ] Trunk-Based Development

- [ ] Proteção de branches
