# Probabilistic Trust Scoring for License Plate Images

In this repo, we have attached our code which implements a **probabilistic, data-centric validation framework** designed to estimate the *pragmatic usability* of visual inputs prior to downstream recognition or OCR pipelines.

Unlike classical preprocessing pipelines that rely on heuristic filters or detector confidence thresholds, this project formalizes data validation as a **latent-space inference problem** grounded in uncertainty modeling and probabilistic representation learning.

The main idea is simple but powerful:

> Not every valid image is a usable image.

We aim to quantify *fitness-for-task* directly from learned latent geometry.

---

## Conceptual Motivation

Modern deep learning pipelines often assume that input data is clean enough to be processed.  
However, in real-world environments, syntactically valid and semantically correct samples may still fail to provide reliable information for recognition tasks.

Instead of focusing on model robustness alone, this project shifts the perspective toward:

- **Pragmatic Data Quality**
- **Latent Reliability**
- **Uncertainty-Aware Filtering**

The core hypothesis is that:

> The structure of the latent distribution encodes implicit signals about perceptual usability.

By exploiting probabilistic embeddings, we move validation from raw pixel space into a structured statistical manifold.

---

## Core Idea

The framework models each license plate image as a **Gaussian latent posterior** learned through a convolutional Variational Autoencoder (VAE):

