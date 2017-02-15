>Brief notes for the very basics


## Jet Clustering Algorithms
* Sequential Algorithms
  * Jet Clustering 

![](http://latex.codecogs.com/gif.latex?d_{ij} = min(p_{Ti}^{2\\alpha}, p_{Tj}^{2 \\alpha}) \\frac{\\Delta R_{ij}^2}{R^2})

alpha=1 ->  kt; alpha=0 -> C/A; alpha=1 -> anti-kt

  * Qjets (non-deterministic jet clustering) 

![](http://latex.codecogs.com/gif.latex?P_{ij} \\propto e^{- \\alpha (d_{ij} - d_{min}) / d_{min}} )

* Minimization
  * k-means
  * deterministic annealing (DA)
  * optimal jet finder (OJF)
  
## Jet Grooming Algorithms
* Pruning: re-cluster the constituents using C/A algo.. Discard soft branches if
  
  ![](http://latex.codecogs.com/gif.latex?\\frac{min(p_{Ti}, p_{Tj})}{p_{Tij}} < z_{cut} ~\\textrm{and}~
  \\Delta R_{ij}> \\frac{2m_j}{p_{Tj}} R_{cut}) 
  
* Trimming: re-cluster the constituents into subjets with kt algo.. Discard all subjets with

  ![](http://latex.codecogs.com/gif.latex?p_{Ti}<f_{cut} p_{TJ})
  
* Filtering: re-cluster the constituents into subjets with C/A algo.. Re-define the jet using only the hardest N subjets.

* Softdrop: re-cluster all the constituents using C/A. Iteratively **undo** the last stage of C/A clustering from j to subjets j1, j2. Discard the softer subjet if ... and repeat.

![](http://latex.codecogs.com/gif.latex?\\frac{min(p_{T1}, p_{T2})}{p_{T1}+p_{T2}} < z_{cut}
\\left( \\frac{\\Delta R_{12}}{R} \\right)^\\beta)
