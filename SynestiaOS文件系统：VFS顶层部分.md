文件系统是SynestiaOS内核的另一大组成部分，SynestiaOS实现了`VFS(Virtual File System)`，VFS可以理解为一个真实文件系统和用户进程之间的隔离层，也就是类和对象的关系，所以使用VFS，可以统一文件/目录的上层操作方法，而具体到某一处实现细节的时候，就可以由各个文件系统来完成。

VFS和系统调用直接关联，使得用户程序可以使用open()、read()、write()这样的系统调用，而不用去考虑文件系统的具体实现细节。SynestiaOS的系统调用遵循 `POSIX` 协议，用户程序可以利用标准系统调用对不同的文件系统、不同介质上的文件系统进行读写操作。

同时每种文件系统可以作为一个模块存在于SynestiaOS中，关于SynestiaOS的模块实现，请点击[这里]()。



















