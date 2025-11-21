
| Estrategía | Definición                                                                                                                                                                 | Ventaja                       | Desventaja                                                                                 |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------ |
| Basico     | Todos los nodos son actualizados al mismo tiempo                                                                                                                           | Simple                        | Riesgo de downtime                                                                         |
| Blue/Green | Hay dos ambientes de producción <br>Despliegue se hace un uno mienras que el otro mantiene versión<br>Balanceador redirige flujo al ambiente que no esté siendo modificado | Simple                        | Si org grande => Muy costoso                                                               |
| Rolling    | Nodos actualizados uno a uno                                                                                                                                               | Simple de hacer rollback      | App/BD necesita constancia entre versiones (para poder trabajar con ambas al mismo tiempo) |
| Canary     | Rolling, pero con un set de varios nodos a la vez                                                                                                                          | Solo 1 ambiente de producción | Complejo de testar <br>Herramientas de testeo complejas                                    |

# Definiciones
Baseline
	- conjutno de IC que se toman como referencia para siguientes etapas del desarrollo 
	- Se establece cuando se satisface conjunto de requerimientos 
	- Diferente a release 
Branch
	- Linea de desarrollo separada 
	- Usan una baseline como punto de partida 