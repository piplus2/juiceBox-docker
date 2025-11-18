# JuiceBox and Juicer Tools docker

This repo holds a small Docker setup for running the Juicer Tools and JuiceBox Hi-C tools.

Juicer Tools is compiled with JCuda 10 with full support to GPU.

## What's inside

- `Dockerfile` builds an image with Java, Juicebox, Juicer Tools and the dependencies it needs to run on Linux.
- `LICENSE` explains the project is shared under the MIT license.
- This `README` gives a quick overview for anyone who wants to know what the repo provides.

## How to build

Build the Docker image by running the command:

```bash
docker build -t juicebox:1.13.01 .
```

## How to launch juicer_tools

Juicer Tools can be run with a custom maximum memory for Java:

```bash
docker run --gpus all -e "_JAVA_OPTIONS=-Xmx16g" juicebox:1.13.01 juicer_tools <juicer_tools_command> <arguments>
```
