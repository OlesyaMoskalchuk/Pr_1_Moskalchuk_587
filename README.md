<html>
<head>

<script>

function calc()
{
  var el;

  el = document.getElementById( 'q' );
  var q = parseFloat( el.value );

  el = document.getElementById( 'x' );
  var x = parseFloat( el.value );
  var start_x = x;

  var s = "q = " + q + "<br/>x = " + x + "<br/>Результат:<br/>";

  _q = 1.0 / q;

  x2 = 0;

  for( i = 1; i <= 5; i++ )
  {
    // s = s + x + " => ";

    var n = Math.floor( x / _q );
    s = s + n + "<br/>";

    x = x - n * _q;

    x2 = x2 + n * _q;

    _q = _q / q;
  }

  s = s + "Итоговое число: " + x2 + "</br>Разница: " + (x2 - start_x);

  // alert( s );

  document.getElementById( 'res' ).innerHTML = s;
}

</script>
</head>

<body>
<form>
x: <input type="text" id="x" value="0.35"/><br/>
q: <input type="text" id="q" value="3"/><br/>
<button type="button" onclick="calc()">решение</button>
</form>
<div id="res">Результат</div>
</body>
</html>
# Pr_1_Moskalchuk_otchet
