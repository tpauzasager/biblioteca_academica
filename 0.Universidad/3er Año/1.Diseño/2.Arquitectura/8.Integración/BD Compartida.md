- Se usa BD central para integrar componentes
- Centrado en **Integración de datos** (no en funcionalidades)
- Permite integración **asincróna y sincróna** (sin es asincróna -> es pull-based, pq bd no puede llamar a un sistema) 
- Simple de implementar
- Cada componente puede tener diferente stack tecnológico
- Cada componente de lógica es independiente en su disponibilidad (Los componentes pueden funcionar sin la necesidad de que todos los demás esten funcionando))

Problemas
- Problemas de performance (pq se necesita hacer un pull cte para tener los datos actualizados)
- Elevado **acoplamiento** (no permite versionado)
- Difícil de cambiar 
- Seguridad de los datos 