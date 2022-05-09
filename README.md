 -Vi s-a întâmplat vreodată să vă doriți să cumpărați mobilier și să nu vă dați seama din imagini și descriere dacă este potrivit pentru                      dumneavoastră? Ei bine, 3D Furniture View este soluția! 

Razwan  -Probabil vă întrebați "Ce face acest site mai exact?"
          Ei bine, 3D Furniture View este un magazin online ce permite utilizatorului să vadă obiectul 3D pe site, sau chiar cum ar arăta acesta în                  realitate înainte de a-l cumpăra cu ajutorul tehnologiei AR. 

Haz     -Ce înseamnă "AR"?
         AR vine de la "Augmented Reality", ceea ce în română înseamnă "Realitate Augmentată".
         Cu ajutorul AR, un model 3D poate fi așezat virtual în locuri din realitate cu ajutorul camerei telefonului mobil, corespunzând exact cu                   dimensiunile obiectului real, oferindu-i utilizatorului șansa de a lua decizia cea mai corectă înainte de cumpărare. 

Razwan  -Acest tip de site este foarte util, probabil ajungând chiar un trend al viitorului, însă, în prezent, nu toate telefoanele acceptă AR, acest lucru încetinind popularitatea în momentul de față. 
         
Haz     -Acum sa va prezentam interfata site-ului
navbar




<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Dent</title>
    <link rel="stylesheet" href="style.css">
    <script
    src="https://code.jquery.com/jquery-3.4.1.slim.min.js"
    integrity="sha256-pasqAKBDmFT4eHoN2ndd6lN370kFiGUFyTiUHWhU7k8="
    crossorigin="anonymous"></script>
    <script>
    $(function() {
    $(".toggle").on("click", function() {
        if ($(".item").hasClass("active")) {
            $(".item").removeClass("active");
        } else {
            $(".item").addClass("active");
        }
    });
});
    </script>
</head>
<body>
    <nav>
        <ul class="menu">
            <li class="logo"><h1><img src="Logg2.png" alt="sit" class="logo2"></h1></li>
            <li class="item"><a href=# class="a1">Home</a></li>
            <li class="item"><a href=# class="a1">About</a></li>
            <li class="item"><a href=# class="a1">Cos</a></li>
            <li class="item button"><a href="#" class="a1">Log In</a></li>
            <li class="toggle"><button class="hamburger">
                <span></span>
                <span></span>
                <span></span>
                </button></li>
        </ul>
    </nav>
     <script src="script.js"></script>
</body>
</html>


/*presets&&fonts*/
@import url('https://fonts.googleapis.com/css2?family=Arimo:ital@1&family=EB+Garamond:ital@1&family=Lobster&family=Oxygen:wght@300&family=Quicksand:wght@300;400;500&family=Titillium+Web&display=swap');
/*
font-family: 'Arimo', sans-serif; ~Descriere Produs~
font-family: 'EB Garamond', serif; ~About Us~
font-family: 'Lobster', cursive; ~stilizare~
font-family: 'Oxygen', sans-serif; ~Produs~
font-family: 'Quicksand', sans-serif; ~Stele testao~
font-family: 'Titillium Web', sans-serif; ~Navbar~
*/
:root{
    --text-primary: #b6b6b6;
    --text-secondary: #ececec;
    --bg-primary: #101214;
    --primary: #2c2c36;
    --light: #EEEEEE;
    --dark: #020114;
}
/*presets&&fonts*/


/*basic*/
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}



nav{
    font-family: 'Titillium Web', sans-serif;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 99;
    background-color: var(--dark);
    padding: 5px 20px;
    border-bottom: px solid var(--primary);
}
.logo2{
    width: auto;
    height: 60px;
}

