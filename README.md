# RBO Explorer

An interactive explainer for **rank-biased overlap** (RBO), the top-weighted similarity measure for rankings introduced by Webber, Moffat and Zobel (2010). It shows how the persistence parameter *p* decides which ranks a score depends on.

**Live page:** https://breuert.github.io/rbo/

## What you can do

- Set *p* with a logarithmic slider, by typing a value, or with presets, and watch every number update.
- Compare two rankings depth by depth: overlap, agreement, depth weight and each depth's contribution to the score. Lines between shared items get thicker the more that item adds at the current *p*.
- Reorder items by dragging them, or focus an item and press ↑/↓. You can also shuffle or reverse a list, load an example, or type your own lists.
- Read RBO<sub>ext</sub> together with its bounds RBO<sub>min</sub> and RBO<sub>max</sub>, both at the current *p* and as a curve over all values of *p*.
- See how much of the total weight the top *d* ranks hold.
- Compare six variations of one ranking and watch their order change as *p* moves.

The address bar stores *p* and both rankings, so a copied link reproduces the current view.

## How it is built

`index.html` is a single self-contained file. HTML, CSS and JavaScript are inline, there is no build step, and the page makes no external requests (formulas use native MathML). Open it directly in a browser or serve the folder with any static web server.

The computations follow the paper: RBO<sub>min</sub>, RBO<sub>max</sub> (= RBO<sub>min</sub> + RBO<sub>res</sub>) and the point estimate RBO<sub>ext</sub>, including the paper's extension for lists of different lengths.

GitHub Pages serves the site from the root of the `main` branch. The empty `.nojekyll` file turns off Jekyll processing.

## Reference

William Webber, Alistair Moffat and Justin Zobel. 2010. A similarity measure for indefinite rankings. *ACM Transactions on Information Systems* 28(4), Article 20. https://doi.org/10.1145/1852102.1852106
