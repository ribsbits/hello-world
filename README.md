# R - notes

THis is a file for notes from courera tutorial about R.

## Objects:
R has five "atomic" (basic) classes of objects:
* charatcer
* numeric (real numbers)
** Treated as numeric obejcts, unless explicitly noted with "L"
** Inf represents infinity
** NaN represents "not a number"
* integer
* complex
* logical (T/F)
* Can have names
** names(x) <- c(name1, name2, ..., namen)

### Vector - only contains ojets of the same class
Created using vector(class, length), c(x1, x2, ..., xn), list(), vector (type, length)
Lists, however, can contain elements of different functions
* list((x, y, "z", T, etc)
** indexed by "[[" ]]"
Different classes can cause "coercion", which converts to an easiest class/least common denominator.

#### Factor
* Categorical data; ordered (ordered; 1, 2, 3) or unordered
* Using a label is more descriptive and self-descriptive
** ie, Male/Female
* factor(vector, levels = vector(first, second, third)) - if you don't use levels it goes by alphabetical
** table(factor) - gives the number of each factor
** unclass(factor) - gives the number attribute

### Matrix - only contains objects of the same class
Have a dimensional attribute
matrix(nrow = x, ncol = y)
dim() = dimension output rows columns
* can assign a dimension (dim()) to a vector; dim(matrix) <- c(2,5) will create a matrix with 2 rows and 5 columns
* can also use cbing(x,y) or rbind(x,y)
Filled columnw-wise initially

#### Name using dimnames(matrix) <- list(c(rows), c(cols))

### Data Frames
Used to store tabular data
Every element has same length, but doesn't have to have the same element
* row.names
* can be created using read.table() or read.csv()
* Convert to matix by calling data.matrix()
* data.frame(c(), c(), c())
nrow()
ncol() counts columns

#### Named by creating list; x <- list(a = 1, b = 2, c = 3)

### Missing values
is.na() - test to see if there are missing values
NA can have classes
is.nan() - test for NaN (not a number)


### Attributes
* names, dimnames
* dimensions
* class(x)
** Convert with as.-----; as.numeric(x), as.logical(x), as.character(x)
*** Can get "NA" if it doesn't work
* length (number of elements)
* other user-defined attributes/metadata
** attributes()


## Reading and writing data

### read.table, read.csv [comma is the default in csv] - both read text files and return a data frame
* read.table(file, header = T, sep = ",", colClasses [character vector  indicating calss of each column], nrows [ number of rows], comment.char [ character string indiciating the comment character], skip [ number of lines to skip from teh beginning], stringsAsFactors [ default is T, code character variables as factors]) 

**write.table - does the opposite and writes the table into a file
### readLines - read lines of a text file
### source read R codes
### dget
### load, unseralize - read

