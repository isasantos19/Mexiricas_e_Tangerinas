<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        body{
            background: linear-gradient(135deg, #f5c16c, #d94f30);
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            color: #5a2e0c;
        }

        .conteudo{
            text-align: center;
            background: #fff3d6;
            padding: 30px;
            border-radius: 25px;
            border: 6px solid #f0a500;
            box-shadow: 0 15px 30px rgba(0,0,0,0.3);
        }

        h1{
            font-size: 40px;
            font-style: italic;
            color: #c0392b;
            margin-bottom: 15px;
        }

        label{
            display: block;
            margin-top: 10px;
            font-weight: bold;
            font-size: 18px;
        }

        input[type="number"]{
            padding: 10px;
            margin-top: 5px;
            border-radius: 10px;
            border: 2px solid #f0a500;
            text-align: center;
            width: 80%;
        }

        input[type="button"]{
            background: #c0392b;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 15px;
            cursor: pointer;
            font-weight: bold;
            margin-top: 15px;
            transition: 0.3s;
        }

        input[type="button"]:hover{
            background: #a93226;
            transform: scale(1.05);
        }

        span{
            font-weight: bold;
            color: #8e2c0c;
            background: #ffe0a3;
            padding: 6px 12px;
            border-radius: 10px;
            margin: 5px;
            display: inline-block;
        }
    </style>

</head>
<body>

<div class="conteudo">
    <h1><i>🍝 Bhaskara</i></h1>

    <label for="inputA">A</label>
    <input type="number" id="inputA">
    
    <label for="inputB">B</label>
    <input type="number" id="inputB">
    
    <label for="inputC">C</label>
    <input type="number" id="inputC">
   
    <input type="button" value="Calcular 🍗" onclick="funcaocalcular()">
    <br><br>

    <h1><i>Resultado</i></h1>

    <label for="resp">X1 =</label>
    <span id="resp">___</span>

    <label for="resp2">X2 =</label>
    <span id="resp2">___</span>
</div>

<script>
    function funcaocalcular(){
        let A=parseFloat(document.getElementById("inputA").value);
        let B=parseFloat(document.getElementById("inputB").value);
        let C=parseFloat(document.getElementById("inputC").value);
        let e="";
        let f="";

        let delta=(B**2)-(4*A*C);
        if(delta<0){
            alert("É impossível Calcular")}
            else{
        
         e= (-B+ Math.sqrt(delta))/2*A;
         f= (-B- Math.sqrt(delta))/2*A;
    }

        document.getElementById("resp").innerHTML=e;
        document.getElementById("resp2").innerHTML=f;

    }
</script>

</body>
</html>
