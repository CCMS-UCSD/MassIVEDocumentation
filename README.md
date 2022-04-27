## Development Setup

1. Install miniconda3 (https://docs.conda.io/en/latest/miniconda.html)
2. Create conda environment

```conda create -n mkdocs```

3. Install requirements

```
conda install -c conda-forge mkdocs
conda install -c conda-forge mkdocs-material
pip install mkdocs-minify-plugin
```

4. Serve locally

```mkdocs serve```

This will start a local web server (address displayed on the command line - typically something like http://127.0.0.1:8000/) to test any documentation changes before deploying.

NOTE: Default system Python may already have an outdated version of `mkdocs` installed. In this case, explicitly specify the new conda-installed version with:

```<conda_install_location>/envs/mkdocs/bin/mkdocs```
