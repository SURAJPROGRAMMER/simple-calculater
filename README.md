# simple-calculater

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <style>
        p.large-number-red{
            font-size: 20px;
            color: red;
        }
    </style>
</body>  
<body>  
    <h2>Simple Calculator</h2>
    <h1>
      <div class="calculator">
        <input type="text" id="display" disabled><br>
        <input type="button" value="7" onclick="appendToDisplay('7')">
        <input type="button" value="8" onclick="appendToDisplay('8')">
        <input type="button" value="9" onclick="appendToDisplay('9')">
        <input type="button" value="/" onclick="appendToDisplay('/')"><br>
        <input type="button" value="4" onclick="appendToDisplay('4')">
        <input type="button" value="5" onclick="appendToDisplay('5')">
        <input type="button" value="6" onclick="appendToDisplay('6')">
        <input type="button" value="-" onclick="appendToDisplay('-')"><br>
        <input type="button" value="1" onclick="appendToDisplay('1')">
        <input type="button" value="2" onclick="appendToDisplay('2')">
        <input type="button" value="3" onclick="appendToDisplay('3')">
        <input type="button" value="+" onclick="appendToDisplay('+')"><br>
        <input type="button" value="0" onclick="appendToDisplay('0')">
        <input type="button" value="." onclick="appendToDisplay('.')">
        <input type="button" value="=" onclick="calculate('*')">
        <input type="button" value="cal" onclick="calculate('/')"><br>
        <input type="buttum" value="clear" onclick="clear data"
      </div>    
        <script>
            function appendToDisplay(value) {
                document.getElementById('display').value += value;
            }
            function clearDisplay() {
                document.getElementById('display').value = '';
            }
            function calculate() {
                try {
                    var result = eval(document.getElementById('display').value);
                    document.getElementById('display').value = result;
                } catch(error) {
                    document.getElementById('display').value = 'Error';
                }
            }
        </script>
</body>
</html>
