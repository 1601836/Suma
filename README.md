
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        *{
            margin: 0;
            padding: 0;
            font-family: sans-serif;
        }
        main{
            display: grid;
            place-items: center;
            background-color: beige;
            height: 100dvh;
        }
        .caja_suma{
            margin: 50px 0;
            width: 300px;
            height: 500px;
            background-color: aqua;
            display: grid;
            place-items: center ;
        }
        form{
            display: grid;
            place-items: center;
        }
        h1{
            margin-bottom: 40px;
        }
        input{
            display: block;
        }
        button{
            margin-top: 50px;
            margin-bottom: 50px;
        }
        .resultado{
            border: 5px solid blue;
            width: 200px;
            height: 50px;
            background-color: beige;
        }
        div{
            display: grid;
            place-items: center;
        }


    </style>
</head>
<body>
    <main>
        <div class="caja_suma">
            <form id="sumas_cajita">
                <h1>sumar numeros</h1>
                <label for="">numero 1:</label>
                <input type="number" id="one">
                <label for="">numero 2:</label>
                <input type="number" id="two">
                <button type="submit">Sumar</button>
                <div class="resultado" id="resultado"></div>
            </form> 
        </div>
    </main>

    <script>
        document.getElementById("sumas_cajita").addEventListener("submit", function(event) {
        event.preventDefault();
            const one = parseInt(document.getElementById("one").value);
            const two = parseInt(document.getElementById("two").value);

            const five = one + two;
            document.getElementById("resultado").textContent = "FINAL:" + five;
    
        });
    </script>
</body>
</html>
