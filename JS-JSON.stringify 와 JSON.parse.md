# JSON.stringify

JavaScript 값을(Object를) JSON 문자열로 변환

```js
var message = {
  event: "command",
  func: "playVideo",
  args: ""
};

JSON.stringify(message);

// {"event":"command","func":"playVideo","args":""}
```

# JSON.parse

JSON 문자열을 JavaScript Object로 변환

```js
var message = {
  event: "command",
  func: "playVideo",
  args: ""
};

var jsonMessage = JSON.stringify(message);
JSON.parse(jsonMessage);

// Object {event: "command", func: "playVideo", args: ""}
```
