# Download and install Anaconda environment for Python 3.11

- Navigate to https://www.anaconda.com/download/
- Select **Grapphical Installer**
- Mac users: 
    - Note the dedicated version for M1. 
    - To test your installation, open `Terminal` and run `conda list`. You're good to go if you see a list of installed packages.
    - Cf. [Installing on macOS](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html). 
    
- Windows users: 
    - To test your installation, go to your Start menu, find `Anaconda3`, and open `Anaconda Powershell Prompt`. In the prompt window, run `conda list`. You're good to go if you see a list of installed packages.
    - If you want to use your PowerShell and can't, try running `conda init powershell` in Anaconda Prompt.
    - Cf. [Installing on Windows](https://docs.conda.io/projects/conda/en/latest/user-guide/install/windows.html).

# Create new anaconda environment for this class

```sh
conda create --name anlp python=3.11
 ```

# Activate environment

```sh
source activate anlp
```

# Check version (should be 3.11.4)

```sh
python --version 
```
https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html

# Install packages

Be sure to install these specific versions to make debugging easier for everyone in class.

```sh
conda install nltk=3.8.1
conda install -c conda-forge spacy=3.6.1
conda install scikit-learn=1.3.0
conda install pandas=2.0.3
conda install matplotlib=3.7.1
conda install jupyter=1.0.0
```

## Install PyTorch

Mac:

```sh
conda install pytorch==2.0.0 torchvision==0.15.0 torchaudio==2.0.0 -c pytorch
```

Windows:

```sh
conda install pytorch==2.0.0 torchvision==0.15.0 torchaudio==2.0.0 cpuonly -c pytorch
```


## Install spaCy English model

```sh
python -m spacy download en_core_web_sm
```

# Use Jupyter notebooks

That's it! Whenever you're ready to use a Jupyter notebook in this setup, open up the terminal and navigate to the folder containing the notebook; then activate the anlp environment to access these libraries and start up the notebook:

```sh
source activate anlp
jupyter notebook
```

We'll be using Jupyter notebooks extensively in this class; if you're new to them, check out the tutorial here:

* [Jupyter notebook tutorial](https://www.dataquest.io/blog/jupyter-notebook-tutorial/)

If you haven't used Github before, you'll just need it to pull course materials (notebooks, data) from the anlp repo.

* [Install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* `git clone git@github.com:dbamman/anlp23.git` or `git clone https://github.com/dbamman/anlp23.git`
* Whenever you want to update your local copy: `git pull`

See here for an intro to Git/Github:

* https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners


