# Virtual Memory Concepts

## Overview

This directory contains documentation about fundamental virtual memory concepts that apply across different operating systems. Virtual memory is a memory management technique that provides an abstraction layer between applications and physical memory, enabling efficient memory usage, protection, and sharing.

## Available Documentation

The following PDF resources are available in this directory:

- **ch9.pdf**: Comprehensive chapter on virtual memory fundamentals [[click here]](./documentation/linux/README.md)
- **CSE351-L02-memory-I_17wi.pdf**: University course materials on memory basics [click here](./documentation/linux/README.md)
- **Lecture21.pdf**: Academic lecture on virtual memory implementation [click here](./documentation/linux/README.md)
- **Lecture_2_Addressing_Data_in_Memory_Microprcessor-Design.pdf**: Memory addressing in modern processors [click here](./documentation/linux/README.md)
- **Operating System Virtual Memory.pdf**: OS-level virtual memory implementation [click here](./documentation/linux/README.md)
- **os_virtual_memory.pdf**: Alternative perspective on OS virtual memory [click here](./documentation/linux/README.md)
- **publication_3_22584_1575.pdf**: Research publication on virtual memory optimization [click here](./documentation/linux/README.md)

## Core Virtual Memory Concepts

### Memory Address Translation

- **Virtual Address**: Memory address as seen by processes
- **Physical Address**: Actual hardware memory location
- **Translation Lookaside Buffer (TLB)**: Cache for address translations
- **Page Tables**: Data structures mapping virtual addresses to physical addresses

### Paging

- **Page**: Fixed-size block of memory (typically 4KB to 64KB)
- **Page Frame**: Physical memory unit corresponding to a page
- **Page Fault**: Exception raised when accessed memory isn't in physical RAM
- **Demand Paging**: Loading pages into memory only when needed

### Memory Protection

- **Protection Bits**: Read/Write/Execute permissions
- **Rings/Privilege Levels**: Separation between user/kernel modes
- **Memory Isolation**: Preventing processes from accessing each other's memory
- **Shared Memory**: Controlled sharing of memory between processes

### Page Replacement Algorithms

- **Least Recently Used (LRU)**: Removes pages that haven't been used for longest time
- **First-In-First-Out (FIFO)**: Removes oldest pages first
- **Clock Algorithm**: Approximation of LRU with lower overhead
- **Working Set Model**: Tracks active memory pages a process needs

## GPU Virtual Memory

### CUDA Virtual Memory Management

- **Virtual Address Reservation**: Pre-allocating virtual address space for GPU operations
- **Physical Memory Allocation**: Allocating GPU memory with specific alignment requirements
- **Memory Mapping**: Connecting virtual addresses to physical GPU memory
- **Access Control**: Setting permissions for GPU memory regions
- **Memory Release**: Properly deallocating GPU memory resources

## Additional Resources

### Online Resources

- [CUDA Virtual Memory API Guide](https://developer.nvidia.com/blog/introducing-low-level-gpu-virtual-memory-management/)
- [MIT's Operating Systems Engineering Course](https://ocw.mit.edu/courses/6-828-operating-system-engineering-fall-2012/)
- [Berkeley's CS162: Operating Systems Course](https://cs162.org/)
- [Stanford's CS140: Operating Systems Course](https://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/index.php)
- [VMware's Virtual Memory Resource Management Guide](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.resmgmt.doc/GUID-1C2784AD-D855-4FEB-A26F-88F304E21BC3.html)

### Books

- "Operating Systems: Three Easy Pieces" - Remzi H. Arpaci-Dusseau and Andrea C. Arpaci-Dusseau
- "Modern Operating Systems" - Andrew S. Tanenbaum
- "Computer Architecture: A Quantitative Approach" - John L. Hennessy and David A. Patterson
- "Windows Internals" - Mark E. Russinovich, David A. Solomon, and Alex Ionescu
- "Understanding the Linux Kernel" - Daniel P. Bovet and Marco Cesati

## Key Comparisons

### Virtual Memory Across Platforms

| Feature | Linux | Windows | macOS |
|---------|-------|---------|-------|
| Page Size | 4KB default (configurable) | 4KB (small) / 2MB (large) | 4KB (base) / 16KB (ARM) |
| Address Space | User/Kernel split | User/Kernel split | User/Kernel split |
| Swapping | Swap partitions/files | Page files | Swap files |
| Large Pages | Huge pages | Large pages | Superpage support |
| Memory Pressure | kswapd | Working Set Manager | Memory pressure handler |

### Historical Evolution

- Early systems with no virtual memory
- Introduction of segmentation
- Development of paging systems
- Modern combined approaches
- Future directions in memory management
