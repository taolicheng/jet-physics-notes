>Brief notes for the very basics

* [Theoretical Foundation](#theoretical-foundation)
* [Practical Aspects](#practical-aspects)
 * [Jet Clustering Algorithms](#jet-clustering-algorithms)
 * [Jet Grooming Algorithms](#jet-grooming-algorithms)
 * [Jet Observables](#jet-observables)


## Theoretical Foundation
>Core questions:
>* Can jet substructure be predicted by first-principle QCD calculations and compared to data in a meaningful way?
>* How accurately is jet substructure described by state-of-the-art MC tools?
>* How does the impact of additional p-p collisions limit jet substructure performance at the LHC, now and in future operating scenarios?
>* How powerful is jet substructure in studies of boosted top production, and how can it be made even more powerful?

NLO Calculation + Resummation 

![] (http://latex.codecogs.com/gif.latex? \\sigma(v) = \\sigma_0 g(\\alpha_s) e^\\beta)

![](http://latex.codecogs.com/gif.latex?\\beta = L g_1(\\alpha_s L) + g_2(\\alpha_s L) + \\alpha_s g_3(\\alpha_s L) + ..)

Jet substructure calculation at high precision, see [Larkoski's talk](https://indico.cern.ch/event/439039/contributions/2194580/attachments/1310623/1961016/BOOST_2016_Larkoski.pdf)

## Practical Aspects

### Jet Clustering Algorithms
* Sequential Algorithms
  * Jet Clustering 

  ![](http://latex.codecogs.com/gif.latex?d_{ij} = min(p_{Ti}^{2\\alpha}, p_{Tj}^{2 \\alpha}) \\frac{\\Delta R_{ij}^2}{R^2})
  
  ![](http://latex.codecogs.com/gif.latex?d_{iB} = p_{Ti}^2)

  alpha=1 ->  kt; alpha=0 -> C/A; alpha=1 -> anti-kt

  * Qjets (non-deterministic jet clustering) 

  ![](http://latex.codecogs.com/gif.latex?P_{ij} \\propto e^{- \\alpha (d_{ij} - d_{min}) / d_{min}} )

* Minimization
  * k-means
  * deterministic annealing (DA)
  * optimal jet finder (OJF)
  
### Jet Grooming Algorithms
* Pruning: re-cluster the constituents using C/A algo.. Discard soft branches if
  
  ![](http://latex.codecogs.com/gif.latex?\\frac{min(p_{Ti}, p_{Tj})}{p_{Tij}} < z_{cut} ~\\textrm{and}~
  \\Delta R_{ij}> \\frac{2m_j}{p_{Tj}} R_{cut}) 
  
* Trimming: re-cluster the constituents into subjets with kt algo.. Discard all subjets with

  ![](http://latex.codecogs.com/gif.latex?p_{Ti}<f_{cut} p_{TJ})
  
* Filtering: re-cluster the constituents into subjets with C/A algo.. Re-define the jet using only the hardest N subjets.

* Softdrop: re-cluster all the constituents using C/A. Iteratively **undo** the last stage of C/A clustering from j to subjets j1, j2. Discard the softer subjet if ... and repeat.

  ![](http://latex.codecogs.com/gif.latex?\\frac{min(p_{T1}, p_{T2})}{p_{T1}+p_{T2}} < z_{cut}
\\left( \\frac{\\Delta R_{12}}{R} \\right)^\\beta)

### Jet Observables
* jet area:
* jet mass: 
* jet substructure observables
  * Angular Correlation Functions: 
  * N-subjettiness:  ![](http://latex.codecogs.com/gif.latex?\\tau_N^\\beta) quantifies how well the radiation in the jet is aligned along N directions.
   ![](http://latex.codecogs.com/gif.latex?
   \\tau_N^\\beta = \\frac{1}{d_0} \\sum_i p_{Ti} min(\\Delta R_{1i}^\\beta, ..., \\Delta R_{Ni}^\\beta)
   ~\\textrm{with}~ 
   d_0 = \\sum_i p_{Ti} R^\\beta
   )

  * ratio 
  
  ![](http://latex.codecogs.com/gif.latex? \\tau_{N, N-1}^\\beta \\equiv \\frac{\\tau_N^\\beta}{\\tau_{N-1}^\\beta})
  
  * Energy correlation functions ECF and the double ratio (![](http://latex.codecogs.com/gif.latex?C_N^\\beta))
  
  ![](http://latex.codecogs.com/gif.latex?
   C_N^\\beta = \\frac{ECF(N+1, \\beta) ECF(N-1, \\beta)}{ECF(N, \\beta)^2})
   
   ![](http://latex.codecogs.com/gif.latex?
   ECF(N, \\beta) = \\sum_{i_1 < i_2 < ... < i_N \\in j} \\left(\\prod_{a=1}^N p_{Ti_a}\\right)
   \\left( \\prod_{b=1}^{N-1} \\prod_{c=b+1}^N \\Delta R_{i_b i_c} \\right)^\\beta)
   ![](http://latex.codecogs.com/gif.latex?
   e_N^\\beta = \\frac{ECF(N, \\beta)}{p_{TJ}^N})
  
  *  ![](http://latex.codecogs.com/gif.latex?M_2^\\beta, ~D_2^\\beta) with power counting [Larkoski, Moult, Neill]
  
  ![](http://latex.codecogs.com/gif.latex?
  M_2^\\beta = \\frac{_1e_3^\\beta}{e_2^\\beta} ~ D_2^\\beta = \\frac{e_3^\\beta}{(e_2^\\beta)^3}
  )
* color flow
* jet charge

![](http://latex.codecogs.com/gif.latex?
Q_j = \\frac{1}{p_{Tj}^\\kappa} \\sum_{i\\in T} q_i \\times (p_T^i)^\\kappa
)

## Applications (Subtopics)
### Quark-Gluon Discrimination

### Jet Substructure / Boosted non-QCD Jet Tagging
#### Boosted W-Tagging

#### Top-Tagging

#### Higgs-Tagging

### Jet Superstructure / Colorflow Analysis

### Jet Charge
* ATLAS results [[inspire]](http://inspirehep.net/record/1313120) 

## Experimental Perfomance
>Jet measurements at the LHC. More physics results see [LHC Results](./lhc-results.md)

## Open Questions / Unsolved Problems
