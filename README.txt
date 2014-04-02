PMI-0.4-Runtime-Demo
====================

PMI version for basic perfusion analysis in DCE-MRI, DSC-MRI and DCE-CT.

Author : Steven Sourbron 
Email  : s.sourbron@leeds.ac.uk
Software page: https://sites.google.com/site/plaresmedima
Personal page: http://medhealth.leeds.ac.uk/profile/500/407/steven_sourbron


Functionality
=============

Skeleton menu
Slices menu
Dynamics menu
Perfusion menu 

    Semi-quantitative (Pixel)
    -------------------------

        Calculates maps of three semi-quantitative parameters, ie. 
        - Maximum Enhancement (a measure of perfusion)
        - Area under the curve (a measure of distribution space)
        - The ratio Area/maximum (a measure of mean transit time)

    Model-free (Pixel)
    ------------------

        Calculates maps of three quantitative parameters
        using model-free deconvolution (Ostergaard et al MRM 1996): 

        - Tissue plasma Flow (ml/min/100g)
        - Extracellular volume (% or ml/100g)
        - Mean Transit Time (sec)

        Note: the volume (or MTT) equals plasma volume (or plasma MTT) 
        when an intravascular indicator is used, 
        or when the indicator does not leak due to physiological barriers (ie. BBB).
        In all other conditions these parameters characterise the entire extracellular space.

    Modified Tofts (Pixel)
    ----------------------

        Calculates maps of Ktrans, kep and ve using a linearised fit 
        for the modified Tofts model (Murase et al MRM 2004). 

    Exchange models (ROI)
    ---------------------

        Offers fits on ROI basis to a set of models that apply to 
        tissue composed of vascular-interstitial spaces with 
        symmetric exchange between them.
        The choice of model is interactive:

        - Maximum slope
        - Uptake 
        - Steady State
        - Patlak
        - Model-free
        - Compartment
        - Tofts
        - Modified Tofts
        - Modified Tofts (Linear)
        - 2-compartment uptake
        - 2-compartment exchange

        Note: for a detailed discussion of these models and nomenclature,
        see Sourbron and Buckley NMR Biomed 2013. 
 
    Kidney models (ROI)
    -------------------

        Offers fits on ROI basis to a set of models that apply
        to renal cortex regions (or voxels), or whole-kidney regions:

        - Maximum slope
        - Model-free
        - Patlak
        - Modified Tofts
        - 2-compartment uptake
        - 2-compartment Filtration

        Note: A discussion of these models and nomenclature can be found
        in Sourbron et al Invest Radiol 2008
      
    Liver models (ROI)
    ------------------
    
        Offers fits on ROI basis to a set of dual-inlet models
        that apply to liver parenchyma. 
        Fitting of delays is optional and either of the inlet functions 
        can be turned on/off interactively. 
        The following dual-inlet models are implemented:

        - One compartment
        - Patlak
        - Modified Tofts
        - Uptake
        - Exchange
        - Exchange-Uptake

        Note: Some discussion on nomenclature can be found in 
        Sourbron et al Radiology 2012. 
        The Patlak, Modified Tofts and Uptake models 
        use a nomenclature designed for Gadoxetic acid;  
        they assume the central compartment 
        is the extracellular space (plasma and interstitium)
        and the second compartment is the intracellular space.
        The exchange model describes exchange between plasma and 
        interstitium without involvement of an intracellular space
        The exchange-uptake model is three-compartmental 
        (plasma, interstitium, intracellular). These last two models
        are likely to be overparametrized in most situations.
        








