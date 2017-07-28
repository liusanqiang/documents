# 使用阿里云 Symantec 免费型DV SSL 生成JKS

## 生成 pkcs12
```bash
$ openssl pkcs12 -export -in 214208344690717.pem -inkey 214208344690717.key -out pkcs.p12 -name ts
```
Enter Export Password: 123456

## 生成 jks
```bash
$ keytool -importkeystore -deststorepass 123456 -destkeypass 123456 -destkeystore ts.jks -srckeystore pkcs.p12 -srcstoretype PKCS12 -srcstorepass 123456 -alias ts
```