/*basic*/
/*hamburger*/
.hamburger{
    display: block;
    position: relative;
    z-index: 1;
user-select: none;
appearance: none;
    border: none;
    outline: none;
    background: none;
    cursor: pointer;
}
.hamburger span {
display: block;
width: 33px;
height: 4px;
margin-bottom: 5px;
position: relative;
background-color:white;
border-radius: 6px;
z-index: 1;
transform-origin: 0 0;
transition: 0.5s;
}
.hamburger:hover span:nth-child(2){
    transform: translateX(10px);
    background-color: blue;
    
}

.hamburger.is-active span:nth-child(1){
    transform: translate(0px, -2px) rotate(45deg);
}
.hamburger.is-active span:nth-child(3){
    transform: translate(-3px, 3px) rotate(-45deg);
}
.hamburger.is-active span:nth-child(2){
    opacity: 0;
    transform: translate(15px);
}
.hamburger.is-active:hover span{
    background-color: blue;
}
.menu a.is-active, .menu a:hover{
    background-color: var(--primary);
}
/*hamburger*/

ul {
  list-style-type: none;
}
a {
  color: white;
  text-decoration: none;
}
a:hover {
  text-decoration: none;
}
.menu li:not(.toggle,.logo) {
  font-size: 15px;
  padding: 10px 10px;
  white-space: nowrap;
}

/*Meniu butoane*/

.menu a{
    color: #FFF;
    margin: 0 13px;
    font-weight: 600;
    text-decoration: none;
    transition: .75s;
    padding: 8px 16px;
    border-radius: 40px;
}

/*Meniu butoane*/

/* Telefon*/
.menu {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
}
.toggle {
  order: 1;
}
.item.button {
  order: 2;
}
.item {
  width: 100%;
  text-align: center;
  order: 3;
  display: none;

}
.item.active {
  display: block;
   
}

.toggle {
  cursor:pointer;
}
/* Telefon*/

/*Tableta */
@media all and (min-width: 489px) {
  .menu {
      justify-content: center;
  }

  .logo {
      flex: 1;
  }

  .item.button {
      width: auto;
      order: 1;
      display: block;
  }
  .toggle {
      order: 2;
  }
  .button a {
      padding: 7.5px 15px;
      background: ;
      border: 1.7px #4f4f69 solid;
      border-radius:50em;
  }
  .button a:hover {
      text-decoration: none;
      transition:all .25s;
  }
  .button a:hover {
      background: #2c2c36;
      border-color: #343445;
  }
}
/*Tableta */

/* Desktop */
@media all and (min-width: 824px) {
  .item {
      display: block;
      width: auto;
  }
  .toggle {
      display: none;
  }
  .logo {
      order: 0;
  }
  .item {
      order: 1;
  }
  .button {
      order: 2;
  }
  .menu li:not(.toggle,.logo) {
      padding: 15px 10px;
  }
  .menu li.button {
      padding-right: 0;
  }
    .logo2{
padding: 0px;
}
}

/*scrollbar*/

::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
  background: #888;
 border-radius: 5px;
}

::-webkit-scrollbar-thumb:hover {
  background: #555;
}

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <link rel="stylesheet" href="obiecte.css">
    <title></title>
</head>
<body>
<div class="container ctn1">
  <div class="card">
      
    <div class="imgBx">
      <img src="images/1.png" class="pro-img">
      </div>
    <div class="contentBx">
      <h2>masa jmek</h2>
      <div class="color">
        <h3>Color :</h3>
        <span><button class="btnspa btn1" onclick="changeImage(this)">
             <img src="images/1.png" class="hood">
            </button></span>
        <span><button class="btnspa btn2" onclick="changeImage(this)"><img src="images/2.png" class="hood"></button></span>
        <span><button class="btnspa btn3" onclick="changeImage(this)"><img src="images/1.jpg" class="hood"></button></span>
      </div>
      <a href="#">More details</a>
    </div>
  </div>
