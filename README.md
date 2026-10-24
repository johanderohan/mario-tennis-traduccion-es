# Mario Tennis (Game Boy Color) — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Traducción al **español de España** de *Mario Tennis* (Game Boy Color, 2001), el
juego de tenis de Camelot y Nintendo con modo historia en la Real Academia de Tenis.
Se ha traducido desde la versión **estadounidense en inglés**.

La traducción se reparte como **parche**: no incluye el juego. Necesitas tu propia
copia para aplicarlo.

## Estado

Última versión: **[v1.0 — Primera publicación](../../releases/tag/v1.0)**.

| Parte | Estado |
|---|---|
| Modo historia (Mario Tour), diálogos, menús y ayudas | **4008 de 4008 cadenas** traducidas y revisadas (las 101 restantes son de depuración y no se ven) |
| Diccionario de tenis | 95 términos y definiciones, **reordenados alfabéticamente en castellano** |
| Reglas de minijuegos, retos y créditos | Traducidos y medidos en sus ventanas |
| Rótulos gráficos de menús, partido y presentación | En castellano (menú principal, estadísticas, pistas, mensajes del partido, pantalla final…) |
| Rejilla para escribir el nombre | Con **Ñ ñ á é í ó ú** |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿** |
| Logotipo «MARIO TENNIS» y nombre del modo «MARIO TOUR» | Se conservan, por ser imagen de marca |
| Revisión durante una partida | Parcial (ver abajo) |

Los términos de tenis siguen el uso de España (saque, resto, volea, globo, dejada,
remate, liftado, cortado, iguales, ventaja, tie-break, *ace* y *passing shot*). Lo que
se dice a tu personaje y a tu pareja vale igual si es chico o chica. Mario y compañía
conservan su «-a» característico.

### Cambios técnicos

- El castellano ocupa más que el inglés, así que el parche **amplía la ROM a 4 MB**
  (MBC5) y reubica todo el texto. Se ha agrandado el búfer de mensajes y se han
  movido dos búferes del motor que pisaban los mensajes largos.
- Fuente con letras españolas nuevas en la tipografía de los diálogos y en la de los
  menús, con el **mismo color, grosor y sombra** que el original.
- Rótulos gráficos recomprimidos con el mismo formato del juego.

### Comprobaciones y trabajo pendiente

- Cada una de las 4109 cadenas se vuelve a leer desde la ROM construida, tal como la
  lee el juego, y coincide con el guion. Una auditoría automática comprueba el
  código nuevo, la fuente y los límites de cada caja y ventana.
- Se ha jugado en emulador (mGBA), **desde partida nueva** y sin trucos, en cuatro
  rondas: creación de personaje y nombre con ñ, el primer día en la Academia, el
  comedor, la residencia, el centro de entrenamiento, los menús de pausa y del mapa,
  **guardar y cargar** (también arrancando en frío), partidos de exhibición completos,
  los minijuegos disponibles con sus reglas, el diccionario y los datos guardados.
  Las cuatro rondas suman unos 100 minutos de juego y más de 8.500 capturas, todas
  revisadas. La versión publicada se ha comprobado con una prueba de humo
  (presentación, partida nueva, diálogos y carga de una partida guardada); respecto a
  la anterior solo cambian los rótulos de la presentación.
- **Pendiente:** una partida completa (no se ha llegado al Open de la Isla, a las
  clases sénior ni a Mundo Mario en el juego, aunque su texto está revisado), algunos
  mensajes del partido que no salieron en las pruebas (falta, doble falta, red, bola
  de set, récord), el juego por cable, la prueba en consola física y una revisión
  humana independiente. La traducción y su revisión se han hecho con asistencia de
  IA. Por eso la versión figura «en revisión»; si encuentras algo, abre una incidencia.
- Las mayúsculas acentuadas de la fuente pequeña (Á, É, Í, Ó, Ú) son algo más bajas
  que el resto, porque la letra no deja sitio encima para la tilde.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego en versión **USA**. El parche solo funciona con esa
   versión exacta:

   | | |
   |---|---|
   | Archivo | `Mario Tennis (USA).gbc` |
   | Tamaño | 2.097.152 bytes (2 MB) |
   | MD5 | `50af67f7321d84bd052f0e793ee0613c` |
   | CRC32 | `A781C63C` |

   ```bash
   md5sum "Mario Tennis (USA).gbc"                        # Linux
   md5 "Mario Tennis (USA).gbc"                           # macOS
   CertUtil -hashfile "Mario Tennis (USA).gbc" MD5        # Windows
   ```

   Si el MD5 no coincide, el parche fallará.
3. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "Mario Tennis (USA).gbc" mario-tennis-gbc-es-v1.0.xdelta "Mario Tennis (ES).gbc"`
4. Comprueba que la ROM resultante mide **4.194.304 bytes** (4 MB) y tiene MD5
   **`6bd8a7a4802168b412b22b0765095692`**.
5. Empieza una **partida nueva** en tu emulador o flashcart (debe admitir ROMs MBC5
   de 4 MB, como la mayoría).

Las partidas guardadas con la versión inglesa no se han probado con la traducida.

## Cambios por versión

### v1.0 — 24 de octubre de 2026

- Primera publicación: modo historia, menús, diccionario, reglas, créditos y rótulos
  gráficos en castellano de España.
- Fuente española nueva, ROM ampliada a 4 MB y diccionario en orden alfabético castellano.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación
alguna con Nintendo ni Camelot. Aquí no se distribuye el juego ni ninguna parte de él:
solo un parche que modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia
y lo hago.
