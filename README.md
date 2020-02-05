# GLOSARIO y breve explicación de nombres relacionados con los proyectos que sostienen el mundo Científico-Python (SciPy)
- PYTHON: es un lenguaje. Sintaxis muy parecida a Matlab.
	Mucho más potente y capaz de realizar más cosas y en general más rápido que Matlab.
	El lenguaje y las librerías son libres y gratuitas. Muchas se actualizan rápido y de verdad.
	En su conjunto aun tiene partes que no están tan maduras como Matlab, pero suficiente como para trabajar sin problemas. Otras partes superan con creces a Matlab.	
	Es un lenguaje basado en scripts. No se tiene que compilar para ejecutarlo, como Matlab cuando se ejecuta en terminal. Se puede ejecutar un script en otro PC muy fácilmente y editarlo de forma instantánea. Especialmente conveniente para controlar tareas automáticas. Matlab tiene que compilarlo y es muy engorroso.

- SPYDER: es un IDE (Integrated Development Environment), el programa para escribir/ejecutar scripts, manipular datos y depurar código.
	* Es el que hay que EJECUTAR para trabajar!

- IPYTHON: es una versión mejorada de la terminal de Python. Básicamente aparece en Spyder como terminal por defecto. Permite autocompletado, sugiere nombres de funciones, lleva control de historial, número de líneas...

- ANACONDA: es una distribución de Python adecuada al mundo científico. Contiene Python + librerías "científicas" + Spyder (IDE)
	Esto es lo cómodo para instalar todo, la distribución es preparada por la empresa Continuum . https://store.continuum.io/cshop/anaconda/
	* Ver la última versión en la web!
	* Existe también Miniconda, que no contiene paquetes por defecto y hay que instalarlos. Interesante para tener una instalación ligera.

	Hay que elegir Python 2 o 3. Elegir 3 (>=3.4)
		* Casi todas las cosas de 2 está en 3, especialmente la parte científica. Python 3 es la versión más moderna y es muy similar a 2.
	Hay que elegir sistema operativo y versión 32/64 bits.
*NOTA: Existe también Miniconda que no contiene ninguna librería por defecto, pero se pueden instalar explicitamente solamente las necesarias. Mucho más ligero.

## LIBRERIAS http://docs.continuum.io/anaconda/pkg-docs.html
Para procesar, visualizar y representar datos existen librerías "científicas", como las de Matlab, aunque algunas son para obtener funcionalidades que vienen por defecto en Matlab.
* Hay que importar al principio de cada script cada libreria explícitamente, para mantener un control de los nombres de cada librería (espacio de nombres). Pero se puede poner todo por defecto con un pequeño fichero de configuración junto con los directorios de path, al igual que Matlab.

* Si no están ya instaladas en Anaconda, se tienen que instalar desde la linea de comandos de Windows 'cmd' con el comando 'conda install "nombre_libreria"'. Si no estuviera en los repositorios de Anaconda, habría que instalarlas mediante 'pip install "nombre_libreria"'. Si no existe como librería, se debería usar directamente como paquete de Python, en un fichero *.py

	Control de librerias:
		Se pueden actualizar, instalar, desinstalar desde linea de comandos: 'cmd'.
		p. ej. 'conda update spyder'

Las más usuales son:
- SCIPY: funciones de cálculo numérico, muchas tienen la misma sintáxis que en Matlab
	p. ej. trapz()
- NUMPY: implementa tipo de dato 'array' que permite operaciones vectoriales, tipo Matlab. No necesita la sintaxis con punto típica de Matlab (.*, ...). Una vez creado (o leido) el objeto Numpy la sintaxis es transparente.
	p. ej. a = b * c, donde b y c son vectores.
