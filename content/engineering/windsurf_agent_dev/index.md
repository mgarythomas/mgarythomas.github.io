---
title: "Windsurf Agent Dev"
summary: "Windsurf Agent Development using a Gemini Model"
description: "Building a simple agent to show integration with Windsurf, Gemini, Jupyterlab and Anaconda"
draft: true
tags: ["windsurf", "agent", "jupyterlab", "gemini", "anaconda"]
categories: ["engineering"]
author: "Gary Thomas"
date: 2025-04-28
---

## Introduction

Windsurf Agent Dev is a tool for developing and testing Windsurf Agent.

## Setup.

I decided to start with Python 3.12. This is up to date for Anaconda, but support in Windsurf was something to validate (definitely 3.10 and 3.11 are supported).

I also needed to install Jupyterlab and Anaconda.

### Create a new environment

```bash
conda create -n windsurf_agent python=3.12
```

### Activate the environment

```bash
conda activate windsurf_agent
```

### Install Jupyter (jupyterlab comes with jupyter)

```bash
conda install jupyter notebook
```

**Note**: I got different results when I went and prompted chat gpt 4-o and claude 3.7 sonnet about the python install

Also add the ipykernel to the environment so we can specify this from within jupyterlab.

```bash
conda install ipykernel
```

Now create the kernel for the environment:

```bash
python -m ipykernel install --user --name windsurf_agent --display-name "windsurf_agent"
```

### Install the library dependencies for Gemini

For this, there is not a conda package, so I used pip:

```bash
pip install google-generativeai
```

### Install some additional dependencies

I added some other library dependencies that I will likely use as I build the agent:

```bash
pip install plotly matplotlib pandas numpy
```

### Create a windsurf project

```bash
mkdir windsurf_agent
cd windsurf_agent
```

### Create a requirements.txt file

### Export the python environment 
Now that the dependencies are installed, we can export the environment to a environment.yml file:

```bash
conda env export > environment.yml

### Setup windsurf to point to the correct python environment
I know this is simple and apologies if everyone already knows this, but within Windsurf, you need to go to the settings and point to the correct python environment.

    1. Open Command Palette (Cmd+Shift+P)
    2. Search for Python: Select Interpreter
    3. Pick the interpreter that matches your windsurf_agent Conda env (should look like conda-env:windsurf_agent)