# sass-bem-mixins

[![npm version](https://badge.fury.io/js/sass-bem-mixins.svg)](https://badge.fury.io/js/sass-bem-mixins)

Npm Module for some simple BEM mixins for Sass. Heavily inspired by [CSS Tricks](https://css-tricks.com/snippets/sass/bem-mixins/) and [Grsmto](https://gist.github.com/Grsmto/7791840).

[Github Pages Demo](https://torch2424.github.io/sass-bem-mixins/).
[NPM Module Link](https://www.npmjs.com/package/sass-bem-mixins).

## Usage

Install to the project:

```
npm install --save sass-bem-mixins
```

Simply import at the top of a sass file to get going:

```scss
@import './node_modules/sass-bem-mixins/index.scss';

// Other Sass down here...
```

## Example

Please see the [docs](https://github.com/torch2424/sass-bem-mixins/tree/master/docs) folder for a very simple example project that is on the [Github Pages](https://torch2424.github.io/sass-bem-mixins/).

```scss
@import 'node_modules/sass-bem-mixins/index';

@include block('exampleBlock') {
  background-color: blue;
  color: white;

  @include element('exampleElement') {
    background-color: red;

    @include modifier('modified') {
      background-color: green;
    }
  }
}

/*******************
// Would give the output

.exampleBlock {
  background-color: blue;
  color: white;
}

.exampleBlock__exampleElement, .exampleBlock__exampleElement--modified {
  background-color: red;
}

.exampleBlock__exampleElement--modified {
  background-color: green;
}

*******************/
```

## Contributing

Clone the project:

```
git clone https://github.com/torch2424/sass-bem-mixins.git
```

Install devDependencies:

```
npm install
```

Run the command: `npm run build`, to continuously see changes to the `index.html` in the `docs` folder. Sorry, but no livereload or watch is set up for this (Since it's just a simple little package).

## LICENSE

[MIT](https://choosealicense.com/licenses/mit/#)
