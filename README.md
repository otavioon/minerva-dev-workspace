# Minerva dev workspace

Simplify the process of setting up a development workspace for Minerva. This repository have a `.devcontainer` folder that contains a `Dockerfile` and a `devcontainer.json` file that will be used by Visual Studio Code to create a development workspace.

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Remote - Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Getting started

1. Clone this repositort into your home folder.
2. Run `git submodule update --init --recursive`.
3. Copy data: `cp -r /home-local/otavio.napoli/data/ ~/minerva-dev-workspace/`.
4. Open VSCode in remote machine. Then, open the folder `~/minerva-dev-workspace`. You will be prompted to reopen the project in a container. Click on the "Reopen in Container" button. Or type `Remote-Containers: Reopen in Container` in the command palette (`Control+Shift+P`).
5. The development workspace will be created and you will be able to start working on Minerva. 

## Download data

Download data and put in the `data` folder. 
