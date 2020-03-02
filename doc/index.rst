Vervain: Vascular Model Based Perfusion Quantification for DSC-MRI
------------------------------------------------------------------

.. image:: vervain_image.jpg
   :scale: 75 %
   :alt: vervain image
   :align: right

Vervain is a python based Bayesian Inference tool for quantification of perfusion and other haemodynamic 
parameters from Dynamic Susceptibility Contrast perfusion MRI of the brain. 

Vervain complements
the `OXASL <https://oxasl.readthedocs.io/>`_ pipeline for the quantification of 
perfusion using Arterial Spin Labelling MRI and is 
built on the same core inference algorithm (`FABBER <https://fabber_core.readthedocs.io>`_). 

Vervain uses a specific physiological 
model for capillary transit of contrast within the blood generally termed the 'vascular model'
that was first described by Ostergaard (see below). In Vervain the model has been extended to 
explicitly infer the mean transit time and also to optionally include correction for macro 
vascular contamination - contrast agent within arterial vessels - more information on the 
model can be found in the `theory section of the FABBER_DSC documentation <https://fabber-dsc.readthedocs.io/en/latest/theory.html>`_.

Vervain takes a model-based approach to the analysis of DSC-MRI data in contrast to alternative 
'non-parametric' approaches, that often use a Singular Value based Deconvolution to quantify 
perfusion. An alternative Bayesian Deconvolution approach is also available, but not currently 
distributed as part of FSL. For more information see the reference below and contact the senior
author.

Vervain is base on the VERBENA tool included in `FSL <https://fsl.fmrib.ox.ac.uk/fsl/fslwiki>`_ 
v6.0.1 and later. It is designed to be compatible but also offers some additional functionality.

.. toctree::
   :maxdepth: 1
   :caption: Contents:
  
   command

Referencing
~~~~~~~~~~~

If you use Vervain in your research, please make sure that you reference Chappell et al [1]_.

.. [1] *Chappell, M.A., Mehndiratta, A., Calamante F., "Correcting for large vessel contamination 
   in DSC perfusion MRI by extension to a physiological model of the vasculature", e-print ahead of 
   publication. doi: 10.1002/mrm.25390*

The following articles provide more background on the original vascular model from which the Vervain 
model is derived:

.. [2] *Mouridsen K, Friston K, Hjort N, Gyldensted L, Østergaard L, Kiebel S. Bayesian estimation of 
   cerebral perfusion using a physiological model of microvasculature. NeuroImage 2006;33:570–579. 
   doi: 10.1016/j.neuroimage.2006.06.015.*

.. [3] *Ostergaard L, Chesler D, Weisskoff R, Sorensen A, Rosen B. Modeling Cerebral Blood Flow and Flow 
   Heterogeneity From Magnetic Resonance Residue Data. J Cereb Blood Flow Metab 1999;19:690–699.*

An alternative Bayesian 'non-parametric' deconvolution approach has been published in:

.. [4] *Mehndiratta A, MacIntosh BJ, Crane DE, Payne SJ, Chappell MA. A control point interpolation 
   method for the non-parametric quantification of cerebral haemodynamics from dynamic susceptibility 
   contrast MRI. NeuroImage 2013;64:560–570. doi: 10.1016/j.neuroimage.2012.08.083.*
