# 🛒 Carrinho de Compras

Bem-vindo ao projeto **Carrinho de Compras**! Este projeto é uma aplicação web simples que permite adicionar produtos a um carrinho, calcular o valor total e limpar o carrinho quando necessário.

## 🚀 Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript (Vanilla JS)

## 📌 Funcionalidades

✅ Adicionar produtos ao carrinho<br>
✅ Calcular o valor total da compra<br>
✅ Limpar o carrinho com um clique<br>

## 📂 Estrutura do Projeto

```
📂 carrinho-de-compras
│-- 📂 assets (Imagens e ícones utilizados)
│-- 📂 css (Estilos da aplicação)
│-- 📂 js (Scripts JavaScript)
│   └── app.js
│-- index.html (Página principal do projeto)
│-- README.md (Este arquivo!)
```

## 🎨 Estilização

A estilização foi feita utilizando CSS e fontes externas do Google Fonts para melhorar a aparência da interface do usuário.

## ⚡ Como Usar

1. Clone este repositório:
   ```sh
   git clone https://github.com/seu-usuario/carrinho-de-compras.git
   ```
2. Acesse o diretório do projeto:
   ```sh
   cd carrinho-de-compras
   ```
3. Abra o arquivo `index.html` em um navegador.
4. Escolha um produto, defina a quantidade e clique em **Adicionar**.
5. Veja o total da compra e, se desejar, clique em **Limpar** para esvaziar o carrinho.

## 🛠 Código Principal

```javascript
function adicionar() {
    let produto = document.getElementById('produto').value;
    let nomeProduto = produto.split('-')[0];
    let valorUnitario = produto.split('R$')[1];
    let quantidade = document.getElementById('quantidade').value;
    
    let preco = quantidade * valorUnitario;
    let carrinho = document.getElementById('lista-produtos');

    carrinho.innerHTML += `<section class="carrinho__produtos__produto">
      <span class="texto-azul">${quantidade}x</span> ${nomeProduto} <span class="texto-azul">${preco}</span>
    </section>`;

    totalGeral += preco;
    document.getElementById('valor-total').textContent = ` R$ ${totalGeral}`;
    document.getElementById('quantidade').value = 0;
}
```

## 💡 Melhorias Futuras

- Implementar armazenamento local para salvar o carrinho ao recarregar a página.
- Adicionar animações e transições CSS.
- Criar uma API para armazenar produtos dinamicamente.

## 📝 Licença

Este projeto está sob a licença MIT. Sinta-se à vontade para usar e modificar! 🎉

