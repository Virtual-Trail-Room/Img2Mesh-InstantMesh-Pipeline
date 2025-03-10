# Img2Mesh: [InstantMesh](https://github.com/TencentARC/InstantMesh?tab=readme-ov-file)

## Set up
First, clone InstantMesh

```
$ git clone https://github.com/TencentARC/InstantMesh
```

Then, download model weights from the [model card](https://huggingface.co/TencentARC/InstantMesh). Create a `{path-to-InstantMesh}/ckpts` directory put the weights in there.

You can either download them by clicking download button on model card or use [git lfs](https://docs.github.com/en/repositories/working-with-files/managing-large-files/installing-git-large-file-storage) to download through cli

To install on virtual machine: 
```
$ sudo apt-get install git-lfs
$ git lfs install
```

Clone models using git-lfs:
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

## Quick Start
For a quick start for a single file:
```
$ python run.py configs/instant-mesh-large.yaml examples/hatsune_miku.png --save_video
```

You can also pass in an entire folder and it will make meshs of the entire folder

```
$ python run.py configs/instant-mesh-large.yaml examples --save_video
```

## Uploading to virtual cluster and saving to local machine

If you are using the lambda vitual clusters, I recommend using the zip cli, which lets you zip and unzip files through the cli. The lambda virtual machines do not let you zip files in their interface, nor does it allow for you to download more than 9 files at a time.

To install: 
```
$ sudo apt-get install zip
```
Zip: 
```
$ zip -r {filename.zip} {foldername}
```

Unzip:
```
$ unzip {filename.zip}
```