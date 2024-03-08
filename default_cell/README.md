Default Cell
=========

Adds and runs a default cell at the top of each new notebook. To change the default cell, edit the `add_cell` function in the `main.js` file. The relevant section is:

`Jupyter.notebook.insert_cell_above('code').set_text(``)`

Set the `text` to the default notebook cell you would like.

This extension also adds a button to the toolbar allowing you to insert and run the
default cell above your current cell. This can be helpful if you open an already-started notebook
and notice you are missing some common imports.
