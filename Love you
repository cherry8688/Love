<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Love Message</title>
<style>
    body {
        margin: 0;
        height: 100vh;
        background: pink;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-family: Arial, sans-serif;
        overflow: hidden;
    }

    h1 {
        font-size: 2.5em;
        color: white;
        opacity: 0;
        transition: opacity 1.5s ease-in-out;
    }

    input {
        padding: 10px;
        font-size: 1em;
        border-radius: 20px;
        border: none;
        outline: none;
        text-align: center;
    }

    button {
        margin-top: 10px;
        padding: 10px 20px;
        border: none;
        border-radius: 20px;
        background-color: white;
        color: pink;
        font-size: 1em;
        cursor: pointer;
    }

    .heart {
        position: absolute;
        width: 20px;
        height: 20px;
        background-color: white;
        transform: rotate(45deg);
        animation: floatUp 5s linear infinite;
    }

    .heart::before,
    .heart::after {
        content: '';
        position: absolute;
        width: 20px;
        height: 20px;
        background-color: white;
        border-radius: 50%;
    }

    .heart::before {
        top: -10px;
        left: 0;
    }

    .heart::after {
        left: 10px;
        top: 0;
    }

    @keyframes floatUp {
        from {
            transform: translateY(0) rotate(45deg);
            opacity: 1;
        }
        to {
            transform: translateY(-800px) rotate(45deg);
            opacity: 0;
        }
    }
</style>
</head>
<body>

<input type="text" id="nameInput" placeholder="Enter name">
<button onclick="showLove()">Submit</button>
<h1 id="loveText"></h1>

<script>
function showLove() {
    let name = document.getElementById("nameInput").value.trim();
    if (name) {
        let text = document.getElementById("loveText");
        text.textContent = `I love you ${name}`;
        text.style.opacity = 1;
    }
}

function createHeart() {
    const heart = document.createElement('div');
    heart.classList.add('heart');
    heart.style.left = Math.random() * window.innerWidth + 'px';
    heart.style.animationDuration = (Math.random() * 3 + 2) + 's';
    document.body.appendChild(heart);
    setTimeout(() => {
        heart.remove();
    }, 5000);
}

setInterval(createHeart, 300);
</script>

</body>
</html>
