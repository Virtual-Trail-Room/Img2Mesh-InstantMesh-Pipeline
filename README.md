# Img2Mesh: [InstantMesh](https://github.com/TencentARC/InstantMesh?tab=readme-ov-file)

First, clone InstantMesh

```
$ git clone https://github.com/TencentARC/InstantMesh
```

Then, download model weights from the [model card](https://huggingface.co/TencentARC/InstantMesh). Create a `{path-to-InstantMesh}/ckpts` directory put the weights in there.

You can either download them by clicking download button on model card or use [git lfs](https://docs.github.com/en/repositories/working-with-files/managing-large-files/installing-git-large-file-storage) to download through cli

```
$ git lfs clone https://huggingface.co/TencentARC/InstantMesh ckpts
```

Then follow the steps listed on the [InstantMesh](https://github.com/TencentARC/InstantMesh?tab=readme-ov-file) to create a conda env. 

I however don't use conda env and like to use venv with the latests updates, and found that you can simply remove all version controls and use the latest version of python and each of the libraries. To do this, replace the `requirements.txt` from their repo with the one attached to this repo. Create venv and install all requirements.

```
$ python -m venv .venv
$ source .venv/bin/activate
$ pip install -r requiremetns.txt
```

Now, you can follow the instructions from the [InstantMesh README](https://github.com/TencentARC/InstantMesh?tab=readme-ov-file#running-with-command-line) to run using cli
