# Natural Convection And Phase Change

<!---
![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.6.0-red)
![CUDA](https://img.shields.io/badge/CUDA-12.4-green)
-->

$$
\begin{aligned}
\nabla \cdot \mathbf{u} &= 0, \\
\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u}\cdot\nabla)\mathbf{u} + \nabla p - \frac{1}{Re}\nabla^2\mathbf{u} - F(\theta)\mathbf{e} - A(\theta)\mathbf{u} &= 0, \\
\frac{\partial \theta}{\partial t} + (\mathbf{u}\cdot\nabla)\theta - \frac{1}{Re Pr}\nabla^2\theta + \frac{1}{Ste}\frac{\partial \varphi_\delta(\theta)}{\partial t} &= 0.
\end{aligned}
$$

Physics Informed Neural Networks for the natural convection problems and for phase change materials

 * time indep natural convection
 * time dep natural convection
 * convection of water
 
 * Phase change materials
 * Phase change materials with cylindrical geometry
 
 - Implemented PINN architectures
    - Multi-Layer Perceptron 
    - FF
    - ST - FF
 
 - Other
    - Adaptative Loss Weights
    
    
<br>

<p align="center">
  <img src="docs/Gif/Okada.gif" height="300">
  &nbsp;&nbsp;
  <img src="docs/Gif/Luo.gif" height="300">
</p>

<p align="center">
  <em> Temperature field (T) and phase-change interface evolution (s) predicted by Physics-Informed Neural Networks.</em>
</p>

<br>

<!--

# Contributors

**List of contributors:** ...

# Cite us

Please consider citing our work if you found it useful to yours, using this [Test](https://www.sciencedirect.com/science/article/pii/S0017931025007690?casa_token=1TaxBElUNmAAAAAA:md-kcpgBhBkPRF1DRkYPRcLGgx-DZWMHl9A2BTsZzDXjiWraMfpE1N66jHPHC-6zAgXJNhu-Etv-)

```bibtex
@article{madir2025physics,
  title={Physics Informed Neural Networks for Heat Conduction with Phase Change},
  author={Madir, Bahae-Eddine and Luddens, Francky and Lothod{\'e}, Corentin and Danaila, Ionut},
  journal={International Journal of Heat and Mass Transfer},
  volume={252},
  pages={127430},
  year={2025},
  publisher={Elsevier}
}
```

# Acknowledgement

Special thanks to ...

-->