</div>
    <div class="container ctn2">
  <div class="card">
    <div class="imgBx">
      <img src="canapea.png" class="pro-img2">
    </div>
    <div class="contentBx">
      <h2>Canapea smek</h2>
      <div class="color">
        <h3>Color :</h3>
        <span><button class="btnspa btn1" onclick="changeImage2(this)">
             <img src="images/1.png" class="hood">
            </button></span>
        <span><button class="btnspa btn2" onclick="changeImage2(this)"><img src="images/2.png" class="hood"></button></span>
        <span><button class="btnspa btn3" onclick="changeImage2(this)"><img src="images/1.jpg" class="hood"></button></span>
      </div>
      <a href="#">More details</a>
    </div>
  </div>
</div>
    <div class="container ctn3">
  <div class="card">
    <div class="imgBx">
      <img src="masa.png" class="pro-img3">
    </div>
    <div class="contentBx">
      <h2>masa urata</h2>
      <div class="color">
        <h3>Color :</h3>
        <span><button class="btnspa btn1" onclick="changeImage3(this)">
             <img src="images/1.png" class="hood">
            </button></span>
        <span><button class="btnspa btn2" onclick="changeImage3(this)"><img src="images/2.png" class="hood"></button></span>
        <span><button class="btnspa btn3" onclick="changeImage3(this)"><img src="images/1.jpg" class="hood"></button></span>
      </div>
      <a href="#">More details</a>
    </div>
  </div>
</div>
    <script>
    function changeImage(event){
    document.querySelector(".pro-img").src=(event.children[0].src)
}
        function changeImage2(event){
    document.querySelector(".pro-img2").src=(event.children[0].src)
}
        function changeImage3(event){
    document.querySelector(".pro-img3").src=(event.children[0].src)
}
    </script>
</body>
</html>

@import url('https://fonts.googleapis.com/css2?family=Arimo:ital@1&family=EB+Garamond:ital@1&family=Lobster&family=Oxygen:wght@300&family=Quicksand:wght@300;400;500&family=Titillium+Web&display=swap');



body{
  font-family: 'Oxygen', sans-serif; 
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: #131313;
}

.container .card{
  position: relative;
  width: 320px;
  height: 450px;
  background: #333333;
  border-radius: 30px;
  overflow: hidden;
}
/*basic*/


/*media*/
@media only screen and (max-width: 1145px) and (min-width: 900px)  {
  
.container .card{
    margin: 20px;
     align-items: center;
  position: relative;
  width: 270px;
  height: 400px;
  background: #333333;
  border-radius: 30px;
  overflow: hidden;
    }}
@media all and (max-width: 900px) {
 .container{
        position:absolute;
    align-items: center;
 }
    .ctn2{
        margin-top: 1090px;
    }
    .ctn3{
        margin-top: 2180px;
    }
}
/*media*/


/*slide*/
.container .card:before{
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #202120 ;
  clip-path: inset(0% 0 0% 0);
  transition: 0.5s ease-in-out;
}

.container .card:hover:before{
 clip-path: inset(75% 0 0% 0);
}
/*slide*/

/*txt bg*/
.container .card:after{
  content: '';
  position: absolute;
  top: 30%;
  left: -20%;
  font-size: 12em;
  font-weight: 800;
  font-style: italic;
  color: rgba(255,255,25,0.05)
}
/*txt bg*/


/*miscare obiecte*/
.container .card .imgBx{
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  z-index: 10000;
  width: 100%;
  height: 220px;
  transition: 0.5s;
}
.container .card:hover .imgBx{
  top: 0%;
  transform: translateY(0%);
    
}
.container .card .imgBx img{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%) ;
  width: 270px;
}
.container .card .contentBx{
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 100px;
  text-align: center;
  transition: 1s;
  z-index: 10;
}
/*miscare obiecte*/


/*miscare txt*/
.container .card:hover .contentBx{
  height: 210px;
}

.container .card .contentBx h2{
  position: relative;
  font-weight: 600;
  letter-spacing: 1px;
  color: #fff;
  margin: 0;
}
/*miscare obiecte*/


