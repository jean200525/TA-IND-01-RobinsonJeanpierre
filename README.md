# TA-IND-01 — IEEE 29148 y tipos de requisitos de un sistema conocido

Repositorio de la actividad sumativa individual **TA-IND-01** de la asignatura
**Ingeniería de Requerimientos (ISR-401)**, Facultad de Ciencias de la
Computación, Universidad Técnica Estatal de Quevedo.

- **Estudiante:** Jean Pierre Robinson
- **Sistema analizado:** aplicación de transporte (Uber / InDrive)
- **Fecha límite:** sábado 7 de noviembre de 2026, 23:59

## Estructura del repositorio

```
.
├── README.md                     Este archivo
├── TA-IND-01/
│   ├── main.tex                  Archivo principal del informe
│   ├── referencias.bib           Bibliografía en formato IEEE (biber)
│   ├── main.pdf                  PDF compilado (se sube al repositorio)
│   ├── entrega-sga.tex           PDF de una página para el SGA (opcional)
│   ├── entrega-sga.pdf           PDF de una página ya compilado
│   └── figuras/                  Capturas propias del sistema (mínimo 3)
│       ├── captura-01.png
│       ├── captura-02.png
│       └── captura-03.png
└── .gitignore
```

## Compilador y dependencias

- **Compilador:** pdfLaTeX (MiKTeX 24.x o superior, o TeX Live 2024+).
- **Gestor de bibliografía:** Biber (incluido en MiKTeX y TeX Live).
- **Paquetes LaTeX:** `babel-spanish`, `geometry`, `microtype`, `graphicx`,
  `booktabs`, `longtable`, `array`, `tabularx`, `enumitem`, `xcolor`,
  `csquotes`, `caption`, `hyperref`, `biblatex` con estilo `ieee`.
  MiKTeX los instala automáticamente al compilar.

## Cómo compilar el informe

Desde la carpeta `TA-IND-01/`:

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

El orden importa: la primera pasada genera los auxiliares, `biber` procesa
`referencias.bib`, y las dos pasadas finales resuelven citas, referencias
cruzadas y numeración de tablas. El resultado es `main.pdf`.

Si se usa `latexmk`:

```bash
latexmk -pdf -bibtex-cond main.tex
```

### Compilación en Overleaf (alternativa)

1. Subir el contenido de `TA-IND-01/` respetando la carpeta `figuras/`.
2. En *Menu → Settings*, elegir **Compiler: pdfLaTeX** y
   **Bibliography: Biber**.
3. Compilar. El archivo principal es `main.tex`.

## Cómo compilar la hoja de entrega del SGA

```bash
pdflatex entrega-sga.tex
```

Genera un PDF de **una sola página** con los datos informativos y la URL del
repositorio en una sola línea.

## Figuras

Las tres capturas deben ser propias (tomadas del sistema en uso) y guardarse
en `TA-IND-01/figuras/` con los nombres `captura-01.png`, `captura-02.png` y
`captura-03.png`. El documento compila aunque falten: en ese caso muestra un
recuadro rojo de advertencia que debe desaparecer antes de la entrega.

## Checklist antes de entregar

- [ ] No queda ninguna marca `[PENDIENTE: ...]` en `main.pdf`.
- [ ] Las 3 capturas están en `figuras/` y se ven en el PDF.
- [ ] El PDF tiene entre 4 y 7 páginas de contenido.
- [ ] No hay desbordes de texto ni `??` en el PDF.
- [ ] Todas las referencias del `.bib` están citadas en el texto.
- [ ] La declaración de uso de IA está completa (herramienta, versión,
      propósito y verificación).
- [ ] `main.pdf` y `entrega-sga.pdf` están subidos al repositorio.
- [ ] El PDF de una página se subió al SGA (ningún otro archivo).

## Uso de inteligencia artificial

La infraestructura LaTeX de este repositorio (estructura del documento,
`README.md`, plantilla de referencias y resolución de errores de compilación)
se elaboró con apoyo de un asistente de IA. El contenido evaluable —análisis
de la norma, glosario, requisitos, autoevaluación y reflexión— es de autoría
del estudiante y se declara en la sección correspondiente del informe.
