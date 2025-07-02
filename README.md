# PyQt examples 2022

These PyQt examples show you how to create a desktop app with Python and Qt. Start with "Hello World" or browse the official PyQt demos. You can run every example yourself on Windows, Mac or Linux. All you need is Python 3. For instructions, please see [below](#running-the-examples).

| <a href="01 PyQt QLabel"><img src="screenshots/pyqt-qlabel.png" alt="PyQt QLabel" width=100px></a> | <a href="02 PyQt Widgets"><img src="screenshots/pyqt-widgets.png" alt="PyQt widgets screenshot" width=200px></a> | <a href="03 QVBoxLayout PyQt6"><img src="screenshots/qvboxlayout-pyqt5.png" alt="QVBoxLayout PyQt6" width=100px></a> | <a href="04 PyQt Signals and Slots"><img src="screenshots/pyqt-signals-and-slots.jpg" alt="PyQt Signals and Slots" width=170px></a> | <a href="05 Qt Designer Python"><img src="screenshots/qt-designer-windows.png" alt="Qt Designer Python" width=190px></a> |
| :--: | :--: | :--: | :--: | :--: |
| <a href="01 PyQt QLabel">Hello World!</a> | <a href="02 PyQt Widgets">Common PyQt Widgets</a> | <a href="03 QVBoxLayout PyQt6">Layouts</a> | <a href="04 PyQt Signals and Slots">Signals and Slots</a> | <a href="05 Qt Designer Python">Qt Designer & Python</a> |

| <a href="06 QML Python example"><img src="screenshots/qml-python-example.png" alt="QML Python example" width=200px></a> | <a href="07 Qt Text Editor"><img src="screenshots/qt-text-editor.png" alt="Qt Text Editor" width=180px></a> | <a href="08 PyQt6 exe"><img src="screenshots/pyqt5-exe.png" alt="PyQt6 exe" width=213px></a> | <a href="09 Qt dark theme"><img src="screenshots/qt-dark-theme.png" alt="Qt dark theme" width=180px></a> |
| :--: | :--: | :--: | :--: |
| <a href="06 QML Python example">QML Python example</a> | <a href="07 Qt Text Editor">Qt Text Editor</a> | <a href="08 PyQt6 exe">Packaging & deployment</a> | <a href="09 Qt dark theme">Qt Dark Theme</a> |

| <a href="10 QPainter Python example"><img src="screenshots/qpainter-python-example.png" alt="QPainter Python example" width=200px></a> | <a href="11 PyQt Thread example"><img src="screenshots/pyqt-thread-example.png" alt="PyQt Thread example" width=175px></a> | <a href="12 QTreeView example in Python"><img src="screenshots/qtreeview-example-in-python.png" alt="QTreeView example in Python" width=260px></a> | <a href="13 PyQt6 QListView"><img src="screenshots/pyqt5-qlistview.png" alt="PyQt6 QListView" width=138px></a> |
| :--: | :--: | :--: | :--: |
| <a href="10 QPainter Python example">Action Shooter</a> | <a href="11 PyQt Thread example">Chat Client</a> | <a href="12 QTreeView example in Python">Tree Views</a> | <a href="13 PyQt6 QListView">Lists</a> |

| <a href="14 QAbstractTableModel example"><img src="screenshots/qabstracttablemodel-example.png" alt="QAbstractTableModel example" height=120px></a> | <a href="15 PyQt database example"><img src="screenshots/pyqt-database-example.png" alt="QAbstractTableModel example" height=120px></a> |
| :--: | :--: |
| <a href="14 QAbstractTableModel example">Custom Tables</a> |  <a href="15 PyQt database example">PyQt database example</a> |

These examples are taken from the following book:

<p align="center">
    <a href="https://build-system.fman.io/pyqt6-book"><img src="https://build-system.fman.io/static/public/img/pyqt5-book.jpg" alt="PyQt6 book"></a>
    <br/>
    <a href="https://build-system.fman.io/pyqt6-book">Python and Qt: The Best Parts</a>
    <br/>
    by Michael Herrmann
</p>

## Official PyQt demos

The [PyQt source archive](https://www.riverbankcomputing.com/software/pyqt/download5) also contains a large number of sample files. You can find them reproduced here in the [`pyqt-official`](pyqt-official) directory. The easiest way to start them is to follow the [instructions about running examples](#running-the-examples) below, then execute the following commands:

    cd pyqt-official/qtdemo
    python qtdemo.py

This starts the PyQt example launcher:

<p align="center"><img src="screenshots/pyqt-examples-launcher.png" alt="PyQt Examples launcher"></p>

You can use it to easily browse and run the official demo applications. The following examples are quite nice for instance:

 * Quick / Animation / ColorAnimation
 * Graphics Effects / Lighting and Shadows
 * Desktop / System Tray
 * Desktop / Screenshot
 * Widgets / Tetrix

## Running the examples

Running the examples is really easy. The only thing you need is [Python 3](https://www.python.org/downloads/).

First, download the [ZIP archive of this repository](https://github.com/pyqt/examples/archive/_.zip) and unpack it. Open a command prompt and use `cd` to navigate into the top-level directory of the archive.

Create a virtual environment via the command:

    python3 -m venv venv

This creates the folder `venv/` in your current directory. It will contain the necessary libraries for running the examples.

To activate the virtual environment, use the following command:

```
# On Windows:
call venv\Scripts\activate.bat
# On Mac / Linux:
source venv/bin/activate
```

Now execute the following to install the necessary dependencies:

    pip install -Ur requirements.txt

Once you have done this, use `cd` to navigate to the example you're interested in in the [``](src) folder. For example:

    cd "01 PyQt QLabel"

You'll find a `.py` file there, typically `main.py`. You can run it with the command:

    python main.py

Please note that the virtual environment must still be active for this to work.

## Using PySide

This repository uses PyQt6 to use Qt from Python. Another, alternative binding is PySide6 (also called "Qt for Python"). It is less mature than PyQt6 but has the advantage that you can use it for free in commercial projects.

If you want to use PySide6 instead of PyQt6, simply replace all mentions of the latter by the former. For instance, in [`requirements.txt`](requirements.txt), replace `PyQt6` by `PySide6`. Similarly for any code examples: `from PyQt6.QtWidgets ...` becomes `from PySide6.QtWidgets ...` etc.

Alternatively, if you don't want to commit to either of the two bindings at this stage, you can also use [Qt.py](https://github.com/mottosso/Qt.py). This is an abstraction over PySide6 and PyQt6. It loads whichever of the two bindings is available. To use it for the examples presented here, replace all mentions of `PyQt6` by just `Qt`.

## Licensing

Except where otherwise indicated, you may use the source code of examples 1 - 15 in the [`` directory](src) under the terms of the MIT or GPLv3 licenses.

The official PyQt demos in [`pyqt-official`](pyqt-official) are [licensed under the GPL](pyqt-official/LICENSE).

The screenshots in this repository may be used under the terms of the [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) if you prominently mention and link to [Michael Herrmann's PyQt6 book](https://build-system.fman.io/pyqt6-book). 
