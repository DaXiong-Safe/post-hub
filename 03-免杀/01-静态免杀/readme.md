## CobaltStrike、Metasploit静态免杀思路
### 1、loader + shellcode
1.1、c语言实现的loader  
1.2、go语言实现的loader  
1.3、loader变形  
```
异或加密
睡眠函数，C语言睡眠函数：Sleep(1000)
base64编码
gzip压缩
```
1.4、（多篇文章提到）生成64位的shellcode比32位shellcode免杀效果更好一些

## 待尝试思路记录：
DNS分离免杀：https://mp.weixin.qq.com/s/bM_rsh8KxXwwyEkbHRTKsw  

狼组团队：https://github.com/wgpsec/CS-Avoid-killing  
https://mp.weixin.qq.com/s/G1hmsDVTO2208Ymlia_ggQ  
https://github.com/An0ny-m0us/DesertFox  
知道创宇公司：https://github.com/knownsec/shellcodeloader  

Kill杀软：https://github.com/Yaxser/Backstab + https://github.com/secretsquirrel/SigThief
