# Simulaciones de bifurcaciones — Sistemas Dinámicos

Sitio web estático listo para **GitHub Pages**.

## Contenido

- `index.html` — página de acceso a las tres simulaciones.
- `silla_nodo.html` — forma normal de bifurcación silla-nodo, `dx/dt = r - x²` (simulación nueva).
- `transcritica_laser.html` — simulación original del umbral láser, una bifurcación **transcrítica**, no silla-nodo.
- `hopf.html` — simulación de Hopf de la reacción química (versión con gráficas progresivas).

Todos los archivos son autónomos, con CSS y JavaScript integrados. No requieren bibliotecas externas ni servidor de cálculo.

## Publicar en GitHub Pages

1. Crea un repositorio público en GitHub, por ejemplo `simulaciones-bifurcaciones`.
2. Extrae el ZIP y sube **los cuatro archivos HTML y este README a la raíz** del repositorio (no la carpeta contenedora).
3. En el repositorio abre **Settings → Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**; elige rama `main` y carpeta `/(root)` y guarda.
5. Cuando GitHub Pages publique el sitio, la dirección será aproximadamente `https://TU_USUARIO.github.io/simulaciones-bifurcaciones/` (usa la URL real que muestre GitHub).

Para añadirlo en Beamer, tras publicar el sitio:

```latex
\href{https://TU_USUARIO.github.io/simulaciones-bifurcaciones/}{\beamerbutton{Abrir simulaciones}}
```

No utilices `run:` para abrir HTML desde el PDF de Overleaf, porque normalmente se bloquea.

## Nota

El archivo que se proporcionó como “silla-nodo” era en realidad la simulación de la bifurcación transcrítica del láser. Para no perderla, este paquete incluye esa simulación **además** de una nueva simulación de silla-nodo y la de Hopf.
