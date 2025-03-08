# Legibilidad

## Códigos

| Retos       | Enlace |
|------------------|--------|
| **WhacAMole** | [Code1](https://github.com/paulaqing/prg1-22-23/blob/main/retos/entregas/paulaDiestro/WhacAMole.java) |
| **RetoCCCF**          | [Code2](https://github.com/paulaqing/prg1-22-23/blob/main/retos/entregas/paulaDiestro/retoCCCF.java) |

## Nombrado

monigote un nombre más claro podría ser topo o mole (dependiendo el idioma), ya que el juego se llama "Whac-A-Mole". [Code1]((https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/WhacAMole.java#L7))

casilla podría llamarse casillaGolpeada para mayor claridad. [Code1]((https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/WhacAMole.java#L9))

unaCola podría llamarse personasEnCola, ya que el nombre actual no es claro. [Code2](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/retoCCCF.java#L10)

## Comentarios

Ausencia de comentarios en todos los códigos.

## Formato y Consistencia 

j = j + 1 y i = i + 1 pueden simplificarse a j++ y i++. [Code1](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/WhacAMole.java#L31C12-L32C61)

Espaciado inconsistente en aciertos=aciertos +1 ;, debería ser aciertos = aciertos + 1;. [Code1](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/WhacAMole.java#L60)

minuto = minuto + 1 puede simplificarse a minuto++. [Code2](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/retoCCCF.java#L22)

Espaciado inconsistente en algunas asignaciones. Hay líneas en las que aparece unaCola = unaCola -1;y en otras unaCola = unaCola - 1;. [Code2](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/retoCCCF.java#L42)

## Código Muerto 

Línea innecesaria [Code1](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/WhacAMole.java#L15) Al inicio de cada turno es redundante porque golpe se vuelve a inicializar en el bucle anidado.

Línea sin uso [Code2](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/retoCCCF.java#L3)

## DRY

Las condiciones if (casilla == agujero && casilla == golpe) y else if (casilla == monigote && casilla == golpe) imprimen el mismo resultado. Se puede combinar en una sola condición. [Code1](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/WhacAMole.java#L34C2-L37C52)

La lógica de asignación de personas a las cajas es repetitiva. Se puede simplificar con un array o una estructura iterativa. [Code2](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/retoCCCF.java#L35C4-L54C14)

Los if para reducir el tiempo de cada caja (cajaX = cajaX - 1;) también se pueden unificar en un bucle. [Code2](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/retoCCCF.java#L56C4-L78C58)

## YAGNI

La variable dimension se usa solo en los bucles for, y su valor es fijo. No es realmente necesaria si el tablero es siempre de 4x4. Se podría eliminar y directamente iterar hasta 4. [Code1](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/WhacAMole.java#L5)

tiempoTotal = 12 * 60 podría simplemente definirse como 720 [Code2](https://github.com/paulaqing/prg1-22-23/blob/fc0837c6208f4b8ac7d9d9d959799292e16836c5/retos/entregas/paulaDiestro/retoCCCF.java#L8)