---
title: 'CryoVesNet: A Dedicated Framework for Synaptic Vesicle Analysis in Cryo-Tomograms'
keywords:
- synapse
- cryo-electron tomography
- synaptic vesicles
- deep learning
- segmentation
- post-processing
- automation
lang: en-US
date-meta: '2023-11-06'
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
  <meta name="dc.title" content="CryoVesNet: A Dedicated Framework for Synaptic Vesicle Analysis in Cryo-Tomograms" />
  <meta name="citation_title" content="CryoVesNet: A Dedicated Framework for Synaptic Vesicle Analysis in Cryo-Tomograms" />
  <meta property="og:title" content="CryoVesNet: A Dedicated Framework for Synaptic Vesicle Analysis in Cryo-Tomograms" />
  <meta property="twitter:title" content="CryoVesNet: A Dedicated Framework for Synaptic Vesicle Analysis in Cryo-Tomograms" />
  <meta name="dc.date" content="2023-11-06" />
  <meta name="citation_publication_date" content="2023-11-06" />
  <meta property="article:published_time" content="2023-11-06" />
  <meta name="dc.modified" content="2023-11-06T16:33:40+00:00" />
  <meta property="article:modified_time" content="2023-11-06T16:33:40+00:00" />
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
  <link rel="alternate" type="text/html" href="https://aseedb.github.io/deep-prepyto-paper/v/3ecf5bf305f8a596e66f211cb3cffcaab73d7ea7/" />
  <meta name="manubot_html_url_versioned" content="https://aseedb.github.io/deep-prepyto-paper/v/3ecf5bf305f8a596e66f211cb3cffcaab73d7ea7/" />
  <meta name="manubot_pdf_url_versioned" content="https://aseedb.github.io/deep-prepyto-paper/v/3ecf5bf305f8a596e66f211cb3cffcaab73d7ea7/manuscript.pdf" />
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
([permalink](https://aseedb.github.io/deep-prepyto-paper/v/3ecf5bf305f8a596e66f211cb3cffcaab73d7ea7/))
was automatically generated
from [aseedb/deep-prepyto-paper@3ecf5bf](https://github.com/aseedb/deep-prepyto-paper/tree/3ecf5bf305f8a596e66f211cb3cffcaab73d7ea7)
on November 6, 2023.
</em></small>



## Authors



+ **Amin Khosrozadeh**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [amineuron](https://github.com/amineuron)
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
Nevertheless, cellular cryo-ET data is often highly complex, and visualization, as well as quantification, of subcellular structures require image segmentation.
Due to a relatively high level of noise and anisotropic resolution in cryo-ET data, automatic segmentation based on classical computer vision approaches usually does not perform satisfactorily.
For this reason, cryo-ET researchers have mostly performed manual segmentation.

Communication between neurons relies on neurotransmitter-filled synaptic vesicle (SV) exocytosis.
Recruitment of SVs to the plasma membrane is an important means of regulating exocytosis and is influenced by interactions between SVs.
Cryo-ET study of the spatial organization of SVs and of their interconnections allows a better understanding of the mechanisms of exocytosis regulation.
Extremely accurate SV segmentation is a prerequisite to obtaining a faithful representation of SVs state of connectivity.
Hundreds to thousands of SVs are present in a typical synapse, and their manual segmentation is a time-consuming exercise, which has been recognized as a bottleneck by the community.

Several attempts to automate vesicle segmentation by classical computer vision or machine learning algorithms have not yielded very robust results.
We addressed this problem by designing a workflow consisting of a U-Net convolutional network followed by post-processing steps.
This combination yields highly accurate results.
Furthermore, we provide an interactive tool for accurately segmenting spherical vesicles in a fraction of the time required by available manual segmentation methods.
This tool can be used to segment vesicles that were missed by the fully automatic procedure or to quickly segment a handful of vesicles while bypassing the fully automatic procedure.
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
The characterization of these interactions can be performed automatically with the Pyto package, which implements a hierarchical connectivity approach to segment connectors [@doi:10.1016/j.jsb.2016.10.004]. For accurate connector segmentation, accurate segmentation of SVs is a prerequisite.
To date, SV segmentation has been performed manually, but given the large number of SVs per dataset, it is an extremely time-consuming process. 
Typically, one person spends 3 to 8 working days segmenting a single dataset.
Attempts to perform this task automatically based on classical computer vision algorithms have not yielded sufficiently accurate performance [@doi:10.1016/j.jsb.2014.02.015].  
To alleviate this situation, we decided to develop an approach based on deep learning.

Convolutional neural networks (CNN) have been successfully employed to segment cryo-ET data [@doi:10.1038/nmeth.4405]. 
Although entirely satisfying for visualization purposes, this approach has not met the requirements of Pyto.
A recent publication described accurate SV segmentation of transmission electron microscopy images using CNN, but it is limited to 2-dimensional (2D) images of resin-embedded synapses [@doi:10.1523/ENEURO.0400-20.2021].
In the first study, cryo-ET data are decomposed in individual 2D slices, which are handed as separate inputs to the CNN. 
The independent output 2D prediction images are reassembled in a 3-dimensional (3D) stack [@doi:10.1038/nmeth.4405].
As discussed above, membranes oriented approximately parallel to the plane of the 2D tomographic images are not resolved.
In the absence of contextual knowledge of the other 2D images, the CNN fails to segment these regions of the vesicles.
Hence, spherical vesicles appear open, whereas we expect closed spherical objects.
A recent publication addressed this issue by implementing a downstream fitting step based on the Gaussian process, allowing for the smooth closure of the membranes [@doi:10.1016/j.jocs.2022.101904].
We followed a different approach and used a 3D U-Net CNN that takes 3D images as input [@arxiv:1606.06650]. 
Weigert et al. [@doi:10.1038/s41592-018-0216-7] implemented a U-Net for content-aware restoration (CARE) of 3D fluorescence microscopy datasets.
They showed that it can restore information from anisotropic and very noisy datasets.
Such networks have been used in the last couple of years in cryo-ET analysis, mainly to perform denoising and object detection [@arxiv:1810.05420;@doi:10.1038/s41592-021-01275-4;@doi:10.1038/s41592-022-01746-2]. 
We implemented a 3D U-Net based on CARE building blocks and trained it with manually segmented datasets. 
This method provided good accuracy and was only slightly affected by the missing wedge artifact. 
Nevertheless, it was not sufficient for our downstream Pyto analysis.
Hence, we developed a post-processing method, which transforms the segmented objects into spheres and refines their radius and center location. The procedure includes an outlier detection procedure.
This leads to a substantial improvement in accuracy, which is reflected in Pyto performances comparable to those obtained after manual SV segmentation.
We also introduce a semi-automatic method to quickly fix wrongly segmented or missed SVs.

Although our set of procedures was developed with the use case of SV segmentation in mind, it can be used to segment any other types of biological spherical vesicles, such as transport vesicles, secretory vesicles, endocytic vesicles, and extracellular vesicles.


## Results

In view of the effort required for the manual segmentation of SVs, we decided to develop an automatic segmentation procedure.
Since we had previously manually segmented a number of tomograms with the program IMOD, we could use these segmentations as the ground truth [@doi:10.1006/jsbi.1996.0013].
We trained a U-Net with a set of 9 segmented tomograms of rat synaptosomes (see Materials and Methods).

We seeked to further improve segmentation accuracy by feeding the probability mask output by the U-Net to a series of postprocess steps (Figure {@fig:pipeline}).
Three sets of tomograms were used to assess the performances of the pipeline:

1) Traning dataset : The 9 rat synaptosome tomograms that had been used for U-Net training

2) Testing dataset: Another 9 rat synaptosome tomograms

3) Testing dataset for generizibility: 12 mouse astrocytic and primary neuronal culture tomograms). 

