---
layout: page
title: Research
description: Dan Simpson's research
---

## Summary of contributions


Throughout my career, my research has been inspired by the problems in spatial statistics. Datasets with a spatial or spatiotemporal components are increasingly being collected in fields as diverse as ecology, epidemiology, atmospheric science, fisheries science, and forestry. The main challenge emerging is the increasing size of modern datasets: bringing about a corresponding increase in the complexity of the associated statistical models. In this environment, there is a natural attraction to Bayesian (and particularly hierarchical) modelling, which provides a framework for building increasingly complex models.

The fundamental idea of Bayesian statistics is that there is a unique, principled way to update a probabilistic model in the presence of new information. The success of this update depends on the quality of the prior probabilistic model, and for a large number of problems in applied statistics, there is no guidance on how to specify these prior probabilities. Furthermore, there are few tools that allow non-expert statisticians to validate their computational method or their models either before or after encountering data (Gelman et al., 2017). The ambition of my research program has been to fill this gap for spatial models. More abstractly, I have primarily worked with the class of Latent Gaussian Models (LGMs), which is a flexible class of models that generalize Generalized Linear Models, Multilevel models, and any model with a correlated Gaussian random effect.

My early work focused on extending the [R-INLA](http://r-inla.org/) open source software for performing fast approximate inference on LGMs (Martins et al. 2013; Rue et al. 2017). My work particularly focused on improving the spatial capabilities of the R-INLA software (Simpson et al. 2012a, 2012b, 2016; Hu et al. 2013a, 2013b, 2015; Fuglstad et al. 2015a, 2015b; Bakka et al. 2018, 2019; Krainski et al. 2019). The tight integration between my research and the R-INLA user community has enabled me to focus on moving beyond individual research projects and attempt to develop a holistic “best practice” workflow in order to furnish applied statisticians with the computational and modelling tools they need to solve practical problems.  

This desire to develop workflows for the R-INLA and [Stan](http://mc-stan.org/) communities has pushed my research beyond its initial focus on spatial models. I now have a significant body of research on modern methods for specifying (Simpson et al. 2016; Riebler et al. 2016; Fuglstad et al. 2018), interrogating (Gabry et al. 2018; Sørbye et al. 2018; Gelman et al. 2017), and justifying weakly informative prior distributions on parameters in LGMs. This aim has also inspired my recent research into visualization (Gabry et al. 2018; Vehtari et al. 2019a) and computational diagnostics (Yao et al. 2018; Talts et al. 2018; Vehtari et al. 2019a).

### Key papers: Spatial Modelling

<u>Daniel Simpson, Janine Illian, Finn Lindgren, Sigrunn Sørbye and Håvard Rue. (2016). Going off grid: Computationally efficient inference for log-Gaussian Cox processes. Biometrika. 103(1): 49--70.  </u>

This paper, incidentally one of the longest that Biometrika has ever published, has several major technical and practical contributions. Fundamentally, the paper re-considers the standard computational approximation of the log-Gaussian Cox process (LGCP) model. The aim of this was to find a form of the approximation that was better suited to finite dimensional Gaussian random fields (that is, random fields that are specified from a finite set of basis functions) such as those produced with the Stochastic Partial Differential Equation (SPDE) method of Lindgren et al. (2011). To do this, we applied direct quadrature to the LGCP likelihood. I then used theory from the inverse problems literature to bound the error in posterior computed using this approximate likelihood. This error bound contained an explicit rate, and as a corollary I derive the explicit rate for the convergence of the standard approximation, which was possibly an order of magnitude slower than our new approximation. A second major contribution to this paper was to provide explicit bounds on the convergence of the SPDE method in terms of the GRF being approximated and the approximation properties of the basis functions. This was a conclusion of the work we began in Simpson et al. (2012a-b).

<u>Geir-Arne Fuglstad, Daniel Simpson, Finn Lindgren, and Håvard Rue. (2018). Constructing Priors that Penalize the Complexity of Gaussian Random Fields. Journal of the American Statistical Association. Volume 114(525), pp. 445–452.</u>

This paper, written with my PhD student Geir-Arne Fuglstad, is the first investigation into principled prior distributions for Gaussian random fields (or Gaussian processes) in 3 or fewer dimensions that is broadly applicable. The only previous work on this topic was a mathematically and computationally difficult method for setting reference priors for a very small set of models that use Gaussian random fields. As well as using the PC prior framework to construct weakly-informative priors for the hyper-parameters, we also use appropriate asymptotic approximations to avoid complex and expensive design dependence in the resulting priors.

<u>Haakon Bakka, Håvard Rue, Geir-Arne Fuglstad, Andrea Riebler, David Bolin, Elias Krainski, Daniel Simpson, and Finn Lindgren (2018). Spatial modelling with R-INLA: A review. WIRE Computational Statistics. Volume 10(6).
Elias T. Krainski, Virgilio Gómez-Rubio, Haakon Bakka, Amanda Lenzi, Daniela Castro-Camilo, Daniel Simpson, Finn Lindgren and Håvard Rue. (2019) Advanced Spatial Modeling with Stochastic Partial Differential Equations Using R and INLA. CRC/Tayor and Francis Group.</u>

 This review paper and book are written by the research group that introduced both the SPDE method for scalable spatial modelling and the R-INLA software for fast approximate inference. They show the breadth of our work on this topic and demonstrate the ways that we have worked to make our research outputs available to the wider spatial modelling community.


<!--
#### <u>The effects of increased eye contact on feeding portions</u>
*In this paper I estimate the effect of increased eye contact on the size of feeding portions delivered by my humans. Over a period of several months I varied the amount of time I spent in locked eye contact with my masters while secretely recording the total amount of food provided each day. The results incidate that the relationship between eye contact and portion size is concave, in that as eye contact increases, the portion size increases up until a point where it begins to decrease. Future research will examine whether time spent cuddling exhibits a similar relationship.*

[click here for the most recent version of the paper]({{ BASE_PATH}}/pages/working_papers/sample-working-paper.pdf)
.-->

<!-- Note: this is how to write a comment in HTML. Everything in here won't show up on your webpage.-->

<!--
To increase the size of the title, use fewer # in front of the paper title.
To decrease the size of the title, use more #.
To remove the italics, remove the * before and after the description
To remove the underline from the title, remove the <u> tags (<u> and </u>)
-->
