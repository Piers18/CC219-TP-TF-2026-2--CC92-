# Análisis de comentarios de tecnología en YouTube

Proyecto del curso **CC219 – Aplicaciones de Data Science**. Por ahora, el repositorio contiene el **análisis exploratorio de datos (EDA)**; aún no contiene modelos entrenados ni resultados de clasificación.

## Objetivo

Analizar comentarios sobre celulares y laptops para preparar dos tareas: clasificar su sentimiento y estudiar la popularidad de los comentarios de celulares.

## Integrantes

- Piero Antonio Aguilar Anticona
- Juan Diego Bismarck Aquino
- Orianna Milagros Icaza Brocos

## Datos

| Archivo | Contenido |
|---|---|
| `data/dataset_semiestructurado.json` | 2825 comentarios de celulares de 39 videos y 15 canales, con texto, fecha, «me gusta» y respuestas. |
| `data/dataset_no_estructurado_comentarios.txt` | 2852 líneas sobre laptops; 33 vacías y 2819 comentarios utilizables. |
| `data/imagenes/` | 29 miniaturas de videos de laptops. El TXT no permite asociar una línea concreta con una imagen. |
| `data/dataset_preparado_celulares.csv` | Campos seleccionados del JSON, texto con espacios normalizados y variables descriptivas. |
| `data/dataset_preparado_laptops.csv` | Líneas no vacías del TXT, texto con espacios normalizados y variables descriptivas. |

Los archivos originales permanecen en `data/`. Los CSV preparados se generan de nuevo al ejecutar el notebook.

## Código y ejecución

El análisis está en [`code/EDA_trabajofinal.ipynb`](code/EDA_trabajofinal.ipynb). Incluye tablas, gráficos y una interpretación después de cada bloque de resultados.

1. Instala Python 3 y las bibliotecas `pandas`, `matplotlib`, `Pillow` y `notebook`.
2. Abre Jupyter desde la raíz del repositorio: `jupyter notebook code/EDA_trabajofinal.ipynb`.
3. Ejecuta las celdas en orden. El notebook también funciona si el directorio de trabajo es `code/`.

## Conclusiones preliminares del EDA

- La mediana de longitud es de 15 palabras en celulares y 16 en laptops.
- El 70,5 % de los comentarios de celulares tiene cero «me gusta»; una futura clasificación de popularidad deberá considerar ese desbalance.
- Los datos no incluyen etiquetas verificadas de sentimiento. Se necesita un conjunto etiquetado antes de entrenar y evaluar esa tarea.
- El TXT de laptops carece de fecha e interacciones por comentario, por lo que no se puede usar directamente para predecir popularidad.

## Licencia y procedencia

**Licencia del código: pendiente de definir por los integrantes.** Los comentarios y las miniaturas proceden de YouTube y pueden tener derechos de terceros; no se incluyen bajo una licencia otorgada por este repositorio. La presencia de los archivos aquí no implica permiso para reutilizarlos fuera de las condiciones aplicables de la fuente.
