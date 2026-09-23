# samflynn.github.io

My personal site. Built with Quarto and served by GitHub Pages from the `docs/` folder.

## Install these first

Quarto 1.10.18, uv 0.12.5, and R 4.6.1.

You don't need to install renv. `.Rprofile` and `renv/activate.R` are already in the repo, and they set it up the first time R starts here. uv fetches Python 3.14 by itself, per `.python-version`.

## Build it

Clone, then run every command from the top level of the repo.

```bash
git clone https://github.com/samflynn/samflynn.github.io.git
cd samflynn.github.io

uv sync                        # Python env from uv.lock
Rscript -e 'renv::restore()'   # R env from renv.lock, takes a few minutes
uv run quarto render
```

## Where the site is

The build writes to `docs/`. Open it with:

```bash
open docs/index.html
```

## Where the data comes from

Both posts use Palmer Penguins: https://allisonhorst.github.io/palmerpenguins/, cited as Horst, Hill and Gorman (2020), doi:10.5281/zenodo.3960218. 

Data is CC0, package is MIT, collected by the Palmer Station Antarctica LTER.