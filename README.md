# Pygments base theme using Sass

A simple [Pygments](http://pygments.org/) base theme, using [Sass](http://sass-lang.org).

## Usage

In you main Sass file, just define the variable you want. See `my-pygments-theme.scss.sample` as a base. Just uncomment & define variable you need.
By default there is no color defined.
At least define one the color in the first block in the sample :)

Checkout `pygment-theme-freshcut.scss` for an usage example.

### Options

Set variables `$code-base-selector(-*)` to `null` to avoid global & block styles.
Set any variables to null to avoid generated color.

## Live Example

Generate the example ([FreshCut theme](https://github.com/daylerees/colour-schemes#freshcut)): pygments sass base theme highlighed by itself :)

```bash
pygmentize -f html -o example.html _pygments.scss
sass pygments-theme-freshcut.scss example.css
echo "<link rel=\"stylesheet\" href=\"example.css\" /><style>body{-webkit-font-smoothing: antialiased}</style>" | cat - example.html > /tmp/out && mv /tmp/out example.html
```

![render example](https://raw.github.com/MoOx/pygments-sass-base-theme/master/pygments-theme-freshcut.png)