/*hover show*/
.container .card .contentBx .size, .container .card .contentBx .color {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 8px 20px;
  transition: 0.5s;opacity: 0;
  visibility: hidden;
  padding-top: 0;
  padding-bottom: 0;
}
.container .card:hover .contentBx .size{
  opacity: 1;
  visibility: visible;
  transition-delay: 0.5s;
}
.container .card:hover .contentBx .color{
  opacity: 1;
  visibility: visible;
  transition-delay: 0.6s;
}
.container .card .contentBx .size h3, .container .card .contentBx .color h3{
  color: #fff;
  font-weight: 300;
  font-size: 14px;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-right: 10px;
}
.container .card .contentBx .size span {
  width: 26px;
  height: 26px;
  text-align: center;
  line-height: 26px;
  font-size: 14px;
  display: inline-block;
  color: #111;
  background: #fff;
  margin: 0 5px;
  transition: 0.5s;
  color: #111;
  border-radius: 4px;
  cursor: pointer;
}
.btnspa{

    height: 20px;
    width: 23px;
    border:none;
    border-radius: 50%;
    background: transparent;
    outline:none;
    cursor:pointer;
    
}
.container .card .contentBx .size span:hover{
  background: #9bdc28;
}
.container .card .contentBx .color span{
  width: 20px;
  height: 20px;
  background: #ff0;
  border-radius: 50%;
  margin: 0 5px;
  cursor: pointer;
}
.container .card .contentBx .color span:nth-child(2){
  background: #9bdc28;
}
.container .card .contentBx .color span:nth-child(3){
  background: #03a9f4;
}
.container .card .contentBx .color span:nth-child(4){
  background: #e91e63;
}
.container .card .contentBx a{
  display: inline-block;
  padding: 10px 20px;
  background: #fff;
  border-radius: 4px;
  margin-top: 10px;
  text-decoration: none;
  font-weight: 600;
  color: #111;
  opacity: 0;
  transform: translateY(50px);
  transition: 0.5s;
  margin-top: 0;
}
.container .card:hover .contentBx a{
  opacity: 1;
  transform: translateY(50px);
  transition-delay: 0.75s; 
}
.hood{
    width: 0px;
}
/*hover show*/


