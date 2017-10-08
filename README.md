# Awesome Cuda

This is a list of useful libraries and resources for CUDA
development.

## Presentations

* [Optimizing Parallel Reduction in CUDA](https://web.archive.org/web/20160729221949/https://docs.nvidia.com/cuda/samples/6_Advanced/reduction/doc/reduction.pdf) - In this presentation it is shown how a fast, but relatively simple, reduction
algorithm can be implemented.

* [CUDA C/C++ BASICS](https://www.olcf.ornl.gov/wp-content/uploads/2013/02/Intro_to_CUDA_C-TS.pdf) - This presentations explains the concepts of CUDA kernels,
memory management, threads, thread blocks, shared memory, thread
syncrhonization. A simple addition kernel is shown, and an optimized stencil
1D stencil kernel is shown.

* [Advanced CUDA - Optimizing to Get 20x
  Performance](https://www.nvidia.com/content/cudazone/download/Advanced_CUDA_Training_NVISION08.pdf) - This presentation covers: Tesla 10-Series Architecture, Particle
  Simulation Example, Host to Device Memory Transfer, Asynchronous
  Data Transfers, OpenGL Interoperability, Shared Memory, Coalesced
  Memory Access, Bank Conflicts, SIMT, Page-locked Memory, Registers,
  Arithmetic Intensity, Finite Differences Example, Texture Memory.

* [Advanced CUDA Webinar - Memory
  Optimizations](http://on-demand.gputechconf.com/gtc-express/2011/presentations/NVIDIA_GPU_Computing_Webinars_CUDA_Memory_Optimization.pdf) - This presentation covers: Asynchronous Data Transfers , Context
  Based Synchronization, Stream Based Synchronization, Events, Zero
  Copy, Memory Bandwidth, Coalescing, Shared Memory, Bank Conflicts,
  Matrix Transpose Example, Textures.

* [Better Performance at Lower
  Occupancy](http://www.nvidia.com/content/GTC-2010/pdfs/2238_GTC2010.pdf) - Excellent presentation where it is shown that we can achieve better
  performance by assigning more parallel work to each thread and by using
  Instruction-level parallelism. Covered topics are:
  Arithmetic Latency, Arithmetic Throughput, Little's Law,
  Thread-level parallelism(TLP), Instruction-level parallelism(ILP),
  Matrix Multiplication Example.

* [Fun With Parallel Algorithms. Segmented Scan. Neutral territory method](http://www.cs.cmu.edu/afs/cs/academic/class/15418-s12/www/lectures/24_algorithms.pdf) - In these slides, it is shown how a segmented scan can easily be implemented using a variation of a normal scan.

* [GPU/CPU Programming for Engineers - Lecture 13](http://www.ce.jhu.edu/dalrymple/classes/602/Class13.pdf) - This lecture provides a good walkthrough of all the different memory types: Global Memory, Texture Memory, Constant Memory, Shared Memory, Registers and Local Memory.  

## Libraries

* [Thrust](https://github.com/thrust/thrust) - A parallel algorithms library whose main goal is programmer productivity and
  rapid development. But if your main goal is reaching the best
  possible performance, you are advised to use a more low-level
  library, such as CUDPP or chag::pp.

* [Hemi](https://github.com/harrism/hemi) - A nice little utility library that
 allows you to write code that can be run either on the CPU or GPU,
 and allows you to launch C++ lambda functions as CUDA kernels. Its
 main goal is to make it easier to write portable CUDA programs.

* [CUDPP](https://github.com/cudpp/cudpp) - A library that provides 15
  parallel primitives. In difference to Thrust, CUDPP is a more
  performance oriented library, and it is also much more
  low-level. Recommended if performance is more important than
  programmer productivity.

* [Parallel Primitives Library: chag::pp](https://newq.net/archived/www.cse.chalmers.se/pub/pp/) - This
  library provides the parallel primitives Reduction, Prefix Sum,
  Stream Compaction, Split, and Radix Sort. The authors have
  [demonstrated](https://newq.net/archived/www.cse.chalmers.se/pub/pp/stream_compaction_pres.pdf)
  that their implementation of Stream Compaction and Prefix Sum are
  the fastest ones available!

## Papers

* [Multireduce and Multiscan on Modern GPUs](http://hiperfit.dk/pdf/marco-eilers-thesis.pdf) - In this
  master's thesis, it is examined how you can implement an efficient
  Multireduce and Multiscan on the GPU.

* [Efficient Parallel Scan Algorithms for Many-core GPUs](http://www.idav.ucdavis.edu/publications/print_pub?pub_id=1041) - In this paper, it is shown how the scan and segmented scan algorithms
  can be efficiently implemented using a divide-and-conquer approach.

* [Ana Balevic's homepage](http://tesla.rcub.bg.ac.rs/~taucet/coding.html) - Ana Balevic has done research in implementing compression
  algorithms on the GPU, and in her publications she describes fast
  implementations of RLE, VLE(Huffman coding) and arithmetic coding on
  the GPU.

* [Run-length Encoding on Graphics
  Hardware](https://www.cs.uaf.edu/media/filer_public/2013/08/27/ms_cs_ruth_rutter.pdf) - Shows another approach to implementing RLE on the GPU. In
  difference to Ana Belvic's fine grain parallelization approach, this
  paper describes an approach where the data is split into blocks,
  and then every thread is assigned a block and does RLE on that block.

* [Efficient Stream Compaction on Wide SIMD Many-Core Architectures](http://www.cse.chalmers.se/~uffe/streamcompaction.pdf) - The paper that the chag::pp library is based on.

* [Histogram calculation in CUDA](http://developer.download.nvidia.com/compute/cuda/1.1-Beta/x86_website/projects/histogram64/doc/histogram.pdf) - This article explains how a histogram can be calculated in CUDA.

* [Modern GPU](https://nvlabs.github.io/moderngpu/index.html) - Modern GPU
is a text that describes algorithms and strategies for writing fast
CUDA code. And it also provides a library where all of the explained
concepts are implemented.

## Articles

* [GPU Pro Tip: Fast Histograms Using Shared Atomics on
Maxwell](https://devblogs.nvidia.com/parallelforall/gpu-pro-tip-fast-histograms-using-shared-atomics-maxwell/) - In this article, it is shown how an even faster histogram
calculation algorithm can be implemented.

* [Faster Parallel Reductions on
Kepler](https://devblogs.nvidia.com/parallelforall/faster-parallel-reductions-kepler/) - It is shown in this article how the reduction algorithm described by [Mark
Harris](https://docs.nvidia.com/cuda/samples/6_Advanced/reduction/doc/reduction.pdf)
can be made faster on Kepler.

* [GPU Pro Tip: Fast Histograms Using Shared Atomics on Maxwell](https://devblogs.nvidia.com/parallelforall/gpu-pro-tip-fast-histograms-using-shared-atomics-maxwell/) - It is shown how we can use shared memory atomics to implement a faster histogram implementation on Maxwell.

## Videos

* [Intro to Parallel Programming CUDA -
  Udacity](https://www.youtube.com/playlist?list=PLGvfHSgImk4aweyWlhBXNF6XISY3um82_) - An Udacity course for learning CUDA.

## Contributing

This list is still under construction and is far from done. Anyone who
wants to add links to the list are very much welcome to do so by a
pull request!

