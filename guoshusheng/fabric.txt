### 理解Fabric
* kakfa相当于一个数组，每个order都有消费offset
* 对于交易打进块的同步，就是依赖于数组的顺序
* tls用于通讯，其他的用于签名
* ca是根，用于生成证书，CA-SERVER就是用来生成证书文件的。手动放到MSP目录下
* PKID交换
