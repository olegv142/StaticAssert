# StaticAssert

The static assertion macro provide the means for checking certain condition at compile time.
Consider the example. You are using some structure and your code rely on the fact that its size
does not exceed certain value. Just place the following line in your code

STATIC_ASSERT(sizeof(struct my_struct) <= MAX_SIZE)

the following version provides you with the more readable message on failure

STATIC_ASSERT2(sizeof(struct my_struct) <= MAX_SIZE, my_struct_size_valid)
