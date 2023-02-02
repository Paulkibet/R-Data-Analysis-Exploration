# R-Data Exploration and Visualization

#Using R for Data Exploration#



##Load the Iris Dataset##

#Metod 1#

library(datasets)
data("iris")

##Viewing iris##

View(iris)

##Method 2 using Rcurl##

install.packages("RCurl")

library(RCurl)

#Viewing variables in the Iris Dataset#

#Type iris$

iris$Sepal.Length
iris

#Assign a variable i.e Assignnspecies to Speciestype

iris$Species

Species <-iris$Species
Species


##Display Summary Statistics of the Data##


iris
View(iris)

##Display the first 4 and Last 4 line(Head/Tail)Function##

head(iris,6)
tail(iris,6)

summary(iris)
summary(iris$Species)


##Find if the dataset has missing values##

summary(is.na(iris))

#skimr expands on summary() by providing larger set of data statistics
install.packages("skimr")


library(skimr)

##Display skimr summary statistics

skim(iris)

##Group data by species

iris%>%
  dplyr::group_by(Species) %>%
  skim()


##Quick Data Visualization##

#Panel plots

plot(iris)
plot(iris, col= "red")

##scatter plot
plot(iris$Sepal.Width, iris$Sepal.Length)

plot(iris$Sepal.Width, iris$Sepal.Length, col= "blue") ##makes the color of the circles in the scatter plot blue


plot(iris$Sepal.Width, iris$Sepal.Length, col= "blue") ##makes the color of the circles in the scatter plot blue
    xlab = 'Sepal width', ylab = 'Sepal length'

##Histogram- this id the frequency of count
hist(iris$Sepal.Width)
hist(iris$Sepal.Width, col = "yellow") #makes the histogram bars red




