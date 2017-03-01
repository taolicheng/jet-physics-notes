Notes for using DNN in Jet Physics

## DNN

_[LeCun, Bengio, Hinton]_
> "Representation learning is a set of methods that allows a machine to be fed with **raw data** and to automatically **discover the representations** needed for detection or classification. Deep-learning methods are representation learning methods **with multiple levels of representation** obtained by composing simple but non-linear modules that each transform the representation at one level (starting with the raw input) into a representation at a higher, slightly more abstract level."

* image -> comes in the form of an array of pixel values -> hierachical concept learning
* "shallow" v.s. deep: **"shallow"** classifier requires a good feature extractor(the conventional opiton is to hand design good feature extractors) that solves the selectively-invariance dilemma; **deep** : features are learnt automatically using a **general-purpose** learning procedure.

> "The key aspect of deep learning is that these layers of features are not designed by human enginners: they are learned from data using a general-purpose learning procedure."

* Pros: 
  * multi-dimentinal data
  * can learn complex structures automatically
  * can take advantage of increases in the amount of available computation and data
* Cons:
  * huge amount of parameters (weights)
  
  

## recent work on treating jets and event using NLP



## jet as image
Basic Steps: https://indico.cern.ch/event/439039/contributions/2194591/attachments/1313452/1966480/BOOST2016_DeepLearning_Nachman.pdf


## jet and event as NLP

## DNN@LHC Building Blocks

* **Parton Shower Uncertainties in Jet Substructure Analyses with Deep Neural Networks**, 
James Barnard, Edmund Noel Dawe, Matthew J. Dolan, Nina Rajcic (ARC, CoEPP, Melbourne) arXiv:1609.00607 [[inspire]](https://inspirehep.net/record/1485081)

  >By investigating network performance on
  samples from the Pythia, Herwig and Sherpa generators, we find differences of up to **fifty** percent
  in background rejection for fixed signal efficiency.   

## Comments
* the key point is to find the best representation of the data, thus
  * image recognition -> 2D ? but in this format, is all the info sufficiently being encoded?
  * 
  