/*media2*/
@media all and (min-width: 1145px) {
.container .card{
  position:relative;
    margin: 45px;
}
/*media2*/

<?php
session_start();
 require 'conectare.php';
if (isset($_POST['email']) && !empty($_POST['email']) && ($_POST['password']) && !empty($_POST['password'])){
    $email = strtolower($_POST['email']);
    $password = $_POST['password'];
    
    $sql = "SELECT * FROM users WHERE email='$email'";
    $result = mysqli_query($conectare, $sql);
    $row = $result->fetch_assoc();
    $hash = $row['password'];
    $check = password_verify($password, $hash);
    if($check == 0){
        header("Location: ../login.php?info=gresit");
        die();
    } else{
        
        $sql = "SELECT * FROM users WHERE email='$email' AND password= '$hash' ";
        $result = mysqli_query($conectare, $sql);
        
        if(!$row = $result->fetch_assoc()){
            echo 'Parola sau usernameul nu se potriveste.';
}else{
            $_SESSION['idl'] =$row['idl'];
            $_SESSION['username'] =$row['username'];
            $_SESSION['email'] =$row['email'];
        }
        header("Location: ../INDEX.php");
    }
    
}

<?php

require 'conectare.php';

if (!empty($_POST['username']) && !empty($_POST['email']) &&!empty($_POST['password']) && isset($_POST['username']) && isset($_POST['email']) && isset($_POST['password']) ){
    
    
$username = $_POST['username'];
$email = strtolower($_POST['email']);
$password = $_POST['password'];

    
$password_hashed = password_hash($password, PASSWORD_DEFAULT);
$sql = "SELECT username FROM users WHERE username='$username'";
$result = mysqli_query($conectare, $sql);
$check = mysqli_num_rows($result);
    
    if($check > 0) {
        header("Location: ../signup.php?info=exista");
         die();   
    } else{
        $sql = "INSERT INTO users (username, email, password) VALUES ('$username', '$email', '$password_hashed')" ;
        
$result = mysqli_query($conectare, $sql);

header("Location: ../signup.php?info=Conectat cu succes😎");
    }


    
} else{
header("Location: ../signup.php?info=eroare");
}


<?php
 require 'credentials.php';

function pdo_connect_mysql() {
    $host = 'localhost';
    $db = 'estore';
    $user = USERNAME;
    $pass = PASSWORD;
    $charset ='utf8mb4';
    
    $dsn = "mysql:host = $host; dbname=$db; charset=$charset";
    $options = [
        PDO::ATTR_ERRMODE            => PDO::ERRMODE_EXCEPTION,
        PDO::ATTR_DEFAULT_FETCH_MODE => PDO::FETCH_ASSOC,
        PDO::ATTR_EMULATE_PREPARES   => false,
    ];
    
    try{
        return new PDO($dsn, $user, $pass, $options);
    }
    catch(PDOException $e) {
        throw new PDOException($e->getMessage(), (int)$e->getCode());
    }
     
    
}




//obiectetest.php 
//Acest script stilizeaza pagina "home.php" care este afisat pe index.
 
/*presets&&fonts*/
@import url('https://fonts.googleapis.com/css2?family=Arimo:ital@1&family=EB+Garamond:ital@1&family=Lobster&family=Oxygen:wght@300&family=Quicksand:wght@300;400;500&family=Titillium+Web&display=swap');
/*
font-family: 'Arimo', sans-serif; ~Descriere Produs~
font-family: 'EB Garamond', serif; ~About Us~
font-family: 'Lobster', cursive; ~stilizare~
font-family: 'Oxygen', sans-serif; ~Produs~
font-family: 'Quicksand', sans-serif; ~Stele testao~
font-family: 'Titillium Web', sans-serif; ~Navbar~
*/
/*===================================================================================*/
body{
  font-family: 'Quicksand';
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: #131313;
}

.container .card{
    
  position: relative;
  width: 320px;
  height: 450px;
  background: #333333;
  border-radius: 30px;
  overflow: hidden;
    
}

.container ctn1{
    flex-basis: 25%;
    min-width: 250px;
    margin-bottom: 30px;
}

.row {
  margin: auto;
  width: 90%;
 /*border: 3px solid #73AD21;*/
  padding: 10px;
    padding-top: 50px;
}
/*basic*/

div .card{
     margin: 10px;
}

/*--------------------------------------MEDIA 1--------------------------------------*/
@media only screen and (max-width: 1528px) and (min-width: 1150px)  {
  .row {
  margin: auto;
  width: 60%;
 /* border: 3px solid #73AD21;*/
  padding: 10px;
      padding-top: 100px;
}

  .container ctn1{
   
    margin: auto;
}
}

/*--------------------------------------MEDIA 2--------------------------------------*/


@media only screen and (max-width: 1149px) and (min-width: 947px){
  .row {
  margin: auto;
  width: 80%;
  /*border: 3px solid #73AD21;*/
  padding: 10px;
      padding-top: 25px;
}

    .container ctn1{

    margin: auto;
}
}





/*--------------------------------------MEDIA 3--------------------------------------*/


@media only screen and (max-width: 947px) and (min-width: 775px){
  .row {
  margin: auto;
  width: 90%;
 /* border: 3px solid #73AD21;*/
  padding: 10px;
            
}

    .container ctn1{

    margin: auto;
}
}


/*--------------------------------------MEDIA 4--------------------------------------*/


@media only screen and (max-width: 775px){
    .row {
  margin: auto;
  width: 40%;
/*  border: 3px solid #73AD21;*/
  padding: 10px;
              padding-top: 25px;
}
}


/*slide*/
.container .card:before{
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #202120 ;
  clip-path: inset(0% 0 0% 0);
  transition: 0.5s ease-in-out;
}





.container .card:hover:before{
 clip-path: inset(75% 0 0% 0);
}
/*slide*/

/*txt bg*/
.container .card:after{
  content: '';
  position: absolute;
  top: 30%;
  left: -20%;
  font-size: 12em;
  font-weight: 800;
  font-style: italic;
  color: rgba(255,255,25,0.05)
}
/*txt bg*/


/*miscare obiecte*/
.container .card .imgBx{
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  z-index: 10;
  width: 100%;
  height: 220px;
  transition: 0.5s;
}
.container .card:hover .imgBx{
  top: 0%;
  transform: translateY(0%);
    
}
.container .card .imgBx img{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%) ;
  width: 270px;
}
.container .card .contentBx{
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 100px;
  text-align: center;
  transition: 1s;
  z-index: 10;
}
/*miscare obiecte*/


