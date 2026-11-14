# QuantumNotebooks
Set of notebooks on selected computational topics of Quantum Physics.

## Contents

Each notebook poses a problem as a semidefinite program and solves it twice: with SCS through CVXPY as a
reference, and through the regularized dual with `sdplab` and `spacecore`.

| Notebook | Problem |
| --- | --- |
| [Quantum state tomography](notebooks/tomography.ipynb) | Reconstruct a state from the measured values of a set of observables |
| [Quantum state discrimination](notebooks/state_discrimination.ipynb) | Find the measurement that best identifies which state of a known ensemble was sent |
| [Multimarginal quantum optimal transport](notebooks/multimarginal_qot.ipynb) | Find the coupling of least cost among states with prescribed marginals |

## Notation

| Symbol | Meaning |
| --- | --- |
| $\mathcal{H}$ | Hilbert space of dimension $d$ |
| $\mathbb{H}(\mathcal{H})$ | Hermitian operators on $\mathcal{H}$ |
| $\mathbb{H}_{\ge}(\mathcal{H})$ | Positive semidefinite Hermitian operators on $\mathcal{H}$ |
| $\mathrm{I}$, $\mathrm{I}_{\mathcal{H}}$ | Identity operator on $\mathcal{H}$ |
| $\operatorname{Tr}$ | Trace |
| $A \succeq B$ | $A - B$ is positive semidefinite |
| $\langle A, B \rangle$ | $\operatorname{Tr}[AB]$ for Hermitian $A$, $B$ |
| $[n]$ | The index set $\{1, \dots, n\}$ |
| $\varepsilon$ | Regularization strength, $\varepsilon > 0$ |
| $\varphi$ | Regularizer: a convex function on $[0, +\infty)$ applied to the eigenvalues |
| $\psi$, $\psi'$ | Legendre transform $\psi = \varphi^*$ and its derivative |
| $X^*$ | An optimizer of the problem in which $X$ is the variable |
| $\mathcal{H}_1 \otimes \cdots \otimes \mathcal{H}_N$ | Joint space of $N$ copies of $\mathcal{H}$ |
| $\operatorname{Tr}^{i}[\Gamma]$ | The $i$-th marginal of $\Gamma$: the partial trace over every factor but $\mathcal{H}_i$ |
| $\Gamma \mapsto (\rho_1, \dots, \rho_N)$ | $\Gamma$ is a coupling: positive semidefinite with $\operatorname{Tr}^{i}[\Gamma] = \rho_i$ for every $i$ |
| $U_1 \oplus \cdots \oplus U_N$ | Kronecker sum $\sum_i \mathrm{I} \otimes \cdots \otimes U_i \otimes \cdots \otimes \mathrm{I}$, with $U_i$ in the $i$-th slot |
