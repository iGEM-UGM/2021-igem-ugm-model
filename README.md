# 2021-igem-ugm-model

## Conda installation
I am using WSL2 with Conda to run this tutorial, some pointers to set it up in my blog: https://matinnuhamunada.github.io/posts/2021/04/jupyter-wsl2/

## Clone the repository
* Clone (or perhaps its better to fork?) the repository to your PC. In my case, I start by running the ubuntu terminal and type:
```
git clone git@github.com:iGEM-UGM/2021-igem-ugm-model.git
# move to the cloned repo
cd 2021-igem-ugm-model
```

## Environment installation
* Install the Conda environment required using the yml file:
```
conda env create -f envs/ugm.yml
```

* Activate the environment:
```
conda activate 2021-ugm-modelling-env
```

* Run Jupyter Lab
```
jupyter lab
# Open Jupyter in a browser by copy-paste the url given
```

## Test if all dependencies are correctly installed
* Run the notebook

* There might be trouble installing Escher Jupyter widget. You can solve it by following the escher docs:
```
# The notebook extenstion should install automatically. You can check by running:
jupyter nbextension list
# Make sure you have version >=5 of the `notebook` package
pip install "notebook>=5"
# To manually install the extension
jupyter nbextension install --py --sys-prefix escher
jupyter nbextension enable --py --sys-prefix escher
# depending on you environment, you might need the `--sysprefix` flag with those commands
jupyter labextension install @jupyter-widgets/jupyterlab-manager
jupyter labextension install escher
```