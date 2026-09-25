# Algorithmic Collusion in Financial Markets

Can self-interested trading algorithms learn to collude without communicating? This project revisits the framework of **Dou et al. (2025)**: a multi-speculator extension of **Kyle (1985)** with information-insensitive investors, in which Q-learning speculators trade against each other.

*Clemente Esquinas Coves, 2026*

📄 **[Read the full report (PDF)](report/algorithmic_collusion_report.pdf)**

## What's inside

**Theory.** Closed-form linear Nash and cartel equilibria (trading intensity χ, price impact λ, per-speculator profit) at ξ = 0, and numerical solutions for ξ > 0. The cartel earns strictly more per speculator than Nash for I ≥ 2.

**Market quality.** Liquidity L = 1/λ, price informativeness, and noise-trader losses, with comparative statics in the number of speculators I at ξ = 0 and ξ = 500, and a discussion of the effective number of insiders I*.

**Q-learning experiments.** Implementation of the Dou et al. (2025) protocol, measurement of the collusion index Δχ in both regimes, and noise-shock impulse-response analysis to separate collusion sustained by price-trigger strategies from collusion driven by over-pruning bias. Includes a multi-seed robustness check.

## Repository structure

```
├── notebooks/
│   └── algorithmic_collusion.ipynb   # all computations, organised by exercise
├── report/
│   └── algorithmic_collusion_report.pdf
├── figures/                          # plots are saved here when the notebook runs
├── requirements.txt
└── README.md
```

## Running it

```bash
git clone https://github.com/<your-username>/algorithmic-collusion-kyle.git
cd algorithmic-collusion-kyle
pip install -r requirements.txt
jupyter notebook notebooks/algorithmic_collusion.ipynb
```

The Q-learning simulations are JIT-compiled with Numba; the multi-seed experiments take noticeably longer than the analytical sections.

## References

- Dou, W. W., Goldstein, I., & Ji, Y. (2025). *AI-Powered Trading, Algorithmic Collusion, and Price Efficiency.*
- Kyle, A. S. (1985). Continuous Auctions and Insider Trading. *Econometrica*, 53(6), 1315–1335.
