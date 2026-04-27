---
tags:
  - osdev
---
The Basic Input/Output System (BIOS) is a crucial piece of software that initializes the hardware components of a system during the boot process.

It performs a Power-On Self-Test (POST) which is a crucial, automated diagnostic sequence immediately upon powering on to verify that essential hardware e.g. the CPU, memory, storage, and controllers are functioning properly before loading the [[Operating System]].

It was created to offer generalized low-level services to early system programmers. It was designed primarily to make [[Operating System]] and application development easier since BIOS services handled most of the hardware-level interface. If a component fails, the POST sends an error signal to the BIOS, which may display a message or beep. A failed POST often results in a blank screen, a Blue Screen of Death (BSOD), or specific beep codes.

These BIOS services are still used especially during boot-up and are often referred to as "BIOS functions". In [[Real Mode]], they can be easily accessed through software [[Interrupts]] using the Assembly language. A list of these functions can be found [here](https://wiki.osdev.org/Ralf_Brown%27s_Interrupt_List).