# Data files for intro workshop

- `gapminder.csv`: Entire GapMinder dataset
    - `gapminder-5060.csv`: 1950s and 1960s
    - `gapminder-7080.csv`: 1970s and 1980s
    - `gapminder-90plus.csv`: 1990s onwards

- **Important note about `gapminder-5060.csv`:
    - The dataset has been altered to add a "data error".
    - Life expectancy for Canada in the year 1967 is coded
    as `999999`, it should actually be `69.96`.
    - For details see [intro-01-slides.Rmd](https://github.com/Reproducible-Science-Curriculum/rr-intro/blob/master/intro-01-slides.Rmd).
    - `gapminder-5060_original.csv` contains the correct data.