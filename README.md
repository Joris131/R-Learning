# R-Learning

## Getting Help in R

    help("")
    ?("") # with an exact name in the branket
    help.search("") 
    ??"" # without an exact name but some indication
    example() # with an exact name in the branket
    library(help="") # with an exact package name, which helps listing all information of the choosing package
    
## installing & packages loading

    install.packages("")
    install.packages("", repos = "http://cran.r-project.org")
    install.packages(file_name_with_path, repo = NULL, type = "source") #to install from the local
    
    library("package Name", lib.loc = "path to library")
    library("")
   
    
## Tips

1. "Alt-" is the keystroke of "<-"
2. typeof() #to see an object'type
3. The downloaded source packages are in
	‘/tmp/Rtmp8YhId6/downloaded_packages’

## Variables & Assignment

    ls() # to see objects we've created in the global envirenment(.Global)
    
## Factors & classes in R

    levels() # to view a factor's levels
    table() # to count how many of each level there are in a factor
    
## R Loading

    getwd() # the present path
    setwd("") # to change the path
    
    read.table() #to read 逗号、分号或制表符分隔的数据
    read.csv() #to read CSV
    read.delim() #to read tab-delimited files
    scan() #读取数据框格式的数据
    
    data() #浏览数据列表和加载数据集（在学习函数使用方法或者新的包的时候，往往希望有实例数据对函数功能进行演示）
    
    load() #R以外的R软件格式数据
   
## Dataframe

    nrow() #return the number of rows
    ncol() #return the number of columns
    dim()  #return the number of both rows and columns
    name_of_the_Data[, "name_of_the_column", drop=FALSE] # To return a dataframe with one column but not it's default behavior: to return a vector
 
### Return the names of the rows/columns/both:

    colnames()
    rownames()
    dimnames()
    
## To remove a column:

    name_of_the_vector_or_dataframe_or_list$name_of_the_column <- NULL

## Debugging R Code:

    browser()
    options(error=recover) #options(error=NULL)
    debug()
    recover()
    
## File briefing:

    head()
    tail()
    str() #structure
    ls.str()
    
## Data edicting

    data.,entry()
    fix()
    rm()
    
    write.table()
   
    
