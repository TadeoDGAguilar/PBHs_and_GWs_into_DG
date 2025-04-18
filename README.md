# PBH Merger Model: Multi-Species Interactions in Dense Clusters

Este repositorio contiene un código numérico en Python para modelar la dinámica de **fusiones de agujeros negros primordiales (PBHs)** en cúmulos densos, considerando múltiples especies generacionales. Está basado en el escenario descrito por García-Bellido et al. (2021, 2022) y extiende la estimación de tasas de fusión y emisión de ondas gravitacionales (GWs) para incluir **interacciones entre PBHs de distinta generación**, lo cual es esencial para modelar **fusiones jerárquicas** y **encuentros hiperbólicos cercanos** (CHEs).

---

## 🎯 Objetivo

Evaluar las tasas de fusión de PBHs en cúmulos con perfiles tipo Plummer, calculando:

- La **tasa de interacciones** para todas las combinaciones posibles entre especies (0G–0G, 0G–1G, 1G–1G),
- La **potencia total radiada** en ondas gravitacionales,
- El **número esperado de colisiones** por cascarón,
- La evolución de **energía y masa en el cúmulo** por interacción.

---

## ✅ Versión actual

La versión actual del código realiza lo siguiente:

1. **Define el perfil de densidad tipo Plummer** para un cúmulo denso de PBHs de masa total conocida.
2. Divide el cúmulo en $N_\text{shells}$ cascarones esféricos para evaluar localmente las tasas de interacción.
3. Define dos especies de PBHs:
   - `0G`: PBHs primordiales originales, de masa fija $M_\text{PBH}$.
   - `1G`: productos de fusión de PBHs 0G–0G, de masa final calculada tras pérdida de energía gravitacional.
4. Calcula **todas las combinaciones con reemplazo** entre especies: (0G–0G), (0G–1G), (1G–1G).
5. Para cada combinación:
   - Evalúa la **densidad numérica**, **velocidades medias cuadráticas**, y **sección eficaz** de fusión.
   - Calcula la **potencia total** radiada por especie en cada cascarón.
   - Estima el **número de eventos esperados** por cascarón y por tipo de interacción.

6. Imprime los resultados en formato tabular, incluyendo:
   - Nombre de la combinación,
   - Potencia radiada,
   - Número total de colisiones,
   - Tiempo característico de generación.

---

## 📦 Requisitos

- Python 3.8+
- Bibliotecas:
  - `numpy`
  - `scipy`
  - `matplotlib`
  - `seaborn`
  - `astropy`
  - `itertools`

---

## 📍 Próximos pasos

- Implementar la **acumulación temporal de potencia radiada** para graficar la evolución de $\Omega_{\mathrm{GW}}(t)$.
- Incorporar nuevas generaciones (2G, 3G) con control de masas y pérdidas energéticas.
- Calcular la **distribución espectral de energía** para CHEs y BBHs por especie.
- Visualizar la evolución jerárquica con gráficos animados.

---

## ✏️ Autor

**Tadeo Dariney Gómez Aguilar**  
Doctorado en Ciencias Físicas  
Instituto de Ciencias Físicas, UNAM

---

## 📚 Referencias

- J. García-Bellido, S. Jaraba, S. Kuroyanagi, *The SGWB from close hyperbolic encounters of PBHs in dense clusters*, Phys. Dark Univ. 36 (2022), [arXiv:2109.11376](https://arxiv.org/abs/2109.11376)
- E. Erfani, T. D. Gómez-Aguilar, J. C. Hidalgo, *Hierarchical merger of primordial black holes in dwarf galaxies*, [arXiv:2205.08906](https://arxiv.org/abs/2205.08906)
- M. Caldarola et al., *Effects of orbital precession on hyperbolic encounters*, [arXiv:2307.00915](https://arxiv.org/abs/2307.00915)

