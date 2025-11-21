# TechPedia: Um Dicionário de Tecnologias

Bem-vindo ao TechPedia! Este é um projeto simples, mas funcional, que atua como um dicionário ou uma enciclopédia rápida para diversas tecnologias, linguagens de programação, frameworks e ferramentas do mundo do desenvolvimento de software. Ele exibe uma lista de tecnologias e permite que o usuário filtre essa lista em tempo real.

Este projeto foi desenvolvido com o objetivo de praticar conceitos fundamentais de HTML, CSS e JavaScript, incluindo manipulação do DOM, consumo de dados de um arquivo JSON e responsividade.

## 🚀 Como Funciona?

A aplicação consiste em uma única página que apresenta um campo de busca e uma lista de "cards". Cada card representa uma tecnologia e contém as seguintes informações:

- **Nome da Tecnologia**: O título do card.
- **Data de Criação**: O ano em que a tecnologia foi criada.
- **Descrição**: Um breve resumo sobre o que é e para que serve.
- **Link**: Um link para a página oficial ou documentação para "Saber mais".

A principal funcionalidade é a **busca dinâmica**: à medida que o usuário digita no campo de busca, a lista de cards é filtrada para mostrar apenas as tecnologias cujo nome ou descrição correspondem ao termo pesquisado.

## 📂 Estrutura do Projeto

O projeto está organizado da seguinte forma:

```
/
|-- index.html         # A estrutura principal da página web
|-- README.md          # Este arquivo que você está lendo
|-- src/
|   |-- style.css      # Arquivo de estilos para a aparência da página
|   |-- script.js      # Arquivo com a lógica de funcionamento (busca, etc.)
|   `-- data.json      # O "banco de dados" com a lista de tecnologias
```

### Detalhes dos Arquivos

- **`index.html`**: Define o esqueleto da página. Contém a tag `<header>` com o título e o campo de busca, e uma `<main>` onde os cards das tecnologias são inseridos dinamicamente pelo JavaScript.

- **`src/style.css`**: Responsável por toda a parte visual. Define as cores, fontes, espaçamentos, o layout dos cards e a responsividade para que a página se adapte bem a diferentes tamanhos de tela (desktop, tablet e mobile).

- **`src/data.json`**: É o coração do conteúdo da aplicação. Este arquivo contém um array de objetos, onde cada objeto representa uma tecnologia e segue a estrutura:

  ```json
  {
    "nome": "Nome da Tecnologia",
    "descricao": "Uma explicação sobre ela.",
    "data_criacao": "Ano",
    "link": "URL para o site oficial",
    "tags": ["tag1", "tag2"]
  }
  ```

- **`src/script.js`**: Contém toda a inteligência da aplicação. Suas principais responsabilidades são:
  1.  **Carregar os Dados**: Usar a função `fetch()` para ler o arquivo `data.json` e armazenar os dados em uma variável.
  2.  **Renderizar os Cards**: Criar os elementos HTML para cada tecnologia e inseri-los na página.
  3.  **Implementar a Busca**: Capturar o que o usuário digita, filtrar o array de dados com base nesse termo e chamar a função de renderização novamente para atualizar a tela com os resultados filtrados.

## 🔧 Como Manter e Evoluir o Projeto

Este projeto foi feito para ser simples de manter. Aqui estão as principais tarefas que você pode precisar fazer:

### Adicionar uma Nova Tecnologia

Para adicionar uma nova tecnologia à lista, você só precisa editar o arquivo `src/data.json`.

1.  Abra o arquivo `src/data.json`.
2.  Vá até o final do arquivo, antes do `]` de fechamento.
3.  Adicione uma vírgula `,` após o último objeto `}`.
4.  Copie e cole a estrutura de um objeto existente e preencha com as informações da nova tecnologia.

    **Exemplo de novo item a ser adicionado:**

    ```json
    {
      "nome": "Nova Tecnologia Fantástica",
      "descricao": "Uma descrição incrível sobre como ela vai mudar o mundo do desenvolvimento.",
      "data_criacao": "2024",
      "link": "https://example.com",
      "tags": ["nova", "fantástica", "web"]
    }
    ```

5.  Salve o arquivo. A aplicação irá automaticamente incluir o novo item na próxima vez que for carregada.

### Modificar o Estilo ou Comportamento

- **Para mudar a aparência**: Todas as alterações visuais, como cores, fontes e tamanho dos cards, devem ser feitas no arquivo `src/style.css`. As cores principais estão definidas como variáveis CSS no seletor `:root`, o que facilita a troca do tema.
- **Para mudar a lógica**: Se você quiser alterar como a busca funciona ou adicionar novas funcionalidades (como um filtro por tags), as modificações devem ser feitas no arquivo `src/script.js`. O código está comentado para ajudar a entender o que cada parte faz.

## 💡 Possíveis Melhorias Futuras

Quer levar o projeto para o próximo nível? Aqui estão algumas ideias:

1.  **Filtro por Tags**: Adicionar botões com os nomes das `tags` e permitir que o usuário clique neles para filtrar as tecnologias.
2.  **Ordenação**: Implementar uma funcionalidade para ordenar os cards por nome (A-Z) ou por data de criação (do mais novo para o mais antigo).
3.  **Animações**: Adicionar animações sutis usando CSS quando os cards aparecem ou são filtrados.
4.  **Página de Detalhes**: Fazer com que, ao clicar em um card, o usuário seja levado para uma página com mais detalhes sobre aquela tecnologia.

Divirta-se codificando!
