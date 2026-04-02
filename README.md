<!DOCTYPE html>
<html>
<head>
<title>Prism - LGBTQ+ Dating App</title>

<style>
body{
font-family: Arial;
background: linear-gradient(45deg,#ff0080,#7928ca);
color:white;
text-align:center;
padding:40px;
}

.container{
background:white;
color:black;
padding:20px;
border-radius:10px;
width:300px;
margin:auto;
}

button{
padding:10px;
margin:5px;
border:none;
border-radius:5px;
background:#7928ca;
color:white;
cursor:pointer;
}
</style>

</head>

<body>

<h1>🌈 Prism</h1>
<p>Find love in every color</p>

<div class="container">

<h3>Create Profile</h3>

<input type="text" id="name" placeholder="Name"><br><br>

<input type="text" id="pronouns" placeholder="Pronouns"><br><br>

<input type="text" id="orientation" placeholder="Orientation"><br><br>

<button onclick="createProfile()">Create Profile</button>

</div>

<br>

<div class="container">

<h3>Profiles</h3>

<div id="profiles"></div>

</div>

<script>

let profiles=[]

function createProfile(){

let name=document.getElementById("name").value
let pronouns=document.getElementById("pronouns").value
let orientation=document.getElementById("orientation").value

let profile={
name:name,
pronouns:pronouns,
orientation:orientation
}

profiles.push(profile)

displayProfiles()

}

function displayProfiles(){

let area=document.getElementById("profiles")

area.innerHTML=""

profiles.forEach(p=>{

area.innerHTML+=`
<div>
<h4>${p.name}</h4>
<p>${p.pronouns}</p>
<p>${p.orientation}</p>
<button>❤️ Like</button>
<button>❌ Pass</button>
</div>
<hr>
`

})

}

</script>

</body>
</html>
