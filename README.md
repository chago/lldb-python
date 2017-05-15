

Start `Debugserver` and `LLDB`，attatch the process you want to debug.

## How to use

#### 1. Import the scripts

`command script import ~/Path/To/objc_msgSend.py`

`command script import ~/Path/To/objc_msgSend.py`

Also, you can put these command above into the file `~/.lldbinit` .


#### 2. Use the imported Debugger commands

`(lldb) help`

```
Current user-defined commands:
  iaslr                 -- Print specified module ASLR.
  ibreak                -- Set specified module breakpoint plus ASLR.
  ievaluate_instruction -- Evaluate current instruction.
  ifaddress             -- Get specified module breakpoint minus ASLR.
  iobjc_msgSend         -- Break at next objc_msgSend.
  iprint_arguments      -- Print current objc_msgSend arguments.
  iraddress             -- Get specified module breakpoint minus ASLR.
  ishow_disassemble     -- Show current disassemble instructions.
```

`(lldb) process interrupt`

`(lldb) iaslr`

`(lldb) iaslr UIKit`

`(lldb) ibreak 0x00000001014479F4 WeChat`		// 00000001014479F4 Copied from IDA

`(lldb) iobjc_msgSend`

`(lldb) ishow_disassemble`


#### 3. Tips

Full enter the commad characters is not necessary , use the `Tab` keyboard key. Take `iobjc_msgSend` as an example:

`(lldb) io + [Tab] + [Enter]`

or if just only one command with prefix `io`:

`(lldb) io + [Enter]`

