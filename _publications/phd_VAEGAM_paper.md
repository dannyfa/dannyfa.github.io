---
title: "Deep Generative Analysis for Task-Based Functional MRI Experiments"
collection: publications
permalink: /publication/phd_VAEGAM_paper
excerpt: 'In this work we follow a Generalized Additive Model (GAM) approach to construct a 3D convolutional VAE capable of more flexibly modeling entire brain volumes, while preserving interpretability.'
date: 2021-08-01
venue: 'Journal of Machine Learning Research'
paperurl: 'https://proceedings.mlr.press/v149/albuquerque21a/albuquerque21a.pdf'
citation: '<strong>De Albuquerque, D.</strong>, Goffinet, J., Wright, R., & Pearson, J. (2021). &quot;Deep Generative Analysis for Task-Based Functional MRI Experiments.&quot; <i>Journal of Machine Learning Research</i>. 149(1-29).'
---

<i>Abstract:</i> While functional magnetic resonance imaging (fMRI) remains one of the most widespread
and important methods in basic and clinical neuroscience, the data it produces—time series
of brain volumes—continue to pose daunting analysis challenges. The current standard
(“mass univariate”) approach involves constructing a matrix of task regressors, fitting a
separate general linear model at each volume pixel (“voxel”), computing test statistics for
each model, and correcting for false positives post hoc using bootstrap or other resampling
methods. Despite its simplicity, this approach has enjoyed great success over the last two
decades due to: 1) its ability to produce effect maps highlighting brain regions whose
activity significantly correlates with a given variable of interest; and 2) its modeling of
experimental effects as separable and thus easily interpretable. However, this approach
suffers from several well-known drawbacks, namely: inaccurate assumptions of linearity
and noise Gaussianity; a limited ability to capture individual effects and variability; and
diculties in performing proper statistical testing secondary to independently fitting voxels.
In this work, we adopt a different approach, modeling entire volumes directly in a manner
that increases model flexibility while preserving interpretability. Specifically, we use a
generalized additive model (GAM) in which the effects of each regressor remain separable,
the product of a spatial map produced by a variational autoencoder and a (potentially
nonlinear) gain modeled by a covariate-specific Gaussian Process. The result is a model that
yields group-level effect maps comparable or superior to the ones obtained with standard
fMRI analysis software while also producing single-subject effect maps capturing individual
differences. This suggests that generative models with a decomposable structure might offer
a more flexible alternative for the analysis of task-based fMRI data.