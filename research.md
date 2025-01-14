---
layout: default
title: Research
---

<input type="button" onClick="document.getElementById('gan').scrollIntoView();" />

<input type="button" onClick="document.getElementById('gan').scrollIntoView();" />

<input type="button" onClick="document.getElementById('gan').scrollIntoView();" />


<div class="text-left" id="ciber">
<!-- <details> -->
  <h2 class="post-title" color=>Dissecting the near-Infrared Universe with the Cosmic Infrared Background ExpeRiment (CIBER)</h2>
<!--   </summary> -->
  [To be filled in soon]
  
  
    <h3>CIBER-1</h3>
    
    
    <h3>CIBER-2</h3>
</div>
<!-- </details> -->

<div class="text-left" id="gan">
<!-- <details> -->
<!-- <summary>  -->
  <h2 class="post-title">Non-linear 3D Cosmic Web Simulation with Heavy-Tailed Generative Adversarial Networks</h2>
<!--   </summary> -->
  
  In collaboration with <a href="https://science.jpl.nasa.gov/people/PBerger/">Philippe Berger</a> and <a href="https://www.cita.utoronto.ca/~gstein/">George Stein</a>, arXiv link <a href="https://arxiv.org/abs/2005.03050">here</a>.
  <br>
  <p>
    Many inference problems in cosmology incorporate information from simulations when making comparisons to observational data. Comparing data to simulations (e.g., N-body, hydrodynamical, etc.) can be challenging when the data are high-dimensional and when generating the simulations is computationally expensive. Some summary statistics can be analytically derived (the power spectrum being one example), but for higher order statistics and covariances these analytical prescriptions often have limitations.
  </p>
  <p>
    I am interested in the ways deep generative modeling can be used to bridge the gap between expensive simulations and robust cosmological inference. Deep generative modeling is a subset of machine learning that seeks to model full probability distributions rather than make classifications conditional on input data. Unlike supervised machine learning, which typically involves training a neural network or some other model with labeled data (X,Y), deep generative modeling is unsupervised in the sense that the goal of the model is to learn a representation of the data X and generate independent samples from that representation, not to make predictions about that data. Unsupervised models like generative adversarial networks (GANs) are often used to generate fake faces (check out <a href="https://thispersondoesnotexist.com/">This Person Does Not Exist</a> for a neat recent example). In that case, the model does not explicitly memorize the faces it trains on, but instead learns a representation of what a "face" is in data space, after which it can generate images of faces that are from the same underlying data distribution. In the same way that supervised methods can reduce high dimensional data down to discrete classifications or a handful of numbers, unsupervised methods can also be used to reduce the dimensionality of the data, such that the task of sampling independent realizations of the data distribution reduces to sampling from a lower dimensional "latent space". 
  </p>
  <p>
    Bringing things back to cosmology, my collaborators and I were interested in seeing how well GANs could emulate evolved dark matter density fields, which are normally obtained with N-body simulations. Deep learning methods excel at modeling non-linear data, so by emulating directly to the data space, summary statistics like the power spectrum and bispectrum can be predicted well into the small-scale, non-linear regime where analytic methods fail but where there is sometimes more constraining power. We found that, with some care in the way the data are pre-scaled and some additional flexibility in the generator latent space, a deep convolutional GAN does quite well at generating independent realizations of the dark matter density field. In particular, the mean power spectra from generated samples agree to within 5% up to k=3 and within 10% for k<5 when compared with N-body simulations, and similar accuracy was obtained for a variety of bispectra. We also showed that a conditional GAN (cGAN) could be used to learn the joint distribution between the dark matter density field and redshift. Though we did not explicitly enforce it in the training process, we found that fixing the latent vector of the generator and varying the (learned) conditional redshift parameter resulted in a smooth interpolation that looks something like gravitational evolution! This can be seen in the GIF below. If this type of method is scalable to larger volumes, it may be possible to generate realizations of large scale structure conditioned on cosmological/astrophysical parameters, paving the way to utilizing the full information content in cosmological data for inference.
  </p>


<!-- </div> -->

  <div class="text-center">
  <p align="center">
  <figure>
<!--   <img align="center" width="600" src='img/real_gen_res.jpg' alt="Subvols"/> -->
  <img align="center" width="600" src='/img/multiz_alpha.gif' alt="Subvol evolution"/>
  </figure>
    <figcaption>
      Visualization of cGAN-generated samples, interpolated from redshift z=3 to z=0. Voxels with higher density are more red and less transparent.
    </figcaption>
  </p>
  </div>
 
<!-- </details> -->
   
<div class="text-left" id="pcat">
<!-- <details> -->
<!-- <summary>    -->
  <h2 class="post-title">Forward modeling of astronomical images with probabilistic cataloging</h2>
