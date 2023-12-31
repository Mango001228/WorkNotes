# Linux内核
<div>
  <img src="https://github.com/Mango001228/WorkNotes/blob/Main-Learning/markdown_Picture/linux%E7%BB%93%E6%9E%84.png" width="700"/>
</div>

1. 最内层是硬件，最外层是用户常用的应用，比如firefox游览器、evolution查看游览器；
2. **硬件**是物质基础，而**应用**提供服务，这两者之间还需要经过一番周折
3. Linux启动时，首先启动**内核**(kernel)，内核是一段计算机程序，这个程序直接管理硬件，包括CPU、内存空间、硬盘接口、网络接口等等，所有计算机操作都要通过内核传递给硬件。
4. linux将内核的功能接口制作成**系统调用**(system call),系统调用看起来就像C语言的函数，可以在程序中直接调用，linux系统中有两百多个这样的系统调用.
   - 系统调用是操作系统的最小功能单位
   - 用户不需要了解内核的复杂结构，就可以使用内核
   - man 2 syscalls && man 2 read  查看系统所有的调用 && 查看系统调用read()的说明
   - 系统调用提供的功能非常基础，使用起来麻烦，而库函数中有设置好的便于我们使用-功能的集成

## Shell
命令行工具，通过shell解释，接着通过系统调用，指挥内核，实现具体的重定向等活动。
- shell可编程
- shell 充当了小功能之间的“胶水”，让不同的程序能够协同工作
- shell种类很多，最常见为bash，另外还有sh、csh、tcsh、ksh
- 一个shell对应一个终端(terminal)，图形化的窗口

**Unix哲学：让每个程序尽量独立的做好一个小的功能**

- Linux利用内核实现软硬件的对话
- 通过系统调用的这个接口，Linux将上层的应用与下层的内核分离，隐藏了底层的复杂性，提高了上层应用的可移植性
- 库函数利用系统调用创造出模块化的功能
- shell提供用户界面，可以使用shell的语法编写脚本，以整合程序
