# Latent Space Oddity - Riemannian Geometry of VAE Latent Spaces

This project, developed for the **Computational Statistics** course at ENS Paris-Saclay, investigates the geometry of Variational Autoencoder (VAE) latent spaces. The main goal is to understand how the **decoder-induced Riemannian metric** shapes the latent-space structure and influences both interpolation and sampling.

## Overview

Variational Autoencoders typically assume a **flat Euclidean latent space**, which may misrepresent the true underlying structure of data. This project explores:

- **Riemannian metric estimation**: Approximate the local latent-space geometry using the **decoder Jacobian**.
- **RBF variance networks**: Regularize the metric in sparse regions to prevent paths or samples from escaping the high-density manifold.
- **Geodesic interpolation**: Compute latent-space paths that respect curvature, producing more meaningful interpolations in data space.
- **Adaptive MCMC sampling** (Our contribution) : Implement geometry-aware and Robbins-Monro adaptive proposals to efficiently explore the latent posterior while maintaining proper acceptance rates and decorrelation.

## Implementation

The project includes:

- **Python code (Juypter Notebook)** for:
  - Training a VAE on MNIST digits (restricted to 0, 1, and 8).
  - Computing approximate local Riemannian metrics.
  - Implementing **RBF variance networks** to guide geodesics and sampling.
  - Running **adaptive MCMC** in latent space with geometry-aware proposals.
  - Visualizing **latent trajectories, acceptance rates, and autocorrelations**.

- **Presentation slides** summarizing:
  - Motivation and problem statement.
  - Theory behind Riemannian metrics and RBF variance.
  - Applications: geodesic interpolation and geometry-aware sampling.
  - Experimental results with figures of trajectories, acceptance rates, and autocorrelation plots.
  - Methodological contributions and takeaways.

## Contributions

- **Hana Feki**:  
  - Developed Python implementations for VAE, metric computation, RBF variance, and adaptive MCMC.  
  - Generated visualizations of latent-space structure and sampling diagnostics.  
  - Prepared presentation slides highlighting both theoretical and experimental aspects.

## References

- Georgios Arvanitidis, Lars Kai Hansen & Søren Hauberg (2018). *Latent Space Oddity: On the Curvature of Deep Generative Models.* [arXiv:1710.11379](https://arxiv.org/abs/1710.11379)
- Kingma, D. P., & Welling, M. (2014). *Auto-Encoding Variational Bayes.* ICLR.
- Rezende, D. J., Mohamed, S., & Wierstra, D. (2014). *Stochastic Backpropagation and Approximate Inference in Deep Generative Models.* ICML.
