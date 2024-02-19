# TesteSite
Estou estudando uma criação simples de um site de ifood
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="index.css">
  <title>Sistema de Pedidos</title>
</head>
<body>
  <header>
    <h1>Burgueria do Seu Zé</h1>
  </header>
  <main>
    <section id="menu">
      <!-- Lista de itens do menu -->
      <ul id="menu-list">
        <li class="menu-item" data-id="1" data-name="Hamburguer Simples" data-price="10.99">Hamburguer Simples - R$10.99<button onclick="addToCart(1, 'Hamburguer Simples', 10.99)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="2" data-name="Pizza Margherita" data-price="15.99">Pizza Margherita - R$15.99<button onclick="addToCart(2, 'Pizza Margherita', 15.99)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="3" data-name="Coca-Cola - 350ml" data-price="4.50">Coca-Cola - 350ml - R$4.50<button onclick="addToCart(3, 'Coca-Cola - 350ml', 4.50)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="4" data-name="Salada Caesar" data-price="8.99">Salada Caesar - R$8.99<button onclick="addToCart(4, 'Salada Caesar', 8.99)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="5" data-name="Sushi Combo" data-price="22.50">Sushi Combo - R$22.50<button onclick="addToCart(5, 'Sushi Combo', 22.50)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="6" data-name="Lasanha à Bolonhesa" data-price="13.75">Lasanha à Bolonhesa - R$13.75<button onclick="addToCart(6, 'Lasanha à Bolonhesa', 13.75)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="7" data-name="Sanduíche de Frango Grelhado" data-price="9.99">Sanduíche de Frango Grelhado - R$9.99<button onclick="addToCart(7, 'Sanduíche de Frango Grelhado', 10.50)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="8" data-name="Sopa de Tomate" data-price="6.50">Sopa de Tomate - R$6.50<button onclick="addToCart(8, 'Sopa de Tomate', 6.50)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="9" data-name="Burrito de Carne" data-price="11.25">Burrito de Carne - R$11.25<button onclick="addToCart(9, 'Burrito de Carne', 11.25)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="10" data-name="Salada de Frutas" data-price="5.99">Salada de Frutas - R$5.99<button onclick="addToCart(10, 'Salada de Frutas', 5.99)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="11" data-name="Macarrão Carbonara" data-price="14.50">Macarrão Carbonara - R$14.50<button onclick="addToCart(11, 'Macarrão Carbonara', 14.50)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="12" data-name="Tacos de Camarão" data-price="17.75">Tacos de Camarão - R$17.75<button onclick="addToCart(12, 'Tacos de Camarão', 17.75)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="13" data-name="Pão de Alho" data-price="3.25">Pão de Alho - R$3.25<button onclick="addToCart(13, 'Pão de Alho', 3.25)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="14" data-name="Frango Assado" data-price="12.99">Frango Assado - R$12.99<button onclick="addToCart(14, 'Frango Assado', 12.99)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="15" data-name="Smoothie de Frutas" data-price="7.50">Smoothie de Frutas - R$7.50<button onclick="addToCart(15, 'Smoothie de Frutas', 7.50)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="16" data-name="Risoto de Cogumelos" data-price="16.50">Risoto de Cogumelos - R$16.50<button onclick="addToCart(16, 'Risoto de Cogumelos', 16.50)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="17" data-name="Bolo de Chocolate" data-price="9.25">Bolo de Chocolate - R$9.25<button onclick="addToCart(17, 'Bolo de Chocolate', 9.25)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="18" data-name="Salmão Grelhado" data-price="18.99">Salmão Grelhado - R$18.99<button onclick="addToCart(18, 'Salmão Grelhado', 18.99)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="19" data-name="Wrap Vegetariano" data-price="10.75">Wrap Vegetariano - R$10.75<button onclick="addToCart(19, 'Wrap Vegetariano', 10.75)">Adicionar ao Carrinho</button></li>
    <li class="menu-item" data-id="20" data-name="Sorvete de Baunilha" data-price="4.99">Sorvete de Baunilha - R$4.99<button onclick="addToCart(20, 'Sorvete de Baunilha', 4.99)">Adicionar ao Carrinho</button></li>

      </ul>
    </section>

    

    <section id="cart">
        <h2>Carrinho</h2>
        <!-- Lista de itens no carrinho -->
        <ul id="cart-list"></ul>
        <button onclick="removeSelected()">Remover Selecionados</button>
        <div class="checkout-container">
          <p id="total">Total: R$<span id="total-amount">0.00</span></p>
          <button onclick="checkout()">Finalizar Pedido</button>
        </div>
      </section>
  </main>

  <script src="index.js"></script>
</body>
</html>

![Capturar](https://github.com/Victor-Antonio-Santos/TesteSite/assets/160191987/1e1fc503-88d3-4746-91a6-afba0c274b96)

#CSS

body {
    background-color: #3da3a7;
    font-family: 'Arial', sans-serif;
  }
  
  header {
    background-color: #0f9da1;
    padding: 10px;
    text-align: center;
  }
  
  main {
    display: flex;
    justify-content: space-between;
    margin: 20px;
  }
  
  #menu, #cart {
    width: 45%;
    border: 1px solid #ccc;
    padding: 15px;
  }
  
  #menu-list, #cart-list {
    list-style: none;
    padding: 0;
  }
  
  .menu-item {
    position: relative;
    cursor: pointer;
    margin-bottom: 15px; /* Ajuste aqui para controlar o espaçamento vertical */
  }
  
  button {
    background-color: #4caf50;
    color: white;
    border: none;
    cursor: pointer;
    position:relative;
    right: 0;
    margin-left: 10px; /* Ajuste aqui para controlar o espaçamento horizontal */
  }
  
  button:hover {
    background-color: #1d9466;
  }

  #JavaScript

  const menuList = document.getElementById('menu-list');
const cartList = document.getElementById('cart-list');
const totalAmountElement = document.getElementById('total-amount');

let cart = [];

menuList.addEventListener('click', addToCart);

function addToCart(event) {
  if (event.target.tagName === 'BUTTON') {
    const listItem = event.target.parentNode;
    const itemId = listItem.dataset.id;
    const itemName = listItem.dataset.name;
    const itemPrice = parseFloat(listItem.dataset.price);

    const itemInCart = cart.find(item => item.id === itemId);

    if (itemInCart) {
      itemInCart.quantity += 1;
    } else {
      cart.push({
        id: itemId,
        name: itemName,
        price: itemPrice,
        quantity: 1,
        selected: false
      });
    }

    displayCart();
  }
}

function displayCart() {
  cartList.innerHTML = '';
  let totalAmount = 0;

  cart.forEach(item => {
    const li = document.createElement('li');

    const checkbox = document.createElement('input');
    checkbox.type = 'checkbox';
    checkbox.checked = item.selected;
    checkbox.addEventListener('change', () => {
      item.selected = checkbox.checked;
    });

    li.appendChild(checkbox);
    li.textContent = `${item.name} x${item.quantity} - R$${(item.price * item.quantity).toFixed(2)}`;
    cartList.appendChild(li);

    totalAmount += item.price * item.quantity;
  });

  totalAmountElement.textContent = totalAmount.toFixed(2);
}

function removeSelected() {
    cart = cart.filter(item => !item.selected);
    displayCart();
  }

function checkout() {
  alert('Pedido finalizado! Total: R$' + totalAmountElement.textContent);
  // Aqui você normalmente enviaria o pedido para o backend para processamento
  // e lidaria com transações financeiras, autenticação do usuário, etc.
}

