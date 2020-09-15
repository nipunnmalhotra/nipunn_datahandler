This package helps in handling missing data values.
Package has various functions to handle the missing data.

Function 1

1.guess_and_fill(input_file)

Function guesses missing values and fills them
    
Arguments:
        input_file : Name of the file to be used
        
        returns: dataset after filling missing values by guessing
        
        **Note: The first coloumn is considered as index and discarded

Function first removes the rows containing missing values and then trains the regressor based on the left data and uses the trained regressor to predict missing values.
**Random Forest Regressor is used.

2.replace_rows(input file,method='backforth')

 Function return dataframe after filling missing values in given file
    by choosen method.
    
    It requires following arguments:
    
    1. input_file : Name of the file    
    
    2. method (Default: backforth): method to fill the missing values
        
        a. mean : takes mean of the coloumn and fills the missing value
        b. mode : takes mode of the coloumn and fills the missing value
        c. median : takes median of the coloumn and fills the missing value
        d. asprevious : fills the value same as previous (remains missing if no value is at previous)
        e. asforward : fills the value same as forward (remains missing if no value is at forward)
        f. backforth : fills the value as mean of forward and backward value (chooses forward value if no backward value is present and vice versa)
    
    returns: dataset after filling missing values by chosen method
    
    **Note: The first coloumn is considered as index and discarded

3. remove_rows(input_file,p=True)

 Function removes rows with missing values
    
    Arguments:
        1.input_file : Name of the file to be used
        
        2.print(bool,default: True): Print number of rows removed or not
        
        returns: dataset after removing rows with missing values
    
    **Note: The first coloumn is considered as index and discarded

