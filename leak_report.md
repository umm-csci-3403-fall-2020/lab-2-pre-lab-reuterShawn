# Leak report

 One way that memory errors can happen is that you can allocate memory that you never free up again. 
 This can happen in c when a function allocates bytes to a pointer that there is no other way of accessing that memory again.
 This happened on line 41 in checkwhitespace.c so in response I used freeded the memory before the method had time to return the data. 
 This way the memory the memory will be available to use again.  