<!--    </summary> -->
  <p>
   Cataloging is a fundamental operation in astronomy. In the case where objects (such as stars, galaxies, etc.) are well separated and and observed with high signal to noise, cataloging is a 
    fairly straightforward task. However, things get complicated in crowded fields. Below is an observation of the globular cluster <a href="https://en.wikipedia.org/wiki/Messier_2">Messier 2</a>. When objects blend together, 
    determining their properties to percent-level precision becomes a much more daunting task. Next generation telescopes like LSST, HSC, WFIRST will have improved sensitivity to pick up faint sources, but will not have 
    sufficient angular resolution to distinguish this population of newly observed sources. This means <i>a significant fraction of future observations will suffer from blending!</i>
  </p>
  </div>
  
  <div class="text-center">
  <p align="center">
  <figure>
  <img align="center" width="600" src='/img/m2_lores.jpg' alt="Messier 2"/>
  </figure>
    <figcaption>
      Messier 2, a globular cluster 11.5 kpc away containing over 150,000 stars.
    </figcaption>
  </p>
<!--   </div> -->
  
  
  <div class="text-left">
  <p>
    Probabilistic cataloging (PCAT) has been proposed as a viable framework to address these problems. PCAT is a Bayesian, hierarchical, and transdimensional sampler designed to explore the 
    space of different catalogs consistent with an observed image. Because the number of objects and in an image may not be known <i>a priori</i>, exploring the "catalog space" involves exploring models with different numbers
    of parameters. This is done by constructing transdimensional proposals that preserve detailed balance -- this is referred to as Reversible Jump Markov Chain Monte 
    Carlo (RJ-MCMC, see <a href="https://pdfs.semanticscholar.org/c440/ea3bbb7fc8dcaa069ea550011ea65ac33fd4.pdf">Green 1995</a>).
  </p>
  <p>
  <h3>Multiband Probabilistic Cataloging</h3>
   <b> Supervised by <a href="https://faun.rc.fas.harvard.edu/nebel/dfink//">Douglas Finkbeiner</a>, in collaboration with <a href="http://portillo.ca/">Stephen Portillo</a> and <a href="tansudaylan.com">Tansu Daylan</a> </b> <br>
    
PCAT has been shown to outperform traditional cataloging methods on single-band optical data in crowded fields (see <a href="https://arxiv.org/abs/1703.01303">Portillo et al. 2017</a>). For my senior thesis, I worked on extending PCAT to the case of multiband observations. By jointly fitting data from multiple bands, point source detection can directly be enhanced through higher effective signal-to-noise. In addition, one can begin to use additional information in the form of color priors to inform PCAT's hierarchical model. We find that, while our fit is sensitive to the astrometric calibration of the observed data across bands, our two-band fits on r+i go 0.4 mag deeper than the corresponding single-band fit of the same cutout from Messier 2, with lower false discovery rates down to r~20.5. When compared to DAOPHOT, a commonly used software for crowded-field photometry, our multiband catalog goes nearly 1.5 mag deeper <i>using the same data</i>! <a href="https://arxiv.org/abs/1907.04929">Check out our paper on the arXiv</a> (August 2019) and the <a href="https://iopscience.iop.org/article/10.3847/1538-3881/ab74cf">published version</a>. And check out <a href="https://aasnova.org/2020/04/24/a-stellar-method-of-catalog-creation/?fbclid=IwAR1m4kUkcipyRn3RGrPtU7uMz-yFy7W6n5A1v0L906mKJpcZwkgiYN3ig8I">this article</a> by AAS Nova about the publication! 
  </p>
</div>
<div class="text-center">
  <p align="center">
  <figure>
  <img width="400" src='/img/ht606_magbins.png' alt="Completeness"/>
  <img width="400" src='/img/sdss_r_magbins.png' alt="False Discovery Rate"/>
  </figure>
  </p>
  <p>
  <h3>Measurement of the thermal Sunyaev-Zel'dovich (tSZ) effect with <i>PCAT-DE</i></h3>
  To be updated soon.
  </p>
</div>
 
<div class="text-left">  
  <p>
  <h3>Application to the Chandra Deep Field - South Survey</h3>
    I worked with Tansu Daylan on the application of probabilistic cataloging to X-ray data, focusing specifically on 
    observations from the <a href="https://en.wikipedia.org/wiki/Chandra_Deep_Field_South">Chandra Deep Field - South Survey (CDF-S).</a>
    CDF-S has been observed for over 8 Ms (the longest exposure of any field taken by the Chandra X-ray telescope), and will be the deepest observation of the extragalactic
    X-ray background accessible for many years to come. The galaxies observed in CDF-S are relatively sparse compared to the stars observed optically in crowded fields. However, the photon statistics from CDF-S observations
    are highly Poissonian -- ~3-5 X-ray photons is sometimes enough to "detect" a galaxy! We use PCAT in this limit to better understand the population of sub-threshold galaxies in relation to the 
    poorly understood cosmic X-ray background (CXB). 

  </p>
<!--  </details> -->
</div>

<!-- <div class="text-left">   -->
<!--   <details>
  <summary>
  <h2 class="post-title">Early Type Galaxies in the <i>Chandra</i> COSMOS Survey</h2>
    </summary>
  Supervised by <a href="https://francesca.civano.it/">Francesca Civano</a>
  <br>
  Paper can be found <a href="https://iopscience.iop.org/article/10.1088/0004-637X/790/1/16">here</a>.
  </details> -->
<!-- </div> -->
