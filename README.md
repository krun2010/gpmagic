# gpmagic  
旨在分享  

使用备份恢复命令，请将  
gpddlbackup  
gpddlrestore  
gpmcbackup  
gpmcrestore  
四个文件直接拷贝到$GPHOME/bin/目录下，修改owner为gpadmin和mod为755：  
[gpadmin@mdw ~]$ cd $GPHOME/bin  
[gpadmin@mdw bin]$ chown gpadmin. gp{mc,ddl}*  
[gpadmin@mdw bin]$ chmod 755 gp{mc,ddl}*  
使用说明可以参考命令的help信息和word文档  

使用跨集群数据传输命令，请将  
gpdbtransfer
文件直接拷贝到$GPHOME/bin/目录下，修改owner为gpadmin和mod为755：  
[gpadmin@mdw ~]$ cd $GPHOME/bin  
[gpadmin@mdw bin]$ chown gpadmin. gpdbtransfer  
[gpadmin@mdw bin]$ chmod 755 gpdbtransfer  
使用说明可以参考命令的help信息和word文档  
