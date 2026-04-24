<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Grid Layout</title>

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
        }

        h1 {
            margin: 20px 0;
            text-transform: uppercase;
        }

        .container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
            padding: 40px;
            background-color: aqua;
            border: 2px solid black;
            max-width: 800px;
            margin: 30px auto;
        }

        .box {
            height: 180px;
            display: flex;
            justify-content: center;
            align-items: center;
            border: 3px solid black;
            background-color: rgb(51, 46, 104);
            color: white;
            font-weight: bold;
            font-size: 24px;
            text-transform: capitalize;
            transition: 0.3s;
        }

        .box:hover {
            background-color: black;
            color: aqua;
        }
    </style>
</head>

<body>
    <h1>Image Box</h1>

    <section>
        <div class="container">
            <div class="box">hero</div>
            <div class="box">heroine</div>
        </div>
    </section>
</body>
</html># Spheronix-task
