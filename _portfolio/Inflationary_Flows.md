---
title: "Inflationary Flows"
excerpt: "Calibrated Bayesian Inference with Diffusion-Based Models<br/><img src='https://sites.duke.edu/ifsprojectassets/files/2024/07/figure1-1.png' width='75%'>"
collection: portfolio
---

<figure>
<br/><center><img src='https://sites.duke.edu/ifsprojectassets/files/2024/07/figure1-1.png' width='85%'></center>
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?...">
</script>
<figcaption><strong>SDE-ODE Duality of diffusion-based models</strong>. The forward (noising) SDE defining the DBM (<strong>left</strong>) gives rise to a sequence of marginal probability densities whose temporal evolution is described by a Fokker-Planck equation (FPE, <strong>middle</strong>). But this correspondence is not unique: the probability flow ODE (pfODE, <strong>right</strong>) gives rise to the <i>same</i> FPE. That is, while both the SDE and the pfODE transform the data distribution in the same way, the former is noisy and mixing while the latter is deterministic and neighborhood-preserving. Both models require knowledge of the score function \( \nabla_\mathbf{x} \log p_t(\mathbf{x}) \), which can learned by training either.</figcaption>
</figure>

In this project we exploited a previously established connection between the stochastic and probability flow ordinary differential equations (pfODEs) underlying
Diffusion-Based Models (DBMs) to derive a new class of models, <i>inflationary flows</i>, that uniquely and deterministically map high-dimensional data to a lower-dimensional 
Gaussian distribution via ODE integration. This map is both invertible and neighborhood-preserving, with controllable numerical error, with the result that uncertainties 
in the data are correctly propagated to the latent space. We demonstrate how such maps can be learned via standard DBM training using a novel noise schedule and are 
effective at both preserving and reducing intrinsic data dimensionality. The result is a class of highly expressive generative models, uniquely defined on a low-dimensional 
latent space, that afford principled Bayesian inference.

Check out additional details by visiting our inflationary flows website! A full preprint for this project is available [here](https://arxiv.org/abs/2407.08843), 
and code for reproducing the experiment results and training new models can be found [here](https://anonymous.4open.science/r/Inflationary_Flows-61F1/).

<!---This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML.--->
