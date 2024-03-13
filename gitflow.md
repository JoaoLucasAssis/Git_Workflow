# Git Flow

O Git Flow é um fluxo de trabalho no Git que ajuda a organizar o desenvolvimento de software.

<p align="">
    <img src="https://miro.medium.com/v2/resize:fit:800/1*u4dlEq4sqIT6iHL_Usvwnw.png" alt="fluxo de trabalho gitflow" width="400px" height="200px"/>
</p>

Consiste no uso de ramificações de recursos e várias ramificações primárias.

Utiliza duas branches principais, `main` e a `develop`, que são permanentes e sempre estarão presentes, e três branches de suporte temporárias: `feature`, `release` e `hotfix`.

|           Principais         |             Suporte            |
|:----------------------------:|:------------------------------:|
|[main](#branches-principais)   |[feature](#branches-de-recurso)   |
|[develop](#branches-principais)|[release](#branches-de-lançamento)|
|                              |[hotfix](#branches-de-manutenção)  |
|                              |[bugfix](#branches-de-correção)    |


O Gitflow tem mais ramificações de vida longa e commits maiores, retardando o merge com a `main` até que o recurso esteja completo.

## Branches Principais

### Main

A branch `main` é a principal do projeto. 

Ela armazena o código base para a versão estável e oficial do projeto.

### Develop

A branch `develop` é a branch de desenvolvimento. 

É a partir desta que novas branches são criadas para adicionar recursos ou funcionalidades ao projeto.

Posteriormente, esses novos recursos ou funcionalidades serão associados a branch `main`.

## Branches de Recurso

Cada novo recurso deve residir em uma branch ramificada a partir da branch `develop` mais recente.

Para criar uma nova `feature`, utilize o prefixo **feature/** seguido de um **nome descritivo** da funcionalidade:

```git
git checkout develop
git checkout -b feature/<nome_descritivo>
```

## Branches de Lançamento

Uma vez que a branch `develop` adquiriu recursos suficientes para um lançamento, é criado uma branch `release`, a partir da `develop`, para ser lançada para a branch `main`.

Cada branch `release` deve ser mesclada a branch `main` com um número de versão.

Caso haja alguma alteração, a `release` também deve ser mesclada com a `develop`.

Para criar uma `release`, utilize o prefixo **release/** seguido pelo **número da versão** correspondente:

```git
git checkout develop
git checkout -b release/<versao>
```

## Branches de Manutenção

As branches de `hotfix` são usadas para fazer correções com rapidez no código base.

Esta é a única branch que deve ser criada direto da ramificação `main`.

Assim que a correção é concluída, deve-se mesclar a `hotfix` tanto com a branch `main` quanto com a `develop`.

> obs: Caso exista uma release atual, o merge deve ser feito nela, e então, posteriormente, será feito o merge com a develop

Para criar uma `hotfix`, utilize o prefixo **hotfix/** seguido pelo **número da versão** correspondente:

```git
git checkout main
git checkout -b hotfix/<versao>
```

## Branches de Correção

A branch `bugfix` é criada a partir da branch `release` para correções encontradas no momento da validação.

Para criar uma `bugfix`, utilize o prefixo **bugfix/** seguido de um **nome descritivo** da correção:

```git
git checkout release
git checkout -b bugfix/<nome_descritivo>
```