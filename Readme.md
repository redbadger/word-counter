
# word-counter

  Watch a text field and live update word count

## Installation

  Install with [component(1)](http://component.io):

    $ component install redbadger/word-counter

## API

  Word counter gives you a ```WordCounter``` object. You create an instance with

```js
  var WordCounter = require('word-counter');

  var counter = new WordCounter("#input-el", ".output-el");
```

  First two parmeters are CSS selectors. First one should match one or more input elements (input or textarea),
  the second one can select any number of general DOM elements.

  WordCounter watches the input elements and whenever the text in them changes, it counts the words in each input,
  sums them up and outputs the number into the output elements.

  If you need a more complex thing, WordCounter accepts a third parameter - a callback that is run with the
  new count for each one of the output elements and its return value is used as output.

```js
  var WordCounter = require('word-counter');

  var counter = new WordCounter("#input-el", ".output-el", function(count, outEl) { return "You have typed " + count + " words!";} );
```

## License

  MIT
