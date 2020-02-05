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
