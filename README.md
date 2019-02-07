## MODULE 07      

<span style="color:blue">***CHALLANGE-01:***</span>

First, create a vector of 1 word character strings comprising the first line of the Gettysburg address: “Four score and seven years ago our fathers brought forth on this continent, a new nation, conceived in Liberty, and dedicated to the proposition that all men are created equal.”

``` {r}
library(stringr)
```

``` {r}
frase <- "Four score and seven years ago our fathers brought forth on this continent, a new nation, conceived in Liberty, and dedicated to the proposition that all men are created equal."
```

``` {r}
split <- c(str_split(frase, " ", simplify=TRUE))
split
```

``` {r}
splitfinal <- split[seq(from=1, to=30, by=3)]
splitfinal
```

``` {r}
gsub("[[:punct:]]","", splitfinal)
```

<span style="color:blue">***CHALLANGE-02:***</span>

Given the matrix, `m <- matrix(data = 1:80, nrow = 8, ncol = 10, byrow = FALSE)`, extract the 2nd, 3rd, and 6th columns and assign them to the variable x

```{r}
m <- matrix(data = 1:80, nrow = 8, ncol = 10, byrow = FALSE)
x <- m[ ,c(2,3,6)]
x
```

- Given the matrix, m, above, extract the 6th to 8th row and assign them to the variable x

```{r}
x <- m[c(6:8), ]
x
```

- Given the matrix, m, above, extract the elements from row 2 to row 6, and column 6 to column 9 and assign them to the variable x

```{r}
x <- m[c(2:6), c(6:9)]
x
```

<span style="color:blue">***CHALLANGE-03:***</span>

Construct a 4-dimensional, 400 element array (5 x 5 x 4 x 4) named a consisting of the numbers 400 to 1 (i.e., a descending series)

```{r}
 a <- array(400:1, dim=c(5,5,4,4))
```

 - Given this matrix, what would the following return?

```{r}
a[1, 1, 1, 2]
```

```{r}
a[2, 3, 2, ]
```

```{r}
a[1:5, 1:5, 3, 3]
```

<span style="color:blue">***CHALLANGE-04:***</span>

Create a list representing the (simplified) primate taxonomy outlined below. HINT: you can use lists as elements in a list.

```{r}
Haplorhini <- list(Anthropoidea=c("Platyrrhini", "Catarrhini"), Tarsioidea = ("Tarsiidae"))
Haplorhini
```

```{r}
Anthropoidea <- list(Platyrrhini=c("Cebidae", "Atelidae", "Pitheciidae"), Catarrhini=c("Cercopithecidae", "Hylobatidae", "Hominidae"))
Anthropoidea
```

```{r}
Strepsirhini <- list(Lorisoidea=c("Lorisidae", "Galagidae"), Lemuroidea=c("Cheirogaleidae", "Lepilemuridae", "Indriidae", "Lemuridae", "Daubentoniidae"))
Strepsirhini
```
``{r}
Primates <- list(Haplorhini=Haplorhini, Anthropoidea=Anthropoidea, Strepsirhini=Strepsirhini)
Primates
```

<span style="color:blue">***CHALLANGE-05:***</span>

Store the following numbers as a 5 x 3 matrix: 3, 0, 1 ,23, 1, 2, 33, 1, 1, 42, 0, 1, 41, 0, 2. Be sure to fill the matrix ROWWISE.

```{r}
a <- matrix(c(3, 0, 1 ,23, 1, 2, 33, 1, 1, 42, 0, 1, 41, 0, 2), nrow=5, ncol=3, byrow=TRUE)
a
```

Then, do the following:

Coerce the matrix to a data frame.

```{r}
b <- data.frame(a)
b
```

As a data frame, coerce the second column to be logical-valued (Boolean)

```{r}
b$X2 <- as.logical(b$X2)
```

As a data frame, coerce the third column to be factor-valued

```{r}
b$X3 <- as.factor(b$X3)
```

When you are done, use the str() command to show the data type for each variable in your dataframe.

```{r}
str(b)
```

