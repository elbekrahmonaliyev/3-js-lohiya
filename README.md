<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./main.css">
    <title>Savat</title>
    <link  rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
</head>
<body>  
 <div class="lake">
     <i  class="fa-solid fa-cart-plus" style="font-size:40px;"></i>
    <button class="box" id="cartBtn" class="fa-solid fa-cart-plus">Savat</button>
 </div>

<div id="cart" class="cart">
  <h3>Savat</h3>
  <ul>
    <li>Mahsulot-olma 1</li>
    <li>Mahsulot-banana 2</li>
    <li>narxi 15 so'm</li>
  </ul>
</div>

    <script src="./app.js"></script>
</body>
</html>

css
.cart {
  display: none;
  position: absolute;
  top: 80px;
  right: 20px;
  width: 250px;
  padding: 15px;
  border: 1px solid #333;
  background: red;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
  
}

.cart.show {
  display: block; 
}
.box{
    background-color: #FD5924;
    width: 110px;
    height: 40px;
    border-radius: 15px;
}
.lake{
display: flex;
justify-content: center;
align-content: center;
}

js
const cart = document.getElementById('cart');
const cartBtn = document.getElementById('cartBtn');
const cartIcon = document.querySelector('.fa-cart-plus');


function  toggleCart() {
  cart.classList.toggle('show');
}
cartBtn.addEventListener('click', toggleCart);
cartIcon.addEventListener('click', toggleCart);
