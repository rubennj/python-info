# Información sobre Python

- [GLOSARIO](#glosario)
  * [Python](#python-cheatsheet)
  * [Spyder](#spyder)
  * [IPython](#ipython)
  * [Conda](#conda)
  * [Miniconda](#miniconda)
  * [Anaconda](#anaconda)
- [LIBRERIAS](#librerias)
  * [Scipy](#scipy)
  * [Numpy](#numpy-cheatsheet)
  * [Matplotlib](#matplotlib-cheatsheet)
  * [Pandas](#pandas-cheatsheet)
  * [PIL/Pillow](#pil-pillow)
- [RECURSOS ON-LINE](#recursos-on-line)
  * [Cursos](#cursos)
  * [Tutoriales](#tutoriales)
  * [Herramientas para datos](#herramientas-para-datos)
    + [Jupyter](#jupyter)
    	- [Binder](#binder)
    	- [Google Colab](#google-colab)
    	- [JupyterHub](#jupyterhub)
    + [Dash](#dash)
  * [Graphing (Matplotlib)](#graphing--matplotlib-)
  * [Herramientas para codigo](#herramientas-para-codigo)
    + [Linters - Code syle/quality](#linters---code-syle-quality)
    + [Documentation](#documentation)
    + [Testing](#testing)
    + [Refactoring](#refactoring)
    + [GitHub](#github)
      - [pre-commit](#pre-commit)
      - [.gitignore](#gitignore)
    + [Argparse](#argparse)
    + [Archivo Config](#archivo-config)
    + [Packaging](#packaging-crear-librerías)
    * [Archivo README](#archivo-readme)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

## GLOSARIO
Breve explicación de nombres relacionados con los proyectos que sostienen el mundo Científico-Python (SciPy) desde un punto de vista de una persona que conoce Matlab.

### Python [[cheatsheet]](python-cheatsheet_mementopython3-english.pdf)
Es el lenguaje. Sintaxis muy parecida a Matlab.
* Mucho más potente y capaz de realizar más cosas y en general más rápido que Matlab.
* El lenguaje y las librerías son libres y gratuitas. Muchas se actualizan rápido y de verdad.
* En su conjunto aun tiene partes que no están tan maduras como Matlab, pero suficiente como para trabajar sin problemas. Otras partes superan con creces a Matlab.	
* Es un lenguaje basado en scripts. No se tiene que compilar para ejecutarlo, como Matlab cuando se ejecuta en terminal. Se puede ejecutar un script en otro PC muy fácilmente y editarlo de forma instantánea. Especialmente conveniente para controlar tareas automáticas. Matlab tiene que compilarlo y es muy engorroso.
* Se puede ejecutar de forma interactiva, lanzando `python` desde cmd sin ningún parámetro.
* Se pueden crear ejecutables.

### Spyder
Es un IDE (Integrated Development Environment), el programa para escribir/ejecutar scripts, manipular datos y depurar código.
* Es el que hay que EJECUTAR para trabajar!

### IPython
Es una versión mejorada de la terminal de Python. Básicamente aparece en Spyder como terminal por defecto. Permite autocompletado, sugiere nombres de funciones, lleva control de historial, número de líneas...

### Conda
Gestor de librerías. Permite instalar, quitar, actualizar, listar.
Mediante el comando `conda install <libreria>` desde `cmd` se instalan las librerías necesarias.
#### Canales
Es la fuente de donde vienen los paquetes. Existe un canal `default` que se toma por defecto y pertenece/actualiza Anaconda, pero que no siempre está actualizado al 100%.
#### Conda-forge
Es un canal estándar de facto mantenido por la comunidad que es actualizado por los propios desarrolladores de las librerías.
* Usar este canal por defecto ejecutando estos comnados:  
`conda config --add channels conda-forge`  
`conda config --set channel_priority strict`

### Miniconda
*_OPCIÓN RECOMENDADA_*
Es una distribución de Python mínima, que solo instala Python + conda (gestor de librerias).
https://docs.conda.io/en/latest/miniconda.html
* Ver la última versión en la web!
* Hay que elegir Python 2 o 3. Elegir 3, ya que la v. 2 está sin soporte.

### Anaconda
Es una distribución de Python adecuada al mundo científico con muchas librerías. Resulta muy pesada, mejor usar miniconda.
https://www.anaconda.com/distribution/
* Es también el nombre de la empresa que crea y mantiene esta distribución.

## LIBRERIAS
Para procesar, visualizar y representar datos existen librerías "científicas", como las de Matlab, aunque algunas son para obtener funcionalidades que vienen por defecto en Matlab.
* Hay que importar al principio de cada script cada libreria explícitamente, para mantener un control de los nombres de cada librería (espacio de nombres).
> No usar `import *` https://www.geeksforgeeks.org/why-import-star-in-python-is-a-bad-idea/
* Si no están ya instaladas, se tienen que instalar desde la linea de comandos de Windows `cmd` con el comando `conda install "nombre_libreria"`. Si no estuviera en los repositorios de Anaconda, habría que instalarlas mediante `conda install conda-forge::"nombre_libreria"` o finalmente con `pip install "nombre_libreria"`. Si no existe como librería, se debería usar directamente como paquete de Python, en un fichero *.py
* ACTUALIZACION! Usar canal `conda-forge` por defecto (ver [Conda](#conda))
* Control de librerias: Se pueden actualizar, instalar, desinstalar desde linea de comandos: 'cmd'.p. ej. 'conda update spyder'

Las más usuales son:
### Scipy
Funciones de cálculo numérico, muchas tienen la misma sintáxis que en Matlab
	p. ej. trapz()

### Numpy [[cheatsheet]](Numpy_Python_Cheat_Sheet.pdf)
Implementa tipo de dato 'array' que permite operaciones vectoriales, tipo Matlab. No necesita la sintaxis con punto típica de Matlab (.*, ...). Una vez creado (o leido) el objeto Numpy la sintaxis es transparente.
	p. ej. a = b * c, donde b y c son vectores.

### Matplotlib [[cheatsheet]](<matplotlib cheatsheets.pdf>)
Objetos y funciones para graficar, tiene sintaxis similar a Matlab. Aunque similar, algunas cosas son más claras.

### Pandas [[cheatsheet]](Pandas_Cheat_Sheet.pdf)
Objetos tipo hoja_cálculo y métodos anexos. Especialmente útil para datos tipo tabla y aun más interesante para Series Temporales. Tiene una sintaxis muy intuitiva y simplificada, especialmente interesante para leer datos.
p. ej.
* Lee fichero .csv, delimitado por tabs, toma como índice de tabla las dos primeras columnas (fecha y hora) y los valores '-' son tomados como 'NaN'
```
mad11 = pd.read_csv(path + 'madrid2011.txt', delimiter='\t', date_parser=parserdatetime, parse_dates=[[0, 1]], index_col=0, na_values='-')
```
* Toma la variable B y Bmj de mad11 (valores minutales) y devuelve la suma resampleada a frecuencia mensual.
```
eff_esp11_men = mad11.Bmj.resample('M', how='sum') / mad11.B.resample('M', how='sum')
```
* OJO copia DataFrames: https://stackoverflow.com/questions/27673231/why-should-i-make-a-copy-of-a-data-frame-in-pandas
* Tricks & Features You May Not Know: https://realpython.com/python-pandas-tricks/

### PIL/Pillow
Manipulación de imágenes.

## RECURSOS ON-LINE
Listado de links con información útil para Python. _El repositorio contiene documentos también útiles_

* Nature - Programming: Pick up Python - A powerful programming language with huge community support
https://www.nature.com/news/programming-pick-up-python-1.16833

### Cursos
* Curso muy ameno, para aprender el lenguaje Python haciendo, hay app
https://www.sololearn.com/Course/Python/
* Software Carpentry realiza talleres sobre programación y publican el material
https://software-carpentry.org/lessons/index.html

### Tutoriales
* Buen tutorial general 
https://docs.python-guide.org/

* Tutoriales temáticos para (casi) todas las características/opciones/librerias del lenguaje
https://realpython.com/

* Guia Python Científico
http://scipy-lectures.org/

* Transitioning from MATLAB to Python
1. https://leportella.com/english/2018/07/22/10-tips-matlab-to-python.html
2. https://hub.gke.mybinder.org/user/gestaltrevision-thon_for_visres-ones2sck/notebooks/Part3/Part3_Scientific_Python.ipynb
3. https://www.enthought.com/wp-content/uploads/Enthought-MATLAB-to-Python-White-Paper.pdf

* Pythonic loops (olvídate de los loops con índice!)
1. https://dbader.org/blog/pythonic-loops
2. https://mlwhiz.com/blog/2019/04/22/python_forloops/

### Herramientas para datos
#### Jupyter
* Presentar datos+código en vivo.
* IDE en web. Dos versiones: _classic_ y _lab_
* Basado en ficheros notebook (.ipynb)
* Conceptos básicos https://nbviewer.jupyter.org/github/jupyter/notebook/blob/master/docs/source/examples/Notebook/Notebook%20Basics.ipynb
1. https://jupyter.org/
2. https://mybinder.org/v2/gh/bloomberg/bqplot/1da9ae2fffcbe317b6b27f6ed4f6d6c8db283452 - Ejemplo en acción
3. https://github.com/losc-tutorial/quickview - Repositorio con Jupyter notebook sobre gravitational waves

* Existen varias alternativas para la ejecución en entorno web: https://www.dataschool.io/cloud-services-for-jupyter-notebook/

##### Binder
* Crea espacio de trabajo en un servidor remoto para ejectuar en vivo Jupyter notebooks, sin necesidad de instalación local.
* Un repositorio tipo GitHub se puede convertir en un espacio de trabajo ejecutable.
1. https://jupyter.org/binder - Información
2. https://mybinder.org/ - Web app para lanzarlo

##### Google Colab
* Similar a Binder. La carga del servicio es notablemente más rápida.
* Orientado y con recursos de Google para ejecutar Machine/Deep Learning
* https://colab.research.google.com/
* Ejemplo tutorial https://colab.research.google.com/github/tensorflow/examples/blob/master/courses/udacity_intro_to_tensorflow_for_deep_learning/l01c01_introduction_to_colab_and_python.ipynb

##### JupyterHub
* Permite crear tu propia nube para servir notebooks, como Binder en privado.
* Muy interesante para clase, evita que los estudiantes se tengan que instalar nada.
* https://jupyter.org/hub

#### Dash
Servidor web para presentar datos interactivamente (by Plot.ly)
https://dash-gallery.plotly.host/Portal/ (Galería)

### Graphing (Matplotlib)
La librería más potente y que permite crear gráficas bien acabadas para publicaciones es MATPLOTLIB (MPL):
* Tutorial básico (rápido) https://towardsdatascience.com/matplotlib-tutorial-learn-basics-of-pythons-powerful-plotting-library-b5d1b8f67596
* Guía (más completa y clara) https://realpython.com/python-matplotlib-guide/
* Guía oficial (más densa) https://matplotlib.org/tutorials/introductory/pyplot.html#sphx-glr-tutorials-introductory-pyplot-py
* MPL Cheatsheets (interesante el de Tips&Tricks) https://github.com/matplotlib/cheatsheets

PANDAS de hecho implementa métodos .plot() que llaman a MPL para visualizaciones rápidas de DF/Series. Para pulir la gráfica hay que llamar a métodos directamente de MPL.
* Tutorial básico (rápido) http://queirozf.com/entries/pandas-dataframe-plot-examples-with-matplotlib-pyplot
* Guía oficial (más densa) https://pandas.pydata.org/pandas-docs/stable/user_guide/visualization.html

### Herramientas para codigo
* (Breve) Listado herramientas https://opensource.com/article/18/7/7-python-libraries-more-maintainable-code
* Sitio con cursos https://software-carpentry.org/lessons/index.html

#### Linters - Code syle/quality
PEP8
* https://realpython.com/python-code-quality/
* https://realpython.com/python-pep8/
* https://docs.python-guide.org/writing/style/

* Ejemplo: pycodestyle (_comprueba código_), autopep8 (_formatea código_)
> Desde consola spyder: `!autopep8 -i file.py` o `!autopep8 -i .`

#### Documentation
PEP 257
* https://realpython.com/documenting-python-code/
* https://docs.python-guide.org/writing/documentation/

* Ejemplo: pydocstyle (_comprueba docstring_), docformatter (_formatea docstring_)
* Info sobre documentar https://realpython.com/documenting-python-code/

#### Testing
* https://realpython.com/python-testing/
* https://docs.python-guide.org/writing/tests/

* Ejemplo: pytest
> Desde consola spyder: `!pytest .`

#### Refactoring
No es realmente una herramienta si no una buena práctica. La idea es limpiar y mejorar la legibilidad del código, muchas veces reordenándolo.\
https://realpython.com/python-refactoring/

#### GitHub
Repositorio distribuido para código y datos usando protocolo `git`. Utilizar herramienta [`GitHub Desktop`](https://desktop.github.com/) para sincronizar repositorio local y remoto.
* 10 min tutorial https://guides.github.com/activities/hello-world/
* Tutorial https://www.edureka.co/blog/how-to-use-github/
* Tutorial [Real Python] https://realpython.com/python-git-github-intro/
* Introdución a GitHub https://github.com/oscarperpinan/intro_github
* A successful Git branching model https://nvie.com/posts/a-successful-git-branching-model/
* How to Write a Git Commit Message https://chris.beams.io/posts/git-commit/
> ##### pre-commit
> Antes de formalizar un `commit` [pre-commit](https://pre-commit.com/) ejecuta automáticamente tareas tales como un linter para formatear el código.

> ##### .gitignore
> Para evitar sincronizar ciertos archivos hay que rellenar el fichero `.gitignore`. Ver https://swcarpentry.github.io/git-novice-es/06-ignore/
> Si ya se han sincronizado previamente, usar `git rm -r --cached [file]`

#### Argparse
Librería estándar para crear CLI (Command Line Interface)
* Tutorial https://realpython.com/command-line-interfaces-python-argparse
* Ejemplo código ISI https://github.com/isi-ies-group/scripts-servidor_helios/blob/master/genera_fichero_meteo.py

#### Archivo Config
Archivo externo adicional que incluye información de configuración a leer (parsear) por una librería.
* Vistazo a varios tipos https://hackersandslackers.com/simplify-your-python-projects-configuration/
* `configparser` librería estándar para ficheros `.ini`
    * Ejemplo código ISI https://github.com/isi-ies-group/meteocheck/blob/master/meteocheck/meteocheck_meteo_stations_example.ini
* `pyaml` librería externa para ficheros `.yaml`
    * Ejemplo código ISI https://github.com/isi-ies-group/pygeonica/blob/master/pygeonica/pygeonica_config.yaml

### Packaging (crear librerías)
Generar paquetes de Python, para instalar desde `pip`
* Tutorial https://python-packaging.readthedocs.io/
* Incluso se puede instalar desde un repositorio: `pip install --upgrade git+https://github.com/isi-ies-group/cpvlib.git`
* `Cookicutter` es una herramienta para generar el andamio de una librería: https://towardsdatascience.com/cookiecutter-creating-custom-reusable-project-templates-fc85c8627b07

### Archivo README
Consejos https://dbader.org/blog/write-a-great-readme-for-your-github-project
