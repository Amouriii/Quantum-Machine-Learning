# Mathematical & Quantum Information Notation

All research notes (`research/`), literature notes (`literature/`), simulation readmes (`simulations/`), and LaTeX manuscripts (`manuscripts/`) must follow the canonical notation below unless an explicit local override is declared in the document's **Notation & Assumptions** section.

---

## 1. Quantum States & Hilbert Spaces

| Concept | Notation | Notes |
| :--- | :--- | :--- |
| Hilbert space (general, dimension $d$) | $\mathcal{H}$, $\dim(\mathcal{H}) = d$ | Finite-dimensional complex Hilbert space unless stated otherwise |
| $n$-qubit Hilbert space | $\mathcal{H}_n = (\mathbb{C}^2)^{\otimes n}$ | Dimension $d = 2^n$ |
| Pure state (ket / bra) | $\|\psi\rangle, \|\phi\rangle \in \mathcal{H}$, $\langle\phi\|$ | Unit-normalized unless noted ($\langle\psi\|\psi\rangle = 1$) |
| Computational basis states | $\|x\rangle$, $x \in \{0, 1\}^n$ | Standard $Z$-basis |
| Inner product | $\langle\phi\|\psi\rangle$ | Linear in the second argument, conjugate-linear in the first |
| Outer product / projector | $\|\psi\rangle\langle\phi\|$, $\Pi$ | Rank-1 projector onto $\|\psi\rangle$: $\|\psi\rangle\langle\psi\|$ |
| Density operator space | $\mathcal{D}(\mathcal{H})$ | Positive semidefinite operators with unit trace: $\rho \succeq 0, \operatorname{Tr}[\rho] = 1$ |
| Density states | $\rho, \sigma \in \mathcal{D}(\mathcal{H})$ | Maximally mixed state on $\mathcal{H}_n$: $I_n / 2^n$ (or $I/d$) |

---

## 2. Operators, Circuits, Channels & Measurements

| Concept | Notation | Notes |
| :--- | :--- | :--- |
| Identity operator | $I$ or $I_n$ | Subscript denotes qubit count or subsystem when disambiguating |
| Single-qubit Pauli operators | $I, X, Y, Z$ (or $\sigma_x, \sigma_y, \sigma_z$) | $n$-qubit Pauli group modulo phases: $\mathcal{P}_n$ |
| Adjoint & transpose | $A^\dagger$, $A^\top$, $A^*$ | Conjugate transpose, transpose, entrywise complex conjugate |
| Unitary operator / group | $U \in \mathcal{U}(d)$ | Special unitary group: $\mathcal{SU}(d)$ |
| Parameterized quantum circuit (PQC) | $U(\boldsymbol{\theta})$, $\boldsymbol{\theta} \in \mathbb{R}^p$ (or $\Theta$) | Specify parameter domain and periodicity explicitly |
| Data-encoding / feature map unitary | $V(\mathbf{x})$ or $U_\phi(\mathbf{x})$ | Maps classical input $\mathbf{x} \in \mathcal{X}$ to quantum state $\rho(\mathbf{x})$ |
| Trace & partial trace | $\operatorname{Tr}[A]$, $\operatorname{Tr}_B[\rho_{AB}]$ | Always use `\operatorname{Tr}` (never bare `Tr`) |
| Commutator & anticommutator | $[A, B] = AB - BA$, $\{A, B\} = AB + BA$ | Specify when nested commutators are used (e.g., $\operatorname{ad}_A(B) = [A, B]$) |
| Quantum channel (CPTP map) | $\mathcal{E} : \mathcal{L}(\mathcal{H}_A) \to \mathcal{L}(\mathcal{H}_B)$ | Completely positive, trace-preserving linear map |
| Observables & Hamiltonians | $O, H$ (Hermitian: $H = H^\dagger$) | Expectation value: $\langle O \rangle_\rho = \operatorname{Tr}[O \rho]$ |
| POVM elements | $\{M_k\}_{k \in \mathcal{K}}$ | $M_k \succeq 0$, $\sum_k M_k = I$; outcome probability $\Pr[k] = \operatorname{Tr}[M_k \rho]$ |

---

## 3. Norms, Distances & Information Measures