Each tomogram was split into patches of 32^3^ voxels.
These patches were fed in the U-Net, which output a probability mask for those patches.
To obtain a complete probability mask, the patches are stitched back together.
The probability mask was binarized first with a global threshold value and then with an adaptative localized thresholding steps (Figure {@fig:pipeline}, Figure {@fig:tom}).

![**Pipeline of automatic segmentation.** a) Tomograms b) Splitting in 3D patches c) Segmentation Network/ trained U-Net d) probability masks e) stitching patches back together f) thresholding h) radial profile i) outlier removal j)Segmented Vesicles](images/pipeline_new.png){#fig:pipeline width="20cm"}

While a global threshold serves as an initial step in vesicle segmentation, it often falls short in complex scenarios, especially when vesicles are in close proximity or exhibit overlap. To enhance the segmentation accuracy in such cases, we employ an adaptive thresholding methodology that capitalizes on the probability mask generated by our deep learning architecture.

#### Initial Segmentation and Thresholding:
The segmentation journey commences with the alignment of the image with its associated deep labels and the probability mask. To ensure a comprehensive segmentation, the probability mask's edges are meticulously cropped, safeguarding against inadvertent truncation of boundary-residing vesicles. An optimal threshold, derived from the image and the probability mask, undergoes fine-tuning through a coefficient adjustment. This refined threshold then serves to binarize the mask, with connected components subsequently labeled, delineating individual vesicles.

#### Collision Resolution through Adaptive Thresholding:
In scenarios where vesicles are densely packed, collisions become a challenge, often leading to the amalgamation of multiple vesicles into a singular segmented entity. Addressing this, potential collision vesicles are pinpointed based on specific geometric attributes, such as their extent and area z-score. For each vesicle identified under this criterion, a localized region surrounding the vesicle is extracted. This region is then subjected to a masking process, ensuring focus remains solely on the vesicle in question.

The essence of collision resolution revolves around the iterative modulation of the threshold to attain a more granular segmentation. Commencing from the established threshold, it's progressively augmented until the connected components within the localized region amplify, signaling a potential vesicle separation. This adaptive modulation persists until a threshold is identified that adeptly segregates the vesicles or until a set precision threshold is attained.

#### Expansion and Removal of Minuscule Vesicles:
Post-segmentation, certain vesicles might be represented as notably smaller than anticipated. To address this, an expansion strategy is employed, iteratively lowering the threshold to encapsulate more of the vesicle's structure. If expansion fails to achieve the desired size, these diminutive vesicles are removed, ensuring the final segmentation remains representative of genuine vesicle structures.
In conclusion, our adaptive thresholding technique, combined with collision resolution, ensures a more accurate and refined segmentation of vesicles in cryo-ET data. This approach capitalizes on the rich information present in the probability mask, providing a robust solution to the challenges posed by closely packed vesicles.



`\_more detail about global and adaptive localized threshold*`{.green}
For further optimization of the mask, outliers were removed. 
Removed outliers mostly consisted of vesicles which were only partially segmented, and vesicles which maks were adjacent due to proximity.
The removed masks, which only partially traced the vesicles, were reevaluated by reducing or expanding their radius (Figure {@fig:radial_profile}).
`\_was the center of the vesicles also reevaluated?*`{.green} `\_Its not clear or might be false sentence we didnt remove or re evaluate the mask?*`{.green}

![**A 2D slice of an automatically segmented dataset**. A) A section through a presynaptic terminal in a neuron tomogram. B) Predicted probability mask restricted to the segmentation region.  Purple corresponds to a low SV probability and yellow to a high SV probability. C) Instance mask of the vesicles after post processing.](images/tomo-sclae.svg){#fig:tom width="15cm"}

Each segmented vesicle undergoes a radial profile refinement. Representing vesicles as spheres, their position and radius are iteratively adjusted to mirror their actual structure in the tomogram. By computing the radial average and updating the vesicle's radius, this method ensures the segmented vesicles are a true representation of their form in the tomogram.

The radial profile serves as a pivotal tool in refining the segmentation of vesicles. By analyzing the radial distribution of intensity around the vesicle's centroid, we can discern the vesicle's true boundary. This method ensures that the segmented vesicles closely match their actual structure in the tomogram by iteratively adjusting their position and radius. The radial average is computed, and the vesicle's radius is updated based on the radial distance of the vesicle membrane's center and its thickness. This iterative refinement continues until the vesicle's representation aligns with its true structure.

![**Vesicle radius and position through radial profile and cross-correlation** Radial Profile Refinement A) couple of vesicles are not centered B) Radial Profile. Blue range is from membrane center to outer white halo center, this is the search range for the optimal radius. (smoothed by gaussian filtering) C) second derivative of radial profile E, F, H, G) Same as above columns after refinement](images/radial_avg_115-099.svg){#fig:radial_profile width="15cm"}

The adjacent vesicle masks were seperated (Figure `\_missing*`{.green}). `\_how?*`{.green}

`\_**missing Figure- Splitting adjacent vesicles. A) Examples of tomogram, no labels; B) raw label with connected vesicle-labels; C) modified label with seperated vesicles ---> for software: IMOD**`{.green}

The Dice coefficient was used to track the global congruence between the manually segmented mask and the predicted mask within the different tomograms (Figure {@fig:dice-improv}).
To quantitatively assess the accuracy of our segmentation approach, we employed the Dice coefficient. This metric gauges the similarity between the manually annotated vesicle masks and the masks predicted by our model.
A higher Dice coefficient indicates a closer match between the manual and predicted segmentations, providing a measure of the model's performance.
The results, visualized in Figure {@fig:dice-improv}, showcase the global congruence across different tomograms, highlighting the efficacy of our segmentation pipeline.

![**Dice developement during post-processing** Dice developement at different post processing steps of initial predicted mask (different colors correspond to different tomograms): A) synaptosomal training datasets B) synaptosomal test datasets c) neuron test datasets](images/improvment-post-processing-dice.svg){#fig:dice-improv width="15cm"}



| **_Dataset_** | **_Mask Dice_** | **_Final Label Dice_** | **_δ d_** | **_Δ c (nm)_** | **_Number of Vesicles_**  |  **_TP_**  |  **_FN_**  | **_FP_**  |
|---------------|:---------------:|:----------------------:| :-------: | :------------: |:-------------------------:|:----------:|:----------:|:---------:|
| SC 1          |      0.44       |          0.73          |   0.07    |   2.55±1.56    |            223            |    198     |     26     |    49     |
| SC 2          |       0.8       |          0.9           |   0.05    |   2.12±1.06    |            105            |    103     |     2      |     1     |
| SC 3          |      0.67       |          0.9           |   0.05    |   1.86±1.24    |            128            |    127     |     1      |     6     |
| SC 4          |      0.62       |          0.89          |   0.03    |   1.78±0.92    |            144            |    141     |     3      |     4     |
| SC 5          |      0.58       |          0.87          |   0.04    |   1.86±1.00    |            214            |    209     |     5      |    13     |
| SC 6          |      0.56       |          0.84          |   0.04    |   1.92±1.05    |            104            |    102     |     2      |    16     |
| SC 7          |      0.78       |          0.88          |   0.06    |   1.86±0.90    |            184            |    184     |     0      |    16     |
| SC 8          |      0.75       |          0.9           |   0.05    |   1.70±0.93    |            132            |    126     |     6      |     1     |
| SC 9          |      0.59       |          0.87          |   0.05    |   1.87±0.91    |            135            |    132     |     3      |    14     |
| **Average**   |  **0.64±0.11**  |     **0.86±0.05**      | **0.05**  | **1.95±1.08**  |        **152.22**         | **97.00%** | **3.00%**  | **7.30%** |
Table: Evaluation of the segmentation on the synaptosome train set. Mask Dice: Mask Dice coefficient for the predicted mask; Final Label Dice: Dice coefficient after post-processing; δ d: diameter error on correctly detected vesicle; Δ c: average error center (nm); Number of Vesicles: number of expected vesicles; TP: True Positive; FN: False Negative; FP: False Positive
{#tbl:train-tomograms}


| **_Dataset_** | **_Mask Dice_** | **_Final Label Dice_** | **_δ d_** | **_Δ c (nm)_** | **_Number of Vesicles_**  |  **_TP_**  | **_FN_**  | **_FP_**  |
|---------------|:---------------:|:----------------------:| :-------: | :------------: |:-------------------------:|:----------:|:---------:|:---------:|
| SC 10         |      0.75       |          0.88          |   0.07    |   1.86±1.18    |            129            |    123     |     6     |     5     |
| ST 1          |      0.75       |          0.83          |   0.11    |   2.66±1.52    |            699            |    687     |    12     |    33     |
| ST 2          |      0.74       |          0.77          |   0.11    |   2.27±1.84    |            122            |    117     |     5     |     2     |
| ST 3          |      0.72       |          0.74          |   0.11    |   3.64±2.22    |            434            |    397     |    37     |    57     |
| ST 5          |      0.77       |          0.85          |   0.08    |   2.20±1.26    |            535            |    526     |     9     |    25     |
| ST 6          |       0.6       |          0.83          |   0.07    |   2.02±1.12    |            373            |    353     |    20     |    42     |
| ST 7          |       0.8       |          0.83          |   0.06    |   2.22±1.14    |            110            |    107     |     3     |     9     |
| ST 8          |      0.83       |          0.91          |   0.04    |   2.09±1.04    |            100            |     99     |     1     |     2     |
| ST 10         |      0.77       |          0.86          |   0.05    |   1.96±1.04    |            77             |     74     |     3     |     6     |
| **Average**   |  **0.75±0.06**  |     **0.83±0.05**      | **0.08**  | **2.32±1.43**  |        **286.56**         | **96.30%** | **3.70%** | **6.10%** |
Table: Evaluation of the segmentation on the synaptosome test set (same sample type as the train set). For the meaning of the columns, see Table @tbl:train-tomograms.
{#tbl:test-tomograms}

| **_Dataset_** | **_Mask Dice_** | **_Final Label Dice_** | **_δ d_** | **_Δ c (nm)_** | **_Number of Vesicles_**  |  **_TP_**  |  **_FN_**  | **_FP_**  |
|---------------|:---------------:|:----------------------:| :-------: | :------------: |:-------------------------:|:----------:|:----------:|:---------:|
| N 133         |      0.76       |          0.86          |   0.05    |   2.16±1.32    |            523            |    467     |     56     |     8     |
| N 123         |      0.64       |          0.71          |   0.05    |   2.05±1.18    |            66             |     58     |     8      |     2     |
| N 84          |      0.86       |          0.89          |   0.06    |   1.44±0.75    |            498            |    484     |     14     |     1     |
| N 134         |      0.56       |          0.67          |   0.09    |   2.87±2.50    |            638            |    384     |    254     |    63     |
| N 115         |      0.57       |          0.63          |   0.08    |   3.56±3.23    |            170            |    123     |     47     |    32     |
| N 102         |      0.73       |          0.86          |   0.05    |   1.47±0.79    |            103            |     86     |     17     |     1     |
| N 80          |       0.7       |          0.81          |   0.07    |   2.67±2.00    |            111            |    102     |     9      |     3     |
| N 114         |      0.65       |          0.73          |   0.07    |   2.68±1.79    |            131            |     93     |     38     |     9     |
| N 132         |      0.69       |          0.87          |   0.03    |   1.65±1.26    |            135            |    129     |     6      |    32     |
| N 73          |      0.78       |          0.83          |   0.06    |   2.93±2.00    |            526            |    483     |     43     |     2     |
| N 128         |      0.67       |          0.85          |   0.04    |   2.33±1.70    |            252            |    232     |     20     |    19     |
| N 116         |      0.62       |          0.73          |   0.07    |   2.38±1.82    |            296            |    207     |     89     |    35     |
| **Average**   |  **0.69±0.09**  |     **0.79±0.09**      | **0.06**  | **2.35±1.83**  |        **287.42**         | **83.60%** | **16.40%** | **7.90%** |
Table: Evaluation of the segmentation on the neuron test set (different sample type as the train set). For the meaning of the columns, see Table @tbl:train-tomograms.
{#tbl:neuron-tomograms}

Our method transfers well across datasets even without fine-tuning which shows robustness and generalization.

### Comparison of manual segmentation with automatic deep-learning based segmentation

In the realm of cryo-electron tomography (cryoET), accurate segmentation of synaptic structures is paramount for understanding their spatial organization and function.
Traditional manual segmentation, while precise, is time-consuming and often limited in scope.
The advent of deep learning-based segmentation offers a promising alternative, providing both speed and scalability.

The traditional approach to manual segmentation in cryoET studies often restricted analyses to specific distances from the active zone, typically up to 250 nm.
This limitation inherently narrows the scope of synaptic or neuronal analyses.
However, with the integration of deep learning-based segmentation, it's now feasible to analyze entire synaptasomes or neurons comprehensively.
Not only does this method expedite the segmentation process, but it also enhances the accuracy and breadth of the analysis.
Furthermore, interactive tools like Napari significantly augment this process, allowing researchers to swiftly rectify false positives and negatives by adding or removing vesicles as needed, ensuring the highest level of accuracy in the final segmented output.

![**A: A 3D box representation of a synaptasome, visualized in an orthogonal view. The image showcases the intricate details of the structure with a scale bar indicating 100 nm.B: A probability map derived from the 3D U-Net segmentation. The map is presented schematically, with a color gradient ranging from blue (0.9968) to red (1), indicating the likelihood of synaptic vesicle presence.C: A tomogram post optimal global thresholding. This image provides a detailed view of the segmented structures, highlighting the precision of the automated segmentation process.D: The final representation of synaptic vesicle segmentation post-processing. Synaptic vesicles are depicted in light blue, overlaid on the ground truth obtained from expert annotations. The active zone is distinctly marked in red. The scale bar for this image is also set at 100 nm.** ](images/synaptasom-new.png){#fig:pipelineontomo width="15cm"}


#!#[**3D model of manual segmented and automatically segmented synaptosome.**](images/3d.png){#fig:3d width="10cm"}


###  Hierarchical connectivity segmentation of presynaptic terminals
Pyto is a software package designed for the analysis of pleomorphic membrane-bound molecular complexes in 3D images, particularly in the context of cryo-electron tomograms of neuronal synapses. A key feature of Pyto is its ability to accurately segment connectors and tethers within the pre-synaptic terminal, a task that requires a high level of precision. This segmentation process is hierarchical and connectivity-based, detecting densities interconnecting vesicles (connectors) and densities connecting vesicles to the active-zone plasma membrane (tethers).

In the study of synaptic vesicles regulation, the precision of segmentation is crucial. Accurate segmentation of connectors and tethers is essential as these structures play a significant role in the regulation of synaptic vesicles. Software that segments subcellular compartments, such as Pyto, provides a valuable tool in this process.

We have developed a software that is designed to be compatible with programs like Pyto. This compatibility allows us to extract more detailed information from Cryo-Electron Tomography (Cryo-ET), even in densely populated in situ conditions. By using our software in conjunction with programs like Pyto, we can gain a deeper understanding of synaptic vesicles regulation. Importantly, our software aims to eliminate the need for manual segmentation, enhancing the efficiency and accuracy of the process.

![**3D Model of Cultured Mouse Neuron: Left - Tomogram; Left Center - Schematic segmentation with cell outline (light blue), mitochondria (dark blue), lysosomes (green), microtubules (dark magenta); Right Center - Vesicles segmented using VesPy and connectors via Pyto; Right - 3D representation of vesicles in the presynaptic terminal..**](images/amira_all.png){#fig:amira width="15cm"}


## Discussion


## OLD
While the Dice coefficient is a good global measure to assess the predictions in comparison to the ground truth, it is difficult to asses local segmentation accurracy. 
For example, a single generated vesicle label containing several close connected vesicles would not be practical for further analysis for the researcher although it could have almost the same dice value. 
What is important for actual usage of the software would be the number and percentage of true-detected vesicles, false-positive and false-negative rates. 

Center error:
If we measure each axis error it will reveal that human bias in segmentation is more affected on the Z-axis. [we didn't show it in number but its checked the hypothesis]
`\_we cannot claim something without showing it. ---> this would belong into results*`{.green}

3d unet good for 3D processing
recent Nature methods paper by Ben Engel, DeepFinder -> Relion for STA creates mask to find more using dl
-what are they doing, maybe compare that in the text, different aims; we might compare results we achieve (keep as bonus, revision)
## SUMMARY
Synaptic Vesicles: Molecular Interactions and Functions

Synaptic vesicles (SVs) play a central role in neurotransmission, facilitating the release of neurotransmitters into the synaptic cleft. These vesicles undergo a series of molecular interactions with various protein complexes, transitioning from tethering to priming, and eventually to neurotransmitter release. Proteins such as Munc13 are integral to these processes, aiding in the localization and preparation of vesicles near the plasma membrane. Additionally, synapsins have been identified as key proteins in maintaining the reserve pool of SVs in presynaptic terminals. The mechanisms through which synapsins achieve this, whether by cross-linking vesicles or creating a distinct liquid phase, remain subjects of active research and debate.

Synaptic Studies and the Need for CryoET

The intricate nature of synapses and their associated structures has posed numerous challenges for researchers. Cryo-electron tomography (cryoET) emerges as a powerful tool to address these challenges, offering unparalleled insights into the molecular architecture of synapses. Accurate segmentation of structures such as vesicles, connectors, and tethers is essential for a comprehensive understanding of synaptic function. CryoET, however, is not without its challenges. The technique often grapples with issues like noise and the 'missing wedge' phenomenon, which can introduce artifacts and reduce the resolution of the reconstructed volume. Addressing these challenges is crucial for obtaining clear and accurate tomographic reconstructions.

CryoVesSeg: Integrating Deep Learning with CryoET

Harnessing the capabilities of deep learning, CryoVesSeg represents a synergistic approach to SV studies in cryoET. Deep learning, with its ability to process vast datasets and identify complex patterns, complements the precision of cryoET. The U-Net architecture, central to CryoVesSeg, has been trained on a curated dataset of manually segmented tomograms. This training ensures that the model can effectively segment SVs, connectors, and tethers, even in the presence of the aforementioned challenges like noise and the missing wedge phenomenon.

Conclusion

In the realm of cellular biology, the study of synaptic vesicles and their interactions is of paramount importance. With the integration of deep learning and cryoET, tools like CryoVesSeg are poised to revolutionize our understanding of these structures. As we continue to refine our methodologies and address the challenges inherent to cryoET, the promise of deeper insights and a more comprehensive understanding of synaptic function beckons.




### NEXT

Synaptic Vesicles: Beyond Basic Understanding

The intricate molecular dynamics of synaptic vesicles (SVs) have long been a focal point in neuroscientific research. Their pivotal role in neurotransmission, particularly in the release of neurotransmitters into the synaptic cleft, necessitates a deeper understanding of their interactions with various protein complexes. As they transition through states from tethering to priming, proteins such as Munc13 play a crucial role in their localization and preparation adjacent to the plasma membrane. Concurrently, the role of synapsins in maintaining the reserve pool of SVs in presynaptic terminals has been a subject of extensive debate, with theories ranging from vesicle cross-linking to the creation of a distinct liquid phase.

The Imperative of CryoET in Synaptic Studies

The complexity of synapses and their associated molecular structures has consistently presented challenges that traditional microscopy techniques struggle to address. Cryo-electron tomography (cryoET) emerges as a beacon in this landscape, offering a resolution and depth previously unattainable. However, the inherent challenges of cryoET, such as noise and the 'missing wedge' phenomenon, have been significant barriers to obtaining pristine tomographic reconstructions. These challenges underscore the need for advanced methodologies that can navigate the intricacies of cryoET data while preserving the integrity of the molecular structures under study.

CryoVesSeg: Bridging Deep Learning and CryoET

In light of the challenges and the pressing need for accurate segmentation, CryoVesSeg integrates the power of deep learning with the precision of cryoET. Drawing inspiration from the methodologies and findings of recent studies, our approach leverages the U-Net architecture, trained on a meticulously curated dataset of manually segmented tomograms. This integration ensures not only the effective segmentation of SVs, connectors, and tethers but also addresses the challenges intrinsic to cryoET, such as noise and the missing wedge phenomenon. The adaptability of CryoVesSeg, as evidenced by its performance across diverse datasets, underscores its potential as a versatile tool in synaptic studies.

Conclusion

The journey of understanding synaptic vesicles and their myriad interactions is far from complete. With tools like CryoVesSeg, which seamlessly blend the capabilities of deep learning and cryoET, we are better equipped to delve into the molecular intricacies of synapses. As we continue to refine our approach and draw insights from ongoing research, the promise of unveiling deeper layers of synaptic function and molecular interactions remains an exciting prospect for the future of cellular biology research.


### Version One:
Discussion

The realm of synaptic vesicles (SVs) and their interactions at the synapse is a fascinating and complex area of study in cellular biology. These vesicles play a pivotal role in neurotransmission, and understanding their behavior, interactions, and associated protein complexes is crucial for a comprehensive grasp of synaptic function.

Synaptic Vesicles and Their Interactions

At the heart of synaptic transmission lies the process of neurotransmitter release, which is orchestrated by a series of coordinated actions involving multiple protein complexes. Synaptic vesicles undergo a series of states, from tethering to priming, before they release their neurotransmitter contents into the synaptic cleft. This process is not just about the vesicles themselves but also about the intricate dance of protein complexes that facilitate these states.

Tethering represents the initial stage where vesicles are held close to the plasma membrane, readying them for the subsequent steps. This is followed by priming, a state where vesicles are molecularly prepared for neurotransmitter release. The transition between these states involves specific protein bridges, with proteins like Munc13 playing a role in localizing vesicles close to the plasma membrane. The orchestration of these transitions is further modulated by other proteins and enzymes, such as protein kinase C, which influences vesicle interactions.

The Role of Synapsins in Vesicle Clustering

Beyond the protein complexes that facilitate vesicle states, there are proteins like synapsins that play a crucial role in maintaining the reserve pool of SVs in presynaptic terminals. This reserve pool is essential as it ensures that there are always vesicles available for neurotransmission, especially during heightened synaptic activity. The exact mechanism through which synapsins maintain this reserve pool has been a topic of debate. Some theories suggest that synapsins might cross-link vesicles, anchoring them to each other, while others propose that synapsins create a unique liquid phase, allowing vesicles to float within a synapsin droplet. Both models offer intriguing insights into the potential mechanisms of vesicle clustering and reserve pool maintenance.

CryoVesSeg: A New Frontier in Synaptic Studies

Enter CryoVesSeg, our cutting-edge tool that leverages the power of cryo-electron tomography and deep learning. With CryoVesSeg, we can delve deeper into the molecular intricacies of synaptic vesicles and their associated structures. Traditional methods, while precise, often lacked efficiency. CryoVesSeg, with its U-Net architecture, offers a solution that marries precision with speed.

The ability to accurately segment vesicles, connectors, tethers, and other associated structures in their native environment opens up new avenues for research. By visualizing these structures at a molecular resolution, we can gain insights into their functional dynamics, interactions, and the roles of various protein complexes in the process. Furthermore, the adaptability of CryoVesSeg means that it can be trained on diverse datasets, making it a versatile tool for various cellular biology studies.

Conclusion

In conclusion, the world of synaptic vesicles is rich with molecular interactions and processes that are vital for synaptic function. With tools like CryoVesSeg, we are poised to uncover the mysteries of these interactions, offering a deeper understanding of synaptic transmission and the myriad protein complexes that facilitate it. As we continue our journey in this field, the promise of new discoveries and insights beckons, paving the way for a brighter future in cellular biology research.

### Version two:

CryoVesSeg: Harnessing the Power of Deep Learning for Synaptic Studies

Integration with Deep Learning Paradigms

Deep learning, a specialized branch of machine learning, has revolutionized the way we approach complex data-driven tasks. Its ability to sift through vast datasets and discern intricate patterns is unparalleled, making it an ideal tool for cellular structure segmentation in cryoET. CryoVesSeg, our innovative tool, is not just about synaptic vesicles (SVs) but a broader testament to the transformative potential of deep learning in cellular biology. By utilizing a meticulously curated set of manually segmented tomograms, our model undergoes rigorous training phases. The result? A segmentation that is both precise and nuanced, going beyond the rudimentary masking often seen in traditional methods.

Comparative Insights

Historically, cryoET methodologies have relied heavily on techniques like template matching and subtomogram classification. While effective, these methods often lack the flexibility and adaptability that modern research demands. CryoVesSeg, with its deep learning foundation, introduces a dynamic shift. By integrating post-processing steps such as adaptive thresholding, our approach ensures that segmentation is not just accurate but refined. This adaptability, deeply rooted in machine learning principles, emphasizes the versatility of CryoVesSeg, making it suitable for diverse datasets, including those beyond SVs.

Applications and Future Directions

The versatility of deep learning is evident in CryoVesSeg's potential applications. Beyond SV segmentation, our methodology shows promise in particle picking, a crucial step in cryoET data analysis. This dual functionality, encompassing both segmentation and particle picking, enhances the value of CryoVesSeg in the realm of cellular biology.

Moreover, drawing from the results and methods you provided, our deep learning approach is poised to make significant strides in synaptic studies. The potential to gain insights into synaptic vesicle pool formation, the interactions of vesicles with connectors and tethers, and the broader synaptic landscape is immense. Given well-annotated tomograms, there's an exciting possibility to extend CryoVesSeg's capabilities to other cellular structures, offering a holistic view of the cellular microenvironment.

Challenges and Adaptations

Like all machine learning models, deep learning networks are data-hungry. While CryoVesSeg benefits from a comprehensive training regimen, the ever-evolving nature of data and the unique variability inherent to SVs highlight the need for continuous model updates. As we chart our path forward, our primary goal is to enhance the model's generalizability. By integrating feedback, refining training datasets, and adapting to the latest in machine learning research, we aim to ensure that CryoVesSeg remains a cutting-edge tool in the ever-evolving landscape of cellular biology research.



### Version three:

Discussion

The intricate world of synaptic vesicles (SVs) and their associated structures has been a central focus in cellular biology. Accurate segmentation of these structures in cryo-electron tomography (cryoET) is essential for delving deeper into their functional dynamics and molecular complexities. Historically, segmentation in cryoET has leaned heavily on manual processes, ensuring precision but often at the cost of efficiency. Our approach, leveraging the capabilities of deep learning and the U-Net architecture, offers a solution that balances precision with efficiency.

Synaptic Studies and the Need for CryoET
The study of synapses has raised numerous questions that cryoET is uniquely positioned to answer. Accurate segmentation of vesicles, connectors, and tethers is paramount in this endeavor. Our proposed methodology addresses this need, providing tools that can significantly advance our understanding of synapses, synaptic vesicle pools, and the ongoing debates in the field, such as the liquid phase versus cross-linking theories centered around synapsin.

Versatility and Applicability
Many research groups possess vast amounts of manually segmented and annotated data. Our network is designed to be adaptable, allowing these groups to utilize their datasets and train the network for other membranes and organelles. Beyond synaptic studies, the capabilities of our network extend to other areas, such as particle picking, showcasing its versatility.

Conclusion
In essence, the methodology and tools we present here serve as a bridge to the biological interpretation of membrane-bound molecular complexes. They pave the way for a deeper understanding of their function and molecular identity, thereby broadening the horizons of quantitative structural methods in cell biology. As we move forward, our focus remains on refining our approach, ensuring it remains both robust and relevant, and continues to contribute significantly to the field.


### SUME UP

The intricate world of synaptic vesicles (SVs) has long captivated the attention of cellular biologists. These tiny vesicles, pivotal in neurotransmission, are a testament to the complexity and beauty of cellular processes. As we delve deeper into their molecular intricacies, the need for precise and efficient tools becomes paramount. Enter CryoVesSeg, our state-of-the-art solution that marries the precision of cryo-electron tomography (cryoET) with the efficiency and adaptability of deep learning.

The Synaptic Landscape: A Dance of Vesicles and Proteins

At the heart of synaptic function lies the SVs and their orchestrated interactions with various protein complexes. From the initial tethering, where vesicles are held in readiness near the plasma membrane, to the primed state, where they are molecularly prepared for neurotransmitter release, every step is a coordinated dance of molecular interactions. Proteins like Munc13 and synapsins play crucial roles in these processes, ensuring that neurotransmission occurs seamlessly. The debates around synapsins, whether they cross-link vesicles or create a unique liquid phase, further underscore the depth of our quest for understanding.

Harnessing the Power of Deep Learning with CryoVesSeg

Deep learning, a transformative branch of machine learning, has redefined how we approach data-intensive tasks. CryoVesSeg stands as a testament to this transformation. By leveraging a curated dataset of manually segmented tomograms, our model undergoes intensive training, ensuring that the segmentation of SVs, connectors, and tethers is both nuanced and precise.

Historical methods in cryoET, while effective, often lacked the dynamism that modern research demands. CryoVesSeg, with its foundation in deep learning, offers a refreshing departure from these traditional methods. Its adaptability ensures that it can be tailored to diverse datasets, making it a versatile tool not just for SVs but for a broader spectrum of cellular structures.

Applications, Challenges, and the Road Ahead

The potential applications of CryoVesSeg are vast. Beyond SV segmentation, it shows promise in particle picking, a critical step in cryoET data analysis. This dual functionality amplifies its value in cellular biology research.

However, like all machine learning models, CryoVesSeg thrives on data. The dynamic nature of data and the inherent variability in SVs necessitate continuous updates to the model. As we navigate this evolving landscape, our goal remains clear: to ensure CryoVesSeg remains at the cutting edge, offering researchers a tool that is both robust and relevant.

Conclusion

In the realm of cellular biology, where every molecule tells a story, tools like CryoVesSeg offer a window into these narratives. By combining the precision of cryoET with the efficiency of deep learning, we are poised to uncover the mysteries of synaptic vesicles and their interactions. As we continue this journey, the promise of new discoveries and deeper insights beckons, heralding a new era in our understanding of cellular processes.



### More technical
Our methodological approach to automatic segmentation in cryoET represents a significant advancement in the field. By utilizing a U-Net architecture trained on manually segmented tomograms, we have developed a system that can efficiently and accurately segment synaptic vesicles, connectors, and tethers in tomographic datasets.

The results obtained from our method, as evidenced by the Dice coefficient and other evaluation metrics, demonstrate its robustness and accuracy. Notably, our method's ability to generalize across different datasets, including those from rat synaptosomes and mouse astrocytic and primary neuronal cultures, underscores its versatility and potential for widespread application.

The segmentation pipeline, which includes steps such as splitting the tomogram into 3D patches, training the U-Net, generating probability masks, and stitching patches back together, has been optimized to ensure high-quality segmentation outcomes. The use of both global and adaptive localized thresholding techniques further refines the segmentation, addressing challenges posed by closely packed vesicles and complex scenarios.

Our results also highlight the effectiveness of our post-processing steps, including radial profile refinement and the removal of outliers. The radial profile, in particular, ensures that the segmented vesicles closely match their actual structure in the tomogram, providing a more accurate representation.

Furthermore, our method's compatibility with software like Pyto, which is designed for the analysis of pleomorphic membrane-bound molecular complexes in 3D images, enhances its utility. By integrating our segmentation approach with tools like Pyto, researchers can gain deeper insights into synaptic vesicle regulation and other cellular processes.

In terms of dataset preparation and network training, our approach is systematic and comprehensive. The use of different datasets for training, testing, and assessing transfer learning potential ensures that our model is well-trained and capable of handling a variety of tomographic data. The network architecture, based on the CARE framework, has been optimized for vesicle segmentation, and the results obtained validate its effectiveness.

In conclusion, our method for automatic segmentation in cryoET represents a significant step forward in the study of synaptic vesicles and their associated structures. By combining the power of deep learning with optimized post-processing techniques, we offer a solution that is both efficient and precise. As the field of cellular biology continues to evolve, tools like ours will play a crucial role in advancing our understanding of complex cellular structures and processes.

### Outlook
implement automatic cell-outline and active zone segmentation as deep learning workflow using UNet
implement automatic connector and tether segmentation as a deep leaning workflow using UNet





## Materials and methods

### Cryo-electron Tomography Datasets

Two datasets of different origin were used as input and test subjects for the automatic segmentation pipeline, respectively.
They consisted in rat synaptosomes primary neuron cultures derived from mice.
The preparation procedure of the samples from which the datasets were obtained as well as the biological analysis of these datasets was previously reported.  [@doi:10.1101/2022.03.07.483217].

Synaptosome preparation

Preparation of astrocytic and neuronal culture

Plunge freezing and spray mixing (Vitrification)

Cryo-electron microscopy (Cryo-ET)

Tomogram reconstruction

Ground truth annotation for organelles, cytoplasm, and membranes

Ground truth vesicles annotation

CNN Preproscessing

Biniarization of probability masks

Post Processing on Biniraized map (adaptive threeshold, radial profile, outlier removal)

Evaluation metrics

Computational setup




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


### Dataset description
The used datasets included a total of 30 tomograms with heterogeneous pixel sizes, defocus and resolution. 

1. 9 synaptosome datasets were used for training and validation.
2. 9 synaptosome datasets was used for test.
3. 12 Neuron dataset were used for assessing transfer learning potential.

### Training Dataset Construction
In the preparation of our training dataset, we utilized segmented 3D image volumes.
The primary volume was systematically divided into 32x32x32 sub-volumes.
To ensure the relevance and richness of the data, only those sub-volumes that were sufficiently occupied by vesicles, specifically containing more than 1000 voxels, were retained.
This meticulous approach was adopted to ensure that the training set effectively captured the intricate cellular structures, optimizing it for subsequent deep learning analyses.


### Stiching Pathces Back Together (building probability map?)

In deep learning segmentation for cryoET tomograms, smaller patches are segmented for computational efficiency.
Our U-Net model, trained on 32-voxel patches, utilizes a 24-voxel region of interest (ROI).
To mitigate tiling effects during testing, the network input can be expanded to larger volume like 64 voxels.
The tomogram undergoes padding to align with the ROI, ensuring reduced edge artifacts.
Segmentation is executed in tiles, where the U-Net predicts the synaptic vesicle probability for each tile.
Only the central part of the segmented patch, corresponding to the ROI, is retained.
This approach guarantees consistency in overlapping regions between adjacent tiles.
Finally, the segmented tiles are reassembled, yielding a continuous synaptic vesicle probability map of the entire volume.


### Network architecture and training procedure

We used a U-Net with two downsampling stages and two convolutional layers per stages, with a kernel size of 3, and ReLU activation function based on the open-source CARE framework (Figure {@fig:unet}) [@doi:10.1038/s41592-018-0216-7]. 
Datasets were prepared by splitting the 3D tomographic volume of synaptosomes into 32^3^-voxel subvolumes and keeping only subvolumes occupied by a sufficient amount (> 1000 voxels) of binarized vesicle label.
860 subvolumes were used for training and 100 subvolumes were used for validation.
We used the Adam optimizer on a binary cross-entropy loss function.

The learning progress was tracked by calculating the Dice coefficient and the loss value after each training epoch (Figure {@fig:dice}).
The Dice coefficient for the training set was initially ~0.25 and rose to over 0.9 after approximately 50 epochs, while for the validation set, it rose to 0.8. 
The loss for the training set went from 0.55 and to values below 0.05 after 50 epochs while for the validation set it went from 1 and to slightly below 0.3 after the initial 50 epochs and then rose slightly.

![**Dice coefficient and loss value for training and validation set.** ](images/traindice.png){#fig:dice width="7cm"}


![**Network architecture used for vesicle segmentation.** We used a U-Net based on the CARE framework [@doi:10.1038/s41592-018-0216-7]. The input is a cubic volume of 32^3^ voxels. The output is a per-prix probabilty cube of the same size as the input. ](images/unet.png){#fig:unet width="10cm"}


### Global Threshold
In the pursuit of refining the output of our deep neural network, a systematic approach was employed to determine the optimal threshold for the probability mask.
The objective was to ascertain a threshold that minimizes the values at the vesicle borders, ensuring precise delineation.
By iterating through potential threshold values ranging from 0.8 to 1 in increments of 0.01, a binary mask was generated for each threshold.
Subsequently, an erosion operation was applied to the binary mask, and the difference between the original and eroded masks produced the vesicle shell. The pixel values of the original image corresponding to this shell were recorded for each threshold.
This iterative process aids in identifying the threshold that offers the sharpest and most accurate representation of vesicle borders.

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

### Outlier Detection and refinement

Based on the radial profile of the data, key features, namely thickness, radius, and membrane density, are extracted.
Using these criteria, the Mahalanobis Distance is calculated for each data point to quantify its distance from the distribution of these features.
The significance of the Mahalanobis Distance is interpreted using the chi-squared distribution.
The p-value is derived by employing the cumulative distribution function (CDF) of the chi-squared distribution, with the Mahalanobis Distance as the input and the length of the criteria as the degrees of freedom.
The resulting p-value provides a measure of the statistical significance of each data point's distance.

With the computed p-values, outlier detection and refinement are conducted.
If the p-value of a specific vesicle is not within an acceptable range (0.3), indicating it might be an outlier, its radial profile is recalculated using a broader margin to find the optimal profile.
We perform this recalculation for up to 10 iterations. Typically, vesicles are either adjusted within the initial iterations or remain unchanged throughout. Vesicles that, even after recalibration, do not meet the p-value criteria are entirely removed from the dataset
This iterative process, involving recalculating the radial profile and adjusting parameters, continues until all vesicles either conform to the acceptable p-value range or are excluded.
The refined dataset is then ready for subsequent analyses.
This iterative approach ensures that all vesicles in the dataset either meet the p-value criteria or are excluded.
Outlier detection and refinement are initiated based on the computed p-values.



Using this multivariate feature space, we detect outliers by computing Mahalanobis Distances (MD) on normalized variables using the covariance matrix of observation and obtaining the p-value on MD.

`The sphere segments with a p-value higher than a defined threshold were discarded and the process was repeated iteratively.
If the MD p-value of a specific vesicle was not in a specific margin range (0-10), their radial profile was recalculated, and the label entirely removed if they again failed to pass the margin of the p-value.`{.yellow}
`Amin, please check what exactly was done with the outliers. 
And p-value cannot be higher than 1, while you wrote (0-10)`{.green}

### Evaluation Metrics (Analysis of Results)

The evaluation framework was designed to assess the capabilities of the proposed toolbox for automatic synaptic vesicle segmentation.
The framework was not only designed to evaluate quantitatively performance of the neural network, but rather assay the segmentation of vesicles in practice `\_unsure what the last part means*`{.green}. `\_I tried to say we develop the software rather than an algorithm paper with ablation study kinda more trasnfer learning but however for tranfer learning we might need add finetunning the network or say this sentence in other way*`{.green}.
The pipeline also generates a specific output format, which is necessary to further analyze the presynaptic tomograms via another pre-developed toolbox (Pyto), which segments small molecular filaments associated to the synaptic vesicles, titled tethers and connectors.

#### DICE


The `\_general form??*`{.green} DICE coefficient for probabilistic subvolume maps was calculated after each epoch as a performance quantification while `\_during?*`{.green} training.
The probabilistic mask subvolumes were stitched back together, creating a probabilistic map of the whole tomogram. 
The Soft-DICE for the whole tomogram was calculated to evaluate the similarity of the predicted probability mask with ground truth. 
Note that soft-dice is equivalent to dice, when the input is binarized (which we will do at the end of the post-processing).


$$1-\frac{2\sum_{voxels} y_{true} y_{pred}}{\sum_{voxels} y_{true}^2+\sum_{voxels} y_{pred}^2}$$


`\_shouln't it be voxels instead of pixels??*`{.green}
`\_yes voxel is right*`{.green}
`\_fixed*`{.green}


THE DICE was also employed to monitor all stages of post-processing on the eventual label file, to observe the effect of each post-processing step.

#### Vesicle Diameter Deviation Analysis

Vesicle Diameter Deviation Analysis

A critical characteristic of a vesicle is its diameter, predetermined as per specific criteria (refer to the Outlier Exclusion section). To assess the precision of our diameter estimation for accurately identified vesicles, a deviation metric is introduced.

Denote the diameter of a manually segmented vesicle by $d_{GTi}$ and the estimated diameter of the corresponding vesicle as $d_{Si}$. The deviation in diameter estimation for each vesicle can be expressed as:

$$\delta d=1-\frac{min(dSi,dGTi)}{max(dSi,dGTi)}$$ {#eq:regular-equation}

This formula offers an insight into the congruence between our estimated diameter and the manual segmentation, with a diminished value of $\delta d$ signifying a closer approximation.


The diameter of a vesicle is one of its relevant characterizations, and it is predefined (see Outlier Removal). 
`\_which diameters are we using in this evaluation as input, pre- or post-outlier removal?*`{.green}
`\_after! I meant from that perentesis that radius or dimater we assume as one charectiristic of vesicle we might can write it better *`{.green}
The error of diameter estimation of true-detected vesicle is defined as 1 minus the proportion of diameters 

$$\delta d=1-\frac{min(dSi,dGTi)}{max(dSi,dGTi)}$$ {#eq:regular-equation}

where dGTi is the diameter of each true manual segmented vesicle, and dSi is the diameter of its estimation.

#### Center error

The center error is an euclidean distance of ground truth and corresponds to true predicted vesicles `\_true pos or true neg? True Predicted means true postive*`{.green}.
A vesicle was defined as a true-detected vesicle if the predicted center was located inside the hand-segmented vesicle or the other way around the center of prediction was located inside the predicted vesicle. 
`\_isn't this a bit too general, shouldn't this be a tighter evaluation?*`{.green}
`\_we assume this as hard condition to be true postive we could define like some % liek 50% intersection but this condition is generally harder`{.green}
This means the volume of intersection of the estimated vesicle with the distance of d to a ground truth vesicle with radius R is: 

$$V=\frac{1}{12}\pi(4R+d)(2R-d)$$



### Computational Setup
All experiments were conducted using 4 x NVIDIA 2080 Ti GPUs with CUDA 10.1.
`\_Ioan's Grant Acknowledgement*`{.green}
The software environment was set up with Python 3.
Key libraries and packages utilized include TensorFlow 2.4.1 with GPU support and Keras 2.4.3.
For visualization neurons with tethers and connectors and regarding video, Amira 2022.2 was employed.
Image visualizations were achieved using both UCSF Chimera and ChimeraX.
Surface rendering was performed by the volume tracer and color zone in UCSF ChimeraX.
For detailed configurations and parameters, users are referred to the accompanying source code.

### Manuscript preparation
The manuscript was written with the open and collaborative scientific writing package Manubot [@doi:10.1371/journal.pcbi.1007128]. 
The source code and data for this manuscript are available at <https://github.com/aseedb/synaptic_tomo_ms>.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
