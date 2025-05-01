Lista de Errores encontrados

**🔧** Error 1: Número aleatorio decimal y fuera del rango (Linea 44)

Problema: El número aleatorio se generaba con Math.random() * 10, lo que producía decimales y un rango incorrecto.

Solución: Se cambió por Math.floor(Math.random() * 100) + 1 para generar un número entero entre 1 y 100.

**🔧** Error 2: Comparación incorrecta entre string y número (Linea 58 y 65)

Problema: El valor ingresado 'userGuess' no se convertía a número, por lo que la comparación userGuess === randomNumber nunca era verdadera.

Solución: Se convirtió userGuess a número con Number(guessField.value) y se agregó una validación con Number.isInteger() para asegurarse de que se ingrese un número entero antes de poder continuar.

**🔧** Error 3: Falta validación de entrada de número entero (Linea 65 a 70)

Problema: El usuario podía ingresar letras u otros caracteres no válidos y aún así se contaba como intento.

Solución: Se agregó una condición que muestra una alerta si el valor ingresado no es un número entero, y se detiene la ejecución de la función sin contar el intento.

**🔧** Error 4: Mensajes de victoria y derrota invertidos (Linea 74 a 80)

Problema: El mensaje de “Felicitaciones” aparecía al perder, y el mensaje de “Pérdistes” al ganar.

Solución: Se reordenaron las condiciones if para que el mensaje correcto se muestre según corresponda.

**🔧** Error 5: Selector incorrecto de elemento con clase .lowOrHi (Linea 49)

Problema: Se usaba document.querySelector('lowOrHi') sin el punto para clase.

Solución: Se corrigió a document.querySelector('.lowOrHi').

**🔧** Error 6: Error de sintaxis en addEventListener (Linea 97 y 105)

Problema: Se escribió incorrectamente addeventListener en minúsculas.

Solución: Se corrigió a addEventListener, respetando mayúsculas.

**🔧** Error 7: Número de intentos incorrecto (46)

Problema: Se configuraron solo 5 intentos en vez de 10.

Solución: Se cambió la constante ATTEMPS de 5 a 10.

**🔧** Error 8: El número aleatorio no se reiniciaba correctamente (Linea 124)

Problema: En la función resetGame() el número aleatorio se regeneraba con Math.floor(Math.random()) + 1, que solo genera 1.

Solución: Se corrigió a Math.floor(Math.random() * 100) + 1.


🧪 Pruebas realizadas

✅ Prueba de entrada válida e inválida.

✅ Prueba de límite de intentos.

✅ Prueba de mensajes como lo son mayor, menor, ganar, perder.

✅ Prueba de colores: negro, rojo, verde según el estado.

✅ Prueba de reinicio del juego.