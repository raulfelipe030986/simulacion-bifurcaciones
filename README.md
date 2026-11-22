# Simulaciones interactivas de bifurcaciones

**Asignatura: Sistemas Dinámicos**

Este repositorio reúne tres simulaciones de sistemas de ecuaciones diferenciales que dependen de un parámetro. Su finalidad es observar cómo cambia **cualitativamente la dinámica en el espacio de estados** cuando el parámetro atraviesa un **valor de bifurcación**.

**[Abrir las simulaciones](./index.html)** · [Silla-nodo](./silla_nodo.html) · [Transcrítica: láser](./transcritica_laser.html) · [Hopf: reacción química](./hopf.html)

## Cómo trabajar con las simulaciones

1. **Identifica el modelo y su parámetro.** Observa qué magnitudes son variables de estado y cuál es el parámetro que puedes cambiar.
2. **Selecciona un valor anterior al crítico.** Localiza los equilibrios y, cuando corresponda, las órbitas periódicas. Ejecuta la simulación y observa hacia dónde evoluciona la solución.
3. **Selecciona el valor crítico.** Comprueba qué cambia en el retrato de fases: ¿coinciden equilibrios?, ¿cambia su estabilidad?, ¿aparecen o desaparecen oscilaciones?
4. **Selecciona un valor posterior al crítico.** Repite la observación y compara los tres casos. No te limites al aspecto de las curvas: interpreta qué ocurre con las trayectorias en el espacio de estados.
5. **Cuando la simulación lo permita, cambia la condición inicial.** Distingue lo que depende del estado inicial de lo que depende del parámetro. Una solución particular no es todo el retrato de fases.

Las gráficas muestran aproximaciones numéricas de las soluciones. Sirven para **visualizar y contrastar** resultados teóricos, pero por sí solas no constituyen una demostración de la existencia de una bifurcación.

---

## 1. Bifurcación silla-nodo

**[Abrir simulación de silla-nodo](./silla_nodo.html)**

Se estudia la forma normal

$$
\dot{x}=r-x^2, \qquad x\in\mathbb{R}.
$$

El parámetro es $r$ y el **valor crítico es $r=0$**. Las líneas de equilibrio del gráfico temporal, los puntos del retrato de fases en la recta y las flechas de dirección permiten identificar cómo cambia el número y la estabilidad de los equilibrios.

| Parámetro | Qué ocurre | Qué observar |
|---|---|---|
| $r=-0{,}25$ | No hay equilibrios. | Todas las soluciones se desplazan hacia valores menores de $x$ mientras existen. |
| $r=0$ | Hay un equilibrio doble $x=0$, semiestable. | Las soluciones que empiezan a su derecha se acercan a $0$; las que empiezan a su izquierda se alejan. |
| $r=0{,}25$ | Aparecen dos equilibrios: $-\sqrt r$ (inestable) y $+\sqrt r$ (asintóticamente estable). | Las flechas cambian de dirección en los equilibrios y las soluciones próximas muestran su estabilidad. |

**Pregunta de análisis:** ¿Qué cambia al pasar de $r<0$ a $r>0$? ¿Por qué esta bifurcación se describe como la **creación de un par de equilibrios** al aumentar $r$?

> Nota: para ciertas condiciones iniciales las soluciones pueden abandonar rápidamente la ventana gráfica; esto no es un fallo de la simulación. La integración se detiene si alcanza el límite inferior indicado en la aplicación.

---

## 2. Bifurcación transcrítica: umbral de emisión de un láser

**[Abrir simulación del láser](./transcritica_laser.html)**

El modelo simplificado es

$$
\dot{x}=(N_0-2)x-x^2,\qquad x\geq 0.
$$

La variable $x(t)$ representa la cantidad relativa de fotones en la cavidad óptica. El parámetro $N_0$ está relacionado con la población de átomos excitados que existiría en ausencia de emisión láser, controlada por el bombeo. **No debe confundirse con el valor inicial $x(0)$.** El valor crítico es **$N_{0,c}=2$**.

