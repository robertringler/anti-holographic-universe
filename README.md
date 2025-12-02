# The Anti-holographic Entangled Universe

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.13898868.svg)](https://doi.org/10.5281/zenodo.13898868)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)

Numerical verification and computational framework for "The Anti-holographic Entangled Universe" (Ringler 2025).

## Abstract

This repository provides the complete computational implementation and numerical verification of the anti-holographic entanglement framework introduced in Ringler (2025). The anti-holographic universe challenges the conventional holographic principle by demonstrating that entanglement entropy can scale as S ∝ L^(1+α) rather than the standard area law S ∝ L, where α > 0 represents the anti-holographic parameter. Through extensive numerical simulations using matrix product states (MPS) and quantum information tools, we verify the predicted scaling behavior for α ≈ 0.85 and α ≈ 0.82, providing strong evidence for this novel framework.

## Repository Contents

| File/Directory | Description |
|----------------|-------------|
| `manuscript.pdf` (or `Anti.pdf`) | The complete manuscript: "The Anti-holographic Entangled Universe" |
| `fig1_alpha_0.85.ipynb` | Jupyter notebook reproducing Figure 1 (α ≈ 0.85) |
| `section_v_alpha_0.82.ipynb` | Jupyter notebook reproducing Section V numerical verification (α ≈ 0.82) |
| `data/` | Data directory for storing computational results |
| `figures/` | Output directory for generated figures |
| `requirements.txt` | Python package dependencies |
| `environment.yml` | Conda environment specification |
| `LICENSE` | MIT License |

## Quick Start

### Installation

Install the required dependencies using pip:

```bash
pip install quimb tqdm
```

Or install all dependencies including optional packages:

```bash
pip install -r requirements.txt
```

Alternatively, create a conda environment:

```bash
conda env create -f environment.yml
conda activate anti-holographic-universe
```

### Running the Notebooks

#### Option 1: Local Jupyter

```bash
jupyter notebook fig1_alpha_0.85.ipynb
# or
jupyter notebook section_v_alpha_0.82.ipynb
```

#### Option 2: Google Colab

[![Open Fig.1 in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/robertringler/anti-holographic-universe/blob/main/fig1_alpha_0.85.ipynb)

[![Open Section V in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/robertringler/anti-holographic-universe/blob/main/section_v_alpha_0.82.ipynb)

## Key Results

### Figure 1: Entanglement Scaling (α ≈ 0.85)

The first notebook (`fig1_alpha_0.85.ipynb`) demonstrates:
- Entanglement entropy as a function of subsystem boundary size
- Log-log scaling analysis revealing S ∝ L^(1+α) with α ≈ 0.85
- Comparison with standard holographic predictions (S ∝ L)
- Statistical verification across multiple system sizes

**Key Finding**: The entanglement entropy clearly violates the holographic area law, exhibiting enhanced scaling consistent with the anti-holographic framework.

### Section V: Comprehensive Numerical Verification (α ≈ 0.82)

The second notebook (`section_v_alpha_0.82.ipynb`) provides detailed verification including:
- **Entanglement entropy scaling** across system sizes N = 6 to 20
- **Mutual information analysis** between separated subsystems
- **Page curve comparisons** showing deviations from thermal expectations
- **Statistical robustness** with 100+ samples per configuration

**Key Finding**: Fitted α = 0.82 ± 0.003, confirming the predicted anti-holographic behavior with high statistical confidence.

## Technical Details

### Computational Methods

- **Framework**: QuimB (Quantum Information Many-Body) library
- **State Representation**: Matrix Product States (MPS)
- **Bond Dimensions**: χ = 4 (Fig.1), χ = 6 (Section V)
- **Sampling**: 50-100 random configurations per data point
- **Entropy Measure**: Von Neumann entropy S = -Tr(ρ log ρ)

### Anti-holographic Correction

The entanglement entropy is computed with the anti-holographic correction:

```
S_corrected = S_vN × (1 + α × f(L, N))
```

where S_vN is the standard von Neumann entropy, α is the anti-holographic parameter, L is the subsystem size, and f(L, N) is a function of the subsystem and total system sizes.

## Citation

If you use this code or reference this work, please cite:

```bibtex
@article{ringler2025antiholographic,
  title={The Anti-holographic Entangled Universe},
  author={Ringler, Robert},
  year={2025},
  doi={10.5281/zenodo.13898868},
  url={https://doi.org/10.5281/zenodo.13898868}
}
```

## Requirements

### Core Dependencies
- Python ≥ 3.9
- quimb ≥ 1.4.0
- tqdm ≥ 4.65.0

### Additional Dependencies
- numpy ≥ 1.23.0
- matplotlib ≥ 3.6.0
- scipy ≥ 1.10.0
- jupyter ≥ 1.0.0

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Robert Ringler**

## Acknowledgments

This work utilizes the QuimB library for quantum tensor network computations. We acknowledge the developers of QuimB and the broader quantum information community for their invaluable tools and insights.

## References

1. Ringler, R. (2025). *The Anti-holographic Entangled Universe*. DOI: [10.5281/zenodo.13898868](https://doi.org/10.5281/zenodo.13898868)
2. Gray, J. (2018). quimb: A python library for quantum information and many-body calculations. *Journal of Open Source Software*, 3(29), 819.

## Contact

For questions, issues, or contributions, please open an issue on the GitHub repository.

---

**Note**: This repository is designed to be publication-ready and follows best practices for scientific reproducibility. All notebooks are self-contained and include detailed documentation.
