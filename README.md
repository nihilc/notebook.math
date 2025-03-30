# Notebook

Aquí se encuentran organizados y estructurados los apuntes que he tomado durante la carrera de Matemáticas en la Universidad.

Este repositorio esta pensado para utilizar con [obsidian](https://obsidian.md/) 

# Funcionamiento
## Estructura de archivos

```ls
├── .config/
│	└──	preamble.sty
├── _files/
│	├── {note_name}_date.png
│	├── {note_name}_date-2.png
│	└──	excalidraw/
│		└──	draw_date.md
└── cursos/
	├── s1/
	└──	s2/
	    ├── nombre_curso/
	    └── nombre_curso/
	        ├── info.md
	        ├── 01-tema1.md
	        ├── 02-tema2.md
	        └── ejercicios/
	            ├── 01-tema1.ej.md
	            ├── 02-tema2.ej.md
				└── 02-tema2.ej-1.md
```

## Explicación Carpetas y Archivos principales:

- `.config/preamble.sty` Aquí se configuran las macros para MathJax
- `_files/` Aquí dentro estarán todas las imágenes, archivos que copies dentro de las notas, configuradas para tener el nombre de la misma junto con la fecha
	- `excalidraw/` Aquí se almacenaran los dibujos que se hagan con el plugin Excalidraw
- `cursos/` Dentro de esta carpeta se organizan los cursos divididos por subcarpetas por semestre `s1/,s2/,...,sX/`
	- `nombre_curso/` Aquí se almacenaran notas relacionadas a un curso de la siguiente forma:
		- `info.md` siempre sera de información del curso, profesor, syllabus, temas, etc.
		- `XX-tema.md` serán como tal los apuntes divididos por cada tema visto en clase o estudiado.
		- `ejercicios/` Aquí se almacenaran notas en las cuales se desarrollen ejercicios propuestos o de estudio se deben guardar de la forma `XX-tema.ej` siento `XX-tema` equivalente nombre de la nota donde se propuso el ejercicio o que trate los temas que se van a trabajar y esta debe estar referenciada en el mismo con un link. Además si en una misma nota de `XX-tema.md` aparecen varios ejercicios, se debe agregar al final `-N` ejemplo `02-tema2.ej` `02-tema2.ej-1`

# Plugins

- Excalidraw
- Extended MathJax
- Git
- Latex Suite
- Minimal Theme Settings
- Paste Image Rename
