## Linux文件系统
<B>发行版本历程：</B>  
ext -> ext2 -> ext3 -> ext4 (extended file system)  
(windows 采取 NTFS 文件系统 New Technology File Syetem)

## 磁盘分区与目录
Linux 必须要有三个分区：
1. 根分区(/):操作系统的核心组件和文件；
2. Boot/EFI 系统分区(/boot): BIOS 启动需要 Boot 分区，UEFI 需要 EFI 系统分区，存储引导加载程序、内核映像文件和引导配置文件；
3. swap分区：用于扩展系统的虚拟内存，以应对物理内存不足的情况；  
   (home 目录即使不创建，根目录下仍存在；在 Linux 中，该存在的目录该有还是有，只是没有将目录挂载到指定分区下的就默认这根分区下了)
