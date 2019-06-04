Write a function called rankhospital() that takes THREE (3) arguments: (a) the TWO(2)-character abbreviated name of a state (state); (b) an outcome (outcome); and © the ranking of a hospital in that state for that outcome (num). The function reads the outcome-of-care-measures.csv file and returns a character vector with the name of the hospital that has the ranking specified by the num argument. For example, the call:

rankhospital(“MD”, “heart failure”, 5)

would return a character vector containing the name of the hospital with the FIFTH (5th) LOWEST THIRTY(30)-day death rate for heart failure. The num argument can take values “best”, “worst”, or an integer indicating the ranking (SMALLER numbers are better). If the number given by num is LARGER THAN the number of hospitals in that state, then the function should return NA. The function should use the following template.

rankhospital <- function(state, outcome, num = "best") {                            
                  ## Read outcome data                                                
                  ## Check that state and outcome are valid                           
                  ## Return hospital name in that state with the given rank           
                  ## THIRTY(30)-day death rate                                        
  }                                                                                
Hospitals that do NOT have data on a particular outcome should be excluded from the set of hospitals when deciding the rankings.

If there is MORE THAN ONE (1) hospital for a given ranking, then the hospital names should be sorted in alphabetical order and the FIRST (1st) hospital in that set should be returned (i.e. if hospitals “b”, “c”, and “f” are tied for a given rank, then hospital “b” should be returned).

The function should check the validity of its arguments. If an invalid state value is passed to rankhospital(), the function should throw an error via the stop() function with the exact message “invalid state”. If an invalid outcome value is passed to rankhospital(), the function should throw an error via the stop() function with the exact message “invalid outcome”. The num variable can take values “best”, “worst”, or an integer indicating the ranking (SMALLER numbers are better). If the number given by num is larger than the number of hospitals in that state, then the function should return NA.

Save your code for this function to a file named rankhospital.R. To run the test script for this part, make sure your working directory has the file rankhospital.R in it.
