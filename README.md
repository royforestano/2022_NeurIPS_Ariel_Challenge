# 2022_NeurIPS_Ariel_Challenge

Our Team, 'Gators', consisting of me, alongside Alex Roman, Eyup Unlu, and Professors Konstantin Matchev and Katia Matcheva, won the Regular Track for this competition and placed second in the Light Track.


In this machine learning challenge, we created a retrieval model to obtain the planet parameters, including surface temperature and atmospheric composition of trace gases, from transit (spectral) data and both star and planet parameters. Our solution was generated using a Neural Network in PyTorch, where we demonstrated data analysis, data cleaning, feature engineering and enhancement, dimensionality reduction, and interpretability. The challenge consisted of two tracks, the light track to predict three quantiles (16%,50%,84%) of the planet parameters and the regular track to predict the full distribution of the planet parameters. The Ariel Space mission is a European Space Agency mission to be launched in 2029. Ariel will observe the atmospheres of 1000 extrasolar planets - planets around other stars - to determine how they are made, how they evolve and how to put our own Solar System in the gallactic context.


-----------------------------------------------------------------------------------------------


In this repsoitory, we will first use a PyTorch neural network in order to predict an 18-dimensional space consisting of the 16th, 50th, and 84th percentiles (Light Track) of planet parameters (T,ln(H2O),ln(CO2),ln(CH4),ln(CO),ln(NH3)) from a 52-dimensional space of spectra values (one dimension for each wavelength bin), as well as, a 9 dimensional space of planet paramters. Then, we will use a similar model to predict the full distribution of the planet parameters (Regular Track). For the regular track, I did not include this hdf5 file here, it can be reproduced from the Ariel baseline solution notebook. The Ariel Baseline solution was included in this notebook, along with their helper functions in order to see how to compute the spec_matrix. I added their Light Track solution, which is the Ariel submission csv file.

Data Files from NeurIPS 2022 Ariel Data Challenge:

Ariel Website (includes data): [https://www.ariel-datachallenge.space]

Zenodo (includes data): [https://zenodo.org/record/6770103#.Y1r51-zMLPb]

Features 1: AuxiliaryTable: Star and Planet Parameters (91392,10)
Features 2: spec_matrix: Wavelength bin [0], spectra (transit depth) [1], noise in the transit [2], error in wavelength bin [3] for 52 wavelength bins (91392,52,4)
The entire 91392 values for the spectra data for the challenge were given, however, the file was too large to be uploaded here.

Targets: FM_Parameter_Table: Consists of Planet Temperature, and log traces concentrations for H2O, CH4, CO2, CO, NH3 (91392,6)
The test versions of these files consist of 500 instances rather than 91392, and only the test auxilliary data, spectra, and noise are provided here.

The 'all_training.npz' file was too large to upload here. This will take the same format as the 'all_testing.npz' file, and all data can be downloaded from the links above. Ariel separates the data into different files, whereas, we have condensed it into one.

Collaborators on this Project: Alex Roman and Eyup Unlu.
