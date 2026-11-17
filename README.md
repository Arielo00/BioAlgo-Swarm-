# BioAlgo-Swarm-

Para una visualización del proyecto, por favor visita: https://arielo00.github.io/BioAlgo-Swarm-/

Optimización bioinspirada en dos frentes:

- Siete funciones del banco **CEC 2022** (Ackley, Bent Cigar, Griewank, HGBat, High Conditioned Elliptic, Rastrigin y Rosenbrock), resueltas con **algoritmos genéticos** y comparadas con un **enjambre de partículas (PSO)**.
- Cuatro diseños clásicos de ingeniería con restricciones (viga soldada, recipiente a presión, reductor de velocidad y resorte), resueltos con un **enjambre de partículas** y comparados con los resultados publicados por Cagnina, Esquivel y Coello Coello (2008).

## Contenido

| Archivo | Qué es |
|---|---|
| `index.html` | Página interactiva: del remolino de estorninos al algoritmo, los siete paisajes en 3D, el genético paso a paso, un laboratorio para enfrentar PSO y genético, la estadística de 30 corridas y el enjambre diseñando las cuatro piezas de ingeniería. Es un solo archivo, sin dependencias, en español e inglés. |
| `algoritmos_bioinspirados_cec2022.ipynb` | Cuaderno con fórmulas, superficies, los programas, un genético unificado, PSO, búsqueda aleatoria, la comparación estadística en 2 y 10 variables y los cuatro problemas de ingeniería con 30 corridas cada uno. |
| `codigo/` | Los programas en Python. |

## Programas

| Problema | Programa | Algoritmo |
|---|---|---|
| Ackley | `ackley_a.py` | Genético: cruce aritmético, mutación gaussiana |
| Ackley | `pso_ackley.py` | Enjambre de partículas, versión original (sin inercia) |
| Bent Cigar | `bentcigar.py` | Genético: un punto, mutación uniforme |
| Griewank | `griewank_k.py` | Genético con parada temprana y 30 corridas |
| HGBat | `HGBatFunction.py` | Genético: un punto, mutación uniforme |
| High Conditioned Elliptic | `HighConditionedEllipticFunction.py` | Genético: un punto, mutación uniforme |
| Rastrigin | `rastrigin.py` | Genético: un punto, mutación uniforme |
| Rosenbrock | `rosenbrock_k.py` | Genético con parada temprana y 30 corridas |
| Viga soldada, recipiente a presión, reductor de velocidad, resorte | `pso_ingenieria.py` | Enjambre con reglas de factibilidad, variables discretas e inercia de 0.9 a 0.4 |

Con 40 partículas y 600 generaciones (24 000 evaluaciones, el presupuesto del artículo), `pso_ingenieria.py` alcanza el mejor diseño conocido en los cuatro problemas: 1.724852, 6059.714, 2996.348165 y 0.012667.

Requisitos: Python 3, `numpy`, `matplotlib` y, para el cuaderno, `pandas`.

## Referencias

- Banco CEC 2022 en Kaggle: https://www.kaggle.com/code/kooaslansefat/cec-2022-benchmark
- Kennedy, J. y Eberhart, R. (1995). *Particle swarm optimization.*
- Reynolds, C. (1987). *Flocks, herds and schools: a distributed behavioral model.*
- Ballerini, M. et al. (2008). *Interaction ruling animal collective behavior depends on topological rather than metric distance.* PNAS.
- Cagnina, L., Esquivel, S. y Coello Coello, C. (2008). *Solving engineering optimization problems with the simple constrained particle swarm optimizer.* Informatica 32, 319–326.
- Shi, Y. y Eberhart, R. (1998). *A modified particle swarm optimizer.*
- Video del remolino de estorninos: Disquete Magazine, https://www.youtube.com/watch?v=qbXzYBIh1Ho