| Concept | Notation | Definition / Notes |
| :--- | :--- | :--- |
| Vector $\ell_p$ / Euclidean norm | $\|\mathbf{v}\|_p$, $\|\mathbf{v}\|_2$ | $\|\mathbf{v}\|_2 = \sqrt{\sum_i \|v_i\|^2}$ |
| Trace norm (Schatten $1$-norm) | $\|A\|_1$ | $\|A\|_1 = \operatorname{Tr}[\sqrt{A^\dagger A}]$ |
| Frobenius / Hilbert–Schmidt norm | $\|A\|_F$ (or $\|A\|_2$) | $\|A\|_F = \sqrt{\operatorname{Tr}[A^\dagger A]}$ (specify if Schatten-$2$ notation is used) |
| Spectral / operator norm | $\|A\|_\infty$ (or $\|A\|_{\mathrm{op}}$) | Largest singular value $\sigma_{\max}(A)$ |
| Diamond norm | $\|\mathcal{E}\|_\diamond$ | Completely bounded trace norm over $\mathcal{E} \otimes \mathcal{I}$ |
| Trace distance | $D(\rho, \sigma)$ | $D(\rho, \sigma) = \frac{1}{2}\|\rho - \sigma\|_1$ |
| Quantum fidelity (Uhlmann) | $F(\rho, \sigma)$ | **Always state** whether $F(\rho, \sigma) = \left(\operatorname{Tr}\sqrt{\sqrt{\rho}\sigma\sqrt{\rho}}\right)^2$ or its square root is used |
| Von Neumann entropy | $S(\rho)$ | $S(\rho) = -\operatorname{Tr}[\rho \log \rho]$ (state logarithm base: $\log_2$ vs. $\ln$) |
| Quantum relative entropy | $D(\rho \| \sigma)$ | $D(\rho \| \sigma) = \operatorname{Tr}[\rho(\log \rho - \log \sigma)]$ when $\operatorname{supp}(\rho) \subseteq \operatorname{supp}(\sigma)$ |

---

## 4. Probability, Learning Theory & Computational Complexity

| Concept | Notation | Notes |
| :--- | :--- | :--- |
| Expectation & variance | $\mathbb{E}_{X \sim \mu}[\cdot]$, $\operatorname{Var}_{X \sim \mu}[\cdot]$ | Always subscript the distribution or Haar measure ($\mathbb{E}_{U \sim \mu_H}$) |
| Probability | $\Pr[\cdot]$ | Use `\Pr` with square brackets |
| Input, label & hypothesis spaces | $\mathcal{X}$, $\mathcal{Y}$, $\mathcal{F}$ | Training sample $S = \{(\mathbf{x}_i, y_i)\}_{i=1}^m \sim \mathcal{D}^m$ |
| True & empirical risk | $R(f)$, $\hat{R}_S(f)$ | Specify loss function $\ell : \mathcal{Y} \times \mathcal{Y} \to \mathbb{R}_{\ge 0}$ |
| Quantum kernel | $k(\mathbf{x}, \mathbf{x}') = \operatorname{Tr}[\rho(\mathbf{x})\rho(\mathbf{x}')]$ | Or state inner-product variant $\|\langle \psi(\mathbf{x}) \| \psi(\mathbf{x}') \rangle\|^2$ |
| Asymptotic notation | $\mathcal{O}(\cdot), \Omega(\cdot), \Theta(\cdot), \tilde{\mathcal{O}}(\cdot)$ | $\tilde{\mathcal{O}}(\cdot)$ hides polylogarithmic factors; state hidden parameters |
| Complexity classes | $\mathsf{P}, \mathsf{BPP}, \mathsf{BQP}, \mathsf{NP}, \mathsf{QMA}, \mathsf{PP}, \mathsf{PostBQP}$ | Always use `\mathsf{...}` |
| Logarithms | $\log_2$, $\ln$ | Specify base explicitly whenever constant factors matter (e.g., entropy, sample complexity) |

---

## 5. General Formatting Rules

1. **Bold vectors, calligraphic spaces:** Classical vectors in bold lowercase ($\mathbf{x}, \boldsymbol{\theta}$), matrices/operators in uppercase ($U, H, O$), spaces/classes/channels in calligraphic ($\mathcal{H}, \mathcal{X}, \mathcal{E}$), complexity classes in sans-serif ($\mathsf{BQP}$).
2. **No ambiguous overloads:** Never reuse the same symbol for different quantities within a single document (e.g., circuit depth $L$ vs. Lipschitz constant $L$ — disambiguate as $L_{\mathrm{depth}}$ or $L_{\mathrm{Lip}}$).
3. **Explicit parameter dependencies:** When proving scaling bounds, list all variables hidden inside $\mathcal{O}(\cdot)$ or $\Omega(\cdot)$ constants.
4. **Local Overrides:** If an adapted external theorem uses conflicting notation (e.g., $\tilde{F}$ for fidelity or $D$ for circuit depth), declare the mapping explicitly in the document's **Notation & Assumptions** section before reproducing the statement.
