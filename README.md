# Workshop 1 · Seguimiento de estudiantes

Presentación de apoyo del Workshop 1 de **ARTI · Fundamentos de Arquitectura**,
Universidad de los Andes, periodo 2026-20.

- **Docente:** Maria Camila Romero
- **Equipo:** Andrés Felipe García Caycedo · David Felipe Laverde Parra · Jose Carlos Salgado Pacheco
- **Caso:** evaluación y seguimiento de estudiantes, a partir del testimonio de un
  profesor de cátedra de arquitectura empresarial.

Son las 13 diapositivas de la sustentación, con la misma estructura y los mismos
textos de la presentación del grupo:

1. Portada
2. La pregunta que tenemos que poder contestar
3. Qué decidimos modelar
4. El metamodelo
5. Un lenguaje para que lo lea el profesor
6. El modelo
7. El punto de vista
8. La vista de consulta
9. Los problemas
10. Los supuestos
11. Los accionables inmediatos
12. La línea conceptual
13. El reparto de los quince minutos

Lo que agrega sobre el PowerPoint, sin cambiar un texto:

- Los seis diagramas van completos y se abren a tamaño original con zoom y
  arrastre, desde el botón **Ampliar** o la tecla `F`.
- El tablero de la vista de consulta está vivo: al pulsar una celda dice de qué
  instancia sale y por qué camino de asociaciones.
- Las cuatro cajas del metamodelo se abren: la raíz muestra sus cinco
  asociaciones, las herencias sus atributos propios, las restricciones las
  dieciséis completas y la verificación los siete bloques de comprobaciones.
- Los quince símbolos del lenguaje son pulsables y muestran qué dibuja cada uno
  y cómo lo llama el profesor.
- Las tres tarjetas de la pregunta, los cuatro hallazgos del modelo y los siete
  accionables se abren con el detalle que los respalda.
- Las tres familias de problemas resaltan sus filas en la matriz.
- Los supuestos muestran los cuatro principales, con un botón para ver los nueve.
- Las cifras suben desde cero al entrar en cada diapositiva, y el cronómetro de
  quince minutos va en el riel superior.

---

## Publicarlo en GitHub Pages

### Opción A · repositorio nuevo (lo más rápido)

1. En GitHub, **New repository**. Nombre sugerido: `workshop1-arti-seguimiento`.
   Déjelo **Public** (Pages gratis exige repositorio público) y **no** marque
   "Add a README".
2. Suba el contenido de esta carpeta. Desde la web: **Add file → Upload files**,
   arrastre `index.html`, `logo.png`, `.nojekyll`, `README.md` y las carpetas
   `fig/` y `sim/` completas. Commit.
3. **Settings → Pages**. En *Source* elija **Deploy from a branch**, rama `main`,
   carpeta `/ (root)`. Guarde.
4. En uno o dos minutos la URL queda en
   `https://<su-usuario>.github.io/workshop1-arti-seguimiento/`.

Por consola, desde esta misma carpeta:

```bash
git init
git add .
git commit -m "Workshop 1 ARTI: presentacion de sustentacion"
git branch -M main
git remote add origin https://github.com/<su-usuario>/workshop1-arti-seguimiento.git
git push -u origin main
```

Y después active Pages en **Settings → Pages** como dice el paso 3.

### Opción B · dentro de un repositorio que ya tenga

Copie esta carpeta como subcarpeta (por ejemplo `workshop1/`) y publique desde la
raíz del repositorio. La URL queda en
`https://<su-usuario>.github.io/<repo>/workshop1/`.

---

## Qué hay en la carpeta

| Archivo | Qué es |
|---|---|
| `index.html` | La presentación entera: HTML, CSS, JavaScript y los datos del metamodelo, todo en un solo archivo. No necesita servidor ni compilación. |
| `fig/` | Los seis diagramas en resolución original (PNG). El metamodelo son 14 480 × 6 564 px. |
| `sim/` | Los 16 pictogramas del lenguaje gráfico, uno por archivo. |
| `logo.png` | Escudo de la Universidad de los Andes. |
| `.nojekyll` | Le dice a GitHub Pages que sirva los archivos tal cual, sin procesarlos con Jekyll. **No lo borre.** |

Las rutas son todas relativas, así que funciona igual en la raíz del dominio, en
una subcarpeta o abriendo `index.html` directamente desde el disco.

La única dependencia externa son las tipografías de Google Fonts (Newsreader, IBM
Plex Sans e IBM Plex Mono). Sin conexión la presentación sigue funcionando: el
navegador cae a Georgia y a la tipografía de sistema.

---

## Cómo se maneja en la sustentación

| Tecla | Qué hace |
|---|---|
| `→` `Espacio` `AvPág` | Siguiente diapositiva |
| `←` `RePág` | Diapositiva anterior |
| `Inicio` / `Fin` | Primera / última |
| `I` | Abre y cierra el índice de las 13 diapositivas |
| `F` | Amplía la figura de la diapositiva actual |
| `T` | Cambia entre tema claro y oscuro |
| `Esc` | Cierra el visor o el índice |

En el visor de figuras: `+` y `−` para el zoom, `0` para ajustar a la pantalla,
arrastrar para desplazar, rueda del ratón para acercar. En móvil o tableta se pasa
de página deslizando el dedo.

El cronómetro del riel superior marca los quince minutos: **Iniciar** lo arranca y
**pulsar el reloj** lo reinicia. La etiqueta de al lado indica a quién le toca
hablar en la diapositiva en la que esté:

| Presenta | Diapositivas |
|---|---|
| Andrés Felipe García | 1 a 5 · portada, testimonio, proceso, decisiones, metamodelo |
| David Felipe Laverde | 6 a 8 · lenguaje gráfico, modelo, punto de vista |
| Jose Carlos Salgado | 9 a 13 · vista de consulta, problemas, supuestos, accionables, sustentación |

---

## Si quiere cambiar algo

Todo el contenido vive en el propio `index.html`:

- Los textos están escritos directamente en el HTML, dentro de cada
  `<section class="slide">`.
- Los datos del metamodelo, el modelo y los artefactos están en el bloque
  `<script type="application/json" id="datos">`, cerca del final. De ahí salen el
  explorador de conceptos, el tablero, la matriz de problemas y las cifras de la
  portada.
- Los colores son variables CSS declaradas en `:root`, al principio del archivo, y
  se redefinen para el tema oscuro un poco más abajo.
