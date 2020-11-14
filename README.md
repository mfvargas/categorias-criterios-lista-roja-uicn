# Categorías y criterios de la Lista Roja de la UICN
Este repositorio contiene un [Jupyter Notebook](https://jupyter.org/), desarrollado en el lenguaje de programación [Python](https://www.python.org/), para la aplicación de las [categorías y criterios](https://www.iucn.org/es/content/categor%C3%ADas-y-criterios-de-la-lista-roja-de-la-uicn-versi%C3%B3n-31-segunda-edici%C3%B3n) de la [Lista Roja de la Unión Internacional para la Conservación de la Naturaleza (UICN)](https://www.iucnredlist.org/es/).

El _notebook_ recibe como entrada una lista de nombres científicos de especies y genera para cada uno:
- Un archivo CSV con los registros de presencia.
- Un mapa interactivo de distribución basado en los registros de presencia.
- Un mapa interactivo de registros de presencia agrupados (_clustered_).
- Un registro en otro archivo CSV, que resume los resultados de la evaluación, con las siguientes columnas:
  - La extensión de presencia de la especie.
  - El área de ocupación de la especie.
  - La altitud mínima y la altitud máxima en las que la especie ha sido reportada.
  - La lista de países en los que está presente la especie.
  - La lista de áreas protegidas en las que está presente la especie.
  - Los enlaces a los otros mapas y archivos.

## Creación de un ambiente Conda, clonación del repositorio y ejecución del notebook
Se recomienda ejecutar estos comandos desde la línea de comandos de [Anaconda](https://www.anaconda.com/), en el directorio en el que desea almacenar el repositorio clonado.
```shell
# Actualización de Conda
conda update -n base -c defaults conda

# Creación del ambiente
conda create -n categorias-criterios-lista-roja-uicn

# Activación del ambiente
conda activate categorias-criterios-lista-roja-uicn

# Instalación de módulos
conda config --env --add channels conda-forge
conda config --env --set channel_priority strict
conda install jupyter scipy geopandas folium fiona

# Clonación del repositorio (debe sustituir la palabra "usuario" por su nombre de usuario en GitHub)
git clone https://github.com/mfvargas/categorias-criterios-lista-roja-uicn.git
cd categorias-criterios-lista-roja-uicn

# Ejecución de Jupyter Notebook
jupyter notebook categorias-criterios-lista-roja-uicn.ipynb

# Actualización del repositorio
$ git add .
$ git commit -m "Actualizar notebook"
$ git push

# Desactivación del ambiente Conda
$ conda deactivate
```
