# HTML
DIGITAL PAGE
<!doctype html>
<html>
  <head>
    <title>Digital Calculator</title> 
  </head> 
  <body>
    <form> 
      <fieldset>
        <p style="text-align:center"><font color="blue" size="20">Digital Calculator Presented by Sundar</font></p>
        <br>
        <img src="https://cdn.pixabay.com/photo/2017/06/05/15/52/calculator-2374442_1280.png" width="400" height="300"> 
        <br>
        Input1: <input type="number" id="input1">
        <br>
        Input2: <input type="number" id="input2"> 
        <br> 
        select operation:
        <select id="operation"> 
          <option value="select..">select..</option> 
          <option value="ADD">ADD</option>
          <option value="SUBTRACT">SUBTRACT</option>
          <option value="MULTIPLY">MULTIPLY</option> 
          <option value="DIVIDE">DIVIDE</option> </select>
        <br>y
        <button type="button" onclick="performOperation()">Submit</button> <button type="reset">Reset</button>
      </fieldset>
    </form>
    <script>
      function performOperation() {
        var input1 = parseFloat(document.getElementById('input1').value);
        var input2 = parseFloat(document.getElementById('input2').value);
        var operation = document.getElementById('operation').value; 
        var result;
        switch (operation) {
          case 'ADD':
            result = input1 + input2;
            break;
          case 'SUBTRACT':
            result = input1 - input2;
            break;
          case 'MULTIPLY':
            result = input1 * input2;
            break;
          case 'DIVIDE': result = input1 / input2;
            break;
          default:
            result = 'Please select a valid operation';
        }
        alert('The result is: ' + result);
      }
    </script>
  </body>
</html>
