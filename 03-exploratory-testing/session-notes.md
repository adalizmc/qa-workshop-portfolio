# Sesión 1

## Charter
Explorar el comportamiento del carrito y el flujo de compra realizando distintas acciones sobre los productos (agregar, modificar cantidades y eliminar), con el objetivo de identificar fallos en validaciones, inconsistencias en el estado del carrito y problemas al finalizar la compra.

## ÁREAS
Se trabajó principalmente sobre el catálogo, el carrito de compras y el proceso de checkout del sistema JPetStore.

## INICIO
11/04/2026 - 10:30 (Duración aproximada: 40 minutos)

## TESTER
Ada Liz Melgarejo Cano

## DESGLOSE DE TAREAS
10 min: Exploración del catálogo y selección de productos

20 min: Manipulación del carrito (agregar productos, modificar cantidades, eliminar)

10 min: Ejecución del flujo de compra y verificación del estado final

## ARCHIVOS DE DATOS
Se utilizaron únicamente los productos disponibles en la plataforma. No se emplearon datos externos.

## NOTAS DE PRUEBA
Durante la sesión se agregaron productos de distintas categorías para observar el comportamiento del carrito en diferentes escenarios.

Al modificar las cantidades, se probaron valores altos y extremos. En estos casos se observó que el sistema acepta números muy grandes sin ningún tipo de validación.

También se revisó el contador del carrito en la parte superior. Se detectó que el número mostrado aumenta según la cantidad de unidades, no según la cantidad de productos distintos, lo que puede resultar confuso.

Se realizaron combinaciones de acciones como agregar y eliminar productos repetidamente para ver si el estado del carrito se mantenía consistente.

Finalmente, se completó el proceso de compra. Luego de finalizarlo, se observó que los productos permanecen en el carrito, cuando se introduce un número exageradamente grande, este comportamiento rompe el sistema.

## LISTA DE RIESGOS
Existe el riesgo de que el sistema permita compras con cantidades irreales debido a la falta de validación.

El estado del carrito podría no reflejar correctamente lo que el usuario realmente compró.

El usuario podría confundirse con la información mostrada en el carrito, especialmente con el contador.

Podrían generarse pedidos incorrectos o duplicados si el carrito no se limpia correctamente.

## DEFECTOS (BUGS)
Bug 1: No se valida la cantidad máxima de productos en el carrito

Resultado esperado:
El sistema debería limitar la cantidad o validar contra el stock disponible.

Resultado actual:
Permite ingresar valores extremadamente altos sin ningún tipo de restricción.

Impacto:
Alto – afecta directamente la lógica de compra y el inventario.

Bug 2: El contador del carrito refleja unidades en lugar de productos

Resultado esperado:
El contador debería ser claro para el usuario y representar la cantidad de productos de forma intuitiva.

Resultado actual:
Muestra la suma total de unidades, lo que puede generar confusión.

Impacto:
Medio – problema de usabilidad.

Bug 3: El sistema permite cantidades excesivas provocando bloqueo y estado inconsistente del carrito
Resultado esperado:
El sistema debería validar la cantidad ingresada y evitar valores excesivos, manteniendo el flujo de compra estable y consistente.

Resultado actual:
Al ingresar una cantidad extremadamente grande en el carrito:

El flujo de compra se completa de forma inconsistente
El carrito no se reinicia correctamente después del checkout

Impacto:
Alto – puede provocar bloqueo del sistema, mala experiencia de usuario y generación de pedidos inconsistentes

## INCIDENTES (ISSUES)
1. No está claro si existe un límite máximo de productos por compra
2. No se define el comportamiento esperado del contador del carrito
3. No hay especificación sobre el estado del carrito después del checkout
4. No se evidencia validación de stock en el flujo de compra