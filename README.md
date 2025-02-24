Welcome to the Food Junction landing page project! This project is a simple, visually appealing landing page designed for a fictional food ordering service. It uses HTML, CSS, and JavaScript to create an interactive and responsive webpage.

Features
Responsive Design: The page adapts to various screen sizes using CSS Flexbox and other responsive techniques.
Interactive Elements:
Hover effects on food images and buttons.
Social Media Icons that change color when hovered over.
A search bar and hamburger menu for a modern and user-friendly experience.
Background Image: A visually stunning background image of food that covers the entire viewport with a subtle blur effect to make the content stand out.

//HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Landing Page</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css" integrity="sha512-Evv84Mr4kqVGRNSgIGL/F/aIDqQb7xQ2vcrdIwxfjThSH8CSR7PBEakCr51Ck+w+/U6swU2Im1vVX0SVk9ABhg==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <link rel="stylesheet" href="style.css">
</head>


<body>
   <div class="top">
    <div class="logo">Food Junction</div>
   <div class="nav">
  <a href="">Home</a>
  <a href="">Menu</a>
  <a href="">About</a>
  <a href="">Location</a>
  <a href="">Contact</a>
   </div>
   <div class="search">
    <i class="fa-solid fa-magnifying-glass"></i>
    <i class="fa-solid fa-bars"></i>
   </div>
   </div>
   <div class="heading">
    <div class="left">
        <p>Are you Hungry</p>
        <h1>Don't wait!!</h1>
        <p>Let start to order food now</p>
        <button>check out Menu</button>
    </div>
   

   <div class="right" id="food"></div>
   <div class="socialmedia ">
    <i class="fa-brands fa-facebook"></i>
    <i class="fa-brands fa-twitter"></i>
    <i class="fa-brands fa-instagram"></i>
    <i class="fa-brands fa-whatsapp"></i>
   </div>

</div>

<div class="bottom">
    <div class="menu">
        <div id="food1"></div>
        <div id="food2"></div>
    </div>
</div>
<script src="food.js"></script>
</body>
</html>

//Style
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    width: 100%;
    height: 100vh;
    background-image: url(img/backgroundimg.png);
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    backdrop-filter: blur(10px);
}

.top {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    height: 80px;
    align-items: center;
    padding: 0px 40px;
}

.logo {
    font-size: 30px;
    color: orange;
    box-shadow: 0 0 30px rgba(255, 140, 0, 0.5);
}

.nav {
    position: relative;
    left: -180px;
}

a {
    padding: 5px 15px;
    color: darkcyan;
    font-size: 20px;
    text-decoration: none;
    transition: color 0.3s, box-shadow 0.3s;
}

a:hover {
    color: white;
    text-decoration: underline;
    text-underline-position: under;
    box-shadow: 0 0 30px orange;
}

.search {
    font-size: 25px;
}

.search i {
    padding: 5px 20px;
    color: white;
}

.heading {
    display: flex;
    justify-content: space-evenly;
    padding-top: 65px;
    align-items: center;
}

.right {
    width: 440px;
    height: 440px;
    background-image: url('img/burger.png');
    background-size: cover;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    overflow: hidden;
}

.right::before {
    content: "";
    position: absolute;
    width: 430px;
    height: 430px;
    border: 2px solid white;
    border-radius: 50%;
    top: 5px;
    left: 5px;
    transition: all 0.3s;
    padding: 10px;
}

.right:hover::before {
    width: 450px;
    height: 450px;
    top: -5px;
    left: -5px;
}

 .right:hover {
    color: beige;
} 

.left p:nth-child(1) {
    color: white;
    font-size: 30px;
    letter-spacing: 1px;
    font-style: italic;
}

.left h1 {
    font-size: 90px;
    color: white;
}

.left p:nth-child(3) {
    color: orange;
    font-size: 30px;
    font-style: italic;
}

.left button {
    width: 150px;
    height: 40px;
    font-size: 15px;
    border-radius: 20px;
    border: 2px solid white;
    background-color: transparent;
    color: white;
    margin: 20px 0px;
    transition: background-color 0.3s, color 0.3s;
}

.left button:hover {
    background-color: white;
    color: black;
}

.socialmedia {
    position: absolute;
    right: 0;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    flex-direction: column;
    width: 40px;
    height: 200px;
    background-color: white;
    font-size: 25px;
}

.socialmedia i:hover {
    color: orange;
}

#food1,
#food2 {
    position: relative;
    background-size: cover;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin: 0px 24px;
    left: 91px;
    transition: transform 0.3s;
}

#food1 {
    background-image: url(img/food1.png);
}

#food2 {
    background-image: url(img/food2.png);
}

#food1:hover,
#food2:hover {
    transform: scale(1.1);
}

.menu {
    display: flex;
    margin: 0px 100px;
    /* justify-content: center; */
}
