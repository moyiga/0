###内存操作系统(RAMOS)是全内存运行，启动后不依赖硬盘的Windows系统。它的原理是利用特殊的软件把多余的内存虚拟为内存盘，然后将制作好的操作系统镜像释放到这个虚拟内存盘中运行，让Windows操作系统和应用软件完全工作于内存之中，从而让操作系统和应用软件获得极快的打开和运行速度，因为操作系统和软件全部是在内存中运行的，所以重启后针对系统盘的操作都会被还原，避免了病毒和恶意软件对系统的损坏，但也可以对操作系统和软件进行热备份操作，确保对操作系统和软件的设置及安装重启生效。
常规的情况下如果要安装多系统，我们不但要为新系统规划安装分区，还要维护它，而多系统的维护也是一个让人头痛的问题。而RAMOS就是一个或多个镜像文件，可以放在本机的任意位置，因此非常便于维护和管理。比如可以在预装Windows 7电脑上安装RAM Windows XP(以下简称RamXP)组成双系统(当然也可以制作RamWin7)。只要你愿意，安装再多的系统也没关系，而且只要删除镜像文件就可以完成卸载。
由于网络安全形势严峻，即使安装杀毒软件也可能会中毒。由于RAMOS在内存中运行，而内存在电脑重启或断电后不会保存任何数据，因此即使RAMOS中毒了，重启后也可以自动复原，所以可以说，RAMOS是永不中毒的“金刚系统”!比影子系统快至少十倍，现在硬盘的速度是系统瓶颈，机械硬盘速度20-120MB/S，SATA-SSD速度550MB/S，NVME-SSD速度3000MB/S很不错了，RAMOS速度随便3000-6000MB/S。
RAMOS的优缺点：
现在的电脑磁盘性能是整机的瓶颈，由于内存读写速度比普通硬盘快，因此RAMOS的运行速度也就更快，而且成功加载到内存后，可以脱离本机硬盘运行，极大地提升计算机性能。因此对于此类用户，使用RAMOS不仅可以提高运行速度，而且还可以大大提高电池续航能力(硬盘耗电量远比内存大)。把系统装进内存，可轻轻松松秒各类优化软件，也可断盘高速运行。任一模式都比顶级的ssd更快，效率更高。好处是体验飞一般的感觉，永远极速，永远秒开，用十年还是这个速度，自带重启恢复的技能，也不怕病毒干扰；坏处是要想畅爽，需要投入一个价值250元的8G内存条。4GB可尝试，要想更爽需要加内存。内存太小是玩不转RAMOS的，比如你在资源管理器里面复制粘贴一个4GB的大文件，复制的时候不占用内存，粘贴的时候占用的内存是逐渐增加的，windows系统有缓存机制，我测试过第一次粘贴一个4GB的文件，内存占用逐渐增大，最大达到要2GB左右；第二次粘贴，占用的内存更多，最大占用大概2.3GB内存（取决于硬盘写入速度，如果粘贴到内存盘则一次性占用4GB），当然文件拷贝结束后内存占用会恢复。那么你内存小的话在正常系统中拷贝文件都需要借助虚拟内存不断地闪转腾挪，你又怎么能够玩得转RAMOS？还有看网络视频、解压缩的情况也是类似的。所以不推荐内存太小的用户玩RAMOS，玩不转反而会说RAMOS不好用，没条件的还是不要硬上了。
4-6GB可用体验 8GB内存是温饱，16GB内存是小康，32GB内存是土豪。
(最完美的推荐方案-使用双路双U主机最完美，爽歪歪)
RAMOS的应用场景
        适用于对速度及性能有较高要求的个人极客用户，它可以代替影子系统、虚拟机，做各类测试也方便，可以跟正常系统一样使用，兼容性非常好，实现起来也非常方便。还适用于千兆网无盘RAMOS，无盘RAMOS客户机启动完毕后，不依赖服务器的支持，客户机和服务器之间网络没有必须的数据交换，服务器关闭后不影响下面的客户端的运行
SSD，拉莫斯速度对比，各种模式速度测试###
