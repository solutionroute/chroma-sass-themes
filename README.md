Sass (SCSS) styles to construct syntax highlighting themes for the Go language package [Chroma](https://github.com/alecthomas/chroma). Chroma generates [Pygments](http://pygments.org/) compatible CSS classes so this tool and any themes produced can be used for either. Thanks @MoOx for starting this off years ago.

Balance of readme unchanged for now:

## Usage

In your main Sass file, just define the variable you want. See `my-pygments-theme.scss.sample` as a base. Just uncomment & define variable you need.
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

![render example](pygments-theme-freshcut.png)
