# Minerva dev workspace

Simplify the process of setting up a development workspace for Minerva. This repository have a `.devcontainer` folder that contains a `Dockerfile` and a `devcontainer.json` file that will be used by Visual Studio Code to create a development workspace.

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Remote - Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Getting started

1. Clone this repository into your home folder and enter in it.
2. Run `git submodule update --init --recursive`.
3. Copy data using `./download_data.sh`. (ONY VALID FOR DISCOVERY NODE 14)
4. Open VSCode in remote machine. Then, open the folder `~/minerva-dev-workspace`. You will be prompted to reopen the project in a container. Click on the "Reopen in Container" button. Or type `Remote-Containers: Reopen in Container` in the command palette (`Control+Shift+P`).
5. The development workspace will be created and you will be able to start working on Minerva. 

## Running some pipelines

Enter in `minerva-seismic` folder. 

### SETR Train Pipeline

A pipeline for training SETR model for seismic facies segmentation.

```bash
python -m minerva.pipelines.lightning_pipeline --config configs/pipelines/lightning_pipeline/setr_pup_f3_segmentation_train.yaml
```


## UNet Train Pipeline

A pipeline for training UNet model for seismic attribute calculation.

```bash
python -m minerva.pipelines.lightning_pipeline --config configs/pipelines/lightning_pipeline/unet_f3_reconstruct_train.yaml 
```