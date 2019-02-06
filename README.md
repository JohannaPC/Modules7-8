# Modules7-8

``` {r}
library(stringr)
```

``` {r}
frase <- "Four score and seven years ago our fathers brought forth on this continent, a new nation, conceived in Liberty, and dedicated to the proposition that all men are created equal."
```

``` {r}
split <- c(str_split(frase, " ", simplify=TRUE))
```

``` {r}
splitfinal <- split[seq(from=1, to=30, by=3)]
```

``` {r}
gsub("[[:punct:]]","", splitfinal)
```
