# 🍝 Delizie e Dolcezze - Cardápio Interativo

Este é um projeto de um cardápio online interativo para o restaurante fictício "Delizie e Dolcezze". Desenvolvido com tecnologias web modernas, o site oferece uma experiência de usuário fluida e agradável, permitindo que os clientes explorem os pratos, montem um pedido e o enviem diretamente via WhatsApp.

## ✨ Funcionalidades

- **Carregamento Dinâmico:** O cardápio é carregado a partir de um arquivo `data.json`, facilitando a adição ou modificação de pratos sem alterar o código HTML.
- **Busca Inteligente:** Filtre os pratos em tempo real digitando no campo de busca. A pesquisa funciona tanto pelo nome quanto pela descrição do item.
- **Visualização Detalhada:** Clique na imagem de um prato para expandi-la em um modal, exibindo mais detalhes e uma imagem maior.
- **Carrinho de Compras Completo:**
  - Adicione itens ao seu pedido com um clique.
  - Um ícone flutuante mostra a quantidade de itens no carrinho.
  - Um modal de carrinho permite visualizar todos os itens, ajustar quantidades (`+` / `-`) ou remover produtos.
  - O valor total do pedido é calculado e atualizado automaticamente.
- **Integração com WhatsApp:** Ao finalizar o pedido, uma mensagem formatada com todos os itens e o valor total é gerada e aberta no WhatsApp, pronta para ser enviada.

## 🚀 Tecnologias Utilizadas

- **HTML5:** Para a estrutura semântica do site.
- **CSS3:** Para estilização completa, incluindo layout responsivo com Grid e Flexbox, animações e design de modais.
- **JavaScript (ES6+):** Para toda a interatividade, incluindo:
  - Manipulação do DOM.
  - Requisições `fetch` para carregar dados do JSON.
  - Lógica de busca e filtragem.
  - Gerenciamento do estado do carrinho de compras.
  - Geração da mensagem para a API do WhatsApp.

## 📂 Estrutura do Projeto

```
├── assets/                 # Pasta para as imagens dos pratos
├── config.js               # Arquivo de configuração (ex: número do WhatsApp)
├── data.json               # Arquivo com os dados dos pratos (nome, preço, descrição, etc.)
├── index.html              # Arquivo principal da estrutura HTML
├── script.js               # Lógica principal da aplicação em JavaScript
├── style.css               # Folha de estilos principal
└── README.md               # Este arquivo
```

## ⚙️ Configuração e Execução

### Pré-requisitos

Para que a integração com o WhatsApp funcione, você precisa configurar o número de telefone.

1.  Crie um arquivo chamado `config.js` na raiz do projeto.
2.  Dentro deste arquivo, adicione o seguinte código, substituindo pelo número desejado:

    ```javascript
    // /config.js
    export const WHATSAPP_PHONE_NUMBER = "5511999999999"; // Use o formato: código do país + DDD + número
    ```

### Executando o Projeto

Como este projeto utiliza `fetch` para carregar o `data.json` e módulos JavaScript (`import`/`export`), ele precisa ser servido por um servidor web para funcionar corretamente devido às políticas de segurança do navegador (CORS).

1.  **Usando a extensão Live Server (VS Code):**
    - Instale a extensão Live Server no Visual Studio Code.
    - Abra a pasta do projeto no VS Code.
    - Clique com o botão direito no arquivo `index.html` e selecione "Open with Live Server".

2.  **Usando Python:**
    - Navegue até a pasta do projeto pelo terminal.
    - Execute o comando: `python -m http.server`
    - Abra seu navegador e acesse `http://localhost:8000`.

##  Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.