# onehost [![Build Status](https://secure.travis-ci.org/fengmk2/onehost.png)](http://travis-ci.org/fengmk2/onehost) [![Coverage Status](https://coveralls.io/repos/fengmk2/onehost/badge.png)](https://coveralls.io/r/fengmk2/onehost)

One host only, redirect other hosts to bind host.

* jscoverage: [100%](http://fengmk2.github.com/coverage/onehost.html)

## Usage

```js
var connect = require('connect');
var onehost = require('onehost');

var app = connect(
  onehost({
    host: 'localhost.cnodejs.org',
    // exclude: 'dev.cnodejs.org',
  }),
  function (req, res) {
    res.end(JSON.stringify({headers: req.headers, url: req.url}));
  }
);

app.listen(1984);
```

### Install

```sh
$ npm install onehost
```

test on nodejs:

```bash
$ npm test
```

## License 

(The MIT License)

Copyright (c) 2012 - 2013 fengmk2 <fengmk2@gmail.com>.

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
