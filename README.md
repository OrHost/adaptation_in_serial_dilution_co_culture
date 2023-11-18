# Adaptation in a Serial-Dilution Co-culture

A consumer-resource modeling framework in a serial-dilution setup, where $m$ species compete for $p$ nutrients in a series of batches. At each batch, a nutrient mixture with a fixed composition $\lbrace c_i(t=0)\rbrace_{i=1}^p$ and total amount $c_0=\sum_i c_i(0)$. Similarly, a mixture of species $\lbrace\rho_\sigma(t=0)\rbrace_{\sigma=1}^m$ is added, with a fixed total amount $\rho_0=\sum_\sigma \rho_\sigma(0)$. Species grow until the depletion of nutrients, the culture is diluted, and a new batch starts, while keeping relative species populations.
Each species has a *metbolic strategy*, $\vec{\alpha}_ \sigma$, which is a vector of enzyme levels, while given a fixed enzyme budget $E_\sigma=\sum_i \alpha_{\sigma,i}$. Nutrient consumption rates are given by $j_{\sigma,i}=\frac{c_i}{K+c_i}\alpha_{\sigma,i}$.

Dynamics within each batch are given by (Erez et al.):
```math
\frac{d\rho_\sigma}{dt}=\rho_\sigma \sum_{i=1}^p j_{\sigma,i}   \quad,
```
```math
\frac{dc_i}{dt}=-\sum_{\sigma=1}^m \rho_\sigma j_{\sigma,i}   \quad,


```
```math
\frac{d\alpha_{\sigma,i}}{dt}=(\mathbb{P}_{\sigma,i} E_\sigma-\alpha_{\sigma,i})\sum_{i'=1}^p j_{\sigma,i'}
```

## Script Index



## Data and Plots

Data and corresponding figures are automatically saved with easily identifiable, corresponding file names (including the simulation type and important parameter values), in the [*Data*](Data/) and [*Plots*](Plots/) directories, respectively.