/*miscare txt*/
.container .card:hover .contentBx{
  height: 210px;
}

.container .card .contentBx h2{
  position: relative;
  font-weight: 600;
  letter-spacing: 1px;
  color: #fff;
  margin: 0;
}
/*miscare obiecte*/


/*hover show*/
.container .card .contentBx .size, .container .card .contentBx .color {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 8px 20px;
  transition: 0.5s;opacity: 0;
  visibility: hidden;
  padding-top: 0;
  padding-bottom: 0;
    margin-top: 20px;
}
.container .card:hover .contentBx .size{
  opacity: 1;
  visibility: visible;
  transition-delay: 0.5s;
}
.container .card:hover .contentBx .color{
  opacity: 1;
  visibility: visible;
  transition-delay: 0.6s;
}
.container .card .contentBx .size h3, .container .card .contentBx .color h3{
  color: #fff;
  font-weight: 300;
  font-size: 14px;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-right: 10px;
}
.container .card .contentBx .size span {
  width: 26px;
  height: 26px;
  text-align: center;
  line-height: 26px;
  font-size: 14px;
  display: inline-block;
  color: #111;
  background: #fff;
  margin: 0 5px;
  transition: 0.5s;
  color: #111;
  border-radius: 4px;
  cursor: pointer;
}
.btnspa{

    height: 20px;
    width: 23px;
    border:none;
    border-radius: 50%;
    background: transparent;
    outline:none;
    cursor:pointer;
    
}
.container .card .contentBx .size span:hover{
  background: #9bdc28;
}
.container .card .contentBx .color span{
  width: 20px;
  height: 20px;
  background: #ff0;
  border-radius: 50%;
  margin: 0 5px;
  cursor: pointer;
}
.container .card .contentBx .color span:nth-child(2){
  background: #9bdc28;
}
.container .card .contentBx .color span:nth-child(3){
  background: #03a9f4;
}
.container .card .contentBx .color span:nth-child(4){
  background: #e91e63;
}
.container .card .contentBx a{
  display: inline-block;
  padding: 10px 20px;
  background: #fff;
  border-radius: 4px;
  margin-top: 10px;
  text-decoration: none;
  font-weight: 600;
  color: #111;
  opacity: 0;
  transform: translateY(50px);
  transition: 0.5s;
  margin-top: 0;
}
.container .card:hover .contentBx a{
  opacity: 1;
  transform: translateY(50px);
  transition-delay: 0.75s; 
}
.hood{
    width: 0px;
}
/*hover show*/


.col-3{
    flex-basis: 30%;
    min-width: 250px;
    margin-bottom: 30px;
}

.row{
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    justify-content: center;
}

#main{
    padding-bottom: 300px;
    z-index: 5
}


.buttons{
    width: 100%;
}
 
.schema1{

}
.next{
    margin-left: 90%;
    background-color: darkgreen;
    padding: 10px;
}
.prev{
    margin-left: 10%;
    background-color: red;
    padding: 10px;
}
.orez{
text-align: center;
font-family: 'Quicksand';
    font-size: 4vw;
    margin-top: 25vw;
    padding-top: 100px;
    color: white;
}



