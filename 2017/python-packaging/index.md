class: center, middle, title

# Python Packaging

## Wheels, pip, PyPI, and more...

by `@zoidbergwill`

---

# Life Before Pip

## Python 2 and `easy_install`

## Python 3 and `pip`

## PyPI and eggs

https://pypi.python.org/pypi

---

# Where We Are

## Pip

## Wheels and Manylinux

## Twine

## A Packaging Guide

https://packaging.python.org/

---

# Where We're Going

## Pipfile

## Warehouse

https://pypi.org/

---

# Tools for Packaging a Python Library

## Setuptools

## Wheel

## Twine

---

# The Library to be Distributed

## Minimum

```bash
setup.py
<your package>
```

## More Commonly

```bash
setup.py
setup.cfg
README.rst
MANIFEST.in
<your package>
```

---

# Wheels

> Many packages will be properly installed with only the "Unpack" step (simply extracting the file onto sys.path), and the unpacked archive preserves enough information to "Spread" (copy data and scripts to their final locations) at any later time.

---

# Twine

> Verified HTTPS Connections

> Uploading doesn't require executing setup.py

> Uploading files that have already been created, allowing testing of distributions before release

> Supports uploading any packaging format (including wheels).


---

# Pipfiles

---

# Alternatives: pip-tools

![](pip-tools-overview.png)

---

# Alternatives: A Better Pip Workflow

```bash
rm requirements.txt
virtualenv/bin/pip install -r requirements-to-freeze.txt --upgrade
virtualenv/bin/pip freeze > requirements.txt
```

```bash
django
```

```bash
Django==1.11
pytz==2017.2
```

https://www.kennethreitz.org/essays/a-better-pip-workflow