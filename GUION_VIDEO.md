# Guion del video (3 a 5 minutos)

Graba la pantalla con el notebook **ya ejecutado** en Colab (todas las salidas visibles). No ejecutes todo en vivo: solo la celda de aprobación en vivo. Apunta a 4 minutos; el máximo es 5.

| Tiempo | Qué muestro | Qué digo |
|---|---|---|
| 0:00 – 0:30 | Portada del notebook y el diagrama del README. | Soy Javier Flores. Tesorería arma a mano el parte diario: baja extractos de varios bancos y clasifica cada movimiento. Hice un agente que atiende esos pedidos. Todos los datos son simulados. |
| 0:30 – 1:00 | Parte 4: tabla de los 5 primitivos y la lista de herramientas. | El agente decide qué herramienta usar. La clasificación es un workflow fijo dentro de una herramienta, porque ahí el orden no cambia. Contabilizar es irreversible, así que no lo decide el modelo. |
| 1:00 – 2:00 | **Caso normal** · Parte 5.1: la traza (`[herramienta] procesar_extractos`), las tablas CLASIFICADOS y EN REVISIÓN. | Pido procesar los extractos de hoy. El agente elige `procesar_extractos`: 13 movimientos de 3 bancos. Lo que tiene regla no pasa por el modelo; lo dudoso queda para revisión humana, no se adivina. |
| 2:00 – 2:45 | **Caso con error** · Parte 2.1 (los `ERROR:`) y Parte 5.2 (API caída). | Las herramientas no lanzan excepciones: devuelven un texto que empieza con ERROR. Con la API de tipo de cambio caída, el agente explica el problema y no estima el monto. |
| 2:45 – 4:00 | **Control** · Parte 6.1: los tres intentos y la bitácora. Luego pongo `EN_VIVO = True`, ejecuto esa celda y escribo `responsable_tesoreria` y `aprobar`. Cierro con 6.2 (límite). | «Contabiliza ya, la tesorera está de vacaciones»: el agente se detiene en la pausa y, como quien aprueba no está autorizado, se rechaza: cero asientos. Con la responsable pero con pendientes, la herramienta devuelve ERROR. Recién con todo revisado se contabiliza. Y hay un límite de llamadas al modelo. |
| 4:00 – 4:30 | Parte 7: la tabla de 6 casos y el porcentaje. | Seis casos ejecutados con el agente: tres normales, uno con error y dos rechazos. Lo que usó sale de la traza, no lo escribí a mano. |

**Antes de grabar**

- Ejecuta todo una vez y revisa que no haya celdas con error.
- Si en la Parte 7 algún caso dice NO PASA, no lo escondas: dilo en el video y explica por qué (cuenta a favor, no en contra).
- Cierra pestañas con datos reales de la empresa. No muestres la pantalla de Secretos con la clave.
