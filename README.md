# Spam Detection

Building a neural network to classify emails as spam, as well as "traditional" competitor models. Models are built in `R/models.qmd`. The rendered notebook is also attached as HTML.

![](figures/pca.png)

## Neural Network

Sequential model (multilayer perceptron) built with keras/tensorflow. Key facts: Adam optimizer, weight decay (L2-regularization), learning rate scheduling, early stopping. This is the architecture:

<p align="center">
    <img src="figures/neural_network.png" alt="Description" width="300">
</p>

![](figures/training_curves.png)

![](figures/training_curves_metrics.png)

## Benchmark against traditional models

![](figures/uncertainty_precision.png)

### Test metrics & performance

| Model | Precision | Accuracy | F1 |
|-------|-----------|----------|----|
| Neural Network | 0.932 | 0.939 | 0.922 |
| Random Forest | **0.935** | **0.942** | **0.926** |

![](figures/test_bootstrapped_ci.png)

![](figures/confidence.png)

![](figures/roc_curves.png)
