<!DOCTYPE html>
<html lang="ku">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>پرسیارێکی گرنگ ❤️</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ff758c, #ff7eb3);
            font-family: Arial, sans-serif;
            direction: rtl;
            overflow: hidden;
        }

        .box {
            background: white;
            padding: 40px 25px;
            width: 90%;
            max-width: 500px;
            border-radius: 25px;
            text-align: center;
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
        }

        h1 {
            font-size: 30px;
            margin-bottom: 30px;
            color: #333;
        }

        .buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            position: relative;
            min-height: 55px;
        }

        button {
            border: none;
            padding: 14px 30px;
            border-radius: 12px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.2s;
        }

        #yes {
            background: #28c76f;
            color: white;
        }

        #yes:hover {
            transform: scale(1.1);
        }

        #no {
            background: #ff4757;
            color: white;
            position: relative;
        }

        .message {
            display: none;
            font-size: 25px;
            color: #ff4081;
            margin-top: 25px;
            font-weight: bold;
        }
    </style>
</head>

<body>

    <div class="box">

        <h1>ئایا شووم پێ ئەکەیت؟ ❤️</h1>

        <div class="buttons">

            <button id="yes">
                بەڵێ ❤️
            </button>

            <button id="no">
                نەخێر 😢
            </button>

        </div>

        <div class="message" id="message">
            ئەی وااااا ❤️🥹<br>
            زۆر خۆشحاڵم!
        </div>

    </div>

    <script>

        const noButton = document.getElementById("no");
        const yesButton = document.getElementById("yes");
        const message = document.getElementById("message");

        function moveButton() {

            const maxX =
                window.innerWidth -
                noButton.offsetWidth -
                20;

            const maxY =
                window.innerHeight -
                noButton.offsetHeight -
                20;

            const randomX =
                Math.max(10, Math.random() * maxX);

            const randomY =
                Math.max(10, Math.random() * maxY);

            noButton.style.position = "fixed";
            noButton.style.left = randomX + "px";
            noButton.style.top = randomY + "px";
        }


        // بۆ کۆمپیوتەر
        noButton.addEventListener(
            "mouseenter",
            moveButton
        );


        // بۆ مۆبایل
        noButton.addEventListener(
            "touchstart",
            function(event) {

                event.preventDefault();

                moveButton();

            }
        );


        // کاتێک بەڵێ هەڵدەبژێردرێت
        yesButton.addEventListener(
            "click",
            function() {

                message.style.display = "block";

                yesButton.style.display = "none";

                noButton.style.display = "none";

            }
        );

    </script>

</body>
</html>
