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
Provide basic range, velocity, and angle measurements.

### Range Measurement
Perform Range FFT to obtain range spectrums.

<img src = "figures/rangeFFT.png" width = "300">

### Velocity Measurement
1. Perform Doppler FFT to obtain RD maps.

<img src = "figures/RDM.png" width = "300">

3. Compute micro-Doppler spectrums. Support simultaneous observation of multiple targets through range/RA extraction.

<img src = "figures/MDS.png" width = "300">

### Angle Measurement
1. Configure the antenna array and perform angle estimation algorithms (FFT or digital beamforming) to obtain RA maps. Digital beamforming supports CBF and Capon algorithms and provides signal reconstruction.

<img src = "figures/RAM_AngleFFT.png" width = "265"><img src = "figures/RAM_CBF.png" width = "265"><img src = "figures/RAM_Capon.png" width = "265">

2. Perform 2D angle estimation and accumulate signal strength for human imaging.

<img src = "figures/EAM.png" width = "300">

---

## Point Cloud Processing
Provide point cloud-related functions.

### Range/RD/RA Point Cloud Generation 
Perform 1D/2D CFAR in range spectrum, RD Map, and RA map to generate point clouds.

<img src = "figures/rangePC.png" width = "220"><img src = "figures/RDPC.png" width = "220">$~~~~$<img src = "figures/RAPC.png" width = "340">

### 4D Point Cloud Generation 
Generate 4D point clouds through approaches of 4D FFT (RD point cloud -> 2D Angle FFT) or 2-Pass DBF (RA point cloud -> elevation estimation & signal reconstruction -> Doppler FFT).

<img src = "figures/3DPC_4DFFT.png" width = "300"><img src = "figures/3DPC_DBF.png" width = "300">

### Point Cloud Clustering 
1. Cluster 2D/3D point clouds of different types through DBSCAN.

<img src = "figures/cluster_XY.png" width = "265">  <img src = "figures/cluster_XYZ.png" width = "265"> <img src = "figures/cluster_XYV.png" width = "265">

3. Distinguish nearby targets through GMM clustering.

<img src = "figures/GMM.png" width = "265">

---

## Sensing
Provide various human sensing functions.

### Multi-person Tracking
A multi-person tracking solution with full process optimization involving detection enhancement, interference suppression, continuity maintenance, and trajectory correction. It can be used in conjunction with IMUs to identify users [1].

<img src = "figures/trackingVideoGif1.gif" width = "500">$~~~~$<img src = "figures/trackingGif1.gif" width = "300">

<img src = "figures/trackingVideoGif2.gif" width = "500">$~~~~$<img src = "figures/trackingGif2.gif" width = "300">

<img src = "figures/tracking1.png" width = "820">

<img src = "figures/tracking2.png" width = "820">


### Respiration Monitoring
Perform respiration monitoring on static targets. Support simultaneous observation of multiple targets through range/RA extraction.

<img src = "figures/resp.png" width = "600">

---

## Our Research
Welcome to our research on mmWave radar, and feel free to contact us.

[1] "PmTrack: Enabling personalized mmWave-based human tracking," ACM IMWUT, 2023. (Multi-person tracking and identification)

[2] "Application-oriented privacy filter for mmWave radar," IEEE Communications Magazine, 2023. (Behavior privacy protection)

[3] "PosMonitor: Fine-grained sleep posture recognition with mmWave radar," IEEE Internet of Things Journal, 2024. (Sleep posture recognition)

[4] "VibCamera: mmWave and camera fusion for multi-point vibration monitoring", IEEE ICPADS, 2023. (Vibration measurement)
