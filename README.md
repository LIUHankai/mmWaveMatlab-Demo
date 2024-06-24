# mmWaveMatlab-Demo
Introduction and demos of the mmWaveMatlab project.

#### Auhor: Hankai Liu
#### Organization: Tianjin University
#### Email: hkliu@tju.edu.cn
---
## Introduction
mmWaveMatlab is a Matlab codebase for millimeter wave radar signal processing and human sensing. This document will introduce some of the main features of mmWaveMatlab and show the corresponding results.

---

## Basic Signal Processing
This category provides basic range, velocity, and angle measurements.

### Range Measurement
Perform Range FFT to obtain range spectrums.

### Velocity Measurement
1. Perform Doppler FFT to obtain RD maps.

2. Compute micro-Doppler spectrums. Support simultaneous observation of multiple targets through range/RA extraction.

### Angle Measurement
Configure the antenna array and perform angle estimation algorithms (FFT or digital beamforming) to obtain RA maps. Digital beamforming supports CBF and Capon algorithms and provides signal reconstruction.

## Point Cloud Processing
This category offers a variety of point cloud generation and clustering functions.

### Range/RD/RA Point Cloud Generation 
Perform 1D/2D CFAR in range spectrum, RD Map, and RA map to generate point clouds.

### 4D Point Cloud Generation 
Generate 4D point clouds through approaches of 4D FFT (RD point cloud -> 2D Angle FFT) or 2-Pass DBF (RA point cloud -> elevation estimation & signal reconstruction -> Doppler FFT).

### Point Cloud Clustering 
1. Cluster 2D/3D point clouds of different types through DBSCAN.

2. Distinguish nearby targets through GMM clustering.


