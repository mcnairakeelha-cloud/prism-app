<!DOCTYPE html>
<html>
<head>
<title>Prism</title>

<style>

body{
font-family:Arial;
background:linear-gradient(120deg,#ff0080,#7928ca,#00c6ff);
height:100vh;
display:flex;
justify-content:center;
align-items:center;
color:white;
}

.app{
width:350px;
text-align:center;
}

.card{
background:white;
color:black;
padding:20px;
border-radius:15px;
box-shadow:0 10px 20px rgba(0,0,0,0.3);
}

img{
width:100%;
border-radius:10px;
}

.buttons{
margin-top:15px;
}

button{
padding:12px 20px;
border:none;
border-radius:25px;
margin:5px;
cursor:pointer;
font-size:16px;
}

.like{
background:#ff4d6d;
color:white;
}

.pass{
background:#aaa;
color:white;
}

</style>
</head>

<body>

<div class="app">

<h1>🌈 Prism</h1>
<p>Find love in every color</p>

<div class="card" id="profileCard">

<img id="photo" src="https://via.placeholder.com/300">

<h2 id="name">Name</h2>

<p id="pronouns"></p>

<p id="orientation"></p>

<p id="bio"></p>

<div class="buttons">

<button class="pass" onclick="pass()">❌ Pass</button>

<button class="like" onclick="like()">❤️ Like</button>

</div>

</div>

</div>

<script>

let profiles=[

{
name:"Alex",
pronouns:"They/Them",
orientation:"Pansexual",
bio:"Poetry lover and night thinker.",
photo:"https://i.pravatar.cc/300?img=12"
},

{
name:"Jordan",
pronouns:"She/Her",
orientation:"Lesbian",
bio:"Artist, coffee addict, and soft soul.",
photo:"https://i.pravatar.cc/300?img=32"
},

{
name:"Kai",
pronouns:"He/They",
orientation:"Queer",
bio:"Music producer and gamer.",
photo:"https://i.pravatar.cc/300?img=45"
}

]

let current=0

function showProfile(){

let p=profiles[current]

document.getElementById("name").innerText=p.name
document.getElementById("pronouns").innerText=p.pronouns
document.getElementById("orientation").innerText=p.orientation
document.getElementById("bio").innerText=p.bio
document.getElementById("photo").src=p.photo

}

function like(){

alert("You liked "+profiles[current].name)

nextProfile()

}

function pass(){

nextProfile()

}

function nextProfile(){

current++

if(current>=profiles.length){

alert("No more profiles")

current=0

}

showProfile()

}

showProfile()

</script>

</body>
</html>
