# drag, select 사용하지 않기!

~~~~
$('body').on({
  selectstart: function () { return false; },
  dragstart: function () { return false; }
});
~~~~
