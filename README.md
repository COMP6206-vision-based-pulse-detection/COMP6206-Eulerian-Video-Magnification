# COMP6206-Eulerian-Video-Magnification
Vision Based Blood Pressure/Pulse Detection

# To reproduce the results shown in the paper:
1) Run "make.m" to build pyramid toolbox libraries:

% Build matlabPyrTools
fprintf('Building matlabPyrTools...\n');
run(fullfile('matlabPyrTools', 'Mex', 'compilePyrTools.m'));

2) Run "install.m":

addpath('./matlabPyrTools');
addpath('./matlabPyrTools/MEX');

3) Run "reproduceResults.m" to reproduce all the results in the paper.

Example function for colour result from face2.mp4:
% Color
amplify_spatial_Gdown_temporal_ideal(inFile,resultsDir,50,6, ...
50/60,60/60,30, 1);
% Spatial Filtering: Gaussian blur and down sample
% Temporal Filtering: Ideal bandpass

# Current issues:
Uses pyramid toolbox (matlabPyrTools) - requires "make.m" to build library
Uses MATLAB's Image Processing Toolbox