//INDEX.PHP

<?php
//LOGARE LA SITE
include 'ESTORE/configRR/dbconnection.php';
include 'ESTORE/modeleRR/functions.php';

$pdo = pdo_connect_mysql();

$page = isset($_GET['page']) && file_exists($_GET['page']).'.php' ? $_GET['page'] : 'home';
?>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
  
   <body onLoad="smoothscroll()"></body>

    <?php

     include $page . '.php';
    ?>
    
    <script>
function smoothscroll() {
  document.documentElement.style.scrollBehavior = "smooth";
}
</script>
</body>
</html>



//Generare pagini pentru fiecare obiect

<?php
if (isset($_GET['id'])) {

    $stmt = $pdo->prepare('SELECT * FROM products WHERE id = ?');
    $stmt->execute([$_GET['id']]);

    $product = $stmt->fetch(PDO::FETCH_ASSOC);

    if (!$product) {

        exit('Product does not exist!');
    }
} else {

    exit('Product does not exist!');
}

$pdo = NULL;
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <link rel="stylesheet" href="CSS/obiect.css">
    <script type="module" src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js"></script>
    
</head>
<body class="corp">
 <?php
    include 'navbar.php';
    ?>

    
 <div id="container">
<div class="small-container single-product">
    <div class="row">
       <div class="col-2">
      
    <div class="imgBx">
      <model-viewer src="GLB/<?=$product['glb1']?>" seamless-poster autoplay="true" enable-pan camera-controls auto-rotate id="ProductImg" class="<?=$product['class']?>" 
          
      ios-src="<?=$product['usdz']?>" shadow-intensity="3.0" shadow-softness="1.2" auto-rotate-delay="0"     ></model-viewer>
      </div>
    <div class="contentBx">
      <div class="color">
        <button class="btnspa <?=$product['color1']?>" style=" background: url(./images/<?=$product['img1']?>);  background-size: 85px; background-repeat: no-repeat;" onclick="<?=$product['change']?>(this)"><model-viewer src="GLB/<?=$product['glb1']?>" seamless-poster autoplay="true"  shadow-intensity="3.0" shadow-softness="1.2" auto-rotate-delay="0"    enable-pan camera-controls auto-rotate id="ProductImg" class="imggg" ios-src="<?=$product['usdz']?>" ></model-viewer>
            </button>
        <span><button class="btnspa <?=$product['color2']?>"  style=" background: url(./images/<?=$product['img2']?>);  background-size: 85px; background-repeat: no-repeat;" onclick="<?=$product['change']?>(this)"> <model-viewer src="GLB/<?=$product['glb2']?>" seamless-poster autoplay="true"  shadow-intensity="3.0" shadow-softness="1.2" auto-rotate-delay="0"    enable-pan camera-controls auto-rotate id="ProductImg" class="wait" ios-src="<?=$product['usdz']?>" ></model-viewer></button></span>
        
        <span><button class="btnspa <?=$product['color3']?>"  style=" background: url(./images/<?=$product['img3']?>);  background-size: 85px; background-repeat: no-repeat;" onclick="<?=$product['change']?>(this)"><model-viewer src="GLB/<?=$product['glb3']?>" seamless-poster autoplay="true"  shadow-intensity="3.0" shadow-softness="1.2" auto-rotate-delay="0"  enable-pan camera-controls auto-rotate id="ProductImg" class="wait" ios-src="<?=$product['usdz']?>" ></model-viewer></button></span>
      </div>
    </div>
  </div>
        <div class="col-2">
            <h1><?=$product['name']?></h1>
            <h2>$<?=$product['price']?></h2>
            <select>
                <option>
                  Select SIZE  
                </option>
                <option>80-100cm</option>
                <option>100-120cm</option>
                <option>120-140cm</option>
            </select>
            <form action="INDEX.php?page=cart" method="post">
            <input type="number" name="quantity" value="1"  min="1" max="<?=$product['quantity']?>" placeholder="Quantity" required class="norocos">
            <input type="hidden" name="product_id" value="<?=$product['id']?>">
            <input type="submit" class="btn4" value="Add to Cart">
            </form>
            <h3>Product Details</h3>
            <br>
            <p><?=$product['desc']?> </p>
        </div>
    </div></div> 
   </div>
    <script>
    function changeImage1(event){
    document.querySelector(".pro-img1").src=(event.children[0].src)
}
        function changeImage2(event){
    document.querySelector(".pro-img2").src=(event.children[0].src)
}
        function changeImage3(event){
    document.querySelector(".pro-img3").src=(event.children[0].src)
}
        function changeImage4(event){
    document.querySelector(".pro-img4").src=(event.children[0].src)
}
        function changeImage5(event){
    document.querySelector(".pro-img5").src=(event.children[0].src)
}
    </script>
    
