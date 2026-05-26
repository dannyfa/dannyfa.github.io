---
title: "Dynamic Compression Flows for Neuroscience Data"
excerpt: "Low-dimensional, identifiable, and dynamics preserving representation learning for neuroscience data using Flow-Matching<br/><center><img src='https://sites.duke.edu/ifsprojectassets/files/2026/05/DCF_concept.jpg' width='70%'></center>"
collection: portfolio
mathjax: true
---

<figure>
<br/><img src='https://sites.duke.edu/ifsprojectassets/files/2026/05/DCF_concept.jpg' width='70%'>
<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js">
</script>
<figcaption><strong>Dynamic Compression Flows for dimension reduction.</strong> Dynamical data \( \mathbf{x}_t \) at \( \tau=1 \) with dynamics defined by \( \mathbf{v}_{\boldsymbol{\theta}} \) are mapped to a lower-dimensional compressed representation (\( \tau=0 \)) via a compressive/generative flow \( \mathbf{u}_{\boldsymbol{\phi}} \). Both \( \mathbf{u}_{\boldsymbol{\phi}} \) and \( \mathbf{v}_{\boldsymbol{\theta}} \) are trained via flow matching defined by an encoder/coupling \( \boldsymbol{\mu}_{\boldsymbol{\psi}} \).</figcaption>
</figure>

Modern neuroscience data are often thought to be complex and can have up to hundreds of thousands of dimensions. However, recent work has shown that these data are actually governed by much lower-dimensional dynamics. As such, developing techniques capable of capturing these low-dimensional representations of the data has become all but essential to neuroscientists. Existing methods often focus on either 1) finding low-dimensional representations of the data (while disregarding temporal structure), 2) capturing the temporal dynamics of the data (without compression), or 3) both, but often with unrealistic, strong modeling assumptions. 

In this project, we used an existing deep generative model technique called “Flow Matching” to learn flow-fields capable of seamlessly transporting the data into a lower-dimensional representation while also preserving its intrinsic temporal structure. We applied this new method to multiple real open-source neuroscience datasets (see example below), and compared it against several competing approaches showing its ability to discover lower-dimensional dynamics directly from data, even in challenging scenarios where conventional models tend to fail. Of note, we also showed that the low-dimension representations learned are unique (up to sign flips) and can be recovered consistently across different experimental runs. We hope that this work can provide a tool for neuroscientists to analyze and better understand their data, ultimately yielding new insights into brain dynamics and function.

Our [manuscript](https://www.biorxiv.org/content/10.64898/2026.02.12.705535v1) on this work was accepted to ICML 2026. Additional details on this project can be found in our [project website](https://dannyfa.github.io/DCF_Teaser/) and code for reproducing experimental results can be found in this [repository](https://github.com/dannyfa/Velocity_Flow_Matching/tree/cleaned).


<figure>
<br/><img src='https://sites.duke.edu/ifsprojectassets/files/2026/05/musal_main_comparison-scaled.jpg' width='100%'>
<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js">
</script>
<figcaption><strong>Example of latent structure discovered by our model in mouse behavioral video.</strong><strong>(A)</strong> Flowed latent structure forms four prominent bands (colored points), with outliers marked by maximal latent distance (brown \( \times \)) and maximal velocity magnitude (cyan \( \times \)).<strong>(B)</strong> Representative snapshots along each band (top/mid/low in \( \mu_3 \)). Lowering \( \mu_3 \) corresponds to stronger mouth movement, paw lift, or both. <strong>(C)</strong> Outlier frames selected by maximal latent distance (left) or maximal velocity magnitude (right), correspond to transient paw and controller movements.<strong>(D)</strong> 3D Latent representations across 6 different comparison models. Most either collapse the four bands or fail to capture outliers.</figcaption>
</figure>


<!---This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML.--->
