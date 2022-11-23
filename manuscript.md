---
title: Deep-learning based automatic segmentation of vesicles in cryo-electron tomograms
keywords:
- synapse
- cryo-electron tomography
- synaptic vesicles
- deep learning
- segmentation
- post-processing
- automation
lang: en-US
date-meta: '2022-11-23'
author-meta:
- Amin Khosrozadeh
- Raphaela Seeger
- Julika Radecke
- Guillaume Witz
- Jakob B. Sørensen
- Benoît Zuber
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta property="og:type" content="article" />
  <meta name="dc.title" content="Deep-learning based automatic segmentation of vesicles in cryo-electron tomograms" />
  <meta name="citation_title" content="Deep-learning based automatic segmentation of vesicles in cryo-electron tomograms" />
  <meta property="og:title" content="Deep-learning based automatic segmentation of vesicles in cryo-electron tomograms" />
  <meta property="twitter:title" content="Deep-learning based automatic segmentation of vesicles in cryo-electron tomograms" />
  <meta name="dc.date" content="2022-11-23" />
  <meta name="citation_publication_date" content="2022-11-23" />
  <meta property="article:published_time" content="2022-11-23" />
  <meta name="dc.modified" content="2022-11-23T14:32:42+00:00" />
  <meta property="article:modified_time" content="2022-11-23T14:32:42+00:00" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Amin Khosrozadeh" />
  <meta name="citation_author_institution" content="Institute of Anatomy, University of Bern, Bern, Switzerland" />
  <meta name="citation_author_institution" content="Graduate School for Cellular and Biomedical Sciences, University of Bern" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <meta name="citation_author" content="Raphaela Seeger" />
  <meta name="citation_author_institution" content="Institute of Anatomy, University of Bern, Bern, Switzerland" />
  <meta name="citation_author_institution" content="Graduate School for Cellular and Biomedical Sciences, University of Bern" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <meta name="citation_author" content="Julika Radecke" />
  <meta name="citation_author_institution" content="Institute of Anatomy, University of Bern, Bern, Switzerland" />
  <meta name="citation_author_institution" content="Department of Neuroscience, Faculty of Health and Medical Science , 2200 Copenhagen N, University of Copenhagen, Copenhagen, Denmark" />
  <meta name="citation_author_institution" content="Diamond Light Source Ltd, Didcot, Oxfordshire, United Kingdom" />
  <meta name="citation_author_orcid" content="0000-0002-5815-5537" />
  <meta name="citation_author" content="Guillaume Witz" />
  <meta name="citation_author_institution" content="Science IT Service, University of Bern, Bern, Switzerland" />
  <meta name="citation_author_institution" content="Microscopy Imaging Center, University of Bern, Bern, Switzerland" />
  <meta name="citation_author_orcid" content="0000-0003-1562-4265" />
  <meta name="citation_author" content="Jakob B. Sørensen" />
  <meta name="citation_author_institution" content="Department of Neuroscience, University of Copenhagen, Blegdamsvej 3B, 2200 Copenhagen N, Denmark" />
  <meta name="citation_author_orcid" content="0000-0001-5465-3769" />
  <meta name="citation_author" content="Benoît Zuber" />
  <meta name="citation_author_institution" content="Institute of Anatomy, University of Bern, Bern, Switzerland" />
  <meta name="citation_author_orcid" content="0000-0001-7725-5579" />
  <link rel="canonical" href="https://aseedb.github.io/deep-prepyto-paper/" />
  <meta property="og:url" content="https://aseedb.github.io/deep-prepyto-paper/" />
  <meta property="twitter:url" content="https://aseedb.github.io/deep-prepyto-paper/" />
  <meta name="citation_fulltext_html_url" content="https://aseedb.github.io/deep-prepyto-paper/" />
  <meta name="citation_pdf_url" content="https://aseedb.github.io/deep-prepyto-paper/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://aseedb.github.io/deep-prepyto-paper/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://aseedb.github.io/deep-prepyto-paper/v/d1bae491dd1716d9c760d29740bd065635cd0fe0/" />
  <meta name="manubot_html_url_versioned" content="https://aseedb.github.io/deep-prepyto-paper/v/d1bae491dd1716d9c760d29740bd065635cd0fe0/" />
  <meta name="manubot_pdf_url_versioned" content="https://aseedb.github.io/deep-prepyto-paper/v/d1bae491dd1716d9c760d29740bd065635cd0fe0/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://aseedb.github.io/deep-prepyto-paper/v/d1bae491dd1716d9c760d29740bd065635cd0fe0/))
