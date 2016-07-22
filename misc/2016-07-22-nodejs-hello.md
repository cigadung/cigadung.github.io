Title: Express.JS Hello
Category: coding
Date: 2016-07-22
Tags: javascript

Hello World via Express.JS


```javascript
var express = require('express');
var app = express();

app.get('/', function (req, res) {
  res.send('Hello World!');
});

app.listen(3000, function () {
  console.log('Example app listening on port 3000!');
});
```

Hope, automatic build ok now.
