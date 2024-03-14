# Boas Práticas de Commits

Adotar boas práticas de commits é essencial para manter um histórico de alterações claro e organizado.

Explique de forma breve as alterações realizadas, evitando descrições genéricas ou ambíguas.

Realize commits pequenos e focados em uma única alteração ou tarefa.

No final, escrever boas mensagens de commit demonstra que você é um bom colaborador.

```git
git commit -a -m "<tipo>[escopo opcional]: <descrição>
[corpo opcional]
[rodapé opcional]"
```

> obs: Os commits devem ser realizados com os seguintes tipos e rótulos:
> 
> feat - Adicionar um novo recurso à aplicação.
> 
> fix - Corrigir um bug na aplicação.
> 
> chore - Indicar um trabalho em progresso de uma funcionalidade.
> 
> build - Alterações que afetam o sistema de build ou dependências externas.
>
> static - Alterações no conteúdo de arquivos estáticos, como dados .json, imagens, etc.
> 
> docs - Alterações exclusivamente na documentação.
> 
> refactor - Alterações de código que não corrigem um bug nem modificam a forma como o usuário utiliza a aplicação.
> 
> style - Alterações que não afetam o significado do código, como espaços em branco, formatação, ponto e vírgula, etc.
> 
> test - Adicionar testes ausentes ou corrigir testes existentes.

## Bons exemplos de commits

```git
git commit -a -m "docs: Atualiza o README.md com instruções de instalação

Adicionada informações detalhadas sobre como instalar e configurar o projeto"
```

```git
fix[login]: Corrige validação de senha inválida

Aprimorada a lógica de validação de senha para tratar corretamente senhas inválidas

Issue #123
```

```git
refactor: Refatora função de ordenação

Simplificada a implementação da função de ordenação, melhorando o desempenho e a legibilidade do código
```