was automatically generated
from [aseedb/deep-prepyto-paper@d1bae49](https://github.com/aseedb/deep-prepyto-paper/tree/d1bae491dd1716d9c760d29740bd065635cd0fe0)
on November 23, 2022.
</em></small>



## Authors



+ **Amin Khosrozadeh**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [ameen-khosrowzadeh](https://github.com/ameen-khosrowzadeh)
    <br>
  <small>
     Institute of Anatomy, University of Bern, Bern, Switzerland; Graduate School for Cellular and Biomedical Sciences, University of Bern
     · Funded by Grant XXXXXXXX
  </small>

+ **Raphaela Seeger**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [elatella](https://github.com/elatella)
    <br>
  <small>
     Institute of Anatomy, University of Bern, Bern, Switzerland; Graduate School for Cellular and Biomedical Sciences, University of Bern
  </small>

+ **Julika Radecke**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0002-5815-5537](https://orcid.org/0000-0002-5815-5537)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [julikaradecke](https://github.com/julikaradecke)
    <br>
  <small>
     Institute of Anatomy, University of Bern, Bern, Switzerland; Department of Neuroscience, Faculty of Health and Medical Science , 2200 Copenhagen N, University of Copenhagen, Copenhagen, Denmark; Diamond Light Source Ltd, Didcot, Oxfordshire, United Kingdom
  </small>

+ **Guillaume Witz**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0003-1562-4265](https://orcid.org/0000-0003-1562-4265)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [guiwitz](https://github.com/guiwitz)
    <br>
  <small>
     Science IT Service, University of Bern, Bern, Switzerland; Microscopy Imaging Center, University of Bern, Bern, Switzerland
  </small>

+ **Jakob B. Sørensen**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-5465-3769](https://orcid.org/0000-0001-5465-3769)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [JBSorensen](https://github.com/JBSorensen)
    <br>
  <small>
     Department of Neuroscience, University of Copenhagen, Blegdamsvej 3B, 2200 Copenhagen N, Denmark
     · Funded by Novo Nordisk Fonden, NNF17OC0028516.; Carlsbergfondet, CF17-0875; Independent Research Fond Denmark, 8020-00228A; Lundbeckfonden, R277-2018-802
  </small>

+ **Benoît Zuber**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-7725-5579](https://orcid.org/0000-0001-7725-5579)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [aseedb](https://github.com/aseedb)
    <br>
  <small>
     Institute of Anatomy, University of Bern, Bern, Switzerland
     · Funded by Swiss National Science Foundation, 179520; ERA-NET NEURON, NEURON-119
  </small>


::: {#correspondence}
✉ — Correspondence possible via [GitHub Issues](https://github.com/aseedb/deep-prepyto-paper/issues)

:::


## Abstract {.page_break_before}

Cryo-electron Tomography (Cryo-ET) has the potential to reveal cell structure down to atomic resolution.
Nevertheless, cellular cryo-ET data is often highly complex and visualization, as well as quantification, of subcellular structures require image segmentation.
Due to a relatively high level of noise and to anisotropic resolution in cryo-ET data, automatic segmentation based on classical computer vision approaches usually does not perform satisfyingly.
For this reason, cryo-ET researchers have mostly performed manual segmentation.

Communication between neurons rely on neurotransmitter-filled synaptic vesicle (SV) exocytosis.
Recruitment of SVs to the plasma membrane is an important means of regulating exocytosis and is influenced by interactions between SVs.
Cryo-ET study of the spatial organization of SVs and of their interconnections allows a better understanding of the mechanisms of exocytosis regulation.
Extremely accurate SV segmentation is a prerequisite to obtain a faithful representation of SV state of connectivity.
Hundreds to thousands of SVs are present in a typical synapse, and their manual segmentation is a time-consuming exercice, which has been recognized as a bottleneck by the community.

Several attempts to automate vesicle segmentation by classical computer vision or machine learning algorithms have not yielded very robust results.
We addressed this problem by designing a workflow consisting of a U-Net convolutional network followed by post-processing steps.
This combination yields highly accurate results.
Furthermore, we provide an interactive tool for accurately segmenting spherical vesicles in a fraction of the time required by available manual segmentation methods.
This tool can be used to segment vesicles that were missed by the fully automatic procedure or to quickly segment a handful of vesicles, while bypassing the fully automatic procedure.
Our pipeline can in principle be used to segment any spherical vesicle in any cell type as well as extracellular vesicles.


## Introduction

The fine architecture of cells can be investigated by cryo-electron tomography (cryo-ET) [@doi:10.1016/j.jmb.2021.167187].
Cellular structures are preserved down to the atomic scale through vitrification and observation of the samples in a fully hydrated state.
When a macromolecule is present in a sufficient number of copies in the cells imaged by cryo-ET, it is possible to obtain its atomic structure in situ using subtomogram averaging [@doi:10.1101/2022.01.10.475481; @doi:10.1038/s41596-021-00648-5].
Cellular cryo-ET datasets are usually extremely complex, making them difficult to analyze. 
This is aggravated by the sensitivity of biological samples to electron radiation, which limits the signal-to-noise ratio in cryo-ET datasets [@doi:10.1146/annurev.biochem.73.011303.074112].
Tomographic reconstructions are generated from a series of images of the sample acquired at different viewing angles.
The geometry of the samples prevents acquisition at certain angles, resulting in anisotropic spatial coverage.
The resolution in the directions close to the axis of the electron beam incident on the untilted sample is strongly reduced. 
This effect, commonly referred to as the missing-wedge artifact, further complicates data analysis. 
In particular, organelles fully bounded by a membrane appear to have holes at their top and bottom (relative to the electron beam axis) [@doi:10.1146/annurev.biochem.73.011303.074112].

The synapse is a specialized cellular contact at which information is transmitted from a neuron to another. 
The former neuron is called presynaptic and the latter is postsynaptic. 
In most cases, the signal is transmitted by the release of neurotransmitters into the intercellular space.
Neurotransmitters are stored in SVs and are released following the fusion of an SV with the presynaptic plasma membrane.
A synapse contains hundreds of SVs and their mobility and recruitability for neurotransmitter release depends on inter-vesicle interactions through so-called connector structures [@doi:10.1083/jcb.200908082 ]. 
The characterization of these interactions can be performed automatically with the pyto package, which implements a hierarchical connectivity approach to segment connectors [@doi:10.1016/j.jsb.2016.10.004]. For accurate connector segmentation, an accurate segmentation of SVs is prerequisite.
To date, SV segmentation has been performed manually, but given the large number of SVs per dataset, it is an extremely time-consuming process. 
Typically, one person spends 3 to 8 working days to segment a single dataset.
Attempts to perform this task automatically based on classical computer vision algorithms have not yielded sufficiently accurate performance [@doi:10.1016/j.jsb.2014.02.015].  
To alleviate this situation, we decided to develop an approach based on deep learning-based.

Convolutional neural networks (CNN) have been successfully employed to segment cryo-ET data [@doi:10.1038/nmeth.4405]. 
Although entirely satisfying for visualization purposes, this approach has not met the requirements of pyto.
A recent publication described accurate SV segmentation of transmission electron microscopy images using CNN, but it is limited to 2-dimensional (2D) images of resin-embedded synapses [@doi:10.1523/ENEURO.0400-20.2021].
In the first study, cryo-ET data are decomposed in individual 2D slices, which are handed as separate input to the CNN. 
The independent output 2D prediction images are reassembled in a 3-dimensional (3D) stack [@doi:10.1038/nmeth.4405].
As discussed above, membranes oriented approximately parallel to the plane of the 2D tomographic images are not resolved.
In the absence of contextual knowledge of the other 2D images, the CNN fails to segment these regions of the vesicles.
Hence, spherical vesicles appear open, whereas we expect closed spherical objects.
To overcome this limitation, we used a U-Net CNN that takes 3D images as input [@arxiv:1606.06650].
Weigert et al. [@doi:10.1038/s41592-018-0216-7] implemented a U-Net for content-aware restoration (CARE) of 3D fluorescence microscopy datasets. They showed that it can restore information from anisotropic and very noisy datasets.
We implemented a 3D U-Net based on CARE building blocks and trained it with manually segmented datasets. 
This method provided good accuracy and was only slightly affected by the missing wedge artifact. 
Nevertheless, it was not sufficient for our downstream pyto analysis.
Hence, we developed a post-processing method, which transforms the segmented objects into spheres and refines their radius and center location. The procedure includes an outlier detection procedure.
This lead to a substantial accuracy improvement, which is reflected in pyto performances comparable to those obtained after manual SV segmentation.
We also introduce a semi-automatic method to quickly fix wrongly segmented or missed SVs.

Although our set of procedures was developed with the use case of SV segmentation in mind, it can be used to segment any other types of biological spherical vesicles, such as transport vesicles, secretory vesicles, endocytic vesicles, and extracellular vesicles.


## Results

In view of the effort required for the manual segmentation of SVs, we decided to develop an automatic segmentation procedure.
Since we had previously manually segmented a number of tomograms with the program IMOD, we could use these segmentations as the ground truth [@doi:10.1006/jsbi.1996.0013].
`\_maybe add this somewhere else: In a next step, filaments connecting the synaptic vesicles with each other (connectors) and to the active zone (AZ) were automatically segmented with the algorithm application Pyto [@doi:10.1016/j.jsb.2016.10.004].*`{.green}
We trained a U-Net with a set of 9 segmented tomograms of rat synaptosomes (see Materials and Methods).
The learning progress was tracked by calculating the Dice coefficient and the loss value after each training epoch (Figure {@fig:dice}).
The Dice coefficient for the training set was initially ~0.25 and rose to over 0.9 after approximately 50 epochs, while for the validation set, it rose to 0.8. 
The loss for the training set went from 0.55 and to values below 0.05 after 50 epochs while for the validation set it went from 1 and to slightly below 0.3 after the initial 50 epochs and then rose slightly.

![**Dice coefficient and loss value for training and validation set.** ](images/traindice.png){#fig:dice width="7cm"}

`\_---->add figures of local measurements such as diameter or center error as an extra figure, why else listed in M&M??"*`{.green}

We seeked to further improve segmentation accuracy by feeding the probability mask output by the U-Net to a series of postprocess steps (Figure {@fig:pipeline}).
Three batches of tomograms were used to assess the performances of the pipeline: 1) The 9 rat synaptosome tomograms that had been used for U-Net training, 2) Another 9 rat synaptosome tomograms, 3) 12 mouse primary neuronal culture tomograms). 

![**Pipeline of automatic segmentation.** a) tomograms b) splitting in 3D patches c) Segmentation Network/ trained U-Net d) probability masks e) stitching patches back together f) thresholding g) adaptive localized thresholding h) outlier removal i) radial profile](images/pipeline.svg){#fig:pipeline width="15cm"}

Each tomogram was split into patches of 32^3^ voxels.
These patches were fed in the U-Net, which output a probability mask for those patches.
To obtain a complete probability mask, the patches are stitched back together.
The probability mask was binarized first with a global threshold value and then with an adaptative localized thresholding steps (Figure {@fig:pipeline}, Figure {@fig:tom}).

![**2D Slices** A) a section from z axis of a tomogram’s presynaptic terminal of a neuron B) instance mask of the vesicles after post processing; purple corresponds to a low probability of SVs and yellow corresponds to a high probability of synaptic vesicles C) predicted probability mask by the segmentation network](images/tomo-sclae.svg){#fig:tom width="15cm"}

`\_more detail about global and adaptive localized threshold*`{.green}
For further optimization of the mask, outliers were removed. 
Removed outliers mostly consisted of vesicles which were only partially segmented, and vesicles which maks were adjacent due to proximity.
The removed masks, which only partially traced the vesicles, were reevaluated by reducing or expanding their radius (Figure {@fig:radial_profile}).
`\_was the center of the vesicles also reevaluated?*`{.green} `\_Its not clear or might be false sentence we didnt remove or re evaluate the mask?*`{.green}

![**Vesicle radius and position through radial profile and cross-correlation** Radial Profile Refinement A) couple of vesicles are not centered B) Radial Profile. Blue range is from membrane center to outer white halo center, this is the search range for the optimal radius. (smoothed by gaussian filtering) C) second derivative of radial profile E, F, H, G) Same as above columns after refinement](images/radial_avg_115-099.svg){#fig:radial_profile width="15cm"}

The adjacent vesicle masks were seperated (Figure `\_missing*`{.green}). `\_how?*`{.green}

`\_**missing Figure- Splitting adjacent vesicles. A) Examples of tomogram, no labels; B) raw label with connected vesicle-labels; C) modified label with seperated vesicles ---> for software: IMOD**`{.green}

The Dice coefficient was used to track the global congruence between the manually segmented mask and the predicted mask within the different tomograms (Figure {@fig:dice-improv}).

![**Dice developement during post-processing** Dice developement at different post processing steps of initial predicted mask (different colors correspond to different tomograms): A) synaptosomal training datasets B) synaptosomal test datasets c) neuron test datasets](images/improvment-post-processing-dice.svg){#fig:dice-improv width="15cm"}


### Final Eval Tables

Table 1- Evaluation of the segmentation: Mask Dice: Mask Dice coefficient for the predicted mask; Final Label Dice: Dice coefficient after post-processing; δ d: diameter error on correctly detected vesicle; Δ c: average error center (nm); # of Vesicles: number of expected vesicles; TP: True Positive; FN: False Negative; FP: False Positive

#### Train Dataset

| **_Dataset_**  | **_Mask DICE_** | **_Final Label DICE_** |     | **_δ d_** | **_Δ c (nm)_** | **_\# of Vesicles_** |   **TP**   |  **FN**   |  **FP**   |
| -------------- | :-------------: | :--------------------: | :-: | :-------: | :------------: | :------------------: | :--------: | :-------: | :-------: |
| Synaptosome C1 |      0.44       |          0.73          |     |   0.07    |   2.55±1.56    |         223          |    198     |    26     |    49     |
| Synaptosome C2 |       0.8       |          0.9           |     |   0.05    |   2.12±1.06    |         105          |    103     |     2     |     1     |
| Synaptosome C3 |      0.67       |          0.9           |     |   0.05    |   1.86±1.24    |         128          |    127     |     1     |     6     |
| Synaptosome C4 |      0.62       |          0.89          |     |   0.03    |   1.78±0.92    |         144          |    141     |     3     |     4     |
| Synaptosome C5 |      0.58       |          0.87          |     |   0.04    |   1.86±1.00    |         214          |    209     |     5     |    13     |
| Synaptosome C6 |      0.56       |          0.84          |     |   0.04    |   1.92±1.05    |         104          |    102     |     2     |    16     |
| Synaptosome C7 |      0.78       |          0.88          |     |   0.06    |   1.86±0.90    |         184          |    184     |     0     |    16     |
| Synaptosome C8 |      0.75       |          0.9           |     |   0.05    |   1.70±0.93    |         132          |    126     |     6     |     1     |
| Synaptosome C9 |      0.59       |          0.87          |     |   0.05    |   1.87±0.91    |         135          |    132     |     3     |    14     |
| **Average**    |  **0.64±0.11**  |     **0.86±0.05**      |     | **0.05**  | **1.95±1.08**  |      **152.22**      | **97.00%** | **3.00%** | **7.30%** |

#### Test Dataset (Same preparation and microscope with training set)

| **_Dataset_**   | **_Mask DICE_** | **_Final Label DICE_** |     | **_δ d_** | **_Δ c (nm)_** | **_\# of Vesicles_** |   **TP**   |  **FN**   |  **FP**   |
| --------------- | :-------------: | :--------------------: | :-: | :-------: | :------------: | :------------------: | :--------: | :-------: | :-------: |
| Synaptosome C10 |      0.75       |          0.88          |     |   0.07    |   1.86±1.18    |         129          |    123     |     6     |     5     |
| Synaptosome T1  |      0.75       |          0.83          |     |   0.11    |   2.66±1.52    |         699          |    687     |    12     |    33     |
| Synaptosome T2  |      0.74       |          0.77          |     |   0.11    |   2.27±1.84    |         122          |    117     |     5     |     2     |
| Synaptosome T3  |      0.72       |          0.74          |     |   0.11    |   3.64±2.22    |         434          |    397     |    37     |    57     |
| Synaptosome T5  |      0.77       |          0.85          |     |   0.08    |   2.20±1.26    |         535          |    526     |     9     |    25     |
| Synaptosome T6  |       0.6       |          0.83          |     |   0.07    |   2.02±1.12    |         373          |    353     |    20     |    42     |
| Synaptosome T7  |       0.8       |          0.83          |     |   0.06    |   2.22±1.14    |         110          |    107     |     3     |     9     |
| Synaptosome T8  |      0.83       |          0.91          |     |   0.04    |   2.09±1.04    |         100          |     99     |     1     |     2     |
| Synaptosome T10 |      0.77       |          0.86          |     |   0.05    |   1.96±1.04    |          77          |     74     |     3     |     6     |
| **Average**     |  **0.75±0.06**  |     **0.83±0.05**      |     | **0.08**  | **2.32±1.43**  |      **286.56**      | **96.30%** | **3.70%** | **6.10%** |

#### Test Dataset 3 (Neuron Dataset)

| **_Dataset_** | **_Mask DICE_** | **_Final Label DICE_** |     | **_δ d_** | **_Δ c (nm)_** | **_\# of Vesicles_** |   **TP**   |   **FN**   |  **FP**   |
| ------------- | :-------------: | :--------------------: | :-: | :-------: | :------------: | :------------------: | :--------: | :--------: | :-------: |
| Neuron 133    |      0.76       |          0.86          |     |   0.05    |   2.16±1.32    |         523          |    467     |     56     |     8     |
| Neuron 123    |      0.64       |          0.71          |     |   0.05    |   2.05±1.18    |          66          |     58     |     8      |     2     |
| Neuron 84     |      0.86       |          0.89          |     |   0.06    |   1.44±0.75    |         498          |    484     |     14     |     1     |
| Neuron 134    |      0.56       |          0.67          |     |   0.09    |   2.87±2.50    |         638          |    384     |    254     |    63     |
| Neuron 115    |      0.57       |          0.63          |     |   0.08    |   3.56±3.23    |         170          |    123     |     47     |    32     |
| Neuron 102    |      0.73       |          0.86          |     |   0.05    |   1.47±0.79    |         103          |     86     |     17     |     1     |
| Neuron 80     |       0.7       |          0.81          |     |   0.07    |   2.67±2.00    |         111          |    102     |     9      |     3     |
| Neuron 114    |      0.65       |          0.73          |     |   0.07    |   2.68±1.79    |         131          |     93     |     38     |     9     |
| Neuron 132    |      0.69       |          0.87          |     |   0.03    |   1.65±1.26    |         135          |    129     |     6      |    32     |
| Neuron 73     |      0.78       |          0.83          |     |   0.06    |   2.93±2.00    |         526          |    483     |     43     |     2     |
| Neuron 128    |      0.67       |          0.85          |     |   0.04    |   2.33±1.70    |         252          |    232     |     20     |    19     |
| Neuron 116    |      0.62       |          0.73          |     |   0.07    |   2.38±1.82    |         296          |    207     |     89     |    35     |
| **Average**   |  **0.69±0.09**  |     **0.79±0.09**      |     | **0.06**  | **2.35±1.83**  |      **287.42**      | **83.60%** | **16.40%** | **7.90%** |


Our method transfers well across datasets even without fine-tuning which show robustness and generalization.

### Comparison of manual segmentation with automatic deep-learning based segmentation

![**3D model of manual segmented and automatically segmented synaptosome.**](images/3d.png){#fig:3d width="10cm"}


## Discussion

While the Dice coefficient is a good global measure to assess the predictions in comparison to the ground truth, it is difficult to asses local segmentation accurracy. 
For example, a single generated vesicle label containing several close connected vesicles would not be practical for further analysis for the researcher although it could have almost the same dice value. 
What is important for actual usage of the software would be the number and percentage of true-detected vesicles, false-positive and false-negative rates. 

Center error:
If we measure each axis error it will reveal that human bias in segmentation is more affected on the Z-axis. [we didn't show it in number but its checked the hypothesis]
`\_we cannot claim something without showing it. ---> this would belong into results*`{.green}

3d unet good for 3D processing
recent Nature methods paper by Ben Engel, DeepFinder -> Relion for STA creates mask to find more using dl
-what are they doing, maybe compare that in the text, different aims; we might compare results we achieve (keep as bonus, revision)

### Outlook
implement automatic cell-outline and active zone segmentation as deep learning workflow using UNet
implement automatic connector and tether segmentation as a deep leaning workflow using UNet





## Materials and methods

### Cryo-electron Tomography Datasets

Two datasets of different origin were used as input and test subjects for the automatic segmentation pipeline, respectively.
They consisted in rat synaptosomes primary neuron cultures derived from mice.
The preparation procedure of the samples from which the datasets were obtained as well as the biological analysis of these datasets was previously reported  [@doi:10.1101/2022.03.07.483217].

### Manual segmentation and automatic interboundary segment detection

Manual segmentation of SVs, mitochondria, the active zone PM, and of the segmentation region was done in IMOD (???Figure S4A&B???) [@10.1006/jsbi.1996.0013]. SVs were segmented as spheres.
The segmentation region marked the region to be analyzed by Pyto [@doi:10.1016/j.jsb.2016.10.004].
The analysis by Pyto was essentially the same as described previously [@doi:10.1083/jcb.200908082; @doi:10.1016/j.jsb.2016.10.004].
In short, the segmented region is divided in 1 voxel thick layers parallel to the active zone for distance calculations.
A hierarchical connectivity segmentation detects densities interconnecting boundaries.
The boundaries were synaptic vesicles and the active zone PM. Detected intervesicular segments are termed connectors and segments connecting vesicles to the active zone PM are called tethers (Figure `\_add figure number*`{.green}).
Distance calculations respective to SVs were done from SV center.
The segmentation procedure is conservative and tends to miss some tethers and connectors because of noise.
Consequently, the numbers of tethers and connectors should not be considered as absolute values, but rather to compare experimental groups.
As it was done before, an upper limit was set between 2100 and 3200 nm^3^ on segment volume.
The tomograms that were used for this analysis were binned by a factor of 2 to 3, resulting in voxel sizes between 2.1 and 2.4 nm.

### Pre-processing of manual segmentation outputs from IMOD for further use (jupyter notebook pre-pyto)
`probably not necessary to mention output from IMOD to prepyto input label file procedure`

`put this somewhere else`{.green}
The used datasets included a total of 30 tomograms with heterogeneous pixel sizes, defocus and resolution. 

1. 9 synaptosome datasets were used for training and validation.
2. 9 synaptosome datasets was used for test.
3. 12 Neuron dataset were used for assessing transfer learning potential. 

### Network architecture and training procedure

We used a U-Net of depth 2, two convolutional layers per depth, a convolutional kernel size of 3, and ReLU activation function based on the open-source CARE framework (Figure {@fig:unet}) [@doi:10.1038/s41592-018-0216-7]. 
Datasets were prepared by splitting the 3D tomographic volume of synaptosomes into 32^3^-voxel subvolumes and keeping only subvolumes occupied by a sufficient amount (> 1000 voxels) of binarized vesicle label.
860 subvolumes were used for training and 100 subvolumes were used for validation.
We used the Adam optimizer on a binary cross-entropy loss function.


![**Network architecture used for vesicle segmentation.** We used a U-Net based on the CARE framework [@doi:10.1038/s41592-018-0216-7]. The input is a cubic volume of 32^3^ voxels. The output is a per-prix probabilty cube of the same size as the input. ](images/unet.png){#fig:unet width="10cm"}


### U-Net output threshold refinement

The probability mask output by the U-Net was first made binary by determining a global threshold value. To this end, the mask was binarized for a range of threshold values comprised between 0.8 and 1. For each probability value a 1-voxel thick label shell  was computed. 
The shell mask was then applied on the input data and the average masked voxel intensity was computed.
Since the shell of correctly segmented vesicles corresponds to the vesicle membrane, we expect low intensity pixels.
The threshold value resulting in the minimal average intensity of the shell masked voxels was used as the global threshold.  
`Amin please write the equations for these steps`{.green}.
The probability mask was binarized using the global threshold and was each separate segment was assigned an individual label with `scikit-image label` method.


A majority of vesicles were correctly segmented but we noticed some segments included two vesicles.
We therefore evaluated each segment with two criteria based on the fact that synaptic vesicles have a homogenous size and are spherical. 
Firstly we calculated the volume z-score $z$ for each segment:
$$z(S_i) = \frac{V(S_i) - \mu}{\sigma}$$ {#eq:z-score-volume}
where $S_i$ is the segment $i$, $V(S_i)$ is the volume of $S_i$, $\mu$ the average volume of all segments, and $\sigma$ the standard deviation of the segment volumes.
Secondly, we computed the segment extent $e$:
$$e(S_i) = \frac{V(S_i)}{B(S_i)}$$ {#eq:extent}
where $B(S_i)$ is the volume of segment $i$ bounding box.
The extent of a sphere equals $\frac{\pi}{6}$.
Segments with both a z-score $z > 1$ and an extent $e < 0.25$ were considered as potentially comprising two vesicles.
For each of these segments, the probability mask threshold was increased until two distinct segments were generated.
Subsequently, the extent and volume of all segments was evaluated again. Any segment with $e < 0.25$, or $e > 0.75$, or $V < k$ was discarded. 
This ensured that segments deviating highly from spherical shape and segments with a volume smaller than an acceptable volume $k$ were removed.

Even if most synaptic vesicles were detected and well segmented, segmentation accuracy was not sufficient for our downstream application.
To improve accuracy, each segment was converted to a spherical segment and its radius and position was refined.
Initial spherical conversion was done by setting the center of the sphere $C$ at the position of the centroid of the segment, while the radius $r$ was defined as half the length of the bounding box longest edge. 
The segment position and radius was iteratively refined as follows. 
1. The radial average $\langle I(d)\rangle$ was computed:
$$\langle I(d)\rangle = \frac{1}{4\pi ^2 r^2} \int_{0}^{2\pi}\int_{0}^{2\pi}I(d,\theta ,\phi) \, d\phi \, d\theta$$ {#eq:radial_average}
where $d$ is the radial distance from the segment center, $\theta$ the polar angle, and $\phi$ the azimuthal angle.
2. The radius of the vesicle $r$ was updated as:
$$r = d_m + \frac{t_m}{2}$$ {#eq:vesicle_radius}
where $d_m$ is the radial distance of center of the vesicle membrane, and $t_m$ the thickness of the vesicle membrane.
$d_m$ was defined as the radial distance for which the radial average was minimal.
$\frac{t_m}{2}$ was calculated as the distance between the center of the vesicle membrane and the minimum of the second derivative of the radial profile in the interval between the center of the vesicle membrane and the maximum of the Fresnel fringe outside the membrane.
3. The radial average was back projected in 3-dimension:
$$I(x,y,z) =  \langle I(\sqrt{x^2+y^2+z^2})\rangle$$ {#eq:3d-average}
where $(x,y,z)=(0,0,0)$ is the coordinate of the segment center.
4. We computed by cross-correlation the shift between the obtained 3-D average and the 3-D image in the cubic box with central coordinates $C$ and edge length $l = 2r + c$, where $c$ is a constant.
$C$ was updated by subtraction of the shift. 
5. Steps 1 to 4 were repeated for a maximum of 10 iterations until convergence or until a total shift of $\frac{1}{2}\sqrt{3l_o^2}$, where $l_o is the edge length of the initial box. 
The feature space of predicted vesicle labels was computed, containing membrane thickness $t_m$, membrane intensity $\rho$, and vesicle radius $r$.
$\rho$ was defined as the mean intensity of the radial average within the radial distance interval $[d_m - \frac{t_m}{2}\,,\,d_m + \frac{t_m}{2}]$.

Using this multivariate feature space, we detect outliers by computing Mahalanobis Distances (MD) on normalized variables using the covariance matrix of observation and obtaining The p-value of MD.
`The sphere segments with a p-value higher than a defined threshold were discarded and the process was repeated iteratively.
If the MD p-value of a specific vesicle was not in a specific margin range (0-10), their radial profile was recalculated, and the label entirely removed if they again failed to pass the margin of the p-value.`{.yellow}
`Amin, please check what exactly was done with the outliers. 
And p-value cannot be higher than 1, while you wrote (0-10)`{.green}

### Analysis of Results

The evaluation framework was designed to assess the capabilities of the proposed toolbox for automatic synaptic vesicle segmentation.
The framework was not only designed to evaluate quantitatively performance of the neural network, but rather assay the segmentation of vesicles in practice `\_unsure what the last part means*`{.green}. `\_I tried to say we develop the software rather than an algorithm paper with ablation study kinda more trasnfer learning but however for tranfer learning we might need add finetunning the network or say this sentence in other way*`{.green}.
The pipeline also generates a specific output format, which is necessary to further analyze the presynaptic tomograms via another pre-developed toolbox (Pyto), which segments small molecular filaments associated to the synaptic vesicles, titled tethers and connectors.

#### DICE

The `\_general form??*`{.green} DICE coefficient for probabilistic subvolume maps was calculated after each epoch as a performance quantification while `\_during?*`{.green} training.
The probabilistic mask subvolumes were stitched back together, creating a probabilistic map of the whole tomogram. 
The Soft-DICE for the whole tomogram was calculated to evaluate the similarity of the predicted probability mask with ground truth. 
Note that soft-dice is equivalent to dice, when the input is binarized (which we will do at the end of the post-processing).


$$1-\frac{2\sum_{pixels} y_{true} y_{pred}%}{\sum_{pixels} y_{true}^2+\sum_{pixels} y_{pred}^2}$$

`\_shouln't it be voxels instead of pixels??*`{.green}
`\_yes voxel is right*`{.green}

THE DICE was also employed to monitor all stages of post-processing on the eventual label file, to observe the effect of each post-processing step.

#### Diameter Error

The diameter of a vesicle is one of its relevant characterizations, and it is predefined (see Outlier Removal). 
`\_which diameters are we using in this evaluation as input, pre- or post-outlier removal?*`{.green}
`\_after! I meant from that perentesis that radius or dimater we assume as one charectiristic of vesicle we might can write it better *`{.green}
The error of diameter estimation of true-detected vesicle is defined as 1 minus the proportion of diameters 

$$\delta d=1-\frac{min(dSi,dGTi)}{max(dSi,dGTi)}$$ {#eq:regular-equation}

where dGTi is the diameter of each true manual segmented vesicle, and dSi is the diameter of its estimation.

#### Center error

The center error is an euclidean distance of ground truth and corresponds to true predicted vesicles `\_true pos or true neg*`{.green}.
A vesicle was defined as a true-detected vesicle if the predicted center was located inside the hand-segmented vesicle and the other way around the center of prediction was located inside the predicted vesicle. 
`\_isn't this a bit too general, shouldn't this be a tighter evaluation?*`{.green}
`\_we assume this as hard condition to be true postive we could define like some % liek 50% intersection but this condition is generally harder`{.green}
This means the volume of intersection of the estimated vesicle with the distance of d to a ground truth vesicle with radius R is: 

$$V=\frac{1}{12}\pi(4R+d)(2R-d)$$

### Manuscript preparation
The manuscript was written with the open and collaborative scientific writing package Manubot [@doi:10.1371/journal.pcbi.1007128]. 
The source code and data for this manuscript are available at <https://github.com/aseedb/synaptic_tomo_ms>.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
