# supres-pmct

Diffusion super-resolution and organ-aware classification for cause-of-death identification from thick-slice post-mortem CT (PMCT).

This repository accompanies a manuscript currently under review. **Code will be released here on acceptance.**

---

## What this is

Forensic services hold large archives of thick-slice PMCT, while automated interpretation methods assume the thin-slice acquisition that many services cannot obtain or retain. This project evaluates two routes for making archived thick-slice scans usable for automated cause-of-death identification:

1. **Super-resolution before classification.** A 3D residual-shifting diffusion model reconstructs thin-slice-equivalent volumes from thick-slice input, which are then classified.
2. **Organ-aware classification applied directly.** A multiple-instance learning network with class-conditional attention takes the thick-slice volume alongside an organ mask, with no reconstruction step.

Both were evaluated against real paired thin- and thick-slice reconstructions of the same acquisition, so no synthetic downsampling was involved.

## Data

**This repository contains code only. No imaging data, derived arrays, or decedent identifiers are included or will be added.**

The study used the New Mexico Decedent Image Database (NMDID), maintained by the Office of the Medical Investigator, University of New Mexico. NMDID is available to credentialed researchers under its own data use agreement: <https://nmdid.unm.edu>

Under that agreement the authors cannot redistribute the imaging data or publish decedent identifiers. The cohort selection criteria are reported in full in the manuscript Methods and Supplementary Material so that an equivalent cohort can be reconstructed by credentialed researchers.

The licence in this repository covers the source code only. It confers no rights over NMDID data.

## Environment

| Component | Version |
|---|---|
| Python | 3.14.2 |
| PyTorch | 2.10.0 (CUDA 13.0) |
| MONAI | 1.5.2 |
| TotalSegmentator | 2.12.0 |

Trained model weights are available from the corresponding author on reasonable request.

## Acknowledgement

This study made use of the New Mexico Decedent Image Database. As required by the database's data use agreement:

> The Free Access Decedent Database funded by the National Institute of Justice grant number 2016-DN-BX-0144.

## Citation

Citation details will be added on acceptance.

```bibtex
@article{yuan_supres_pmct,
  title   = {Toward Deployable Virtual Autopsy: Deep Learning for Cause-of-Death
             Identification from Resource-Constrained Post-mortem CT},
  author  = {Yuan, Yu Hui and Li, Shiyi and Sun, Ruochen and Hu, Yuyang
             and Rong, Jia and Xing, Fangxu},
  note    = {Manuscript under review},
  year    = {2026}
}
```

## Licence

See [LICENSE](LICENSE). Applies to source code only, not to NMDID data.
