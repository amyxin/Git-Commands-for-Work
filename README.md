# git命令日常工作使用整理

### 保留某些文件不提交
1.git stash save "remark"  
2.git stash list  ：查看stash了哪些存储  
3.git stash show -p : 显示第一个存储的改动，如果想显示其他存存储，命令：git stash show  stash@{$num} -p ，比如第二个：git stash show stash@{1} -p  
4.git stash apply :应用某个存储,但不会把存储从存储列表中删除，默认使用第一个存储,即stash@{0}，如果要使用其他个，git stash apply stash@{$num} ， 比如第二个：git stash apply stash@{1}  
5.git stash drop stash@{$num} ：丢弃stash@{$num}存储，从列表中删除这个存储  
6.git stash clear ：删除所有缓存的stash  
#### 如果是未添加到版本控制的文件 需要add再存储
