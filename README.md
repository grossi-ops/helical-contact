# 3M — Helical Attractors on Contact 3-Manifolds

**Principia Orthogona · Vol. IV · IMPA Edition**
Pablo Nogueira Grossi · G6 LLC · 2026
DOI: [10.5281/zenodo.19117400](https://doi.org/10.5281/zenodo.19117400)

Publisher hub for *Helical Attractors on Contact 3-Manifolds* — the fourth volume of Principia Orthogona, the IMPA-facing edition, and the support site for the XII Bienal de Matemática 2026 mini-curso at UFRN (Natal-RN).

---

## Live pages (GitHub Pages)

| Path | What it is |
| --- | --- |
| [`index.html`](./index.html) | Publisher landing — cover-forward hero, DOI CTA, companion tiles, embedded 3D sim |
| [`chE-gtct.html`](./chE-gtct.html) | Chapter E — GTCT for Everyone (nine axioms, four theorems, twelve operators) |
| [`sessions/session1-contact-geometry.html`](./sessions/session1-contact-geometry.html) | Mini-curso S1 · 60 min · Contact geometry & the dm³ system |
| [`sessions/session2-theorem-basin.html`](./sessions/session2-theorem-basin.html) | Mini-curso S2 · 60 min · Theorem 2.1 & the asymmetric basin |
| [`sessions/session3-lean-skeleton.html`](./sessions/session3-lean-skeleton.html) | Mini-curso S3 · 60 min · Lean 4 skeleton & AXLE Issue #12 |
| [`sims/helical-attractor.html`](./sims/helical-attractor.html) | Standalone 3D Three.js simulator for the dm³ flow |

## Repo structure

```
3M/
├── index.html                          publisher landing page
├── chE-gtct.html                       Chapter E (GTCT for Everyone)
├── README.md                           this file
├── PO_10_Pablo_Grossi.pdf              SBM 3-page submission (at repo root)
├── Not_PO_T10_Pablo_Grossi.pdf         SBM notification / alt
│
├── assets/                             static assets
│   ├── book-cover.png                  rendered cover (from preprint p.1)
│   └── book-cover-sm.png               thumbnail
│
├── sessions/                           three 60-min mini-curso handouts
│   ├── session1-contact-geometry.html  S1 · contact geometry + dm³
│   ├── session2-theorem-basin.html     S2 · Theorem 2.1 + Table 1
│   └── session3-lean-skeleton.html     S3 · Lean 4 / AXLE Issue #12
│
├── sims/                               interactive visualisations
│   └── helical-attractor.html          Three.js 3D dm³ simulator (r128)
│
├── labs/                               numerical reproducibility
│   └── dm3_numeric.py                  DOP853 reproduction of Table 1
│
└── submissions/                        conference submission PDFs
    └── XII_BM_MINICURSO_T1_Pablo_Grossi_preview.pdf   XII Bienal mini-curso preview
```

## Citation

```bibtex
@misc{Grossi2026Helical,
  author       = {Pablo Nogueira Grossi},
  title        = {Helical Attractors on Contact 3-Manifolds
                  (Principia Orthogona, Vol. IV)},
  year         = 2026,
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.19117400},
  url          = {https://doi.org/10.5281/zenodo.19117400}
}
```

## Companion repositories

- **AXLE** (Lean 4 / Mathlib 4 formalisation): <https://github.com/TOTOGT/AXLE>
- **GTCT** (Generative Temporal Contact Theory): <https://github.com/TOTOGT/GTCT>

## Running the numerical lab

```bash
pip install numpy scipy
python3 labs/dm3_numeric.py            # reproduces Table 1
python3 labs/dm3_numeric.py --plot     # saves dm3_trajectories.png (requires matplotlib)
```

Expected output: five outer-basin rows with $\hat\mu \to -2$, five inner-basin rows showing collapse for $r(0) < 0.80$.

## Design language

All pages share the Principia Orthogona dark-teal publisher aesthetic defined in `chE-gtct.html`:

- Palette: `--t #2dd4bf` (teal), `--bg #060f0e` (near-black), `--bg2 #0c1a18` (panel), `--gd #c9a84c` (accent gold).
- Op-chain colours: `--c #4a9eff` (contract), `--k #e05a3a` (curvature), `--f #50c878` (filter), `--u #c084fc` (unfold).
- Typography: Georgia serif for prose, Courier New for chrome/labels.
- MathJax 3 (`tex-svg`) for live math; Three.js r128 for 3D; all loaded from CDN, no build step.

## License

© 2026 Pablo Nogueira Grossi — G6 LLC. MIT License. ORCID: 0009-0000-6496-2186.
