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

gpdbcluster命令暂未经过大规模验证    
建议慎重用于生产环境    
目前已经强化了Standby激活的逻辑，如果无法判断Master的状态就不切换，    
因为，如果gpactivatestandby命令本身也无法判断Master状态的话，    
可能会出现Master和Standby都活着的冲突状态    
    
    
    
    
