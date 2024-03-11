Este repositório tem como propósito principal armazenar documentações elaboradas durante outros projetos que requeriam um fluxo de trabalho colaborativo com Git.

Além disso, sob uma perspectiva educacional, este repositório também visa proporcionar uma compreensão abrangente do conceito de workflow Git, junto de suas abordagens variadas, importância, benefícios, metodologias de trabalho, bem como o fornecimento de diagramas e fluxogramas para uma visualização mais clara e didática.

Com o objetivo de aprender através da prática, foi utilizado o workflow Git Flow no desenvolvimento deste repositório.

## Instalação

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

## Git

O Git é um sistema que nos permite controlar as diferentes versões de nossos arquivos ao longo do tempo, permitindo acompanhar todas as mudanças que fazemos em nossos arquivos e até mesmo voltar a versões anteriores se necessário.

Com o Git, podemos compartilhar nosso projeto com outras pessoas, mesmo que elas estejam em locais diferentes. Podemos enviar nossas mudanças para um "repositório remoto", onde outras pessoas podem ver o que fizemos e até mesmo contribuir com suas próprias mudanças. Isso facilita a colaboração em grandes projetos com equipes dispersas.

Sendo um sistema distribuído de controle de versão, o git permite que cada usuário tenha uma cópia completa do repositório em seu próprio computador, fornecendo assim uma redundância valiosa e a capacidade de restaurar o projeto em caso de falha do servidor central.

![imagem do sistema de versionamento distribuído]()

Com o Git, podemos criar "ramificações" do nosso projeto, podendo trabalhar em diferentes partes do projeto ao mesmo tempo sem interferir no trabalho de outras pessoas. 
> obs: Quando terminamos nosso trabalho em uma ramificação, podemos combiná-la de volta ao projeto principal, chamado de "merge".

Cada vez que fazemos uma alteração em nossos arquivos, podemos "confirmar" essas alterações com uma mensagem. Esses "commits" são como pequenos pacotes de mudanças que são registrados em um histórico, para que possamos ver exatamente o que foi alterado e por quem.

Boas práticas de commits são essenciais para manter um histórico de alterações claro e organizado.
> obs: Para aprender mais sobre boas práticas de commits [clique aqui]()

Para facilitar o gerenciamento eficiente de projetos de software colaborativos, usa-se um workflow Git. Esse workflow define as diretrizes e práticas para coordenar o desenvolvimento, revisão, teste e implantação de código em equipe.

## Git Workflow

## Issues

[ ] Git Flow

[ ] Github Flow

[ ] Gitlab Flow

[ ] Trunk-Based Development

[ ] Proteção de branches