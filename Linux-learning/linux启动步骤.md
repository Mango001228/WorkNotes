## Linux 启动
Linux 是如何启动的？
1. 当我们打开电源时，BIOS（基本输入/输出系统，Basic Input/Output System）或 UEFI（统一可扩展固件接口，Unified Extensible Firmware Interface）固件会从非易失性内存中加载，并执行 POST（开机自检，Power On Self Test）；
2. BIOS/UEFI 检测连接到系统的设备，包括 CPU、内存和存储设备；
3. 选择一个启动设备来启动操作系统。可以是硬盘、网络服务器或 CD ROM；
4. BIOS/UEFI 运行引导加载器 (GRUB)，它提供了一个选择操作系统或内核功能的菜单；
5. 内核准备就绪后，我们现在切换到用户空间。内核启动 systemd 作为第一个用户空间进程，负责管理进程和服务、探测所有剩余硬件、挂载文件系统并运行桌面环境；
6. 系统启动时，systemd 默认激活 default.target 单元。同时还会执行其他分析单元；
7. 系统运行一组启动脚本并配置环境；
8. 用户将看到一个登录窗口，系统现已准备就绪。
