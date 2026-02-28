## 1.¿Es seguro usar variable global?

No es completamente seguro usar variables globales en aplicaciones concurrentes, porque múltiples solicitudes pueden intentar modificar la misma variable al mismo tiempo, lo que puede generar inconsistencias en los datos o errores inesperados.

## 2.¿Dónde aparece el recurso compartido?

El recurso compartido aparece en la lista clientes y en la variable contador_clientes, ya que ambas son variables globales que pueden ser accedidas y modificadas por múltiples peticiones al mismo tiempo.

## 3.¿Se debería usar lock en producción?
Sí, en producción se debería usar algún mecanismo de sincronización como un lock o, mejor aún, una base de datos real que maneje concurrencia automáticamente. Usar solo variables globales no es recomendable para aplicaciones reales con múltiples usuarios.
