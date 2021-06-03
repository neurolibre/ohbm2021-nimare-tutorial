# ohbm2021-nimare-tutorial

[![Binder](https://binder-mcgill.conp.cloud/badge_logo.svg)](https://binder-mcgill.conp.cloud/v2/gh/neurolibre/ohbm2021-nimare-tutorial/main?filepath=notebooks%2Ftutorial.ipynb)
[![Binder Backup](https://img.shields.io/badge/launch-backup--binder-orange.svg)](https://binder.conp.cloud/v2/gh/neurostuff/ohbm2021-nimare-tutorial/main?filepath=notebooks%2Ftutorial.ipynb)

Materials for the OHBM 2021 NiMARE tutorial

## To run this tutorial on Binder

1. Follow the Binder badge above 

2. Run the notebook

## To run this tutorial locally
You must have git, Python >= 3.7, and bash.

1. **Clone this repo** by pasting this in a bash terminal:
```bash
git clone https://github.com/neurostuff/ohbm2021-nimare-tutorial.git
```

2. **Create a virtual environment** with the dependencies needed to run the notebook:
```bash
cd ohbm2021-nimare-tutorial
python3 -m venv venv
source venv/bin/activate
pip3 install --upgrade pip3
pip3 install -r binder/requirements.txt
```
3. **Download the data**:
```bash
DIR=$"../data/nimare_tutorial/"
if [ -d "$DIR" ]; then
    echo "$DIR exists."
else 
    mkdir -p $DIR;
    pip3 install osfclient
    osf -p u9sqa clone  $DIR;
    echo "Created $DIR and downloaded the data";
fi
```

4. **Open the notebook**. Type `jupyter notebook` in the terminal. When the Jupyter Notebook page opens in your browser, navigate to `notebooks/tutorial.ipynb`


