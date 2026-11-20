# A Graph Signal Processing Perspective on Numerical Sequence Representations in LLM In-Context Learning

This repository includes Jupyter notebooks, cached numerical results, and input samples used to reproduce the numerical experiments in the paper *["A Graph Signal Processing Perspective on Numerical Sequence Representations in LLM In-Context Learning"](https://arxiv.org/abs/2608.03015)* by Jiajun Bao, Zihao Qi, Toni J.B. Liu, Gurbir Arora, Raphaël Sarfati, Nicolas Boullé, and Christopher J. Earls.

## Paper Abstract

Pretrained large language models (LLMs) have demonstrated in-context learning (ICL) capabilities for numerical inference over sequences serialized as text.
Prior work has identified and characterized this form of numerical inference primarily through output-level evaluations such as prediction error.
However, how numerical information is organized within LLM representations remains much less understood. To study this internal organization, we adopt a graph signal processing perspective in which attention induces a weighted graph over tokens, while token hidden states define signals on its nodes.
Quantitative graph-spectral diagnostics and qualitative token-graph visualizations reveal that representations become more clearly differentiated by input dynamical complexity as context length increases. Simpler inputs produce attention-induced token graphs with stronger global connectivity and smoother, spectrally concentrated hidden-state signals, whereas more complex inputs produce more localized graphs and hidden-state signals with broader spectral support and greater high-frequency energy. Together, these findings point to systematic, context-dependent internal signatures associated with numerical ICL that are conserved across model families.

## Repository Structure

The repository is organized into two folders corresponding to experiments in the main paper and the appendix. Each notebook begins with an annotation describing the associated study.

- **`Main/`**: Contains the notebooks, cached results, and figures for the main numerical-input studies. `Attention-induced-token-graphs/` examines graph organization across dynamical complexity and context length, while `Graph-spectral-diagnostics/` computes and visualizes layer-averaged spectral diagnostics.
- **`Appendix/`**: Contains additional experiments on input complexity, next-state extrapolation, graph construction and visualization, layerwise diagnostics, non-graph baselines, additional models, and natural-language and programming-language inputs.

#### File Naming Conventions

- **`Generate-*.ipynb`**: Notebooks for computing numerical results and saving caches.
- **`Visualize-*.ipynb`**: Notebooks for loading cached results and producing figures.
- **`Demo-*.ipynb`**: Interactive notebooks for browsing the supplied language and code samples.
- **`.npz`**: NumPy archives containing cached inputs and numerical results.
- **`.jsonl`**: Input samples with text, token IDs, and source metadata.
- **`.pdf`**: Generated figures.

## Environment Details

The software and hardware environment is:

- Python version: 3.12.11
- PyTorch version: 2.7.1
- Transformers version: 4.55.0
- NumPy version: 2.2.5
- SciPy version: 1.16.1
- Matplotlib version: 3.10.9
- NetworkX version: 3.5
- pandas version: 2.3.2
- Accelerate version: 1.9.0
- ipywidgets version: 8.1.5
- OS info: Linux-6.8.0-90-generic-x86_64-with-glibc2.39
- CPU cores: 64
- GPUs: 4 × NVIDIA RTX A4000