| Parámetro | Equilibrios y estabilidad | Qué observar |
|---|---|---|
| $N_0=1$ | $x=0$ estable; la otra rama, $x=N_0-2=-1$, está fuera del dominio físico. | La cantidad de fotones decae hacia cero y la representación del haz pierde intensidad. |
| $N_0=2$ | Las dos ramas coinciden en $x=0$, no hiperbólico. | Las soluciones con $x(0)>0$ decaen lentamente hacia cero. |
| $N_0=3$ | $x=0$ inestable y $x=1$ asintóticamente estable. | Las soluciones positivas se aproximan a un nivel sostenido de fotones y el haz mantiene su intensidad. |

**Pregunta de análisis:** ¿Por qué hablamos de **intercambio de estabilidad** entre dos ramas de equilibrios y no de creación de nuevos equilibrios matemáticos? ¿Qué parte de la bifurcación queda fuera del dominio físico $x\geq0$?

La cavidad y los fotones dibujados son una **representación didáctica**, no un conteo literal de partículas. El modelo omite efectos como la emisión espontánea y el ruido.

---

## 3. Bifurcación de Hopf: reacción química oscilante

**[Abrir simulación de Hopf](./hopf.html)**

Se considera un modelo reducido de una reacción química oscilante (modelo de Lengyel–Epstein):

$$
\begin{cases}
\dot{x}_1=10-x_1-\dfrac{4x_1x_2}{1+x_1^2},\\[5pt]
\dot{x}_2=bx_1\left(1-\dfrac{x_2}{1+x_1^2}\right),
\end{cases}
$$

con $x_1,x_2$ concentraciones adimensionales. El parámetro es $b>0$; el equilibrio es **$(2,5)$** y el valor crítico es **$b_c=3{,}5$**.

A diferencia de los ejemplos anteriores, el espacio de estados es **bidimensional**. Observa a la vez el **retrato de fases** $(x_1,x_2)$, las **series temporales** $x_1(t)$ y $x_2(t)$ —que se dibujan progresivamente— y la representación esquemática del recipiente.

| Parámetro | Qué ocurre | Qué observar |
|---|---|---|
| $b=4$ | El equilibrio $(2,5)$ es asintóticamente estable. | La trayectoria se aproxima al equilibrio y las oscilaciones de las concentraciones se amortiguan. |
| $b=3{,}5$ | Los valores propios de la linealización son puramente imaginarios: es el valor crítico. | Compara el comportamiento cercano al equilibrio con los otros dos casos; el análisis lineal por sí solo no determina la estabilidad en este punto. |
| $b=2$ | El equilibrio es inestable y se observa una oscilación sostenida asociada a un ciclo límite estable. | La trayectoria tiende hacia una órbita cerrada; las concentraciones continúan oscilando en el tiempo. |

**Pregunta de análisis:** ¿Qué diferencia hay entre una trayectoria que **espirala hacia un equilibrio** y otra que **se aproxima a un ciclo límite**? ¿Qué cambio cualitativo aparece al disminuir $b$ y atravesar $b_c$?

El ciclo límite destacado en azul se **estima numéricamente**. Los colores y movimientos del recipiente ilustran las concentraciones calculadas, pero **no predicen el color real de los reactivos**.

---

## Conclusión para las tres simulaciones

Una **bifurcación** es un cambio cualitativo de la dinámica al variar un parámetro. Las tres aplicaciones ilustran fenómenos diferentes:

- **Silla-nodo:** aparecen o desaparecen equilibrios.
- **Transcrítica:** dos ramas de equilibrios se cruzan e intercambian estabilidad.
- **Hopf:** cambia la estabilidad de un equilibrio y, bajo las condiciones apropiadas, aparece o desaparece una familia de órbitas periódicas.

**Al terminar, debes poder explicar qué cambia en el espacio de estados y justificar por qué ese cambio no se reduce a una simple modificación cuantitativa de las soluciones.**

## Uso del repositorio

Abre `index.html` desde GitHub Pages para acceder a las tres simulaciones. Todos los archivos HTML contienen su propio código JavaScript y CSS y no necesitan bibliotecas externas. Se pueden ejecutar también de forma local con un navegador moderno.
