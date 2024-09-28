# Synthetic-Dataset-of-Maneuvering-Low-Earth-Orbit-Satellite-Trajectories-for-AI-Analysis

The LEOMSAT dataset provides synthetic satellite trajectories focused on satellite maneuvering patterns.

The underlying data generation is based on the following:
- Orekit [1], a well-known core layer for space flight dynamics applications.
- Theoretical results about motion perturbations [2] and maneuvering strategies [3-4].
- Real database [5-6]. 

Characteristics of the dataset: 
- There are 400 scenarios of a 1-year satellite's trajectories. 
- 250 scenarios are randomly drawn to cover different satellite characteristics, orbits, and maneuvering strategies. 150 scenarios are based on Starlink's known orbits and satellite characteristics with varying maneuvering strategies.
- We propose a train/test split based on a balanced repartition of orbits, satellite characteristics, and maneuver frequency. 
- Each scenario contains three files. The ephemeris file contains position-velocity data with a one-minute sampling rate in the equinoctial frame [7]. One aims to classify/predict this data. The maneuvers file describes the maneuvers' characteristics for each burn. One uses this data as a label for classification issues. The TLE file gathers mean elements computed during the scenario creation and monitors the maneuvering strategy. One proposes to use these data only for visualization purposes. 

If you use this dataset, please cite the following paper: 

Baudier, S., Velasco-Forero, S., Jean, F., Brooks, D. & Angulo, J. Synthetic Dataset of Maneuvering Low Earth Orbit Satellite Trajectories for AI Analysis. 1st Artificial Intelligence in and for Space conference (SPAICE). (2024).

For further information, please refer to the previous paper, which introduces the data and provides some classification examples.

Link to the dataset on Hugging Face:
https://huggingface.co/datasets/StefanBaudier/LEOMSAT

References:
[1] Maisonobe, L., Pommier-Maurussane, V. & Pommier, V. Orekit : An Open-source Library for Operational Flight Dynamics Applications.
[2] Vallado, D. A. Fundamentals of Astrodynamics and Applications (Vol. 12) Springer Science & Business Media (Space Technology Library, 2007).
[3] Schaub, H., Vadali, S. R., Junkins, J. L. & Alfriend, K. T. Spacecraft Formation Flying Control Using Mean Orbit Elements. The Journal of the Astronautical Sciences 48, 69–87. issn: 00219142, 2195-0571. (2023) (Mar. 2000).
[4] Garulli, A., Giannitrapani, A., Leomanni, M. & Scortecci, F.Autonomous Station Keeping for LEO Missions with a Hybrid Continuous/Impulsive Electric Propulsion System. 32nd International Electric Propulsion Conference (2011).
[5] Space-Track.Org https://www.space-track.org. (2024).
[6] DISCOSweb https://discosweb.esoc.esa.int/. (2024).
[7] Broucke, R. A. & Cefola, P. J. On the Equinoctial Orbit Elements. Celestial Mechanics 5, 303–310. issn: 0008-8714, 1572-9478. (2024) (May 1972).


Papers using the dataset: 
Baudier, S., Velasco-Forero, S., Jean, F., Brooks, D. & Angulo, J. Synthetic Dataset of Maneuvering Low Earth Orbit Satellite Trajectories for AI Analysis. 1st Artificial Intelligence in and for Space conference (SPAICE). (2024).
Baudier, S., Velasco-Forero, S., Jean, F., Brooks, D. & Angulo, J. Deep Matrix Profile for Maneuver Classification in Low Earth Orbit Satellite Trajectories. 32nd European Signal Processing Conference (EUSIPCO). (2024).
