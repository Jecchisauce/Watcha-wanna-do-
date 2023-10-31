# Watcha-wanna-do-
<!DOCTYPE html>
<html>
<head>
    <title>Button Game</title>
    <style>
        p {
            text-align: center;
            font-size: 32px;
            font-family: Candara, Oswald;
        }
        img {
            display: block;
            margin: 0 auto;
            width: 25%;
        }
        body {
            position: relative;
        }
        #botao1 {
            position: absolute;
        }
    </style>
</head>
<body>
    <p>Can we hang out sometime?</p>
    <img src="https://media.tenor.com/zGm5acSjHCIAAAAM/cat-begging.gif">

    <button id="botao1">YES!</button>
    <button id="botao2">NO</button>

    <script>
        const button1 = document.getElementById('botao1');
        const button2 = document.getElementById('botao2');
        let left = 40;
        let topPosition = 40;
        let clicks = 0;

        button1.addEventListener('click', function () {
            if (clicks < 3) {
                left = getRandomLeft();
                top = getRandomTop();
                button1.style.left = left + '%';
                button1.style.top = topPosition + '%';
                clicks++;
            } else {
                alert('YAY! HAPPY TIMES.');
            }
        });

        button2.addEventListener('click', function () {
            alert("Awwee, I guess next time :<");
        });

        function getRandomLeft() {
            return Math.random() * 60; // Change this value to set the range of left positions.
        }

        function getRandomTop() {
            return Math.random() * 60; // Change this value to set the range of top positions.
        }
    </script>
</body>
</html>

