easydata-tutorial
==============================
_Author: Amy Wooding_

Welcome to the [easydata-tutorial] repo! If you're attending the Pydata Global Tutorial, "[Love your (data science) Neighbour: Reproducible Data Science the Easydata Way][pydata-global-talk]", you're in the right place!

You're about to embark on the **Easydata Quest for Reproducibility**. In preparation, you'll need to get your tools ready. In particular, you will need to have the following basic requirements installed on your machine:
* conda >= 4.8 (via Anaconda or Miniconda)
* python >= 3.6
* GNU make
* git

Note that once conda is installed, you can easily use it to install python, make, and even git, if need be; e.g. by doing a:

```
>>> conda create -n easydata python=3 make git
>>> conda activate easydata
```

Windows setup can be especially gnarly. We have [Windows specific setup instructions](reference/easydata/windows-install.md).

To test if you're ready, run:
```
python quest/am_i_ready.py
```

If you get a `SyntaxError`, make sure you are using at least python 3.6!


[easydata-tutorial]: https://github.com/acwooding/easydata-tutorial/
[pydata-global-talk]: https://pydata.org/global2021/schedule/presentation/99/love-your-data-scientist-neighbour-reproducible-data-science-the-easydata-way/


ABOUT EASYDATA
--------------
This git repository is build from the [Easydata](https://github.com/hackalog/easydata) framework, which aims to make
your data science workflow reproducible. The Easydata framework includes:

* tools for managing conda environments in a consistent and reproducible way,
* built-in dataset management (including tracking of metadata such as LICENSES and READMEs),
* a prescribed project directory structure,
* workflows and conventions for contributing notebooks and other code.

EASYDATA REQUIREMENTS
------------
* Make
* conda >= 4.8 (via Anaconda or Miniconda)
* Git

For more on Easydata see [Getting Started](reference/easydata/getting-started.md).


Project Organization
------------
* `LICENSE`
* `Makefile`
    * Top-level makefile. Type `make` for a list of valid commands.
* `Makefile.include`
    * Global includes for makefile routines. Included by `Makefile`.
* `Makefile.env`
    * Command for maintaining reproducible conda environment. Included by `Makefile`.
* `README.md`
    * this file
* `catalog`
  * Data catalog. This is where config information such as data sources
    and data transformations are saved.
  * `catalog/config.ini`
     * Local Data Store. This configuration file is for local data only, and is never checked into the repo.
* `data`
    * Data directory. Often symlinked to a filesystem with lots of space.
    * `data/raw`
        * Raw (immutable) hash-verified downloads.
    * `data/interim`
        * Extracted and interim data representations.
    * `data/interim/cache`
        * Dataset cache
    * `data/processed`
        * The final, canonical data sets ready for analysis.
* `docs`
    * Sphinx-format documentation files for this project.
    * `docs/Makefile`: Makefile for generating HTML/Latex/other formats from Sphinx-format documentation.
* `notebooks`
    *  Jupyter notebooks. Naming convention is a number (for ordering),
    the creator's initials, and a short `-` delimited description,
    e.g. `1.0-jqp-initial-data-exploration`.
* `quest`
    * This is where you'll find materials related to the Easydata Quest for Reproducibility.
    * `quest_codewords.md`: **QUEST TASK** This is the only file in here you'll need to worry yourself with. In fact, go on, take a look at it. It will help you along on your quest.
* `reference`
    * Data dictionaries, documentation, manuals, scripts, papers, or other explanatory materials.
    * `reference/easydata`: Easydata framework and workflow documentation.
    * `reference/templates`: Templates and code snippets for Jupyter
    * `reference/dataset`: resources related to datasets; e.g. dataset creation notebooks and scripts
* `reports`
    * Generated analysis as HTML, PDF, LaTeX, etc.
    * `reports/figures`
        * Generated graphics and figures to be used in reporting.
* `environment.yml`
    * The user-readable YAML file for reproducing the conda/pip environment.
* `environment.(platform).lock.yml`
    * resolved versions, result of processing `environment.yml`
* `setup.py`
    * Turns contents of `src` into a
    pip-installable python module  (`pip install -e .`) so it can be
    imported in python code.
* `src`
    * Source code for use in this project.
    * `src/__init__.py`
        * Makes `src` a Python module.
    * `src/data`
        * Scripts to fetch or generate data.
    * `src/analysis`
        * Scripts to turn datasets into output products.
    * `src/tests`
        * Testing scripts that run via `make test`.

--------

<p><small>This project was built using <a target="_blank" href="https://github.com/hackalog/easydata">Easydata</a>, a python framework aimed at making your data science workflow reproducible.</small></p>
