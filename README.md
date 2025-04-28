Not doing this

# libreframer
Simple C++ API that solves the buffer reframing problem: 
- Imagine a process A generating buffers of size variable size N an algorithm B consuming buffers of fixed size M. 
- We want to process the buffers of A using algorithm B. However, the incoming buffers are variably sized and (probably) do not fit within the fixed size buffers. 
- The solution is buffering. However, this can be tedious to program.
- This library offers a simple API to deal with this: namely, the `reframer::Reframer` class that takes a variable sized input buffer and returns the same number of output samples, automatically handling the buffering internally with minimal algorithmic latency.
