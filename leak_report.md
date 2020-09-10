# Leak report

# How do memory leaks happen
  One way that memory leaks can happen is that you can allocate memory that you never free up again. 
  This can happen in c when a function allocates bytes to a pointer, but there is not way of accessing that pointer again so the memory is practically lost.
 
# How I fixed the memory leak in check whitespace.c
  A function allocated memory to a variable on line 41 in check whitespace.c so in response I freed the memory before the method had time to return the data.
  By doing free(result); after the function allocates data to a pointer called result I freed the data so that the memory be available to use again.  
