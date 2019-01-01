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
可能会出现Master和Standby都活着的冲突状态，
目前进行了进一步强化，常规的Master状态判断使用pg_sleep进行长时间保持，    
如果第一次检测到异常，将会马上再进行3次简单测试，只有4次都异常才认为Master访问异常，   
这一机制的完善主要用于避免可能出现检测SQL被误杀的情况，    
对于出现连接数超过限制的情况，将认为数据库状态是正常的，不会予以切换    
    
gpddlbackup可能还有不足之处，如果在使用过程中有异常退出现象，请联系本人修正    
    
    
