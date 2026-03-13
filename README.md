# My-projects
<!DOCTYPE html>
<html>
<head>
<title>Umar Video Editing Portfolio</title>
<link rel="stylesheet" href="style.css">
</head>

<body>

<header>
<h1>Umar Hussain</h1>
<p>Professional Video Editor</p>
</header>

<nav>
<a href="#portfolio">Portfolio</a>
<a href="#upload">Upload</a>
<a href="#contact">Hire Me</a>
</nav>

<section id="portfolio">
<h2>My Editing Work</h2>

<div class="video-grid" id="videoContainer">

<div class="video-card">
<video controls>
<source src="videos/video1.mp4">
</video>
</div>

</div>
</section>

<section id="upload">

<h2>Add New Video</h2>

<input type="file" id="videoUpload">
<button onclick="addVideo()">Upload</button>

</section>

<section id="contact">

<h2>Hire Me</h2>

<form>

<input type="text" placeholder="Your Name" required>
<input type="email" placeholder="Your Email" required>
<textarea placeholder="Your Project"></textarea>

<button type="submit">Send</button>

</form>

</section>

<footer>
<p>© 2026 Umar Editing Portfolio</p>
</footer>

<script src="script.js"></script>

</body>
</html><!DOCTYPE html>
<html>
<head>
<title>Umar Video Editing Portfolio</title>
<link rel="stylesheet" href="style.css">
</head>

<body>

<header>
<h1>Umar Hussain</h1>
<p>Professional Video Editor</p>
</header>

<nav>
<a href="#portfolio">Portfolio</a>
<a href="#upload">Upload</a>
<a href="#contact">Hire Me</a>
</nav>

<section id="portfolio">
<h2>My Editing Work</h2>

<div class="video-grid" id="videoContainer">

<div class="video-card">
<video controls>
<source src="videos/video1.mp4">
</video>
</div>

</div>
</section>

<section id="upload">

<h2>Add New Video</h2>

<input type="file" id="videoUpload">
<button onclick="addVideo()">Upload</button>

</section>

<section id="contact">

<h2>Hire Me</h2>

<form>

<input type="text" placeholder="Your Name" required>
<input type="email" placeholder="Your Email" required>
<textarea placeholder="Your Project"></textarea>

<button type="submit">Send</button>

</form>

</section>

<footer>
<p>© 2026 Umar Editing Portfolio</p>
</footer>

<script src="script.js"></script>

</body>
</html>body{
background:#0f0f0f;
color:white;
font-family:Arial;
margin:0;
}

header{
text-align:center;
padding:40px;
background:#111;
}

nav{
display:flex;
justify-content:center;
gap:30px;
background:#1a1a1a;
padding:15px;
}

nav a{
color:white;
text-decoration:none;
}

section{
padding:40px;
text-align:center;
}

.video-grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
}

.video-card video{
width:100%;
border-radius:10px;
}

input,textarea{
width:80%;
padding:10px;
margin:10px;
}

button{
padding:10px 20px;
background:#ff4444;
border:none;
color:white;
cursor:pointer;
}

footer{
background:#111;
text-align:center;
padding:20px;
}function addVideo(){

let file = document.getElementById("videoUpload").files[0];

if(!file){
alert("Select a video first");
return;
}

let url = URL.createObjectURL(file);

let videoContainer = document.getElementById("videoContainer");

let div = document.createElement("div");
div.className="video-card";

div.innerHTML =
`<video controls>
<source src="${url}">
</video>`;

videoContainer.appendChild(div);

}
umar-portfolio.netlify.app
