# The Scalenity of a Polygon
*(L'escalenitat d'un polígon)*

**Baccalaureate research project (Treball de Recerca)** — Institut Baix a Mar, Vilanova i la Geltrú, 2024/2025
**Author:** Alan Muros Tapia · **Tutor:** Jordi Font Gonzàlez
**Language:** report in Catalan (with an English abstract); this summary in English

<!-- Optional: add a picture exported from the report (create an "images" folder), e.g.
![Geometric loci](images/geometric-loci.png) -->

## Abstract

This project explores the concept of *scalenity* through several definitions proposed in an article from *The American Mathematical Monthly*. One definition is studied in depth: its ability to grade scalene triangles, the possible values of the scalenity coefficient $k$, and the geometric locus of the third vertex $C$ for each value of $k$. Two further definitions are analysed more briefly: both are shown to exclude isosceles and equilateral triangles, and the maximum range of $k$ is determined for each.

## Starting point

Problem E 1069, *"How un-isosceles can a triangle be?"*, *The American Mathematical Monthly* 61(1), 49–50 (1954). The question: how can we measure, and order, how far a scalene triangle is from being isosceles?

## Main results

Notation: sides $a \ge b \ge c$, opposite to angles $\alpha \ge \beta \ge \gamma$.

**Definition I — ratios of sides:** $k=\min\left(\dfrac{a}{b},\dfrac{b}{c}\right)$

- Isosceles and equilateral triangles give $k=1$; scalene triangles give $k>1$, so the definition grades scalene triangles.
- The triangle inequality gives $k^2 \le k+1$, hence $k\in[1,\varphi)$, where $\varphi$ is the golden ratio (extreme case: sides $\varphi^2,\ \varphi,\ 1$).
- With $c=1$, $A=(0,0)$, $B=(1,0)$, the vertex $C$ lies on circular arcs for each value of $k$. Six cases arise from the possible orderings of the sides. For example, when $a=kb$ the locus lies on the circle with centre $\left(-\tfrac{1}{k^2-1},0\right)$ and radius $\tfrac{k}{k^2-1}$.
- The union of all arcs, and level curves for increasing values of $k$, give a visual grading of scalene triangles (built in GeoGebra).

**Definition II — normalised side differences:** $k=\min\left(\dfrac{a-b}{a+b+c},\dfrac{b-c}{a+b+c}\right)$

- Isosceles and equilateral triangles give $k=0$; scalene triangles give $k>0$.
- Range: $k\in[0,1/6)$.

**Definition III — angle ratios:** $k=\min\left(\dfrac{\alpha}{\beta},\dfrac{\beta}{\gamma}\right)$

- Isosceles and equilateral triangles give $k=1$; scalene triangles give $k>1$.
- Range: $k\in[1,\infty)$ (triangles close to a flat segment give arbitrarily large $k$).

## Open directions (not covered in the report)

Extension to polygons with more sides and to three-dimensional figures, and the same study in metrics other than the Euclidean one.

## Files

| File | Description |
|---|---|
| [`scalenity-report.pdf`](scalenity-report.pdf) | Full report, ~50 pages (Catalan, with English abstract) |

Interactive GeoGebra applet: [open it here](https://www.geogebra.org/YOUR-APPLET-LINK)
