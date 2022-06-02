# Optimize LevelDB Options for Real-World Workload

## Twitter Cache Trace
This repository describes the traces from Twitter's in-memory caching ([Twemcache](https://github.com/twitter/twemcache)/[Pelikan](https://github.com/twitter/pelikan)) clusters. The current traces were collected from 54 clusters in Mar 2020. The traces are one-week-long. 
More details are described in the following paper and blog. 
* [Juncheng Yang, Yao Yue, Rashmi Vinayak, A large scale analysis of hundreds of in-memory cache clusters at Twitter. _14th USENIX Symposium on Operating Systems Design and Implementation (OSDI 20)_, 2020](https://www.usenix.org/conference/osdi20/presentation/yang).

## LevelDB Options
``` c++
// Memtable
size_t write_buffer_size = 4 * 1024 * 1024;

// SST
size_t max_file_size = 2 * 1024 * 1024;
size_t block_size = 4 * 1024;
int block_restart_interval = 16;
int max_open_files = 1000;

// Compression
CompressionType compression = kSnappyCompression;

// BloomFiliter
const FilterPolicy* filter_policy = nullptr;

// Cache
Cache* block_cache = nullptr;
bool fill_cache = true;
```
