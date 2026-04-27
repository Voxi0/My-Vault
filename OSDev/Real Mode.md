---
tags:
  - osdev
---
Real mode refers to the 16-bit mode that is present on all x86 processors, even the modern ones. It was the first x86 design and was used by many early operating systems before [[Protected Mode]] came along. For compatibility reasons, a x86 CPU always begins execution in real mode.
## Compared to [[Protected Mode]]
### Pros
- The [[BIOS]] installs device drivers to control devices and handle [[Interrupts]]
- [[BIOS Functions]] provides the [[Operating System]] with an advanced collection of low-level API functions
- Memory access is faster due to the lack of descriptor tables to check combined with smaller registers
### Cons
- Only 1MB of RAM available for use
- No hardware-based memory protection (GDT) nor any virtual memory
- No builtin security mechanisms to protect against buggy/malicious programs
- The default CPU operand length is only 16-bits
- The memory addressing modes provided are more restrictive than other CPU modes
- Accessing more than 64KB of storage requires the use of [[Segment Registers]] which are difficult to work with
## Common Misconception
32-bit registers are still accessible even in real mode. Simply add the "Operand Size Override Prefix" (0x66) to the beginning of any instruction. Your [[Assembler]] is likely to do this for you, if you simply try to use a 32-bit register.