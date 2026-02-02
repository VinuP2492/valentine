<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8" />  
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>  
<title>Be My Valentine ❤️</title>  
  
<style>  
    body{  
        margin:0;  
        height:100vh;  
        display:flex;  
        justify-content:center;  
        align-items:center;  
        background:linear-gradient(135deg,#ff9a9e,#fad0c4);  
        font-family:Arial, Helvetica, sans-serif;  
        overflow:hidden;  
        text-align:center;  
    }  
  
    .card{  
        background:white;  
        padding:40px;  
        border-radius:20px;  
        box-shadow:0 10px 30px rgba(0,0,0,0.2);  
        position:relative;  
    }  
  
    h1{  
        color:#e91e63;  
        margin-bottom:30px;  
    }  
  
    button{  
        padding:12px 25px;  
        font-size:18px;  
        border:none;  
        border-radius:30px;  
        cursor:pointer;  
        margin:10px;  
        transition:0.2s;  
    }  
  
    #yesBtn{  
        background:#4CAF50;  
        color:white;  
    }  
  
    #noBtn{  
        background:#f44336;  
        color:white;  
        position:absolute;  
    }  
  
    #gifContainer{  
        margin-top:20px;  
        display:none;  
    }  
  
    img{  
        width:250px;  
        border-radius:15px;  
    }  
</style>  
</head>  
  
<body>  
  
<div class="card" id="card">  
    <h1>Will you be my Valentine? ❤️</h1>  
    <button id="yesBtn">Yes 😍</button>  
    <button id="noBtn">No 😜</button>  
  
    <div id="gifContainer">  
        <h2>Yayyyyy!! 🥳❤️</h2>  
        <img src="https://media.giphy.com/media/3oz8xAFtqoOUUrsh7W/giphy.gif" />  
    </div>  
</div>  
  
<script>  
    const noBtn = document.getElementById("noBtn");  
    const yesBtn = document.getElementById("yesBtn");  
    const gif = document.getElementById("gifContainer");  
  
    function moveButton(){  
        const card = document.getElementById("card");  
        const maxX = card.clientWidth - noBtn.clientWidth - 20;  
        const maxY = card.clientHeight - noBtn.clientHeight - 20;  
  
        const randomX = Math.floor(Math.random() * maxX);  
        const randomY = Math.floor(Math.random() * maxY);  
  
        noBtn.style.left = randomX + "px";  
        noBtn.style.top = randomY + "px";  
    }  
  
    noBtn.addEventListener("mouseover", moveButton);  
    noBtn.addEventListener("click", moveButton);  
  
    yesBtn.addEventListener("click", function(){  
        gif.style.display = "block";  
        yesBtn.style.display = "none";  
        noBtn.style.display = "none";  
    });  
</script>  
  
</body>  
</html>  
