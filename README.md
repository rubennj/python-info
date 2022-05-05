# Información sobre Python
- [GLOSARIO](#glosario)
  * [Python](#python-cheatsheet-1-cheatsheet-2)
    + [Terminologia](#terminologia)
    + [Python vs Matlab](#python-vs-matlab)
  * [IDE - Spyder](#ide---spyder)
    + [Otros IDEs interesantes](#otros-ides-interesantes)
  * [IPython](#ipython)
  * [Conda](#conda)
    + [Canales](#canales)
    + [Conda-forge](#conda-forge)
  * [Miniconda](#miniconda)
  * [Anaconda](#anaconda)
- [CURSOS](#cursos)
- [TUTORIALES](#tutoriales)
- [LENGUAJE - PECULIARIDADES](#lenguaje---peculiaridades)
  * [Variables](#variables)
  * [Estilo](#estilo)
  * [Formateo texto](#formateo_texto)
  * [Bucles](#bluces)
  * [Modismos (idioms)](#modismos--idioms-)
  * [Context manager & with](#context-manager---with)
  * [List comprehension](#list-comprehension)
  * [Zip - iteracion paralela](#zip---iteracion-paralela)
  * [Funcion lambda](#funcion-lambda)
  * [Decorador funciones](#decorador-funciones)
  * [Operador ternario (condicional)](#operador-ternario--condicional-)
  * [Generadores (yield)](#generadores--yield-)
  * [args y kwargs](#args-y-kwargs)
  * [Redondeo](#redondeo)
  * [Excepciones](#excepciones)
  * [Clases](#clases)
  * [Break, continue y pass](#break,-continue-y-pass)
  * [Encadenamiento operadores comparacion](encadenamiento-operadores-comparacion)
  * [Underscore - uso sintactico](underscore---uso-sintactico)
- [LIBRERIAS](#librerias)
  * [Scipy](#scipy)
  * [Numpy](#numpy-cheatsheet)
  * [Matplotlib](#matplotlib-cheatsheet)
  * [Pandas](#pandas-cheatsheet-1-cheatsheet-2	)
  * [PIL-Pillow](#pil-pillow)
- [HERRAMIENTAS PARA DATOS](#herramientas-para-datos)
  * [Jupyter](#jupyter)
    + [Binder](#binder)
    + [Google Colab](#google-colab)
    + [JupyterHub](#jupyterhub)
    + [JupyterLite](#jupyterlite)
  * [Dash](#dash)
  * [Streamlit](#streamlit)
  * [PyScript](#pyscript)
- [APP HOSTING](#app-hosting)
  * [Heroku](#heroku)
  * [PythonAnywhere](#pythonanywhere)
  * [Trinket](#trinket)
- [GRAPHING (Matplotlib)](#graphing--matplotlib-)
- [HERRAMIENTAS PARA CODIGO](#herramientas-para-codigo)
  * [Linters - Code syle/quality](#linters---code-syle-quality)
  * [Documentation](#documentation)
  * [Testing](#testing)
  * [Refactoring](#refactoring)
  * [GitHub](#github)
    + [pre-commit](#pre-commit)
    + [.gitignore](#gitignore)
    + [GitHub Actions](#github-actions)
  * [Argparse](#argparse)
  * [Archivo Config](#archivo-config)
- [PACKAGING (crear librerías)](#packaging-crear-librerias)
- [Archivo README](#archivo-readme)
- [API](#api)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

_Este repositorio [https://github.com/isi-ies-group/python-info] contiene documentos útiles. Ver listados de fichero arriba_.  

## GLOSARIO
Breve explicación de nombres relacionados con los proyectos que sostienen el mundo Científico-Python (SciPy) desde un punto de vista de una persona que conoce Matlab.

### Python [[cheatsheet 1]](python-cheatsheet_mementopython3-english.pdf) [[cheatsheet 2]](<python_cheat_sheet by Arianne Colton and Sean Chen.pdf>)
Es el lenguaje, a diferencia de otros conceptos del entorno **Python** que se detallan más adelante.
* Es un lenguaje multiplataforma, más compacto, más legible, más fácil de depurar pero menos rápido, menos voluminoso y con menos control de la máquina respecto a C/C++.
* El lenguaje y las librerías son libres y gratuitas. Las más importantes son ya estándares de facto y se actualizan rápido.
* Es un lenguaje interpretado, basado en scripts. No se tiene que compilar para que se ejecute el código.
* Se puede ejecutar un script en otro PC muy fácilmente y editarlo de forma instantánea. Especialmente conveniente para controlar tareas automáticas.
* Se puede ejecutar de forma interactiva, lanzando `python` desde la línea de comando `cmd` sin ningún parámetro.
* Se pueden crear ejecutables mediante librerías.

#### Terminologia
https://realpython.com/lessons/scripts-modules-packages-and-libraries/#description
* Un **script** es un archivo de Python destinado a ser ejecutado directamente. Cuando se ejecuta, debe hacer algo. Esto significa que los scripts contendrán a menudo código escrito fuera del ámbito de cualquier clase o función.
* Un **módulo** es un archivo de Python destinado a ser importado en scripts u otros módulos. A menudo define miembros como clases, funciones y variables destinadas a ser utilizadas en otros archivos que lo importan.
* Un **paquete** es una colección de módulos relacionados que trabajan juntos para proporcionar cierta funcionalidad. Estos módulos están contenidos en una carpeta y pueden ser importados como cualquier otro módulo. Esta carpeta contendrá a menudo un archivo especial __init__ que indica a Python que es un paquete, que puede contener más módulos anidados en subcarpetas
* Una **biblioteca** es un término paraguas que significa vagamente "un paquete de código". Estos pueden tener decenas o incluso cientos de módulos individuales que pueden proporcionar una amplia gama de funcionalidad.

#### Python vs Matlab
* https://realpython.com/matlab-vs-python/  
* https://numpy.org/doc/stable/user/numpy-for-matlab-users.html

* Python es un lenguaje de propósito general, mientras que Matlab está enfocado a ingeniería.
* Ambas sintaxis son muy parecidas.
* Ambos se pueden usar en entornos REPL (https://elpythonista.com/python-shell-repl) muy útiles para prototipar.
* Python es mucho más potente, capaz de realizar más cosas y en general más rápido que Matlab.
* Python aun tiene partes que no están tan maduras como Matlab (IDE, algunas librerías vs toolkits), pero suficiente como para trabajar sin problemas. Otras partes (potencia lenguaje, librerías) superan con creces a Matlab.
* Pyton no tiene una alternativa madura a Simulink.  
* Son interoperables: https://es.mathworks.com/matlabcentral/fileexchange/72852-using-matlab-with-python?s_tid=FX_rc1_behav

### IDE - Spyder
Es un IDE (Integrated Development Environment), el programa para escribir/ejecutar scripts, manipular datos y depurar código.
* Es el que hay que EJECUTAR para trabajar! - https://www.spyder-ide.org/
* Instalación recomendada [2021-04], usar [instalador individual](http://docs.spyder-ide.org/current/installation.html#standalone-installers-ref). No recomiendan instalarlo como paquete de conda dentro del environment de trabajo por defecto, usando [`conda install spyder`](http://docs.spyder-ide.org/current/installation.html).
 	* Hay que apuntar Spyder al environment de conda que usemos por defecto con todos los paquetes que usemos de forma **explícita**: http://docs.spyder-ide.org/current/faq.html#using-existing-environment

#### Otros IDEs interesantes
* [Visual Studio Code](https://code.visualstudio.com/)
* [PyCharm](https://www.jetbrains.com/es-es/pycharm/)
* [Gitpod](https://www.gitpod.io/)
* Jupyter, ver sección [Jupyter](#jupyter)

### IPython
Es una versión mejorada de la terminal de Python.  
* Básicamente aparece en Spyder como terminal por defecto, aunque se puede lanzar desde `cmd` con el comando `ipython`.
* Permite autocompletado, sugiere nombres de funciones, lleva control de historial, número de líneas...
* https://ipython.readthedocs.io/en/stable/interactive/tutorial.html

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
Conda vs Miniconda vs Anaconda https://ichi.pro/assets/images/max/724/1*O5Jgl-KFuvUyujAZhXHYlQ.png  
Es una distribución de Python mínima, que solo instala Python + conda (gestor de librerias).
https://docs.conda.io/en/latest/miniconda.html
* Ver la última versión en la web!
* Hay que elegir Python 2 o 3. Elegir 3, ya que la v. 2 está sin soporte.

### Anaconda
Es una distribución de Python adecuada al mundo científico con muchas librerías. Resulta muy pesada, mejor usar miniconda.
https://www.anaconda.com/distribution/
* Es también el nombre de la empresa que crea y mantiene esta distribución.

## CURSOS
* Curso muy ameno, para aprender el lenguaje Python haciendo, hay app
https://www.sololearn.com/Course/Python/
* Software Carpentry realiza talleres sobre programación y publican el material
https://software-carpentry.org/lessons/index.html

## TUTORIALES
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

## LENGUAJE - PECULIARIDADES

### Variables
* Tutorial variables https://realpython.com/python-variables/
* Nombres y referencias https://nedbatchelder.com/text/names.html
* Tipos de datos https://pynative.com/wp-content/uploads/2021/02/python-data-types.jpg
* Mapa mental tipos de datos https://devopedia.org/images/article/41/4737.1513052765.jpg
* Paso a funciones https://stackoverflow.com/questions/986006/how-do-i-pass-a-variable-by-reference

### Estilo
PEP 8
* Ver sección [linter](#linter)
* https://docs.python-guide.org/writing/style

### Formateo texto
* https://realpython.com/python-string-formatting/

### Bucles
Pythonic loops (olvídate de los loops con índice!)
* https://dbader.org/blog/pythonic-loops
* https://mlwhiz.com/blog/2019/04/22/python_forloops/

### Modismos (idioms)
* Idiomatic Python https://jerry-git.github.io/learn-python3/#idiomatic-python
* Consejos con idioms https://hackernoon.com/going-beyond-the-idiomatic-python-a321b6c6a5e6
* Ejemplos peor->mejor https://gist.github.com/0x4D31/f0b633548d8e0cfb66ee3bea6a0deff9

### Context manager & with
* https://realpython.com/python-with-statement/

### List comprehension
* https://realpython.com/list-comprehension-python/

```python
sentencia = "el rápido zorro marrón salta sobre el perro perezoso"
palabras = sentencia.split()
longitud_palabra = []
for palabra in palabras:
      if palabra != "el":
          longitud_palabra.append(len(palabra))
```
vs
```python
longitud_palabras = [len(palabra) for palabra in palabras if palabra != "el"]
```

### Zip - iteracion paralela
* https://realpython.com/python-zip-function/

### Funcion lambda
* https://realpython.com/python-lambda/

### Decorador funciones
* https://realpython.com/primer-on-python-decorators/

### Operador ternario (condicional)
* https://realpython.com/python-conditional-statements/#conditional-expressions-pythons-ternary-operator

### Generadores (yield)
* https://realpython.com/introduction-to-python-generators/

### args y kwargs
* https://realpython.com/python-kwargs-and-args/

### Redondeo
* https://realpython.com/python-rounding/
* Python redondea según el convenio tipico en computación según el IEEE 754: por proximidad unbiased, prefiriendo en el caso límite los resultados pares.
```python
>>> round(7.5)
8
>>> round(8.5)
8
```

### Excepciones
* https://realpython.com/python-exceptions/

### Clases
* https://realpython.com/python3-object-oriented-programming/
* Data classes: https://realpython.com/python-data-classes/

### Break, continue y pass
* https://www.digitalocean.com/community/tutorials/how-to-use-break-continue-and-pass-statements-when-working-with-loops-in-python-3-es

### Encadenamiento operadores comparacion
* https://www.geeksforgeeks.org/chaining-comparison-operators-python/

### Underscore - uso sintactico
* https://dbader.org/blog/meaning-of-underscores-in-python

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

### Pandas [[cheatsheet 1]](Pandas_Cheat_Sheet.pdf)[[cheatsheet 2]](<pandas_cheat_sheet by Arianne Colton and Sean Chen.pdf>)
Objetos tipo hoja_cálculo y métodos anexos. Especialmente útil para datos tipo tabla y aun más interesante para Series Temporales. Tiene una sintaxis muy intuitiva y simplificada, especialmente interesante para leer datos.
p. ej.
* Lee fichero .csv, delimitado por tabs, toma como índice de tabla las dos primeras columnas (fecha y hora) y los valores '-' son tomados como 'NaN'
```python
mad11 = pd.read_csv(path + 'madrid2011.txt', delimiter='\t', date_parser=parserdatetime, parse_dates=[[0, 1]], index_col=0, na_values='-')
```
* Lee varios ficheros y los concatena (one-liner)
```python
pd.concat([pd.read_csv(name) for name in glob.glob("*.csv")])
```
* Toma la variable B y Bmj de mad11 (valores minutales) y devuelve la suma resampleada a frecuencia mensual.
```python
eff_esp11_men = mad11.Bmj.resample('M', how='sum') / mad11.B.resample('M', how='sum')
```
* Introducción: https://realpython.com/pandas-python-explore-dataset/
* OJO copia DataFrames: https://stackoverflow.com/questions/27673231/why-should-i-make-a-copy-of-a-data-frame-in-pandas
* Tricks & Features You May Not Know: https://realpython.com/python-pandas-tricks/

### PIL-Pillow
Manipulación de imágenes.

* Nature - Programming: Pick up Python - A powerful programming language with huge community support
https://www.nature.com/news/programming-pick-up-python-1.16833

## HERRAMIENTAS PARA DATOS
### Jupyter
* Presentar datos+código en vivo.
* IDE en web. Dos versiones: _classic_ y _lab_
* Basado en ficheros notebook (.ipynb)
* Conceptos básicos https://nbviewer.jupyter.org/github/jupyter/notebook/blob/master/docs/source/examples/Notebook/Notebook%20Basics.ipynb
1. https://jupyter.org/
2. https://mybinder.org/v2/gh/bloomberg/bqplot/1da9ae2fffcbe317b6b27f6ed4f6d6c8db283452 - Ejemplo en acción
3. https://github.com/losc-tutorial/quickview - Repositorio con Jupyter notebook sobre gravitational waves

* Existen varias alternativas para la ejecución en entorno web: https://www.dataschool.io/cloud-services-for-jupyter-notebook/

#### Binder
* Crea espacio de trabajo en un servidor remoto para ejectuar en vivo Jupyter notebooks, sin necesidad de instalación local.
* Un repositorio tipo GitHub se puede convertir en un espacio de trabajo ejecutable.
1. https://jupyter.org/binder - Información
2. https://mybinder.org/ - Web app para lanzarlo

#### Google Colab
* Similar a Binder. La carga del servicio es notablemente más rápida.
* Orientado y con recursos de Google para ejecutar Machine/Deep Learning
* https://colab.research.google.com/
* Ejemplo tutorial https://colab.research.google.com/github/tensorflow/examples/blob/master/courses/udacity_intro_to_tensorflow_for_deep_learning/l01c01_introduction_to_colab_and_python.ipynb

#### JupyterHub
* Permite crear tu propia nube para servir notebooks, como Binder en privado.
* Muy interesante para clase, evita que los estudiantes se tengan que instalar nada.
* Se puede alojar en recursos propios de nube o físicos: [The Littlest JupyterHub](https://tljh.jupyter.org/en/latest/index.html)
* https://jupyter.org/hub

#### JupyterLite
* https://github.com/jupyterlite/jupyterlite
* Corre totalmente en el navegador: no requiere servidor!
* Se puede alojar directamente en p. ej. GitHub Pages

### Dash
Servidor web para generar un dashboard: permite presentar datos interactivamente (by Plot.ly)
https://dash-gallery.plotly.host/Portal/ (Galería)

### Streamlit
Similar a Dash pero más sencillo y menos maduro.
https://streamlit.io/
* Ofrece un servicio de repositorio y ejecución de apps creadas con esta tecnología: https://streamlit.io/sharing

### PyScript
Framework que permite a los usuarios crear aplicaciones ricas de Python en el navegador utilizando la interfaz de HTML (como PHP)
* https://www.genbeta.com/actualidad/ano-python-navegador-este-nuevo-proyecto-permite-ejecutar-python-tu-html
* https://github.com/pyscript/pyscript/blob/main/GETTING-STARTED.md

## APP HOSTING
Permite correr las apps en la web. Streamlit Sharing lo permite para sus propias apps

### Heroku
### PythonAnywhere
### Trinket

## GRAPHING (Matplotlib)
La librería más potente y que permite crear gráficas bien acabadas para publicaciones es MATPLOTLIB (MPL):
* Tutorial básico (rápido) https://towardsdatascience.com/matplotlib-tutorial-learn-basics-of-pythons-powerful-plotting-library-b5d1b8f67596
* Guía (más completa y clara) https://realpython.com/python-matplotlib-guide/
* Guía oficial (más densa) https://matplotlib.org/tutorials/introductory/pyplot.html#sphx-glr-tutorials-introductory-pyplot-py
* MPL Cheatsheets (interesante el de Tips&Tricks) https://github.com/matplotlib/cheatsheets

PANDAS de hecho implementa métodos .plot() que llaman a MPL para visualizaciones rápidas de DF/Series. Para pulir la gráfica hay que llamar a métodos directamente de MPL.
* Tutorial básico (rápido) http://queirozf.com/entries/pandas-dataframe-plot-examples-with-matplotlib-pyplot
* Guía oficial (más densa) https://pandas.pydata.org/pandas-docs/stable/user_guide/visualization.html

## HERRAMIENTAS PARA CODIGO
* (Breve) Listado herramientas https://opensource.com/article/18/7/7-python-libraries-more-maintainable-code
* Sitio con cursos https://software-carpentry.org/lessons/index.html
* Tutorial con plantilla para empaquetar, probar, documentar y publicar código Python científico [Bootstrap a Scientific Python Library](https://nsls-ii.github.io/scientific-python-cookiecutter/index.html)
* Tutorial gestión proyecto Python https://jacobtomlinson.dev/series/creating-an-open-source-python-project-from-scratch/

### Linters - Code syle/quality
PEP8
* https://pep8.org/
* https://realpython.com/python-code-quality/
* https://realpython.com/python-pep8/
* https://docs.python-guide.org/writing/style/

* Ejemplo: pycodestyle/flake8 (_comprueba código_), autopep8 (_formatea código_)
> Desde consola spyder: `!autopep8 -i file.py` o `!autopep8 -i .`

* Comprobación nombres objetos: variables, clases,... https://github.com/PyCQA/pep8-naming

### Documentation
PEP 257
* https://docs.python-guide.org/writing/documentation/

* Ejemplo: pydocstyle (_comprueba docstring_), docformatter (_formatea docstring_)
* Info sobre documentar https://realpython.com/documenting-python-code/
* Ejemplo docstrings _Numpy-style_ https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_numpy.html

### Testing
* https://realpython.com/python-testing/
* https://docs.python-guide.org/writing/tests/

* Ejemplo: pytest
> Desde consola spyder: `!pytest .`

### Refactoring
No es realmente una herramienta si no una buena práctica. La idea es limpiar y mejorar la legibilidad del código, muchas veces reordenándolo.\
https://realpython.com/python-refactoring/

### GitHub
Repositorio distribuido para código y datos usando protocolo `git`. Utilizar herramienta [`GitHub Desktop`](https://desktop.github.com/) para sincronizar repositorio local y remoto.
* 10 min tutorial https://guides.github.com/activities/hello-world/
* Tutorial https://www.edureka.co/blog/how-to-use-github/
* Tutorial [Real Python] https://realpython.com/python-git-github-intro/
* Introdución a GitHub https://github.com/oscarperpinan/intro_github
* A successful Git branching model https://nvie.com/posts/a-successful-git-branching-model/
* How to Write a Git Commit Message https://chris.beams.io/posts/git-commit/
> #### pre-commit
> Antes de formalizar un `commit` [pre-commit](https://pre-commit.com/) ejecuta automáticamente tareas tales como un linter para formatear el código.

> #### .gitignore
> Para evitar sincronizar ciertos archivos hay que rellenar el fichero `.gitignore`. Ver https://swcarpentry.github.io/git-novice-es/06-ignore/
> Si ya se han sincronizado previamente, usar `git rm -r --cached [file]`

> #### GitHub Actions
> Permite automatizar eventos dentro de GH. Ver https://www.adictosaltrabajo.com/2020/10/28/introduccion-a-github-actions-sintaxis-basica/

### Argparse
Librería estándar para crear CLI (Command Line Interface)
* Tutorial https://realpython.com/command-line-interfaces-python-argparse
* Ejemplo código ISI https://github.com/isi-ies-group/scripts-servidor_helios/blob/master/genera_fichero_meteo.py

### Archivo Config
Archivo externo adicional que incluye información de configuración a leer (parsear) por una librería.
* Vistazo a varios tipos https://hackersandslackers.com/simplify-your-python-projects-configuration/
* `configparser` librería estándar para ficheros `.ini`
    * Ejemplo código ISI https://github.com/isi-ies-group/meteocheck/blob/master/meteocheck/meteocheck_meteo_stations_example.ini
* `pyaml` librería externa para ficheros `.yaml`
    * Ejemplo código ISI https://github.com/isi-ies-group/pygeonica/blob/master/pygeonica/sensores_config.yaml

## PACKAGING (crear librerias)
Generar paquetes de Python, para instalar desde `pip`
* Tutorial https://python-packaging.readthedocs.io/
* https://www.blog.pythonlibrary.org/2021/09/23/python-101-how-to-create-a-python-package
* Incluso se puede instalar desde un repositorio: `pip install --upgrade git+https://github.com/isi-ies-group/cpvlib.git`
* `Cookicutter` es una herramienta para generar el andamio de una librería: https://towardsdatascience.com/cookiecutter-creating-custom-reusable-project-templates-fc85c8627b07
* https://semver.org/ Semantic Versioning: control del número de versión

## Archivo README
Consejos https://dbader.org/blog/write-a-great-readme-for-your-github-project

## API
* Info general: https://realpython.com/python-api/
* Crear API: https://realpython.com/fastapi-python-web-apis/
* REST API: https://realpython.com/flask-connexion-rest-api/
* Listado APIs: https://realpython.com/python-api/#further-reading
