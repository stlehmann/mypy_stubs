# stubs

A collection of stubs for commonly used Python packages.

## Supported Packages

* [PyQt5][1]: Python bindings for the Qt5 framework.
* [sqlalchemy][2]: The Python SQL Toolkit and Object Relational Mapper.

[1]: https://github.com/stlehmann/mypy_stubs_PyQt5
[2]: https://github.com/stlehmann/mypy_stubs_sqlalchemy

## Usage

To use these stubs in a Python package just clone this repository in your package root
directory.

    $ git clone --recurse-submodules https://github.com/stlehmann/stubs.git stubs

Then you need to set the mypy-path in your `mypy.ini` to the stubs directory:

    [mypy]
    mypy_path = stubs
    ignore_missing_imports = True
    follow_imports = silent
    disallow_untyped_calls=true
    disallow_untyped_defs=true

To add more directories e.g. if you use a virtual environment use a colon for
separation.

    [mypy]
    mypy_path = stubs:C:\Users\foo\.virtualenvs\mypackage-2YYl8MPT\Lib\site-packages