- MATPLOTLIB: objetos y funciones para graficar, tiene sintaxis similar a Matlab. Aunque similar, algunas cosas son más claras.
- PANDAS: objetos tipo hoja_cálculo y métodos anexos. Especialmente útil para datos tipo tabla y aun más interesante para Series Temporales. Tiene una sintaxis mus simplificada, especialmente interesante para leer datos.
	p. ej.
	* mad11 = pd.read_csv(path + 'madrid2011.txt', delimiter='\t', date_parser=parserdatetime, parse_dates=[[0, 1]], index_col=0, na_values='-')
		Lee fichero .csv, delimitado por tabs, toma como índice de tabla las dos 1ªs columnas (fecha y hora) y los valores '-' son tomados como 'NaN'

	* eff_esp11_men = mad11.Bmj.resample('M', how='sum') / mad11.B.resample('M', how='sum')
		Toma la variable B y Bmj de mad11 (valores minutales) y devuelve la suma resampleada a frecuencia mensual.
- PIL/PILLOW: manipulación de imágenes.

# Listado de links con información útil para Python
_El repositorio contiene documentos también útiles_

* Nature - Programming: Pick up Python - A powerful programming language with huge community support
https://www.nature.com/news/programming-pick-up-python-1.16833

## CURSOS
https://www.sololearn.com/Course/Python/ (muy ameno, para aprender haciendo, hay app)

## TUTORIALES
* Buen tutorial general 
https://docs.python-guide.org/

* Tutoriales temáticos para (casi) todas las características/opciones/librerias del lenguaje
https://realpython.com/

* Guia Python Científico
http://scipy-lectures.org/

## HERRAMIENTAS
* Jupyter - Presentar datos+código en vivo
https://jupyter.org/

* Dash (by Plot.ly) - Servidor web para presentar datos interactivamente - Galería
https://dash-gallery.plotly.host/Portal/

* Pythonic loops (olvídate de los loops con i!)
https://dbader.org/blog/pythonic-loops
https://mlwhiz.com/blog/2019/04/22/python_forloops/


## GRAPHING - MATPLOTLIB
La librería más potente y que permite crear gráficas bien acabadas para publicaciones es MATPLOTLIB (MPL):
*	Tutorial básico (rápido) https://towardsdatascience.com/matplotlib-tutorial-learn-basics-of-pythons-powerful-plotting-library-b5d1b8f67596
*	Guía (más completa y clara) https://realpython.com/python-matplotlib-guide/
*	Guía oficial (más densa) https://matplotlib.org/tutorials/introductory/pyplot.html#sphx-glr-tutorials-introductory-pyplot-py

PANDAS de hecho implementa métodos .plot() que llaman a MPL para visualizaciones rápidas de DF/Series. Para pulir la gráfica hay que llamar a métodos directamente de MPL.
*	Tutorial básico (rápido) http://queirozf.com/entries/pandas-dataframe-plot-examples-with-matplotlib-pyplot
*	Guía oficial (más densa) https://pandas.pydata.org/pandas-docs/stable/user_guide/visualization.html

## HERRAMIENTAS PARA CODIGO: LINTERS, DOCUMENTATION, TESTING
(Breve) Listado herramientas
https://opensource.com/article/18/7/7-python-libraries-more-maintainable-code

### Code syle/quality – PEP8
https://realpython.com/python-code-quality/
https://realpython.com/python-pep8/
https://docs.python-guide.org/writing/style/

* Ejemplo: pycodestyle (_comprueba código_), autopep8 (_formatea código_)
> Desde consola spyder:
```
!autopep8 -i file.py
!autopep8 -i .
```

### Documentation – PEP 257
https://realpython.com/documenting-python-code/
https://docs.python-guide.org/writing/documentation/

* Ejemplo: pydocstyle (_comprueba docstring_), docformatter (_formatea docstring_)

### Testing
https://realpython.com/python-testing/
https://docs.python-guide.org/writing/tests/

* Ejemplo: pytest

# Instalar entorno trabajo
DESCARGAR [Se recomienda descargar la versión más reciente de Anaconda o Miniconda en web: https://www.continuum.io/downloads]
	- Anaconda (con todas las librerías. Ocupa y tarda bastante en instalar)
	- Miniconda y luego elegir las librerias a mano (RECOMENDADO)

	Elegir:
		* Python 3
		* 32/64 bits

INSTALACION librerias básicas
	- Abrir linea de comandos (símbolo de sistema) y escribir:
	conda install pandas numexpr numpy scipy matplotlib spyder xlrd

USAR
Lanzar Spyder (doble-clic icono telaraña) para poder programar y ejecutar desde un entorno gráfico
