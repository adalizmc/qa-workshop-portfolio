# Coverage Decisions

## Riesgos que se probarán primero

1. El sistema permite finalizar compras sin validar correctamente el carrito
2. El carrito no se actualiza correctamente después de acciones (agregar, eliminar, modificar)
3. Fallos en el proceso de checkout pueden generar pedidos incompletos o duplicados

---

## ¿Por qué esos riesgos son prioridad?

Estos riesgos se priorizan porque impactan directamente en el flujo principal del negocio: la compra de productos.

Cualquier error en el carrito o checkout puede:
- Generar pérdidas económicas
- Provocar pedidos incorrectos
- Afectar la confianza del usuario

Además, son funcionalidades críticas y altamente utilizadas, por lo que su probabilidad de fallo es mayor.

---

## Qué se probará menos o quedará fuera por ahora

- Validaciones avanzadas del registro de usuario
- Performance bajo alta carga
- Consistencia visual (UI/UX menor)

---

## Justificación de exclusiones

Estas áreas se excluyen temporalmente porque:

- No bloquean directamente el flujo de compra
- Tienen menor impacto inmediato en el negocio
- Requieren más tiempo o herramientas específicas (ej: pruebas de performance)

El enfoque inicial está en asegurar que el flujo principal de compra funcione correctamente antes de profundizar en otras áreas.