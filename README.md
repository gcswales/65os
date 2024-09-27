# 65os
A HACKABLE OPERATING SYSTEM FOR THE 65C02

For the last 18 months I have been working on an operating system for the 65C02 and as of writing this is it 80% complete.
Here is a brief description of the system, please feel free to comment.

It is a console based OS similar to DOS or CP/M but written from scratch to take advantage of the 65C02:-

* Requires about 2k of ROM and 512 bytes of RAM (page 2 & 3).
* Transient programs load from $0400 up.
* Hardware boots into BIOS which initialises peripherals then jumps to the OS.
* BIOS only needs to provide 4 simple calls; console get, console put, drive write, drive read.
* 16-bit custom filing system capable of addressing 16Mb of storage.
* Up to 8 files open simultaneously.
* Multiple drive partitions (A..Z) with drive labels ('OS', 'GAMES', etc).
* In-built commands; MON, PUT, DIR, DRV, REN, DEL, OS.
* Installable commands.
* Re-direct-able console; file or additional installed drivers.
* Installation of additional storage drivers; flash, ramdisk, etc.
* Relocatable loading to high-memory.
* Memory aware management; overwriting (commands) or protecting (driver).
* DOS style PATH drive for fall-back search.
* Nested Batch command processing.
* Autoexec batch file running on boot-up.
* Simple JMP table API.
* Comprehensive API fileIO, console, math, and number conversion.
* Memory mapped properties for customization.

...Now for the negatives:-

* Single tasking (doesn't bother me)
* Contiguous file allocation so does require periodic Trash collection
* Only 1 write file open at any time.
* No file appending.
* Simple text output (for now)
* Flat filing system; no directories.
* Relocatable files limited to a few pages in size.

...And possible future additions to take us up to 4k:-

* Command line history/recall
* VT52/100 support for text formatting & colour.
* Sound support?

As mentioned before the system is 80% complete. Many of the more advanced features are the result of interplay between other features. For example the batch file execution is a side-effect of redirecting the console input to a file. The ability to have multiple files open enables nested batch files. The installation of drivers/commands is only possible with relocatable loading.

For fear of sounding like an idiot; I have tried to make the OS work on several levels:-

* It needs to be fast to port; builders want to get their new SBC up and running quickly.
* It needs to be simple to use; it's not about the OS it's about playing games!
* It needs to be expandable; as you improve your system.
* It needs to be customisable; I'm an engineer so what do I know about style.
* It needs to be hackable; because this is just fun.
* it needs to be small/simple so 1 person can understand how everything works.

Please feel free to provide comments/feedback; I'm sick of guessing what people want!

Oh yes; it needs a name. I was thinking Minimal Operating System (MOS).

Bye,

Geoffrey.
