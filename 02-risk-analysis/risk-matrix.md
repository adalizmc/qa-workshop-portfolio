# Risk Matrix

| ID | Riesgo | Impacto | Probabilidad | Nivel | Justificación |
|----|--------|---------|--------------|-------|---------------|
| R1 | El sistema permite finalizar compras sin validar correctamente el carrito (productos, cantidades o stock) | Alto | Alta | Crítico | Impacta directamente en ventas y puede generar pedidos inválidos o inconsistentes |
| R2 | El carrito no se actualiza correctamente después de acciones como agregar, eliminar o modificar productos | Alto | Alta | Crítico | El carrito es clave en el flujo de compra y errores aquí afectan directamente la conversión |
| R3 | El sistema permite registrar usuarios con datos inválidos o incompletos | Medio | Alta | Alto | Puede generar problemas en pedidos, envíos y comunicación con el cliente |
| R4 | Errores en el proceso de login impiden el acceso a usuarios válidos | Alto | Media | Alto | Afecta directamente la experiencia del usuario y puede bloquear compras |
| R5 | El sistema presenta tiempos de carga elevados al navegar el catálogo o realizar búsquedas | Medio | Media | Medio | Puede afectar la experiencia del usuario pero no bloquea completamente el flujo |
| R6 | Inconsistencias entre los datos mostrados en el catálogo y el detalle del producto | Medio | Media | Medio | Puede generar desconfianza o decisiones incorrectas de compra |
| R7 | Fallos en el proceso de checkout pueden generar pedidos incompletos o duplicados | Alto | Media | Alto | Impacta directamente en ingresos y en la operación del negocio |
