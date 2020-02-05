Nature - Programming: Pick up Python - A powerful programming language with huge community support
https://www.nature.com/news/programming-pick-up-python-1.16833

pythonic loops
https://dbader.org/blog/pythonic-loops
https://mlwhiz.com/blog/2019/04/22/python_forloops/

tutorial pandas
https://realpython.com/pandas-python-explore-dataset/


# GRAPHING - MATPLOTLIB
La librería más potente y que permite crear gráficas bien acabadas para publicaciones es MATPLOTLIB (MPL):
•	Tutorial básico (rápido) https://towardsdatascience.com/matplotlib-tutorial-learn-basics-of-pythons-powerful-plotting-library-b5d1b8f67596
•	Guía (más completa y clara) https://realpython.com/python-matplotlib-guide/
•	Guía oficial (más densa) https://matplotlib.org/tutorials/introductory/pyplot.html#sphx-glr-tutorials-introductory-pyplot-py

PANDAS de hecho implementa métodos .plot() que llaman a MPL para visualizaciones rápidas de DF/Series. Para pulir la gráfica hay que llamar a métodos directamente de MPL.
•	Tutorial básico (rápido) http://queirozf.com/entries/pandas-dataframe-plot-examples-with-matplotlib-pyplot
•	Guía oficial (más densa) https://pandas.pydata.org/pandas-docs/stable/user_guide/visualization.html

# HERRAMIENTAS PARA CODIGO: LINTERS, DOCUMENTATION, TESTING
(Breve) Listado herramientas
https://opensource.com/article/18/7/7-python-libraries-more-maintainable-code

## Code syle/quality – PEP8
https://realpython.com/python-code-quality/
https://realpython.com/python-pep8/
https://docs.python-guide.org/writing/style/

*Ejemplo: pycodestyle (comprueba [linter]), autopep8 (cambia [autoformatter])
Desde consola spyder:
!autopep8 -i file.py
!autopep8 -i .

## Documentation – PEP 257
https://realpython.com/documenting-python-code/
https://docs.python-guide.org/writing/documentation/

*Ejemplo: pydocstyle (check), docformatter (fix)

## Testing
https://realpython.com/python-testing/
https://docs.python-guide.org/writing/tests/

*Ejemplo: pytest
