These libraries fall into two categories: (1) C/C++ libraries that makes use of
SIMD or other specialized instructions, (2) Node.js libraries that provide
fast implementations one way or another (SIMD or just careful optimization).

Submissions welcome!

* [base64](https://github.com/aklomp/base64) - **Base64 encoding/decoding**.  
  Type: C99 library.  
  Node.js bindings: https://github.com/lovell/64
  ISA: SSSE3, SSE4.1, SSE4.2, AVX, AVX2, NEON; OpenMP.  

* [bswap](https://github.com/zbjornson/node-bswap) - **Byte-swapping** faster than
  Node.js's built-in `Buffer.swap16/32/64()`.  
  Type: Node.js module.  
  ISA: SSSE3, AVX2, AVX512, NEON.

* [fast-hex](https://github.com/zbjornson/fast-hex) - **Hex encoding/decoding**.  
  Type: C++ header and Node.js module.  
  ISA: AVX2.

* [ISA-L](https://github.com/01org/isa-l) - **crc, erasure coding and deflate** in the Intel Intelligent Storage Acceleration Library (ISA-L)].  
  Type: C and assembly.  
  Node.js bindings: https://github.com/primitybio/node-isal  
  ISA: Runtime dispatch using up to AVX-512

* [levenshtein-sse](https://github.com/addaleax/levenshtein-sse) - **Levenshtein distance**.  
  Type: C++ header.  
  ISA: SSSE3, SSE4.1, AVX2

* [libjpeg-turbo](https://github.com/libjpeg-turbo/libjpeg-turbo) - **JPEG library**.  
  Type: C library.  
  ISA: MMX, SSE2, AVX2, NEON, AltiVec.

* Ivan Dimokvic's implementation of **MWC1616 pseudo-random number generator**. His original code post is no longer online, but a version of it is here: https://github.com/andeplane/MWC1616-PRNG-CPP.  
  Type: Originally C, that repo is C++.  
  ISA: SSE or SSE4. (In my benchmarks on a Skylake processor, the SSE implementation is faster than the SSE4 implementation.)

* [sse-popcount](https://github.com/WojciechMula/sse-popcount) - A few dozen implementations of **population counting**.  
  Type: C++ implementations with benchmarks.  
  ISA: SSE, SSSE3, AVX2, AVX512 or NEON

* [sse4_crc32](https://github.com/anandsuresh/sse4_crc32) and its wrapper with JS-fallback [fast-crc32c](https://github.com/ashi009/node-fast-crc32c) - **CRC32C calculation** for buffers.  
  Note: ISA-L (above) is up to ~3.4x faster.  
  Type: Node.js module.  
  ISA: SSE4.2.

* [turbo-net](https://github.com/mafintosh/turbo-net) - Low-level **TCP** library faster than Node.js's core TCP module.  
  Type: Node.js module.  
  ISA: Generic.

* [volk](https://github.com/gnuradio/volk) - Librarary of vector-optimized **kernels**. A lot of these look like they will be memory throughput-limited, but they show how to do various tasks if you want to combine them to make your own fast functions.  
  Type: C.  
  ISA: Various (looks like up to AVX2).
