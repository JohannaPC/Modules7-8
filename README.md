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


***CHALLANGE-02***

Given the matrix, `m <- matrix(data = 1:80, nrow = 8, ncol = 10, byrow = FALSE)`, above, extract the 2nd, 3rd, and 6th columns and assign them to the variable x

```{r}
m <- matrix(data = 1:80, nrow = 8, ncol = 10, byrow = FALSE)
x <- m[ ,c(2,3,6)]
```

- Given the matrix, m, above, extract the 6th to 8th row and assign them to the variable x

```{r}
x <- m[c(6:8), ]
```

- Given the matrix, m, above, extract the elements from row 2 to row 6, and column 6 to column 9 and assign them to the variable x

```{r}
x <- m[c(2:6), c(6:9)]
```

***CHALLANGE-03***

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


***CHALLANGE-04***

Create a list representing the (simplified) primate taxonomy outlined below. HINT: you can use lists as elements in a list.

l <- list(Primates=c(v1, v9), list(v2, v7), Anthropoidea=c(v3, v5), Platyrrhini=v6)

v0 <- ("Primates") 
v1 <- ("Haplorhini") 
v2 <- ("Anthropoidea")
v3 <- ("Platyrrhini")
v4 <- c("Cebidae", "Atelidae", "Pitheciidae")
v5 <- ("Catarrhini")
v6 <- c("Cercopithecidae", "Hylobatidae", "Hominidae")
v7 <- ("Tarsiodea") 
v8 <- c("Tarsiidae") 

v9 <- ("Strepsirhini") 
v10 <- ("Lorisoidea")
v11 <- c("Lorisidae", "Galagidae") 
v12 <- ("Lemuroidea") 
v13 <- c("Cheirogaleidae", "Lepimuridae", "Indriidae", "Lemuridae", "Daubentoniidae")


***CHALLANGE-05***

Store the following numbers as a 5 x 3 matrix: 3, 0, 1 ,23, 1, 2, 33, 1, 1, 42, 0, 1, 41, 0, 2. Be sure to fill the matrix ROWWISE.

```{r}
a <- matrix(c(3, 0, 1 ,23, 1, 2, 33, 1, 1, 42, 0, 1, 41, 0, 2), nrow=5, ncol=3, byrow=TRUE)
```

Then, do the following:

Coerce the matrix to a data frame.

```{r}
b <- data.frame(a)
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
