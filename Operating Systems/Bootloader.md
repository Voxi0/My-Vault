**Tags: #programming #os**
A piece of software responsible for booting a computer and then an [[Operating System]]. If it also provides an interactive menu allowing you to choose which [[Operating System]] to boot then it's often also called a boot manager.

It basically brings the [[Kernel]] and everything else it needs to bootstrap into memory, provides the [[Kernel]] with the information that it needs to work correctly, switches to the proper environment for the [[Kernel]] and finally, transfers control over to the [[Kernel]].
## Design
Virtually any bootloader follows a common design. Note that on x86 machines, you are usually limited to 512 bytes for a first stage bootloader. Most of this space will be dedicated to [[BIOS]] structures and [[FAT]] headers leaving even less space to work with.
- **Single-Stage:** Consists of a single file that's loaded entirely by the [[BIOS]].
- **Two-Stage:** Consists of two bootloaders after one another. The first one is only for loading the second one. The second one can then contain all the code needed to load the [[Kernel]].
- **Mixed:** A bootloader that's split into two parts where the first half (512 bytes) can load the rest. This can be achieved by inserting a 512 bytes break in the assembly code, making sure that the rest of the bootloader is put after the boot sector.