<?php
    include 'footer.php';
    ?>
    
</body>
</html>


//BACKGROUND HOME.PHP
<!DOCTYPE html>
<html>
    <head>
        <meta include charset="UTF-8">
        <title> </title>
        <link rel="stylesheet" type="text/css" href="CSS/bg.css">
    </head>
    <body>
        <div class="site-content">
 <header class="content-header">
         <video playsinline autoplay muted loop poster="Screenshot%202022-04-10%20134446.png" id="bgvid" width="720" height="480">
  <source src="MEDIA/VIDEO/ico2.mp4" type="video/mp4">
       </video>
       
	<div class="centerlogo">
		<img src="MEDIA/IMG/Logg2.png" class="logonebun">
		<br>
		<h1 class="slogan">Îți facem mobilarea ușoară!</h1>
		<a href="#obj" class="fugi"><br><br><br><br>Mergi la obiecte</a>
	</div>

	</header>
	<div class="incercare"></div>
</div>

    </body>
</html>
    

//CSS Backgropung HOME.PHP


@import url('https://fonts.googleapis.com/css2?family=Arimo:ital@1&family=EB+Garamond:ital@1&family=Lobster&family=Oxygen:wght@300&family=Quicksand:wght@300;400;500&family=Titillium+Web&display=swap');

html, body {
       overflow-x: hidden;
}

.site-content{
    min-width: 100%;
    height: auto;
    margin: 0;
}
.content-header{
margin: 0;
height: 800px;}
video{
    opacity: 1;
    overflow-y: hidden;
    position: relative;
    top: 0;
    width: 100%;
    height: auto;
    filter:blur(8px);
}
.logonebun{
     max-width: 100%;
    height: auto;

}
.centerlogo{
	position: absolute;
	margin-left: 7.5%;
	top: 15%;
	max-width: 100%;
	height: auto;
	text-align: center;
	filter: drop-shadow(0px 5px 5px #222);
    padding: 0 15% 0; 
}
.slogan{
	font-family:"Quicksand";
	font-size: 3vw;
	color: white;
}
  


@media all and (max-width: 1620px) and (min-width: 1470px)  {
    video{
        filter: blur(5px);
    }
    .centerlogo{
        margin-left: 0;
    }}
  @media all and (max-width: 1470px) and (min-width: 900px)  {
    video{
        padding-top: 1%;
        filter: blur(5px);
    }
    .centerlogo{
        top: 4%;
        margin-left: 0;
        
    }}
    @media all and (max-width: 900px) and (min-width: 300px)  {
    video{
        padding-top: 5%;
        filter: blur(5px);
    }
    .centerlogo{
        top: 4%;
        margin-left: 0;
        
    }}
    
    



.fugi{
    font-family:"Quicksand";
	font-size: 2vw;
	color: white;
    text-decoration: underline;
}

.content-media--video iframe {
    position: absolute;
  
}


