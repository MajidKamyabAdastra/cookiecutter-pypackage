# Sphinx introduction:
For a short video of sphinx please take a look at [Sphinx Intro](https://byu-cpe.github.io/ComputingBootCamp/tutorials/sphinx/). By using Sphinx you can easily create documentation using the docstring in the code and other documents in the repository.
## demo of the Sphinx:
To make a new document do the following:
```console
git clone git@github.com:Nutrien/sphinx_template.git
cd docs
make html
```
Then you can find the html directory under `docs/_build/html`
There are multiple options to create the documents and you can see all of them by running the following command In the `/docs` directory.
```console
make
``` 
To use Sphinx in a directory use:
```console
sphinx-quickstart <path to the directory you created>
```
## text formatting syntax
Sphinx supports multiple formatting syntax and here we mention two of the most used ones.
### reStructuredText
reStructuredText is the default text formatting syntax of Sphinx. It is an easy-to-read, what-you-see-is-what-you-get plaintext markup syntax and parser system, you can use the [Restructure text cheat sheet](https://github.com/ralsina/rst-cheatsheet/blob/master/rst-cheatsheet.rst) when you want to use this format.
### Markdown
in order to use Markdown in your repo make sure to include `myst_parser` in the `docs/conf.py` extensions.
 ```python
extensions = ['myst_parser','other extensions']
```
You can use [Markdown cheat sheet](https://www.markdownguide.org/cheat-sheet/) in this case.
### sphinx structure:
Sphinx main parts are the `docs/makefile`, `docs/conf.py`, and `docs/index.rst`. Which are explained below:
- `docs/makefile`: It is used to build the documentation while calling the make command.
- `docs/conf.py`: the configuration of the Sphinx, for more information please visit [Sphinx documentation](https://www.sphinx-doc.org/en/master/usage/configuration.html).
- `docs/index.` The main part is the _toctree_ which is what files to include in the documentation.

## docstring:
Sphinx can update the documentation using the docstrings in the repository. As an example, two of the best practices are google and Numpy docstring formats in which [sphinx.ext.napoleon](https://www.sphinx-doc.org/en/master/usage/extensions/napoleon.html) extension supports it, make sure to add this extension in `conf.py`
```python
extensions=['sphinx.ext.napoleon','other-extensions']
```
If you are using VSCode consider installing [autoDocstring](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring) extension to automatically generate docstring.
 in order to autogenerate the docstring for your repository. Make sure to use [typing](https://docs.python.org/3/library/typing.html) before you use autoDocstring in order to automatically generate the input and output information on docstring.

![typing gif](pictures/typing_docstring.gif "demonstration of how to generate docstring including the type hints")

 In case you are using Pycharm take a look at [pycharm docstring](https://www.jetbrains.com/help/pycharm/creating-documentation-comments.html) .

