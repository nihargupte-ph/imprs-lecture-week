# Machine Learning for Gravitational Waves — IMPRS Lecture Week 2026

A set of three hands-on tutorials covering the machine learning building blocks that show up in modern gravitational-wave data analysis. Each notebook is self-contained and runs in a few minutes on a laptop, and is meant as a starting point for more advanced applications.

## Notebooks

| Notebook | Topic | Colab |
| --- | --- | --- |
| `pytorch_basics.ipynb` | A gentle introduction to PyTorch: building, training, and evaluating a small neural network (teaching an MLP to add two numbers). Covers datasets, dataloaders, models, losses, optimizers, and the training loop. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nihargupte-ph/imprs-lecture-week/blob/main/pytorch_basics.ipynb) |
| `normalizing_flows.ipynb` | Simulation-based inference for GW parameter estimation. Trains a Gaussian posterior model and a masked autoregressive flow (MAF) on simulated IMRPhenomPv2 waveforms to infer the two mass parameters of a binary black hole. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nihargupte-ph/imprs-lecture-week/blob/main/normalizing_flows.ipynb) |
| `transformers.ipynb` | A small Vision-Transformer-style encoder that classifies one-detector whitened frequency-domain strain as either a CBC chirp or a scattered-light glitch — a simplified version of a real data-quality problem. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nihargupte-ph/imprs-lecture-week/blob/main/transformers.ipynb) |

## Getting started

To get started quickly, open any notebook in Google Colab using the badges above. To run it locally (which may be faster), create and activate a Python environment with the required packages. If using `conda`, this can be done with
```
conda create -c conda-forge -n gwml python=3.10 pytorch lalsuite glasflow corner numpy matplotlib jupyterlab
conda activate gwml
```
Alternatively, this repo ships a `pyproject.toml` / `uv.lock`, so you can reproduce the environment with [`uv`](https://docs.astral.sh/uv/):
```
uv sync
uv run jupyter lab
```

## References

* [Stephen's papers](https://inspirehep.net/literature?sort=mostrecent&size=25&page=1&q=a%20green%20%2B%20a%20gair%20%2B%20ac%201-%3E10&ui-citation-summary=true) on the topic
* [Dingo](https://github.com/dingo-gw/dingo), a package for GW inference with neural posterior estimation
* [SBI](https://www.mackelab.org/sbi/), a higher-level package for simulation-based inference
