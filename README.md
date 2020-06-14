# Async-Helper-Ajax-List
Async Helper Ajax List

```js
var actions = [];
$.each(lines, function(key, value) {

    actions.push(function(callback) {
      $.ajax({
          url: 'process.php?id='+val,
          success: function(msg) {
            clearInterval(auto_refresh);

            //
            // Perform your DOM operations here and be sure to call the
            // callback!
            //

            callback();
          }
        });
    });
  }
);


var sequencer = new Sequencer(actions);
sequencer.start();
```
