# Topic
## 1. Compaction
- Policy: Leveled, Tiered
- Compaction Trigger
- Merge Iterator

## 2. WAL
- Log structure
- Flush, Recovery
- Operations: Put

## 3. Memtable
- Data Structure: Skiplist
- Memory Management: Arena
- Immutable Memtable, Flush
- Operations: Put, Get, Seek

## 4. SST file
- SST file format
- Index/Data Block format
- Two Level Iterator
- Operations: Get, Seek

## 5. Bloom Filiter
- Bloom Filiter Structure
- Flush, Compaction
- Operations: Get, Seek

## 6. Cache
- Cache Structure
- Index Block, Data Block
- Replacement Policy: LRU
- Operations: Get, Seek
