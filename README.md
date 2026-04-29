<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grid Animation</title>

    <style>
        * {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f2f2f2;
            animation: fadeIn 1.5s ease-in;
        }

        h1 {
            margin: 20px 0;
            text-transform: uppercase;
            animation: slideDown 1s ease;
        }

        .container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
            padding: 40px;
            background: linear-gradient(135deg, aqua, lightblue);
            border: 2px solid black;
            max-width: 800px;
            margin: 30px auto;
            animation: zoomIn 1.2s ease;
        }

        .box {
            height: 180px;
            border: 3px solid black;
            border-radius: 15px;
            background: linear-gradient(45deg, #332e68, #6a5acd);
            
            /* animation */
            animation: float 3s ease-in-out infinite;
            transition: 0.4s;
        }

        /* delay second box */
        .box:nth-child(2) {
            animation-delay: 0.5s;
        }

        .box:hover {
            transform: scale(1.1) rotate(5deg);
            box-shadow: 0 0 20px aqua, 0 0 40px white;
            background: linear-gradient(45deg, black, #00ffff);
        }

        /* KEYFRAMES */

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes slideDown {
            from {
                transform: translateY(-50px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        @keyframes zoomIn {
            from {
                transform: scale(0.8);
                opacity: 0;
            }
            to {
                transform: scale(1);
                opacity: 1;
            }
        }

        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }

    </style>
</head>

<body>
    <h1>Animated Boxes</h1>

    <section>
        <div class="container">
            <div class="box"></div>
            <div class="box"></div>
        </div>
    </section>
</body>
</html>
