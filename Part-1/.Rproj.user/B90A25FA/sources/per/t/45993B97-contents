### Section 1.1 ###

# Intro to R Lesson
# Feb 16th, 2016
# Interacting with R
## I am adding 3 and 5. R is fun!
3+5
x <- 3
y <- 5
x + y
number <- x + y

### Exercise 
x <- 5
number <- x + y
y <- 10
number <- x + y





### Section 1.2 ###

# Create a numeric vector and store the vector as a variable called 'glengths'
glengths <- c(4.6, 3000, 50000)
glengths
# Create a character vector and store the vector as a variable called 'species'
species <- c("ecoli", "human", "corn")
species
# Forget to put quotes around corn
species <- c("ecoli", "human", corn)
# Create a character vector and store the vector as a variable called 'species'
species <- c("ecoli", "human", "corn")

### Exercise 
combined <- c(glengths, species)

# Create a character vector and store the vector as a variable called 'expression'
expression <- c("low", "high", "medium", "high", "low", "medium", "high")
# Turn 'expression' vector into a factor
expression <- factor(expression)

### Exercise 
samplegroup <- c("CTL", "CTL", "CTL", "KO", "KO", "KO", "OE", "OE", "OE")
samplegroup <- factor(samplegroup)

# Create a data frame and store it as a variable called 'df'
df <- data.frame(species, glengths)
df

### Exercise 
titles <- c("Catch-22", "Pride and Prejudice", "Nineteen Eighty Four")
pages <- c(453, 432, 328)
favorite_books <- data.frame(titles, pages)
favorite_books

list1 <- list(species, df, number)
list1
list2 <- list(species, glengths, number)
list2





### Section 1.3 ###


glengths <- c(glengths, 90) # adding at the end	
glengths <- c(30, glengths) # adding at the beginning
sqrt(81)
sqrt(glengths)
round(3.14159)
?round
args(round)
example("round")
round(3.14159, digits=2)
round(3.14159, 2)


### Exercise  
?mean
mean(glengths)
test <- c(1, NA, 2, 3, NA, 4)
mean(test, na.rm = TRUE)
sort(test, decreasing = TRUE)

# name_of_function <- function(argument1, argument2) {
# statements or code that does something
# return(something)
# }

square_it <- function(x) {
  square <- x * x
  return(square)
}

square_it(5)

### Exercise  
multiply_it <- function(x, y) {
  multiply <- x * y
  return(multiply)
}

multiply_it(x=4,y=6)





### Section 1.4 ###

?read.csv

metadata <- read.csv(file="data/mouse_exp_design.csv")

### Exercise 
proj_summary <- read.table(file = "data/project-summary.txt", header = TRUE, row.names = 1)
summary(proj_summary)

head(metadata)

### Exercise  
class(glength)
class(mettadata)
summary(proj_summary)
length(samplegroup)
dim(proj_summary)
str(rownames(metadata))
length(colnames(proj_summary))





### Section 1 Practice Exercise  ####
## Part 1 ##

temp_conv <- function(temp_f) {
  temp_c = (temp_f - 32) * 5 / 9
  temp_k = temp_c + 273.15
  return (temp_k)
}

## Part 2 ##
round(temp_conv(70), digits = 1)





### Section 2.1 ###

age <- c(15, 22, 45, 52, 73, 81)
age[5]
age[-5]
age[c(3,5,6)]   ## nested
# OR
## create a vector first then select
idx <- c(3,5,6) # create vector of the elements of interest
age[idx]
age[1:4]
age[4:1]

### Exercise  
alphabets <- c("C", "D", "X", "L", "F")
alphabets[c(1,2,5)]
alphabets[-3]
alphabets[5:1]

age
age > 50
age > 50 | age < 18
age
age[age > 50 | age < 18]  ## nested
# OR
## create a vector first then select
idx <- age > 50 | age < 18
age[idx]

which(age > 50 | age < 18)
age[which(age > 50 | age < 18)]  ## nested
# OR
## create a vector first then select
idx_num <- which(age > 50 | age < 18)
age[idx_num]

expression[expression == "high"]    ## This will only return those elements in the factor equal to "high"

### Exercise  
idx <- samplegroup != "KO"
samplegroup[idx]

expression
str(expression)
expression <- factor(expression, levels=c("low", "medium", "high"))     # you can re-factor a factor 
str(expression)

### Excericse
str(samplegroup)
samplegroup <- factor(samplegroup, levels=c("KO", "CTL", "OE"))





### Section 2.2 ###


sessionInfo() #Print version information about R, the OS and attached or loaded packages
# OR
search() #Gives a list of attached packages
install.packages("ggplot2")
library(ggplot2)

### Exercise  
install.packages("tidyverse")
library(tidyverse)
sessionInfo()





### Section 2.3 ###

# Extract value 'Wt'
metadata[1, 1]
# Extract value '1'
metadata[1, 3] 
# Extract third row
metadata[3, ] 
# Extract third column
metadata[ , 3]   
# Extract third column as a data frame
metadata[ , 3, drop = FALSE] 
# Dataframe containing first two columns
metadata[ , 1:2] 
# Data frame containing first, third and sixth rows
metadata[c(1,3,6), ] 
# Extract the celltype column for the first three samples
metadata[c("sample1", "sample2", "sample3") , "celltype"] 
# Check column names of metadata data frame
colnames(metadata)
# Check row names of metadata data frame
rownames(metadata)
# Extract the genotype column
metadata$genotype 
# Extract the first five values/elements of the genotype column
metadata$genotype[1:5]

### Exercise 
metadata[c("sample2", "sample8"), c("genotype", "replicate")] 
metadata$replicate[c(4,9)] 
metadata[, "replicate", drop = FALSE]

metadata$celltype == "typeA"
logical_idx <- metadata$celltype == "typeA"
metadata[logical_idx, ]
which(metadata$celltype == "typeA")
idx <- which(metadata$celltype == "typeA")
metadata[idx, ]
which(metadata$replicate > 1)
idx <- which(metadata$replicate > 1)
metadata[idx, ]
metadata[which(metadata$replicate > 1), ]
sub_meta <- metadata[which(metadata$replicate > 1), ]

### Exercise  
idx <- which(metadata$genotype=="KO")
metadata[idx, ]

list1[[2]]
comp2 <- list1[[2]]
class(comp2)
list1[[1]]
list1[[1]][1]

### Exercise  
random <- list(c(metadata, age, list1, samplegroup, number))
random[[4]]

names(list1)
# Name components of the list
names(list1) <- c("species", "df", "number")
names(list1)
# Extract 'df' component
list1$df

### Exercise 
names(random) <- c("metadata", "age", "list1", "samplegroup", "number")
random$age

