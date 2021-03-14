# simple-grid

***Bloated***

Simple CSS grid framework with media queries support. [Here is a demonstration](https://dreadsd.github.io/simple-grid/).

## Installation
```sh
git clone https://github.com/dreadsd/simple-grid.git
cd simple-grid
```
### Usage
Include `css/base.css` file in your HTML layout.
Now you're able to use the following classes:
```
.grid-[4|8|12|16]
- Example: .grid-8 is a grid with 8 columns
┃
┗━.row-vh-[1|...|4] (viewport height: 25 to 100, step 25)
  .row-pr-[1|...|4] (percentage: 25 to 100, step 25)
  .row-rm-[1|...|6] (rem units: 5 to 30, step 5)
  - Example: row-pr-3 is a row with 75% of the parent container height
  ┃
  ┗━.col-[1|...|num of colums|none] (column span)
    - Example: col-5 is an element that spans 5 columns
```
Define a custom height for the columns if you want to exclude the row class.

Media queries:
`.col-<breakpoint>-[1|...]`
|Breakpoint|  Size  |
|----------|--------|
|    sm    |≥ 576px |
|    md    |≥ 768px |
|    lg    |≥ 992px |
|    xl    |≥ 1200px|

### Development
Install dependencies (requires npm)
```sh
npm install
```
Sass required. Compile `css/scss/` files to `css/base.css`.

## Customization and defaults
Change defaults in `css/scss/_root.scss`.

## License
[MIT](https://opensource.org/licenses/MIT)
