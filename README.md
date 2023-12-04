# <p align="center">CLUSTERING - KMEANS</p>

[Acceso a archivo Jupyter.](https://github.com/mantiads/Clustering/blob/main/clusters.ipynb)

## OBJETIVO PROYECTO

Realizar una clasificación de clientes utilizando datos socioeconómicos y comportamientos sobre contratación de productos, con el fin de identificar patrones y perfiles que ayuden en la toma de decisiones.

## DATOS

El dataset consta de dos tablas: "sociocom_unico.csv" con datos socioeconómicos y "variables productos final.csv" con información sobre el comportamiento de los clientes en productos a lo largo del tiempo.

## SELECCIÓN E INGENIERÍA DE VARIABLES

1. Se calcula la antigüedad a partir de la fecha de alta y se le asignan categorías.
2. Se categoriza la edad en grupos: Estudiantes, Trabajadores y Jubilados.
3. Variable booleana que indica si tiene productos en la última partición.
4. Se definen tres nuevas categorías para agrupar los 15 productos (“Ahorro e Inversión”, “Financiación” y “Servicios”). Para cada usuario se crea una variable por categoría que indica si el cliente ha contratado alguna vez productos de cada categoría.

## ALGORITMO Y EVALUACIÓN

Se utiliza el algoritmo Kmeans para la clasificación y, tras varias pruebas, se determina que el número óptimo de clusters que agrupa de mejor manera a los usuarios es de 12.

<p align="center">
  <img src="/img/clusters.PNG" alt="clustering">
</p>

## CLUSTERS Y PERFILES

Se crean 12 clusters, cada uno con un perfil característico que resume la situación laboral, antigüedad, nivel de productos contratados e interés en ahorro, financiación y servicios.

<p align="center">
  <img src="/img/clustering_heatmap.png" alt="clustering">
</p>

1. **Estudiante Activo Financieramente (Cluster 0):** Estudiante antiguo, tiene productos, no tiene interés en productos de ahorro e inversión ni préstamos, pero si servicios bancarios.
2. **Trabajador Activo Financieramente (Cluster 1):** Trabajador antiguo, tiene productos, no tiene interés en productos de ahorro e inversión ni préstamos, pero si servicios bancarios.
3. **Estudiante Pasivo (Cluster 2):** Estudiante antiguo, no tiene productos, no tiene interés en productos de ahorro e inversión, préstamos ni servicios bancarios.
4. **Estudiante Nuevo Activo Financieramente (Cluster 3):** Estudiante nuevo, tiene productos, no tiene interés en productos de ahorro e inversión ni préstamos, pero si servicios bancarios.
5. **Trabajador Nuevo Pasivo (Cluster 4):** Trabajador nuevo, no tiene productos, no tiene interés en productos de ahorro e inversión, préstamos ni servicios bancarios.
6. **Trabajador Antiguo Pasivo (Cluster 5):** Trabajador antiguo, no tiene productos, no tiene interés en productos de ahorro e inversión, préstamos ni servicios bancarios. 
7. **Trabajador Inversionista (Cluster 6):** Trabajador antiguo, tiene productos, tiene interés en productos de ahorro e inversión, no tiene interés en préstamos, tiene interés en servicios bancarios.
8. **Estudiante Nuevo Pasivo (Cluster 7):** Estudiante nuevo, no tiene productos, no tiene interés en productos de ahorro e inversión, no tiene interés en préstamos ni servicios bancarios.
9. **Trabajador Nuevo Activo Financieramente (Cluster 8):** Trabajador nuevo, tiene productos, no tiene interés en productos de ahorro e inversión ni préstamos, pero si servicios bancarios.
10. **Trabajador Inversionista Activo Financieramente (Cluster 9):** Trabajador antiguo, tiene productos, tiene interés en productos de ahorro e inversión, préstamos y servicios bancarios.
11. **Trabajador Antiguo Pasivo Financieramente (Cluster 10):** Trabajador antiguo, no tiene productos, no tiene interés en productos de ahorro e inversión ni préstamos, pero si en servicios bancarios.
12. **Trabajador Inversionista Activo Bancariamente (Cluster 11):** Trabajador nuevo, tiene productos, tiene interés en productos de ahorro e inversión y servicios bancarios pero no en préstamos.

<p align="center">
  <img src="/img/clustering_distri.png" alt="clustering">
</p>
