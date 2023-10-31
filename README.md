# LISA_Dynamics_Impact_Analysis

## Description of Each Notebook
__LISANodeMeteoroidGlitch.ipynb__ : This notebook utilizes LISA glitch module to create input glitch files, specified by user-defined parameters, for LISANode simulator. 2nd generation Michelson TDI variables are computed using the PyTDI toolbox and the output LISANode files w/ glitch injection. The data is processed (downsampled or filtered or both) in the time domain and frequency domain.

__LISANodeMeteoroidGlitch_2.ipynb__ : Less cluttered version of original notebook.

__LISAOrbits_to_MEM_V2.ipynb__ : Generates LISA Orbits files and prepares them for MEM3 compatibility. '.h5 -> .txt'. Computes sky projection flux maps with MEM3 output data. Content after section 9 is experimental and incoherent.

__LISAOrbits_to_MEM_orionedited.ipynb__ : Original notebook edited by Orion with tweaks regarding the manipulation of the data in the flux maps utilizing Pandas dataframes. 

__MEM_Analysis.ipynb__ : Deeper analysis of MEM3 files. Plot of LPF meteoroid assessment compared to full LISA constellation. Multiple flux maps categorized by momentum.

__MicrometeoroidFluxFrequencyAssessment.ipynb__ : Micrometeoroid analysis of LISA mission prior to utilizing NASA MEM3.

__Micrometeoroid_Impact_Simulation.ipynb__ : Most current notebook. Compilation of most of all the other files. Currently working towards generating enough data points to get good distributions on the histograms (dynamical disturbance amplitude vs. momentum), validating the simulation by backing out the same flux & momentum we started with when we began processing, and implementation of a rotating spacecraft body.  

__SubtractingTTLNoise.ipynb__ : An attempt to follow a paper that discusses subtracting TTL noise in LISA data. (Link posted soon)

__lisanode_mem_glitch.ipynb__ : Preliminary notebook to __Micrometeoroid_Impact_Simulation.ipynb__. Not much to look at here.

__orbit_analysis.ipynb__ : Analysis of LISA constellation orbits and attempts to plot 3D visualizations. 

__simple_lisanode_injection.ipynb__ : Simple glitch injection into LISANode simulator. (simplified version of __LISANodeMeteoroidGlitch.ipynb__)

## Goals
__Micrometeoroid_Impact_Simulation.ipynb__
  - Need to optimize notebook to generate enough data points of impact strikes to get actual distributions in the dynamical disturbance amplitude vs. momentum histograms. Less memory storage consumption (HiPerGator?).
  - Validate simulation by extracting the total flux and momentum at the very end and compare it to what we have in the beginning
  - Implement rotating spacecraft body frame 
