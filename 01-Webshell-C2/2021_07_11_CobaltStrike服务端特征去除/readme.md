### 1、修改默认端口号
```
vim ./teamserver
```
默认端口50050，搜索50050，修改端口号
### 2、修改证书中的特征
执行如下命令查看证书信息
```
#默认密码123456
keytool -list -v -keystore ./cobaltstrike.store
```
可看到证书中多次出现字符串"Cobalt Strike"，如下图  
![image](./pic/0.png)  
使用nmap扫描时可看到此特征，如下图  
![image](./pic/1.png)  
执行如下命令重新生成cobaltstrike.store后  
```
keytool -keystore cobaltstrike.store -storepass 123456 -keypass 123456 -genkey -keyalg RSA -alias xxx.com -dname "CN=XX, OU=xxx.com, O=Xx, L=Xx, ST=Xx, C=XXX"
```
再次执行  
```
keytool -list -v -keystore ./cobaltstrike.store#默认密码123456
```
可以看到，不再有字符串"Cobalt Strike"  
同样，使用nmap扫描后，不再有字符串"Cobalt Strike"  
此处就不截图了  

### 参考链接：  
https://paper.seebug.org/1349/  
https://leaderzhang.com/archives/cobaltstrike  
