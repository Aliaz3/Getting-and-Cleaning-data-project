# Getting-and-Cleaning-data-project
Coursera Getting and Cleaning Data project
required libraries 
'data.table'
Version 1.10.4
Title Extension of `data.frame`
Depends R (>= 3.0.0)
Description Fast aggregation of large data (e.g. 100GB in RAM), fast ordered
joins, fast add/modify/delete of columns by group using
no copies at all, list columns, a fast friendly file reader and parallel file writer. Offers a natural
and flexible syntax, for faster development.
Function used: as.data.table Coerce to data.table
as.data.table is a generic function with many methods, and other packages can supply further
methods.
If a list is supplied, each element is converted to a column in the data.table with shorter elements
recycled automatically. Similarly, each column of a matrix is converted separately.
character objects are not converted to factor types unlike as.data.frame.
If a data.frame is supplied, all classes preceding "data.frame" are stripped. Similarly, for
data.table as input, all classes preceding "data.table" are stripped. as.data.table methods
returns a copy of original data. To modify by reference see setDT and setDF.
keep.rownames argument can be used to preserve the (row)names attribute in the resulting data.table.

‘reshape2'
Version 1.4.2
Author Hadley Wickham <h.wickham@gmail.com>
Maintainer Hadley Wickham <h.wickham@gmail.com>
Description Flexibly restructure and aggregate data using just two
functions: melt and 'dcast' (or 'acast').
URL https://github.com/hadley/reshape
Function used: melt Convert an object into a molten data frame.
Description
This the generic melt function. See the following functions for the details about different data
structures:
Usage
melt(data, ..., na.rm = FALSE, value.name = "value")
Arguments
data Data set to melt
... further arguments passed to or from other methods.
na.rm Should NA values be removed from the data set? This will convert explicit
missings to implicit missings.
value.name name of variable used to store values
Details
• melt.data.frame for data.frames
• melt.array for arrays, matrices and tables
• melt.list for lists

To load the files I used the read.table function, get the features, activity_labels and the X,Y and subject file from the dowloaded zip and stored them in tables.

used grep to get the features that interest us like mean or std from features table and join them with the X tables.

also combine the Y tables with the activity label to get the activity for each ID.

then named the variables in each table most of them with the features names

column binded the test and the train data first X,Y,Subject for each and then both of them in a row bind getting an endata almost tidy

added the labels and melt the data to get the tidy data set and finaly write it to a txt file with write.table


