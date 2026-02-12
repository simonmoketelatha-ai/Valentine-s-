<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tsakane, Be My Valentine ❤️</title>

<style>
body {
    margin: 0;
    font-family: 'Georgia', serif;
    background: linear-gradient(135deg, #1e0033, #660033, #ff3366);
    color: white;
    text-align: center;
    overflow-x: hidden;
}

/* Floating Hearts */
.heart {
    position: fixed;
    bottom: -10px;
    color: rgba(255, 255, 255, 0.7);
    font-size: 20px;
    animation: floatUp 8s linear infinite;
}

@keyframes floatUp {
    0% {transform: translateY(0) scale(1);}
    100% {transform: translateY(-100vh) scale(1.5);}
}

.container {
    padding: 40px 20px;
    position: relative;
    z-index: 2;
}

h1 {
    font-size: 3.5em;
    animation: fadeIn 3s ease-in-out;
}

h2 {
    font-weight: 300;
    margin-bottom: 30px;
}

img {
    max-width: 85%;
    border-radius: 25px;
    box-shadow: 0 0 40px rgba(255, 0, 100, 0.8);
    margin-bottom: 30px;
    transition: transform 0.5s;
}

img:hover {
    transform: scale(1.05);
}

.message {
    max-width: 800px;
    margin: auto;
    font-size: 1.3em;
    line-height: 1.8em;
}

.poem {
    margin-top: 40px;
    font-style: italic;
    font-size: 1.2em;
    white-space: pre-line;
}

.buttons {
    margin-top: 50px;
}

button {
    padding: 15px 35px;
    font-size: 1.2em;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    margin: 10px;
    transition: 0.3s;
}

.yes {
    background: white;
    color: #ff0066;
}

.yes:hover {
    background: #ff0066;
    color: white;
}

.no {
    background: black;
    color: white;
    position: absolute;
}

@keyframes fadeIn {
    from {opacity: 0;}
    to {opacity: 1;}
}
</style>
</head>

<body onclick="playMusic()">

<!-- Background Music -->
<iframe id="music" width="0" height="0" 
src="https://www.youtube.com/embed/W8a4sUabCUo?enablejsapi=1"
frameborder="0" allow="autoplay"></iframe>

<div class="container">
    <h1>Tsakane Molusi ❤️</h1>
    <h2>Will You Be My Valentine?</h2>

    <img src="valentine.jpg" alt="Our Love">

    <div class="message">
        Tsakane…  
        From the first moment you smiled at me, something inside me changed.

        You are the calm in my chaos.  
        The light in my darkest nights.  
        The reason my heart beats a little faster.

        I, Mokete, stand before you with nothing but honesty and love.  
        I don’t just want to hold your hand —  
        I want to build dreams with you.

        Every laugh we share feels like magic.  
        Every memory with you is priceless.

        You are not just special.  
        You are my answered prayer.
    </div>

    <div class="poem">
I see forever when I look in your eyes,
A future written across the skies.
If stars could whisper what I feel,
They'd say this love is strong and real.

Like dandelions in the wind,
My wishes all begin with you.
Every hope my heart has known
Leads me back to loving you.

So here I am, no fear, no disguise —
Just Mokete, asking you:
Will you be my Valentine? ❤️
    </div>

    <div class="buttons">
        <button class="yes" onclick="sayYes()">YES ❤️</button>
        <button class="no" id="noBtn">NO 😢</button>
    </div>
</div>

<script>
// Floating Hearts Generator
setInterval(() => {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 10 + "px";
    heart.style.animationDuration = Math.random() * 5 + 5 + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 8000);
}, 300);

// Runaway NO button
const noBtn = document.getElementById("noBtn");
noBtn.addEventListener("mouseover", () => {
    noBtn.style.top = Math.random() * window.innerHeight + "px";
    noBtn.style.left = Math.random() * window.innerWidth + "px";
});

// YES button
function sayYes() {
    alert("You just made Mokete the happiest man alive! ❤️💍");
}

// Play music after click
function playMusic() {
    const iframe = document.getElementById("music");
    iframe.src += "&autoplay=1";
}
</script>

</body>
</html>
