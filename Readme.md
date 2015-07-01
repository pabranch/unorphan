# unorphan.js

Prevents text orphans.

> *orphan* (n.) A word, part of a word, or very short line that appears by itself at the end of a paragraph. (via [Wikipedia](http://en.wikipedia.org/wiki/Widows_and_orphans))

![](http://ricostacruz.com/unorphan/screenshot.png)

[![Status](https://travis-ci.org/rstacruz/unorphan.svg?branch=master)](https://travis-ci.org/rstacruz/unorphan "See test builds")

<br>

## Usage

Call `unorphan()` on some nodes. This changes last orphan space to a [non-breaking space][nbsp] so the last 2 words stick together.

[nbsp]: https://en.wikipedia.org/wiki/Non-breaking_space

```js
unorphan('h1, p')
// '<h1>Hello there world</h1>' => '<h1>Hello there&nbsp;world</h1>'
```

Or pass on a node, or a list of nodes:

```js
// Node
unorphan(document.querySelector('#top-heading h1'))

// NodeList
unorphan(document.querySelectorAll('h1, p'))

// jQuery
unorphan($('h1, p'))
```

You may also unorphan before line breaks by passing `{ br: true }`.

```js
unorphan('h1, p', { br: true })
// '4 Privet Drive<br>Little Whigging' => '4 Privet&nbsp;Drive<br>Little&nbsp;Whiggnig'
```

<br>

## Download

```
npm install unorphan
```

[![npm version](http://img.shields.io/npm/v/unorphan.svg?style=flat)](https://npmjs.org/package/unorphan "View this project on npm")

<br>

## Thanks

**unorphan** © 2015+, Rico Sta. Cruz. Released under the [MIT] License.<br>
Authored and maintained by Rico Sta. Cruz with help from contributors ([list][contributors]).

> [ricostacruz.com](http://ricostacruz.com) &nbsp;&middot;&nbsp;
> GitHub [@rstacruz](https://github.com/rstacruz) &nbsp;&middot;&nbsp;
> Twitter [@rstacruz](https://twitter.com/rstacruz)

[MIT]: http://mit-license.org/
[contributors]: http://github.com/rstacruz/unorphan/contributors
