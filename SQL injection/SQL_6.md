# Visible error-based SQL injection

### Payload
`Cookie: TrackingId=' AND 1=CAST((SELECT username FROM users LIMIT 1) AS int)--;`
Esto provocó un error porque:

- SELECT username FROM users LIMIT 1 → trae el primer usuario (seguramente 'administrator' o similar).
- CAST(... AS int) → intenta convertir ese string a un número → explota, porque 'administrator' no es un número.

Tener en cuanta que algunas veces el tamaño de la Cookie es definido y entonces puede que sea muy corto, por lo cual como en este caso tenemos que hacer que el payload se lo más corto posible.