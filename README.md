## LaTex Generator using PaLI model

Please read this paper to fully understand this project.
[Key Paper](https://arxiv.org/abs/2402.15307)

### Description
A tool that converts handwriting(InkML format) into LaTex.

### Data preparation
[MathWriting](https://arxiv.org/abs/2404.10690)

### Model Architecture
[PaLI Model](https://arxiv.org/abs/2209.06794)

PaLI model takes two input: Image and Token sequence

For Image, we are going to render the InkML format into (3, IMG_SIZE, IMG_SIZE). The color will represent the speed of the writing. If you want more information, please read the [paper](https://arxiv.org/abs/2402.15307)

For Token sequence, we apply data preprocessing to reduce the sequence length of ink-pixels, and normalize the data.

In this project, we are going to use backbone PaLI model from [here](https://github.com/kyegomez/PALI/tree/main)

### Getting Started - Installing dependencies
Please use [uv-python](https://github.com/astral-sh/uv).
```sh
# check your python version is 3.11.10
$ python --version
Python 3.11.10

# generate venv and activate
$ uv venv
$ source .venv/bin/activate

# install requirments
$ uv pip install requirements.txt

```
### Getting Started - Dataset installation
Use `data-install.sh` script. This will take 5~10 minutes to download+decompress the dataset.
```sh
$ ./data-install.sh

# check the installed data in data/mathwriting-2024 directory
```


