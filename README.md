# Natural Convection And Phase Change

<!---
![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.6.0-red)
![CUDA](https://img.shields.io/badge/CUDA-12.4-green)
-->

## The Enthalpy-Porosity Model

We consider a solid–liquid system placed in a 2D domain $\Omega$. The dimensionless system of equations to be solved in both liquid and solid regions is based on the incompressible Navier–Stokes equations, with Boussinesq approximation for buoyancy effects, and a temperature transforming model for the energy equation:

$$
\begin{aligned}
\nabla \cdot \mathbf{u} &= 0, \\
\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u}\cdot\nabla)\mathbf{u} + \nabla p - \frac{1}{Re}\nabla^2\mathbf{u} - F(\theta)\mathbf{e}_y - A(\theta)\mathbf{u} &= 0, \\
\frac{\partial \theta}{\partial t} + (\mathbf{u}\cdot\nabla)\theta - \frac{1}{Re Pr}\nabla^2\theta + \frac{1}{Ste}\frac{\partial \varphi_\delta(\theta)}{\partial t} &= 0.
\end{aligned}
$$

The buoyancy term $F(\theta)$ models density variations induced by temperature gradients, enabling the simulation of natural convection within the liquid region. The term $A(\theta)\mathbf{u}$ force the velocity to vanish in the solid phase.

The energy equation incorporates the latent heat contribution through the regularized Heaviside function $\varphi_\delta(\theta)$, which smoothly captures the solid–liquid transition. Consequently, the model can represent melting and solidification processes without the need for explicit interface tracking.

---

We investigate several problems involving natural convection and phase change using Physics-Informed Neural Networks (PINNs):

### Natural Convection
- The time independent problem of natural convection for different Rayleigh number $Ra$ regimes ($10^4 - 10^7$).
- The time dependent problem of natural convection at $Ra = 10^6$.
- Natural convection of water, where the density–temperature relationship is non-linear.

### Phase Change
- Melting of *n*-octadecane ([Okada benchmark](https://www.sciencedirect.com/science/article/pii/0017931084901923)).
- Melting in a cylindrical geometry.

The PINN-based strategies developed for these problems are systematically compared against accurate [Finite Element](https://www.sciencedirect.com/science/article/pii/S0010465520302319?casa_token=7a_ArBSS1QAAAAAA:OFWAwbIGBVpRSHVYhvKpzbeEY7XD8NmTarJlbb3QSLm6FyQbhti3Tcng6naA4G_dign_HTKPbXLO) simulations to assess their accuracy.

<br>

<p align="center">
  <img src="docs/Gif/Okada.gif" height="350">
  &nbsp;&nbsp;
  <img src="docs/Gif/Luo.gif" height="400">
</p>

<p align="center">
  <em> Temperature field (T), velocity vector field ([u, v]), and phase-change interface evolution (s) predicted by Physics-Informed Neural Networks.</em>
</p>

<br>

## References

A preprint will be available soon.

<!--
---

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
-->

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
