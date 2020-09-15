#  Leak report

## Description of the memory leak
   One way that memory leaks can happen is that you can allocate memory that you never free up again, this memory leak is one of those situations.
   In the function strip on line 41 there is an assignment statement the is using calloc to assign a specific amount of charactors to the variable result.
   What causes the memory leak to happen is that after the function "is _clean" is done using the variable result, the charactors stored in result are never freed.
   The bytes that were used to store result cannot be used until the variable result is freed.  
 
## How I fixed the memory leak in check whitespace.c
   The function strip allocated memory to a variable on line 41 in check whitespace.c
   In response I freed the memory after the method "is _clean" had time to call strip function with the data.
   I used a if statement to make sure the cleaned variable is not equal to zero then,
   By doing free(cleaned); I freed the data so that the memory be available to use again.  
