# Reflectance Transformation Imaging for Historic Textiles  
### NTNU Colourlab Summer Internship

This project explored the use of **Reflectance Transformation Imaging (RTI)** and **multi-light image collections (MLICs)** for improved visualization of historic textiles.

The work was conducted as a summer internship at **NTNU Colourlab**, supervised by **Irina-Mihaela Ciortan**, with co-supervision from **Yoko Arteaga** and **Giorgio Trumpy**.

## Project Summary

Reflectance Transformation Imaging is a computational imaging technique where the camera and object remain fixed while the illumination direction changes. This allows the surface appearance of an object to be interactively relit from light positions that were not directly recorded.

In this project, I used the **Relight** software framework to process multi-light image collections and generate relightable visualizations of historic textile samples. The goal was to compare different RTI reconstruction algorithms and evaluate how accurately they preserved visual appearance, especially colour and surface detail.

## Motivation

Historic textiles often contain subtle surface, material, and colour information that can be difficult to inspect under fixed illumination. RTI can support cultural heritage analysis by enabling interactive relighting, making surface details more visible without physically manipulating fragile objects.

For cultural heritage applications, however, visual fidelity is critical. A relightable reconstruction is only useful if it preserves important appearance cues such as texture, contrast, and chroma.

## Methods

The project compared several algorithms available in Relight:

- **PTM / LPTM** — Polynomial Texture Mapping
- **HSH** — Hemispherical Harmonics
- **RBF** — Radial Basis Function interpolation
- **YRBF** — RBF variant using separated colour channels for improved chroma fidelity
- **BLN / YBLN** — Bilinear interpolation-based reconstruction

The evaluation used two main approaches:

1. **Visual inspection**  
   Reconstructed RTI images were compared with input images captured from similar light directions.

2. **Quantitative colour analysis**  
   Colour differences between original and reconstructed images were measured using **CIELAB2000 colour difference** across multiple image sets.

## Key Findings

- RTI successfully enabled interactive relighting of historic textile image sets.
- Different reconstruction algorithms showed different behaviour in terms of visual fidelity and chroma preservation.
- A persistent **desaturation issue** appeared in several reconstructed RTI outputs compared with the original input images.
- Troubleshooting included leave-one-out comparisons, excluding shadow-heavy images, testing across operating systems, and raising unresolved software issues.
- The results suggested that further investigation is needed to determine whether the desaturation comes from the software, the dataset, or the RTI creation workflow.
- 
## Open-Source Troubleshooting

During the project, I encountered persistent desaturation in some RTI reconstructions and investigated whether the issue came from the dataset, reconstruction method, or software workflow.

As part of the troubleshooting process, I opened an issue on the Relight GitHub repository and later received feedback from the maintainers:

[Relight GitHub issue on reconstruction desaturation](https://github.com/cnr-isti-vclab/relight/issues/77#issuecomment-4143704394)

## Relevance

This project includes:

- Computational imaging
- Cultural heritage visualization
- Colour appearance analysis
- Interactive visual inspection
- Digital documentation of fragile artefacts

It is especially relevant to applications where visual technologies are used to support interpretation, access, and analysis of cultural heritage objects.

## Materials

- [Poster](docs/poster.pdf)
- [Presentation](docs/presentation.pdf)

## Tools and Topics

`RTI` · `Reflectance Transformation Imaging` · `Multi-light Imaging` · `Relight` · `Cultural Heritage` · `Historic Textiles` · `CIELAB2000` · `Colour Difference` · `Computational Imaging` · `Interactive Visualization`

## Project Status

Completed internship project.  
Future work would involve testing the workflow on additional datasets, improving reproducibility, and investigating the source of the observed desaturation in RTI reconstructions.
