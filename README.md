<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            display: flex;
            justify-content: center; /*for horizontal alignment*/
            align-items: center; /*for vertical alignment*/
            height: 100vh;
        }

        td,th{
            border:none;
        }
        #display{
            margin-bottom: 20px;
            width: 100%;
            height: 40px;
            border-radius: 5px;
            border: none;
            text-align: right;
            background-color: aliceblue;
            color: black;
            font-size:larger ;     
        }

        button{
            width: 60px;
            height: 60px;
            border-radius: 10px;
            border: none;
            background-color: white;
            font-size: 2rem;
            font-weight: bold;
            margin: 5px;
        }

        table{
            background-color: gray;
            border-radius: 10px;
            padding-bottom: 20px;
            padding-top: 20px;
            padding-left: 20px;
            padding-right: 20px;
            border:none;
        }

        .equals_btn{
            background-color: orange;
        }
    </style>
    
</head>

<body>
    <table border="">
        <thead>
            <tr>
                <th colspan="4"><input id="display"readonly type="text" name="pnumber"></th>
            </tr>
        </thead>
        <tbody>
            <tr align="center">
                <td><button onclick="appendToDisplay('7')">7</button> </td> 
                <td><button onclick="appendToDisplay('8')">8</button></td>
                <td><button onclick="appendToDisplay('9')">9</button></td>
                <td><button onclick="appendToDisplay('/')">&divide;</button></td>
            <tr>
                <tr align="center">
                    <td><button onclick="appendToDisplay('4')">4</button></td>
                    <td><button onclick="appendToDisplay('5')">5</button></td>
                    <td><button onclick="appendToDisplay('6')">6</button></td>
                    <td><button onclick="appendToDisplay('*')">&times;</button></td>
                </tr>
                <tr align="center">
                    <td><button onclick="appendToDisplay('1')">1</button></td>
                    <td><button onclick="appendToDisplay('2')">2</button></td>
                    <td><button onclick="appendToDisplay('3')">3</button></td>
                    <td><button onclick="appendToDisplay('-')">&minus;</button></td>
                </tr>
                <tr align="center">
                    <td><button onclick="appendToDisplay('0')">0</button></td>
                    <td><button onclick="appendToDisplay('.')">.</button></td>
                    <td><button onclick="appendToDisplay('+')">+</button></td>
                    <td><button onclick="calculate()" class="equals_btn">=</button></td>
                </tr>
        </tbody>
    </table>
    <script>
        const display = document.getElementById("display");

        function appendToDisplay(input){
            display.value += input;

        }

        function calculate(){
            try{
                display.value=eval(display.value);
            }
            catch(error){
                display.value="Error";

            }

        }

    </script>
</body>

</html>
