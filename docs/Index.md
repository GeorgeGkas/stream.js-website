# stream.js [![Build Status](https://travis-ci.org/dionyziz/stream.js.svg?branch=master)](https://travis-ci.org/dionyziz/stream.js) [![codecov.io](https://codecov.io/github/dionyziz/stream.js/coverage.svg?branch=master)](https://codecov.io/github/dionyziz/stream.js?branch=master)

stream.js is a tiny Javascript library that unlocks a new data structure for you: streams.

## What's so special about them?
Streams are an easy to use data structure similar to arrays and linked lists, but with some **extraordinary** capabilities. Unlike arrays, streams are a magical data structure:

***They can have an infinite number of elements!***

Yes, you heard right. Their power comes from being lazily evaluated, which in simple terms means that they can contain infinite items.

## Installation
In nodejs:

```js
npm install https://github.com/dionyziz/stream.js.git
```

In bower:

```js
bower install stream.js
```

As per [bower.json specification](https://github.com/bower/spec/blob/master/json.md#main),
we have defined the source file for stream.js and not a minified version. You can get a
minified version from [jsDelivr](https://www.jsdelivr.com/projects/stream.js).


## Usage
In nodejs:

```js
var Stream = require('stream.js');
var s1 = Stream.make(1,2,3);
var s2 = new Stream();
s2.append(1).append(2).append(3);
```

In the browser:

```html
<script src="stream.js"></script>
<script>
  var s1 = Stream.make(1,2,3);
  var s2 = new Stream();
  s2.append(1).append(2).append(3);
</script>
```

or with AMD:
```js
define(function(require) {
  var Stream = require("stream.js");
  Stream.make(1,2,3).print();
});
```
