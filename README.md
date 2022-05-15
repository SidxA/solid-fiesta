# plan - should be done by late June if possible!

- extract components from time series
	- build algorithmic structure to extract "phase" information from time series
	- setup of differentiating globally by SSA and DiffMap
- assign phase information to the components by Hilbert Transformation
- build Bifurcation models for data creation for testing

- signal
	- (iterated) phases, T
	- components
		- T
		- phases, T

## ideas

- equal splitting lengthes might make the later comparison of local modes easier
- can we create a structural splitting, by the split and merge with shannon entropy?
- the point is to localize information
- for that we need to split the time series into intervals
- interval selection might be based on brute split, driving period, merging after splitting, 

- the localized multiscale ssa is able to detect a frequency shift aka devilsstaircase in the enso data

- there is the possibility of 'sifting' the signal to get rid of riding waves and to create local mean zero
- there is the possibility of smooth orthogonal projection (bell)
- there is the possibility of merging short intervals in order to avoid redundancy

# computation structure

## 1 mode extraction

- fit the data into a shape that is most convenient for the extraction approaches
- PCA in MultiVariateStats.jl uses general matrix input
- DiffusionMap in ManifoldLearning.jl uses general matrix input
- output storage: log everything in individual run folders!
	
- question of window length: lets make a trial with the PCA, then check the SSA
	

## 2 differentiating properties

## 3 coupling model

# logs
- 05/10
	- global ssa has a problem with unsufficient boundary interpolation at large windows
	- there is still the problem of amplitude reconstruction
- 05/11
	- diffusion map works for $\epsilon>10$, best at $>200$
	- manifoldlearning or fitfrom multivar stats has automatically 8 cores
- 05/15
	- analyticsignal form FourierAnalysis is the hilbert trafo, cation due to extracted DC/mean? component
	- 
