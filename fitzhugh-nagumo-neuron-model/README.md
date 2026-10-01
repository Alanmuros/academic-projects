# Dynamical Study of the FitzHugh–Nagumo Neuron Model

**Course:** Mathematical Methods 1 — BSc in Physics Engineering, UPC (2026)
**Authors:** Alan Muros Tapia, Laia Sardà Vera
**Language:** report in Catalan; this summary in English

<!-- Optional: add a picture exported from the report (create an "images" folder), e.g.
![Bifurcation diagram](images/bifurcation-diagram.png) -->

## Summary

The FitzHugh–Nagumo model reduces the four-dimensional Hodgkin–Huxley equations to two variables — a fast voltage-like variable $V$ and a slow recovery variable $W$ — while keeping the essential features of neuronal excitability: a firing threshold, all-or-none spikes and repetitive firing.

This project studies the model analytically and numerically, using the external current $I_\text{ext}$ as the control parameter:

$$\dot V = V - \frac{V^3}{3} - W + I_\text{ext}, \qquad \dot W = \frac{1}{\tau}\,(V + a - bW)$$

## What was done

- **Qualitative analysis:** nullclines, equilibria (found with Newton's method), linearisation and classification with the trace–determinant criterion (saddle, node, focus).
- **Number of equilibria:** for $b<1$ the equilibrium equation has a single root; for $b>1$ up to three roots are possible.
- **Hopf bifurcation:** the condition $\mathrm{tr}(J)=0$ gives the critical equilibrium $V^*_c=-\sqrt{1-b/\tau}$ and the critical current $I_c$; the transversality condition was checked.
- **Numerical simulation (MATLAB):** phase portraits with vector fields, time series, nullcline shifts for increasing $I_\text{ext}$ and a bifurcation diagram, computed with `ode45` (tolerances $10^{-8}$).
- **Physical interpretation:** saddle as firing threshold, limit cycle as periodic spiking, relaxation oscillations from the fast–slow structure.

## Main results

For the classical parameters $a=0.7$, $b=0.8$, $\tau=12.5$:

| Quantity | Value |
|---|---|
| Critical equilibrium $V^*_c$ | −0.9675 |
| Critical equilibrium $W^*_c$ | −0.3343 |
| Critical current $I_c$ | ≈ 0.3313 |

- $I_\text{ext}<I_c$: stable equilibrium (spiral); the neuron stays at rest.
- $I_\text{ext}=I_c$: Hopf bifurcation; the equilibrium loses stability.
- $I_\text{ext}>I_c$: stable limit cycle, i.e. sustained relaxation oscillations (shown for $I_\text{ext}=0.7$).

## Files

| File | Description |
|---|---|
| [`fhn_report.m`](FHN_Report.pdf) | Full report (Catalan) |
| [`fhn_simulation.m`](FHN_Simulation.pdf) | MATLAB code that generates all the figures |

## How to run

Requires MATLAB R2018b or later (it uses `yline`, `xline` and `sgtitle`); no toolboxes are needed. Open `fhn_simulation.m` and press **Run**. It prints the critical values and the classification of the equilibrium for each current, and produces the phase portraits, the nullcline sweep, the bifurcation diagram and the plots of $f'(V)$.

## References

1. R. FitzHugh, "Impulses and physiological states in theoretical models of nerve membrane", *Biophysical Journal* 1(6), 445–466 (1961).
2. J. Nagumo, S. Arimoto, S. Yoshizawa, "An active pulse transmission line simulating nerve axon", *Proceedings of the IRE* 50(10), 2061–2070 (1962).
3. A. L. Hodgkin, A. F. Huxley, "A quantitative description of membrane current and its application to conduction and excitation in nerve", *The Journal of Physiology* 117(4), 500–544 (1952).
4. S. H. Strogatz, *Nonlinear Dynamics and Chaos*, 3rd ed., CRC Press (2024).
