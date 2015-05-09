# Rune.js
Rune interpreter implemented with javascript

### How to use it?
Just put these codes to your web page.
```
<script src="js/rune.min.js"></script>
<script type="application/rune">
  console = import "stdio";
  console.println "Hello, world!";
</script>
<script>
  Rune.onload = function() {
    Rune.run();
  }
</script>
```

Or load rune script from external page with src attribute.
```
<script src="js/rune.min.js"></script>
<script type="application/rune" src="rune/hello_world.rune"></script>
<script>
  Rune.onload = function() {
    Rune.run();
  }
</script>
```

Also, you can insert multiple rune modules to single page, and select what module will be running.
```
<script src="js/rune.min.js"></script>
<script type="application/rune" src="rune/first_module.rune" data-module="first"></script>
<script type="application/rune" src="rune/second_module.rune" data-module="second"></script>
<script>
  Rune.onload = function() {
    document.getElementById('btn1').onclick = function(e) {
      Rune.run('first');
    }
    document.getElementById('btn2').onclick = function(e) {
      Rune.run('second');
    }
  }
</script>
```
