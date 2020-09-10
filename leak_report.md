# Leak report

# How do memory leaks happen
  One way that memory leaks can happen is that you can allocate memory that you never free up again. 
  This can happen in c when a function allocates bytes to a pointer, but there is not way of accessing that pointer again so the memory is practically lost.
 
# How I fixed the memory leak in check whitespace.c
  The function strip allocated memory to a variable on line 41 in check whitespace.c
  In response I freed the memory after the method isCleaned  had time to call strip function with the data.
  I used a if statement to make sure the cleaned variable is not equal to zero then,
  By doing free(cleaned); I freed the data so that the memory be available to use again.  
