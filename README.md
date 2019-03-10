# R-Learning
## 01 Getting Help in R
## 02 installing & packages loading
## 03 Tips
## 04 Variables & Assignment
## 05 Factors & classes in R
## 06 R Loading
## 07 Dataframe
## 08 Return the names of the rows/columns/both:
## 09 To remove a column:
## 10 Debugging R Code:
## 11 File briefing:
## 12 Data edicting
## 13 dplyr:
## 14 R’s regular expressions
## 15 R scripts documenting
## 16 Saving R objects
## 17 Delete rows
## 18 Showing colname and change colname
## 19 add new row
## 20 getting certain rows or columns of a dataframe
## 21 exporting dataframe
## 22 compare dataframe A and B and find out the unique ones in A
## 23 aggregating the objects in the same column and add up the value in another column
## 24 sorting a column
## 25 Delete A Column Of A Data Frame In R Directly

## 01 Getting Help in R

    help("")
    ?("") # with an exact name in the branket
    help.search("") 
    ??"" # without an exact name but some indication
    example() # with an exact name in the branket
    library(help="") # with an exact package name, which helps listing all information of the choosing package
    
## 02 installing & packages loading

    install.packages("")
    install.packages("", repos = "http://cran.r-project.org")
    install.packages(file_name_with_path, repo = NULL, type = "source") #to install from the local
    library("package Name", lib.loc = "path to library")
    library("")
   
    
## 03 Tips

### 1. "Alt-" is the keystroke of "<-"
### 2. typeof() #to see an object's type
### 3. The downloaded source packages are in
	‘/tmp/Rtmp8YhId6/downloaded_packages’
### 4. learn more about magrittr ’s pipes in help('%>%')	

## 04 Variables & Assignment

    ls() # to see objects we've created in the global envirenment(.Global)
    
## 05 Factors & classes in R

    levels() # to view a factor's levels
    table() # to count how many of each level there are in a factor
    
## 06 R Loading

    getwd() # the present path
    setwd("") # to change the path
    read.table() #to read 逗号、分号或制表符分隔的数据
    read.csv() #to read CSV
    read.delim() #to read tab-delimited files
    scan() #读取数据框格式的数据
    data() #浏览数据列表和加载数据集（在学习函数使用方法或者新的包的时候，往往希望有实例数据对函数功能进行演示）
    load() #R以外的R软件格式数据
   
## 07 Dataframe

    nrow() #return the number of rows
    ncol() #return the number of columns
    dim()  #return the number of both rows and columns
    name_of_the_Data[, "name_of_the_column", drop=FALSE] # To return a dataframe with one column but not it's default behavior: to return a vector
 
## 08 Return the names of the rows/columns/both:

    colnames()
    rownames()
    dimnames()
    
## 09 To remove a column:

    name_of_the_vector_or_dataframe_or_list$name_of_the_column <- NULL

## 10 Debugging R Code:

    browser()
    options(error=recover) #options(error=NULL)
    debug()
    recover()
    
## 11 File briefing:

    head()
    tail()
    str() #structure
    ls.str()
    
## 12 Data edicting

    data.,entry()
    fix()
    rm()
    write.table()
	
## 13dplyr:

    tbl_df() #a simple class that wraps dataframes so that they don’t fill your screen when you print them (similar to using head()).
    arrange()
    filter()
    mutate()
    select()
    summarize() #dplyr’s summarize() handles passing the relevant column to each function and automatically creates columns with the supplied argument names.
    
## 14 R’s regular expressions： 

    grep() #related to Pearl
    regex()
    regexpr()

## 15 R scripts documenting:

    Rmarkdown
    knitr
### Scripts should not use setwd() to set their working directory, as this is not portable to other systems (which won’t have the same directory structure). 
### For the same reason, use relative paths like data/achievers.txt when loading in data, and not absolute paths like /Users/jlebowski/data/achievers.txt. 
### Also, it’s a good idea to indicate (either in comments or a README file) which directory the user should set as their working directory.
### Alternatively, we can execute a script in batch mode from the command line with:

    Rscript --vanilla my_analysis.R
    
### I recommend using --vanilla because by default, Rscript will restore any past saved environments and save its current environment after the execution completes. Usually we don’t want R to restore any past state from previous runs, as this can lead to irreproducible results (because how a script runs depends on files only on your machine).

## 16 Saving R objects:

    save()
    savehistory() # save.history() has saved your skin a few times when I’ve needed to record past interactive work right before a server has crashed.
    save.image()

## 17 Delete rows
	myData <- myData[-c(2, 4, 6), ]

## 18 Showing colname and change colname

	colnames(a)
	colnames(a)[1]
	conames(a) [1] <- "name_want_to_change"

## 19 add new row
	newrow <- data.frame(V1 = 'Others', V2 = 100 - colSums(Control_1887322136[2]))
	
## 20 getting certain rows or columns of a dataframe
	df[1:4,]
	
## 21 exporting dataframe
	write.table(exportingdataframe, "/path/of/the/exportingdataframe")
	
## 22 compare dataframe A and B and find out the unique ones in A
	setdiff(dataframe_A, Dataframe_B)
	
## 23 aggregating the objects in the column A and add up the value in another column
	aggregate(. ~ A, Control_pathabundance, sum)	
	
## 24 sorting a column
	dataframe[order(dataframe$thesortingcolumn), ]
	
## 25 Delete A Column Of A Data Frame In R Directly
	dataframe$columnyouwanttodelete -> NULL	
	
	
	
    
