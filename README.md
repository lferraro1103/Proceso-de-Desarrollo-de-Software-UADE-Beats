# UADE Beats - Versión 0

Proceso de Desarrollo de Software - Grupo 10: Franco Beron y Leandro Ferraro

Es el TP final que entregamos en POO, sin cambios. Es el punto de partida de las iteraciones de esta materia.

## Qué es

Un sistema para gestionar recitales en vivo. El administrador da de alta usuarios y artistas y maneja los eventos, y los usuarios piden entrar a un evento según su plan de suscripción (Free, Premium o Artist Pass), el estado del evento y la capacidad. Cada intento de ingreso queda registrado.

## Qué hay en el repositorio

| Carpeta o archivo | Contenido |
|---|---|
| `TP/Grupo9_POO_EntregaFinal/Codigo/src` | El código en Java, con interfaz de consola (`App`) y ventana Swing (`AppSwing`) |
| `TP/Grupo9_POO_EntregaFinal/datos` | Los archivos de texto donde se guardan usuarios, artistas, eventos y accesos |
| `TP/Grupo9_POO_Diagramas_Pdf` | Los diagramas de clases y de secuencia de la entrega de POO |
| `TP/Grupo9_POO_EntregaFinal.pdf` | El informe de la entrega de POO |

## Cómo se corre

Desde `TP/Grupo9_POO_EntregaFinal`, para que el programa encuentre la carpeta `datos`:

```
javac -encoding UTF-8 -d Codigo/out $(find Codigo/src -name "*.java")
java -cp Codigo/out Main
```

En Windows con PowerShell, el primer comando es `javac -encoding UTF-8 -d Codigo/out (Get-ChildItem -Recurse Codigo/src -Filter *.java).FullName`.

## Qué vamos a corregir

`App` tiene casi mil líneas con el menú, la lectura de datos, las validaciones y la persistencia juntos; `Usuario` y `Artista` repiten los mismos datos; y la persistencia está atada a archivos de texto. Eso es lo que se va corrigiendo en las iteraciones siguientes, cada una en su rama.
