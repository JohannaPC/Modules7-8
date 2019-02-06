# Modules7-8

## MODULE 07
***CHALLANGE-01***

First, create a vector of 1 word character strings comprising the first line of the Gettysburg address: “Four score and seven years ago our fathers brought forth on this continent, a new nation, conceived in Liberty, and dedicated to the proposition that all men are created equal.”

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
