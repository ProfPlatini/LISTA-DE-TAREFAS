# Lista Fácil

Aplicação web de lista de tarefas, feita para ser simples de usar e fácil de estudar. A página permite cadastrar tarefas, definir prioridade e prazo, pesquisar, filtrar, editar, concluir e excluir itens.

## Destaque: Page Agent

Este projeto **tem integração com o Page Agent**. O agente é carregado ao final do `index.html` por meio do script:

```html
<script
  src="https://cdn.jsdelivr.net/npm/page-agent@1.12.4/dist/iife/page-agent.demo.js"
  crossorigin="anonymous"
></script>
```

O Page Agent é a camada de agente da página e pode interagir com a interface para demonstrar ou automatizar ações no aplicativo, como preencher o formulário e manipular tarefas. A integração fica separada da lógica principal da lista, que continua sendo executada pelo JavaScript escrito no próprio arquivo.

> A página exibe um aviso de demonstração com IA externa. Use apenas dados fictícios ao testar o Page Agent.

## Funcionalidades

- Adição de tarefas com título, prioridade e prazo opcional
- Edição, conclusão e exclusão de tarefas
- Busca por texto e filtro de tarefas pendentes
- Indicador visual de progresso do dia
- Persistência no navegador usando `localStorage`
- Layout responsivo para desktop e celular
- HTML semântico e estados de foco para melhor acessibilidade

## Tecnologias

- HTML5
- CSS3, com estilos embutidos no `index.html`
- JavaScript puro, também embutido no `index.html`
- `localStorage` para salvar as tarefas localmente
- Page Agent 1.12.4, carregado externamente via jsDelivr

## Como executar

Como não há dependências nem processo de compilação, basta abrir o arquivo [`index.html`](./index.html) em um navegador.

Para executar por um servidor local, uma opção é usar:

```bash
python -m http.server 8000
```

Depois, acesse <http://localhost:8000>.

## Estrutura

```text
.
├── index.html   # Interface, estilos, lógica da lista e integração com o Page Agent
└── README.md    # Documentação do projeto
```

## Dados e privacidade

As tarefas são armazenadas apenas no `localStorage` do navegador, usando a chave `lista-facil-tarefas-demo-agente`. Elas não são enviadas por esta aplicação para um backend próprio. O Page Agent é carregado de um serviço externo; por isso, a aplicação deve ser usada somente com dados de demonstração.

## Licença

Projeto de demonstração para estudo e experimentação.
