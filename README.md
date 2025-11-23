# Delizie e Dolcezze - Menu Dinâmico



Um projeto de página web elegante e interativa para exibir o menu de um restaurante italiano fictício, "Delizie e Dolcezze". A página carrega dinamicamente os pratos a partir de um arquivo de dados, permite a busca em tempo real e oferece uma visualização detalhada de cada item.

---

## 📜 Documentação e Tutorial

### Funcionalidades Principais

- **Renderização Dinâmica**: Os pratos são carregados a partir de um arquivo `data.json`, facilitando a adição, remoção ou edição de itens sem precisar alterar o código HTML.
- **Busca em Tempo Real**: Um campo de busca permite filtrar os pratos por nome ou descrição instantaneamente, conforme o usuário digita.
- **Visualização Detalhada (Modal)**: Ao clicar na imagem de um prato, um modal expande o card, mostrando mais detalhes, permitindo a leitura da descrição completa e o acesso a links externos.
- **Design Responsivo**: A galeria de pratos se ajusta a diferentes tamanhos de tela, de desktops a celulares, utilizando CSS Grid Layout.

### Tecnologias Utilizadas

- **HTML5**: Para a estrutura semântica da página.
- **CSS3**: Para estilização, layout (Flexbox e Grid) e responsividade.
- **JavaScript (ES6+)**: Para a interatividade, manipulação do DOM, `fetch` de dados (`async/await`) e lógica de busca.

---

### 📂 Estrutura do Projeto

```
/
|-- index.html          # Estrutura principal da página
|-- style.css           # Estilos visuais
|-- script.js           # Lógica e interatividade
|-- data.json           # Banco de dados dos pratos do menu
|-- README.md           # Esta documentação
|-- assets/             # Pasta para as imagens dos pratos
    |-- lasanha.png
    |-- nhoque.png
    |-- ...
```

---

### 🚀 Como Usar

1.  **Executar a Página**:
    - Basta abrir o arquivo `index.html` em qualquer navegador moderno.
    - **Recomendação**: Para evitar possíveis erros de CORS ao carregar o arquivo `data.json` localmente, é ideal usar um servidor local. Uma forma fácil é usar a extensão **Live Server** no Visual Studio Code.

2.  **Como Adicionar um Novo Prato**:
    - **Passo 1**: Adicione a imagem do novo prato (ex: `novo-prato.png`) dentro da pasta `assets/`.
    - **Passo 2**: Abra o arquivo `data.json`.
    - **Passo 3**: Copie um dos objetos existentes, cole no final da lista (antes do `]` final) e altere os valores para o novo prato:

      ```json
      {
          "nome": "Nome do Novo Prato",
          "descricao": "Uma descrição deliciosa do novo prato.",
          "ano": "Origem ou data de criação",
          "link": "https://link-para-mais-infos.com",
          "imagem": "assets/novo-prato.png"
      }
      ```
    - **Passo 4**: Salve o arquivo e recarregue a página. O novo prato aparecerá automaticamente!

---

## ✨ Funcionalidades Futuras (Future Breaches)

Este projeto tem uma base sólida que pode ser expandida com novas funcionalidades para transformá-lo em uma aplicação web mais completa.

### 🛒 Carrinho de Compras

- **Visão**: Implementar um sistema de carrinho de compras onde o usuário pode adicionar os pratos desejados.
- **Como Funcionaria**:
  1. Adicionar um botão "Adicionar ao Pedido" em cada card.
  2. Um ícone de carrinho no cabeçalho mostraria a quantidade de itens.
  3. Ao clicar no ícone, um painel lateral ou uma nova página mostraria os itens selecionados, permitindo ajustar quantidades e ver o subtotal.

### 💬 Pedido via WhatsApp

- **Visão**: Integrar o carrinho de compras com a API do WhatsApp para permitir que o cliente envie seu pedido diretamente para o número do restaurante.
- **Como Funcionaria**:
  1. No carrinho de compras, haveria um botão "Finalizar Pedido via WhatsApp".
  2. Ao clicar, o JavaScript montaria uma mensagem de texto padronizada com a lista de pratos e quantidades (ex: `Olá, gostaria de pedir: 1x Lasanha, 2x Gelato.`).
  3. O usuário seria redirecionado para o WhatsApp com essa mensagem pronta para ser enviada para o número do restaurante, agilizando o processo de pedido.