</html># Hi-loviee-doabieeeee
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Valentine 💖</title>
<style>
    body {
        margin: 0;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background: linear-gradient(135deg, #ff9a9e, #fad0c4);
        font-family: 'Poppins', sans-serif;
        text-align: center;
        overflow: hidden;
        position: relative;
    }

    .container {
        background: white;
        padding: 40px;
        border-radius: 20px;
        box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        position: relative;
    }

    h1 {
        color: #ff4d6d;
    }

    .buttons {
        margin-top: 20px;
    }

    button {
        padding: 12px 30px;
        margin: 10px;
        font-size: 18px;
        border: none;
        border-radius: 50px;
        cursor: pointer;
        transition: 0.2s ease;
        position: relative;
    }

    #yesBtn {
        background-color: #ff4d6d;
        color: white;
    }

    #noBtn {
        background-color: #888;
        color: white;
        position: absolute;
    }

    #message {
        margin-top: 20px;
        font-size: 22px;
        color: #ff4d6d;
        font-weight: bold;
    }
</style>
</head>
<body>

<div class="container">
    <h1>Will you be my Valentine loviee? 💘</h1>

    <div class="buttons">
        <button id="yesBtn">YES</button>
        <button id="noBtn">NO</button>
    </div>

    <div id="message"></div>
</div>

<script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const message = document.getElementById("message");

    const noMessages = [
        "are you sure?",
        "loviee u sure",
        "looooovvvvviiiiieeeeee!!!",
        "just say yes loviee",
        "lovviieee pleaseeee"
    ];

    let noClickCount = 0;

    function moveButton() {
        const container = document.querySelector(".container");
        const containerRect = container.getBoundingClientRect();

        const maxX = container.offsetWidth - noBtn.offsetWidth;
        const maxY = container.offsetHeight - noBtn.offsetHeight;

        const randomX = Math.floor(Math.random() * maxX);
        const randomY = Math.floor(Math.random() * maxY);

        noBtn.style.left = randomX + "px";
        noBtn.style.top = randomY + "px";
    }

    noBtn.addEventListener("mouseover", () => {
        if (noClickCount < noMessages.length) {
            noBtn.innerText = noMessages[noClickCount];
        }
        noClickCount++;
        moveButton();
    });

    noBtn.addEventListener("click", moveButton);

    yesBtn.addEventListener("click", () => {
        message.innerText = "i love u sm loviee doabieeeee 💖";
        yesBtn.style.display = "none";
        noBtn.style.display = "none";
    });
</script>

</body>
