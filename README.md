# docker-conda-tos-solution
A minimal Docker solution for accepting Conda's Terms of Service automatically, , which is often required when using certain Anaconda packages and a continous root of problems when seeting up a Conda-based container.

## What this Dockerfile does

- Starts from the official Miniconda3 image
- Sets environment variables to automatically accept Conda TOS
- Installs the `conda-anaconda-tos` plugin
- Uses the plugin to accept TOS for the required Anaconda channels
- Cleans up temporary files to reduce image size

## How to build the Docker image

Run this command in your terminal (in the same folder as the Dockerfile):
```bash
docker build -t conda-base-with-tos -f Dockerfile.base .

