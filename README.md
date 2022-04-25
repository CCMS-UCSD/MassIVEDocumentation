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

5. Deploy to github pages

```mkdocs gh-deploy```

NOTE: Default system Python may already have an outdated version of `mkdocs` installed. In this case, explicitly specify the new conda-installed version with:

```<conda_install_location>/envs/mkdocs/bin/mkdocs```
