# A Face-On Perspective: Exploring Sersic Indices in Galaxies

![Language](https://img.shields.io/badge/language-Python-blue.svg)
![Status](https://img.shields.io/badge/status-Completed-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue)

## 🌌 Project Overview

This project focuses on characterizing the morphology of three face-on galaxies—NGC3982, NGC2865, and NGC7773—using Sérsic index fitting techniques. The Sérsic index is a fundamental parameter describing how light is distributed in galaxies and reveals information about their bulge-disc structure, formation, and evolution.



## 🧪 Scientific Objective

- Estimate the Sérsic index for each galaxy using observational data.
- Use both single and double Sérsic profile fitting (bulge + disc components).
- Compare the extracted indices with theoretical models to deduce galactic structure.
- Classify galaxies based on the light concentration and morphological type.

## Target Galaxies
| Galaxy       | Type             | Single Sersic  | Bulge n      | Disc n       |
|--------------|------------------|----------------|--------------|--------------|
| NGC3982      | Spiral           | 0.8            | 2.1          | 0.2          | 
| NGC2865      | Elliptical       | 2.4            | 3.1          | 0.3          |
| NGC7773      | Barred Spiral    | 1.9            | 2.3          | 0.2          |



## 📂 Repository Structure

```bash
Galaxy_Sersic_Project/
├── LCO data/                # FITS images from LCO
├── notebooks/
│   ├── NGC3982.ipynb        # Sérsic profile fitting and visualization
├── results/                 # Plots of brightness profiles and fits
├── Paper/                   # Project report (PDF)
├── README.md                # Project documentation
```


## ⚙️ Methodology

### 1. Data Acquisition

- FITS files obtained via LCO telescope observations.
- Targeted face-on galaxies to simplify profile extraction.


### 2. Aperture Photometry

- Used `photutils` to place concentric elliptical apertures.
- Measured flux as a function of radius to build radial surface brightness profiles.


### 3. Sersic Profile Fitting 

- Single sersic via `astropy.modeling.models.Sersic1D`
- Double Sersic model for
  - `bulge` (n_bulge > 2)
  - `Disc` (n_disc ~ 1)

### 4. Curve Fitting

- Fitting done using `scipy.optimize.curve_fit`.
- Data transformed to log scale to linearize intensity fall-off.



## 📚 References

- Astropy Documentation
- Photutils Aperture Photometry
- Fisher & Dory (2008, 2010) - Classical vs Psedobulges
- Gadottu (2009) - Elliptical and pseudo-bulge structures


## Acknowledgements

This project was carried out at the **School of Physics and Astronomy, Cardiff University**, under the guidance of **Dr. Matthew Smith**. Observational data was obtained from the **Las Cumbres Observatory**.


## 📜 License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute this work with proper citation.

## 🔭 Contact

For questions or collaborations:

**Shyam Chinta**  
Email: [shyamgirishchinta@gmail.com]  
GitHub: [@DarXSouls](https://github.com/DarXSouls)
