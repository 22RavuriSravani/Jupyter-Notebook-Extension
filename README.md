# Jupyter Notebook Extension
Extensions are simple add-ons that can significantly improve your productivity in the notebook environment. They automate tedious tasks such as **formatting code** or **adding features** like creating a table of contents. 

They can be installed with

```
pip install jupyter_contrib_nbextensions
jupyter contrib nbextensions install
```
Open your jupyter notebook to check for **Nbextensions** setcion. **Enable** the extensions that you want. 

This will install a collection of extensions here are few
||||
|--------------------|----------------|-------|
| AddBefore |  AutoSaveTime | datestamper|
| Autoscroll | Code prettify |ExecuteTime |
| Codefolding  Collapsible Headings| Freeze | Exercise|
 Export Embedded HTML| zenmode|Tree Filter|
| Hide Header | Help panel |Exercise2 | 
| highlighter | Hide input |Navigation-Hotkeys |
| Hinterland | Scratchpad | Move selected cells |
| Keyboard shortcut editor |  nbTranslate |  Runtools | 
|Skip-Traceback|spellchecker| table_beautifier|


##  Own Extensions - add a code cell above the currently selected cell - Default 

It's possible to write your own extensions to add anything you can think of to Jupyter Notebooks.[Basic to know  the structure , some of the existing documentation](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/internals.html).

### Structure of a Jupyter Notebook Extension 

Any of the extensions should be added to the `nbextensions` subdirectory of the `jupyter_contrib_nbextensions` library installed with pip. 
> You can find the **location of the library** using `pip show jupyter_contrib_nbextensions`.

Example: I place the new extensions at `C:\Users\ravur\anaconda3\Lib\site-packages\jupyter_contrib_nbextensions\nbextensions`

### Structure has 3 parts : 
	 * "name.yaml" file with configuration. 
	 * "README.md" with documentation.  
	 * "main.js" with the Javascript code.
	 
These 3 files should be in a single directory i.e.,`default_cell` . Looks like `nbextensions\default_cell\`.

It then runs the `defaultCellButton` function which places a button on the Jupyter Notebook toolbar. We can use this button to add and run the default cell above the currently selected cell.

#### To see the extension working
1. Make  `default_cell` directory is in the correct location and run 
` jupyter contrib nbextensions install`  
					or
 Make  `jupyter_contrib_nbextensions` directory as current location and run`pip install jupyter_contrib_nbextensions` 

 2. Make `jupyter_contrib_nbextensions` directory as current location  and run ` jupyter_contrib_nbextensions`
 
 3.   Make `Scripts` as current location and run `jupyter contrib nbextension install --user`
 
 4. Start up a Jupyter Notebook server. If you navigate to the `NBExtensions` tab, you will be able to enable the extension i.e, `default_cell` 

### Note :
+ If you don’t have the tab, open a notebook and got to Edit > nbextensions config . 
+ You can change inside `set_text` method in `main.js` to as your own code.

This extension might save you a few seconds !  

## References
@Will Koehrsen and check this out here to get [detail extensions](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/install.html).
