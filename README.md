# Monkey_Pox_Detection
This is an Project used to find whether person suffering from Monkey Pox or not.

## Setup Mac-OS:

 - [Reference](https://medium.com/@jarondlk/installing-tensorflow-metal-on-apple-silicon-macos-with-miniconda-f43121fe3054)

```bash
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh -o Miniconda3-latest-MacOSX-x86_64.sh
bash Miniconda3-latest-MacOSX-x86_64.sh

conda create --name venv python=3.9

conda activate tf

conda install -c apple tensorflow-deps --force-reinstall -n tf

conda install cudatoolkit=9.0 tensorflow-gpu=1.11.0

python3 -m pip install tensorflow-macos==2.9

python3 -m pip install tensorflow-metal==0.5.0    // dont use this

python3 -m pip list | grep tensorflow

python3 -m pip install scipy

conda deactivate
```

```
conda activate tf

jupyter lab
```
