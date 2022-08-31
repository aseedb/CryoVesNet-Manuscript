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
date-meta: '2022-08-31'
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
  <meta name="dc.title" content="Deep-learning based automatic segmentation of vesicles in cryo-electron tomograms" />
  <meta name="citation_title" content="Deep-learning based automatic segmentation of vesicles in cryo-electron tomograms" />
  <meta property="og:title" content="Deep-learning based automatic segmentation of vesicles in cryo-electron tomograms" />
  <meta property="twitter:title" content="Deep-learning based automatic segmentation of vesicles in cryo-electron tomograms" />
  <meta name="dc.date" content="2022-08-31" />
  <meta name="citation_publication_date" content="2022-08-31" />
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
  <link rel="alternate" type="text/html" href="https://aseedb.github.io/deep-prepyto-paper/v/c04a3266911cf1a22ddd43b90164429e81407a5d/" />
  <meta name="manubot_html_url_versioned" content="https://aseedb.github.io/deep-prepyto-paper/v/c04a3266911cf1a22ddd43b90164429e81407a5d/" />
  <meta name="manubot_pdf_url_versioned" content="https://aseedb.github.io/deep-prepyto-paper/v/c04a3266911cf1a22ddd43b90164429e81407a5d/manuscript.pdf" />
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
([permalink](https://aseedb.github.io/deep-prepyto-paper/v/c04a3266911cf1a22ddd43b90164429e81407a5d/))
was automatically generated
from [aseedb/deep-prepyto-paper@c04a326](https://github.com/aseedb/deep-prepyto-paper/tree/c04a3266911cf1a22ddd43b90164429e81407a5d)
on August 31, 2022.
</em></small>

## Authors



+ **Amin Khosrozadeh**^[\*](#equal_contribution)^<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [ameen-khosrowzadeh](https://github.com/ameen-khosrowzadeh)<br>
  <small>
     Institute of Anatomy, University of Bern, Bern, Switzerland; Graduate School for Cellular and Biomedical Sciences, University of Bern
     · Funded by Grant XXXXXXXX
  </small>

+ **Raphaela Seeger**^[\*](#equal_contribution)^<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [elatella](https://github.com/elatella)<br>
  <small>
     Institute of Anatomy, University of Bern, Bern, Switzerland; Graduate School for Cellular and Biomedical Sciences, University of Bern
  </small>

+ **Julika Radecke**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0002-5815-5537](https://orcid.org/0000-0002-5815-5537)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [julikaradecke](https://github.com/julikaradecke)<br>
  <small>
     Institute of Anatomy, University of Bern, Bern, Switzerland; Department of Neuroscience, Faculty of Health and Medical Science , 2200 Copenhagen N, University of Copenhagen, Copenhagen, Denmark; Diamond Light Source Ltd, Didcot, Oxfordshire, United Kingdom
  </small>

+ **Guillaume Witz**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0003-1562-4265](https://orcid.org/0000-0003-1562-4265)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [guiwitz](https://github.com/guiwitz)<br>
  <small>
     Science IT Service, University of Bern, Bern, Switzerland; Microscopy Imaging Center, University of Bern, Bern, Switzerland
  </small>

+ **Jakob B. Sørensen**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0001-5465-3769](https://orcid.org/0000-0001-5465-3769)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [JBSorensen](https://github.com/JBSorensen)<br>
  <small>
     Department of Neuroscience, University of Copenhagen, Blegdamsvej 3B, 2200 Copenhagen N, Denmark
     · Funded by Novo Nordisk Fonden, NNF17OC0028516.; Carlsbergfondet, CF17-0875; Independent Research Fond Denmark, 8020-00228A; Lundbeckfonden, R277-2018-802
  </small>

+ **Benoît Zuber**^[✉](#correspondence)^<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0001-7725-5579](https://orcid.org/0000-0001-7725-5579)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [aseedb](https://github.com/aseedb)<br>
  <small>
     Institute of Anatomy, University of Bern, Bern, Switzerland
     · Funded by Swiss National Science Foundation, 179520; ERA-NET NEURON, NEURON-119
  </small>


::: {#correspondence}
✉ Address correspondence to <benoit.zuber@ana.unibe.ch>.
:::
::: {#equal_contribution}
\* These authors contributed equally.
:::


## Abstract {.page_break_before}

Cryo-electron Tomography (Cryo-ET) has the potential to reveal cell structure down to atomic resolution.
Nevertheless, cellular cryo-ET data is often highly complex and visualization, as well as quantification, of subcellular structures require image segmentation.
Due to a relatively high level of noise and to anisotropic resolution in cryo-ET data, automatic segmentation based on classical computer vision approaches usually does not perform satisfyingly.
For this reason, cryo-ET researchers have mostly performed manual segmentation.

Communication between neurons rely on neurotransmitter-filled synaptic vesicle (SV) exocytosis.
Recruitment of SVs to the plasma membrane is an important means of regulating exocytosis and is influenced by interactions between SVs.
Cryo-ET study of the spatial organization of SVs and of their interconnections allows a better understanding of the mechanisms of exocytosis regulation.
To obtain a faithful representation of SV connectivity state, an absolutely vital prerequisite is an extremely accurate SV segmentation.
Hundreds to thousands of SVs are present in a typical synapse, and their manual segmentation is a burden.
Typically accurately segmenting all SVs in one synapse takes between 3 to 8 days.
This segmentation process has been widely recognized as a bottleneck by the community.

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

The synapse is the functional cellular contact at which information is transmitted from a neuron to another. 
The former neuron is called presynaptic and the latter is postsynaptic. 
In most cases, the signal is transmitted by the release of neurotransmitters into the intercellular space.
Neurotransmitters are stored in SVs and are released following the fusion of a vesicle with the presynaptic plasma membrane.
A synapse contains hundreds of SVs and their mobility and recruitability for neurotransmitter release depends on inter-vesicle interactions through so-called connector structures [@doi:10.1083/jcb.200908082 ]. 
The characterization of these interactions can be performed automatically with the pyto software, which implements a hierarchical connectivity approach to detect and annotate connectors [@doi:10.1016/j.jsb.2016.10.004]. For accurate connector segmentation, an exceptionally precise segmentation of SVs is prerequisite.
To date, this SV segmentation has been achieved manually, but given the massive number of SVs per dataset, it is an extremely time-consuming process. 
Typically, one person spends 3 to 8 working days to segment a single dataset.
Attempts to perform this task automatically based on classical computer vision algorithms have not yielded sufficiently accurate performance [@doi:10.1016/j.jsb.2014.02.015].  
To alleviate this situation, we considered applying deep learning methods.

Convolutional neural networks (CNN) have been successfully employed to segment cryo-ET data [@doi:10.1038/nmeth.4405]. 
Although entirely satisfying for visualization purposes, this approach has not met the requirements of pyto.
A recent publication described accurate SV segmentation of transmission electron microscopy images using CNN, but it is limited to 2-dimensional images of resin-embedded synapses [@doi:10.1523/ENEURO.0400-20.2021]. 
For our use-case, a common issue is that the input data consists of 2-dimensional images.
In the first study, cryo-ET data are decomposed in individual 2-dimensional slices, which are handed as seperate input to the CNN. 
The independent output prediction images are re-assembled in a 3-dimensional stack.[@doi:10.1038/nmeth.4405]
As discussed above, membranes oriented approximately parallel to the plane of the 2-dimensional tomographic images are not resolved.
In the absence of contextual knowledge of the other 2-dimensional images, the CNN fails to segment these regions of the vesicles.
Hence, spherical vesicles appear open, whereas we expect closed spherical objects.
To overcome this limitation, we used a U-Net CNN that takes 3-dimensional images as input.
U-Net architecture has been introduced in 2015 by Ronenberger et al. [@arxiv:1505.04597].
It consists of a contracting path, typical of CNN, and a symmetric expanding path. 
At each expansion step, the correspondingly cropped feature map of the contracting path is concatenated. 
The contracting path captures context, while the expanding path coupled with concatenation enables precise localization.
The U-Net architecture was developed to achieve a fast and accurate segmentation of biomedical two-dimensional images, with the requirement of only a small fraction of training data in comparison to previous CNNs.
*might be redundant*
Arranging the sequence of convolution layers in the contraction path along with skip connection and concatenating into the expansion path bring significant privilege for medical and semantic segmentation.
Concurrent with the appearance of 3D convolutional neural networks (CNN) three-dimensional form of U-Net was also developed for volumetric image analysis.

It was then extended to segment 3-dimensional biomedical images (3D U-Net) [@arxiv:1606.06650].
Weigert et al. [@doi:10.1038/s41592-018-0216-7] implemented a U-Net for content-aware restoration (CARE) of 3-dimensional fluorescence microscopy datasets. They showed that it can restore information from anisotropic and very noisy datasets.

We implemented a 3D U-Net based on CARE building blocks and trained it with manually segmented datasets. 
This method provided good accuracy and was only slightly affected by the missing wedge artifact. 
Nevertheless, it was not quite sufficient for our downstream pyto analysis.
Hence, we developed a post-processing method, which transforms the segmented objects into spheres and refines their radius and center location.
This leads to a substantial accuracy improvement, which are reflected in better pyto performance.
Additionally, we designed a multivariate ranking procedure, highlighting possibly wrongly segmented SVs. 
We also introduce a semi-automatic method to very quickly fix wrongly segmented and missed SVs.

Although our set of procedures was developed with the use case of SV segmentation in mind, it can be used to segment any other types of biological spherical vesicles, such as transport vesicles, secretory vesicles, endocytic vesicles, and extracellular vesicles.


This manuscript is a template (aka "rootstock") for [Manubot](https://manubot.org/ "Manubot"), a tool for writing scholarly manuscripts.
Use this template as a starting point for your manuscript.

The rest of this document is a full list of formatting elements/features supported by Manubot.
Compare the input (`.md` files in the `/content` directory) to the output you see below.

## Basic formatting

**Bold** __text__

[Semi-bold text]{.semibold}

[Centered text]{.center}

[Right-aligned text]{.right}

*Italic* _text_

Combined *italics and __bold__*

~~Strikethrough~~

1. Ordered list item
2. Ordered list item
    a. Sub-item
    b. Sub-item
        i. Sub-sub-item
3. Ordered list item
    a. Sub-item

- List item
- List item
- List item

subscript: H~2~O is a liquid

superscript: 2^10^ is 1024.

[unicode superscripts](https://www.google.com/search?q=superscript+generator)⁰¹²³⁴⁵⁶⁷⁸⁹

[unicode subscripts](https://www.google.com/search?q=superscript+generator)₀₁₂₃₄₅₆₇₈₉

A long paragraph of text.
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Putting each sentence on its own line has numerous benefits with regard to [editing](https://asciidoctor.org/docs/asciidoc-recommended-practices/#one-sentence-per-line) and [version control](https://rhodesmill.org/brandon/2012/one-sentence-per-line/).

Line break without starting a new paragraph by putting  
two spaces at end of line.

## Document organization

Document section headings:

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

### A heading centered on its own printed page{.center .page_center}

<!-- an arbitrary comment. visible in input, but not visible in output. -->

Horizontal rule:

---

`Heading 1`'s are recommended to be reserved for the title of the manuscript.

`Heading 2`'s are recommended for broad sections such as *Abstract*, *Methods*, *Conclusion*, etc.

`Heading 3`'s and `Heading 4`'s are recommended for sub-sections.

## Links

Bare URL link: <https://manubot.org>

[Long link with lots of words and stuff and junk and bleep and blah and stuff and other stuff and more stuff yeah](https://manubot.org)

[Link with text](https://manubot.org)

[Link with hover text](https://manubot.org "Manubot Homepage")

[Link by reference][manubot homepage]

[Manubot Homepage]: https://manubot.org

## Citations

Citation by DOI [@doi:10.7554/eLife.32822].

Citation by PubMed Central ID [@pmc:PMC6103790].

Citation by PubMed ID [@pubmed:30718888].

Citation by Wikidata ID [@wikidata:Q56458321].

Citation by ISBN [@isbn:9780262517638].

Citation by URL [@{https://greenelab.github.io/meta-review/}].

Citation by alias [@deep-review].

Multiple citations can be put inside the same set of brackets [@doi:10.7554/eLife.32822; @deep-review; @isbn:9780262517638].
Manubot plugins provide easier, more convenient visualization of and navigation between citations [@doi:10.1371/journal.pcbi.1007128; @pubmed:30718888; @pmc:PMC6103790; @deep-review].

Citation tags (i.e. aliases) can be defined in their own paragraphs using Markdown's reference link syntax:

[@deep-review]: doi:10.1098/rsif.2017.0387

## Referencing figures, tables, equations

Figure @fig:square-image

Figure @fig:wide-image

Figure @fig:tall-image

Figure @fig:vector-image

Table @tbl:bowling-scores

Equation @eq:regular-equation

Equation @eq:long-equation

## Quotes and code

> Quoted text

> Quoted block of text
>
> Two roads diverged in a wood, and I—  
> I took the one less traveled by,  
> And that has made all the difference.

Code `in the middle` of normal text, aka `inline code`.

Code block with Python syntax highlighting:

```python
from manubot.cite.doi import expand_short_doi

def test_expand_short_doi():
    doi = expand_short_doi("10/c3bp")
    # a string too long to fit within page:
    assert doi == "10.25313/2524-2695-2018-3-vliyanie-enhansera-copia-i-insulyatora-gypsy-na-sintez-ernk-modifikatsii-hromatina-i-svyazyvanie-insulyatornyh-belkov-vtransfetsirovannyh-geneticheskih-konstruktsiyah"
```

Code block with no syntax highlighting:

```
Exporting HTML manuscript
Exporting DOCX manuscript
Exporting PDF manuscript
```

## Figures

![
**A square image at actual size and with a bottom caption.**
Loaded from the latest version of image on GitHub.
](https://github.com/manubot/resources/raw/15493970f8882fce22bef829619d3fb37a613ba5/test/square.png "Square image"){#fig:square-image}

![
**An image too wide to fit within page at full size.**
Loaded from a specific (hashed) version of the image on GitHub.
](https://github.com/manubot/resources/raw/15493970f8882fce22bef829619d3fb37a613ba5/test/wide.png "Wide image"){#fig:wide-image}

![
**A tall image with a specified height.**
Loaded from a specific (hashed) version of the image on GitHub.
](https://github.com/manubot/resources/raw/15493970f8882fce22bef829619d3fb37a613ba5/test/tall.png "Tall image"){#fig:tall-image height=3in}

![
**A vector `.svg` image loaded from GitHub.**
The parameter `sanitize=true` is necessary to properly load SVGs hosted via GitHub URLs.
White background specified to serve as a backdrop for transparent sections of the image.
](https://raw.githubusercontent.com/manubot/resources/main/test/vector.svg?sanitize=true "Vector image"){#fig:vector-image height=2.5in .white}

## Tables

| *Bowling Scores* | Jane          | John          | Alice         | Bob           |
|:-----------------|:-------------:|:-------------:|:-------------:|:-------------:|
| Game 1 | 150 | 187 | 210 | 105 |
| Game 2 |  98 | 202 | 197 | 102 |
| Game 3 | 123 | 180 | 238 | 134 |

Table: A table with a top caption and specified relative column widths.
{#tbl:bowling-scores}

|         | Digits 1-33                        | Digits 34-66                      | Digits 67-99                      | Ref.                                                        |
|:--------|:-----------------------------------|:----------------------------------|:----------------------------------|:------------------------------------------------------------|
| pi      | 3.14159265358979323846264338327950 | 288419716939937510582097494459230 | 781640628620899862803482534211706 | [`piday.org`](https://www.piday.org/million/)               |
| e       | 2.71828182845904523536028747135266 | 249775724709369995957496696762772 | 407663035354759457138217852516642 | [`nasa.gov`](https://apod.nasa.gov/htmltest/gifcity/e.2mil) |

Table: A table too wide to fit within page.
{#tbl:constant-digits}

|          | **Colors** <!-- $colspan="2" --> |                      |
|:--------:|:--------------------------------:|:--------------------:|
| **Size** | **Text Color**                   | **Background Color** |
| big      | blue                             | orange               |
| small    | black                            | white                |

Table: A table with merged cells using the `attributes` plugin.
{#tbl: merged-cells}

## Equations

A LaTeX equation:

$$\int_0^\infty e^{-x^2} dx=\frac{\sqrt{\pi}}{2}$$ {#eq:regular-equation}

An equation too long to fit within page:

$$x = a + b + c + d + e + f + g + h + i + j + k + l + m + n + o + p + q + r + s + t + u + v + w + x + y + z + 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9$$ {#eq:long-equation}

## Special

<i class="fas fa-exclamation-triangle"></i> [WARNING]{.semibold} _The following features are only supported and intended for `.html` and `.pdf` exports._
_Journals are not likely to support them, and they may not display correctly when converted to other formats such as `.docx`._

[Link styled as a button](https://manubot.org "Manubot Homepage"){.button}

Adding arbitrary HTML attributes to an element using Pandoc's attribute syntax:

::: {#some_id_1 .some_class style="background: #ad1457; color: white; margin-left: 40px;" title="a paragraph of text" data-color="white" disabled="true"}
Manubot Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot.
Manubot Manubot.
Manubot.
:::

Adding arbitrary HTML attributes to an element with the Manubot `attributes` plugin (more flexible than Pandoc's method in terms of which elements you can add attributes to):

Manubot Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot.
Manubot Manubot.
Manubot.
<!-- $id="element_id" class="some_class" $style="color: #ad1457; margin-left: 40px;" $disabled="true" $title="a paragraph of text" $data-color="red" -->

Available background colors for text, images, code, banners, etc:  

`white`{.white}
`lightgrey`{.lightgrey}
`grey`{.grey}
`darkgrey`{.darkgrey}
`black`{.black}
`lightred`{.lightred}
`lightyellow`{.lightyellow}
`lightgreen`{.lightgreen}
`lightblue`{.lightblue}
`lightpurple`{.lightpurple}
`red`{.red}
`orange`{.orange}
`yellow`{.yellow}
`green`{.green}
`blue`{.blue}
`purple`{.purple}

Using the [Font Awesome](https://fontawesome.com/) icon set:

<!-- include the Font Awesome library, per: https://fontawesome.com/start -->
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.2/css/all.css">

<i class="fas fa-check"></i> <i class="fas fa-question"></i> <i class="fas fa-star"></i> <i class="fas fa-bell"></i> <i class="fas fa-times-circle"></i> <i class="fas fa-ellipsis-h"></i>

[
<i class="fas fa-scroll fa-lg"></i> **Light Grey Banner**<br>
useful for *general information* - [manubot.org](https://manubot.org/)
]{.banner .lightgrey}

[
<i class="fas fa-info-circle fa-lg"></i> **Blue Banner**<br>
useful for *important information* - [manubot.org](https://manubot.org/)
]{.banner .lightblue}

[
<i class="fas fa-ban fa-lg"></i> **Light Red Banner**<br>
useful for *warnings* - [manubot.org](https://manubot.org/)
]{.banner .lightred}


## Results

Cellular cryo-electron tomography is an upcoming field with a multitude of possible applications.
The manual segmentation of the cellular features is a major bottleneck of this method.
When segmenting cryo-electron tomograms from presynaptic terminals, the manual segmentation of synaptic vesicles is one of the most time-intensive steps.
Synaptic vesicles constitute a large, homogeneous group, constituting a large training set for deep learning applications.
Therefore, we decided to initially develop the automatic segmentation for synaptic vesicles.
The used tomograms were previously manually segmented with IMOD, these manual segmentations were further treated as the ground truth [@doi:10.1006/jsbi.1996.0013].
`\_maybe add this somewhere else: In a next step, filaments connecting the synaptic vesicles with each other (connectors) and to the active zone (AZ) were automatically segmented with the algorithm application Pyto [@doi:10.1016/j.jsb.2016.10.004].*`{.green}

The U-Net neural network was used to train its mask prediction on a training set of 9 tomograms containing untreated synaptosomes.
The learning progress was tracked by calculating the Dice coefficient and the loss value after each training epoch (Figure {@fig:dice}).
The dice value for the training dataset started at a value of ~0.25 and rose to a value of over 0.9 after the initial 50 epoches. 
The loss value of the training dataset had an initial value of over 0.55 and declined to values below 0.05 after the initial 50 epochs and further striving towards 0 in the following depicted epochs.
`\_Validation Dice and loss from treated synaptosome dataset?*`
The validation dataset showed much more fluctuations during both validation and loss progression.
The dice value for the validation dataset started at a value of ~0.27 and rose to an average value of over 0.75 after the initial 50 epoches. 
The loss value of the validation dataset had an initial value 1 and declined to values below 0.3 after the initial 50 epochs.

![**Dice coefficient and loss value for training and validation set.** `\_legend in figure should say "Training Dice"*`{.green} ](images/blinddice.png){#fig:dice width="7cm"}

`\_---->add figures of local measurements such as diameter or center error as an extra figure, why else listed in M&M??"*`{.green}

After the neural network is trained to recognize the synaptic vesicles with a sufficient probability, the trained U-Net was implemented into a pipeline. 
The pipeline for automatic segmentation of vesicles consists of two major parts: the neural network consisting of a U-Net neural network, and the post-processing steps refining the labels generated by the U-Net (Figure {@fig:pipeline}).
The three batches of tomograms (synaptosome control, synaptosome treatment and neuron) were each handed to the pipeline. 

![**Pipeline of automatic segmentation.** a) tomograms b) patchify the tomograms into 3D patches c) Segmentation Network/ trained U-Net d) probability masks e) stitching patches back together f) thresholding g) adaptive localized thresholding h) outlier removal i) radial profile](images/pipeline.svg){#fig:pipeline width="15cm"}

Each tomogram is split into patches of 32x32x32 `\_unit?*`{.green}.
These patches are the fed into the trained U-Net, which outputs a probability mask for those patches.
To obtain a complete probability mask, the patches are stitched back together.
The probability mask is further refined by applying global and adaptive localized thresholding steps (Figure {@fig:pipeline}, Figure {@fig:tom}).

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

Two datasets of different origin were used as input and test subjects for the automatic segmentation pipeline, rat synaptosomes as well as astrocytic and neural cell cultures derived from mice.
Both datasets have been previously analyzed [@doi:10.1101/2022.03.07.483217].

#### Rat synaptosomes

The preparation of the rat synaptosomes were previously described [@doi:10.1038/nprot.2008.171].
After the purification, the synaptosomes were incubated for 30 min at room temperature.
1.3mM CaCl_2_ and 10 nm gold fiducials were added (gold fiducials, #s10110/8. AURION Immuno Gold Reagents & Accessories. Wageningen, The Neatherlands).
The synaptosome solution was applied to a 200-mesh lacey finder carbon film grid (#AGS166-H2. Agar Scientific. Elektron Technology UK Ltd. Stansted, UK).
Manual blotting was used to remove excess liquid with a filter paper.
Thereafter, the grid was immediately plunge frozen in liquid ethane using a home built plunge freezer controlled with a LabView script (National Instruments Corporation. Mopac Expwy Austin, TX, USA).
The grids coated with rat synaptosomes were mounted in a cryo-holder (Gatan, Pleasonton, CA, USA) and transferred to a Tecnai F20 (FEI, Eindhoven, The Netherlands) which was set to low dose conditions, operated at 200 kV, and equipped with a field emission gun.
Images were recorded with a 2k x 2k CCD camera (Gatan) mounted after a GIF Tridiem post-column filter (Gatan) operated in zero-loss mode.
The sample was kept at about -180 °C.
Tilt series were acquired using SerialEM [@doi:10.1016/j.jsb.2005.07.007] for automated acquisition recorded typically from -50° to 50° with a 2° angular increment and an unbinned pixel size of 0.75 or 1.2 nm.
Due to sample thickness (400-700 nm), tomograms were usually not recorded with higher tilt angles.
Defocus was set between -8 to -12 µm and the total electron dose used was about 80-100 e^-^/Å^2^.
Some tomograms were acquired at a Titan Krios equipped with a K2 direct electron detector (Gatan) without energy filter.
The K2 camera was operated in super-resolution counting mode and between 8-40 frames per tilt angle were taken.
Tilt series were acquired using the Latitude software (Gatan) for automated acquisition recorded typically from -60° to 60° with a 2° angular increment and an unbinned pixel size of 0.6 nm.
Defocus was set between -8 to -12 µm and the total electron dose used was about 80-100 e^-^/Å^2^.
Before image processing the frames at each tilt angle, frames were aligned and averaged in 2dx MC_Automator [@doi:10.1016/j.jsb.2014.03.016] with motioncor [@doi:10.1038/nmeth.2472].
3D reconstruction was done in IMOD [@doi:10.1006/jsbi.1996.0013].
The alignments were done using the automated fiducial tracking function and the 3D reconstructions were done using the weighted back projection followed by a nonlinear anisotropic diffusion (NAD) filtering.

#### Astrocytic and neuronal mouse culture

The preparation of astrocytic and neuronal culture has been published before [@doi:10.3791/50783].
After 12 to 14 days of incubation, grids with mouse neurons were plunge frozen with a Vitrobot (Thermofisher Scientific, Mark IV) with a blot time of 3 s and a blot force of -10.
Wait time and drain time were not used. 
Humidity was set to 100% at 4 °C. 
4 µl undiluted 10 nm BSA gold tracer (Aurion) was added directly onto the grid prior to plunge freezing.
Cultured mouse neurons tilt series were acquired at a Titan Krios, equipped with a Falcon 3 direct electron detector (Thermofisher Scientific) without energy filter.
The Falcon camera was operated in linear mode.
Tilt series were acquired using the TEM Tomography software (TFS) for automated acquisition, recorded typically from -60° to 60° with a 2° angular increment and an unbinned pixel size of 0.37 nm.
Defocus was set between -6 to -10 µm and the total electron dose used was about 80-100 e^-^/Å^2^.
Tomogram reconstruction was done in the same way as for the synaptosome datasets.

### Manual segmentation procedures

Manual segmentation of SVs, mitochondria, and the active zone PM was done in IMOD (Figure S4A&B).
The boundary marked the region to be analyzed by Pyto [@doi:10.1016/j.jsb.2016.10.004].
The analysis by Pyto was essentially the same as described previously [@doi:10.1083/jcb.200908082; @doi:10.1016/j.jsb.2016.10.004].

In short, the segmented area is divided in 1 voxel thick layers parallel to the active zone for distance calculations.
A hierarchical connectivity segmentation detects densities interconnecting vesicles (so-called connectors) and densities connecting vesicles to the active zone PM (so-called tethers) (Figure `\_add figure number*`{.green}).
Distance calculations are done with the center of the vesicle.
Mainly default settings were used.
The segmentation procedure is conservative and tends to miss some tethers and connectors because of noise.
Consequently, the numbers of tethers and connectors should not be considered as absolute values, but rather to compare experimental groups.
As it was done before, an upper limit was set between 2100 and 3200 nm^3^ on segment volume.
The tomograms that were used for this analysis were binned by a factor of 2 to 3, resulting in voxel sizes between 2.1 and 2.4 nm.

### Pre-processing of manual segmentation outputs from IMOD for further use (jupyter notebook pre-pyto)



### Description of Machine Learning 

This experiment was conducted on a workstation with an AMD Ryzen Threadripper 3970X CPU with an NVIDIA GeForce RTX 2080 Ti GPU. 
All the framework has been implemented in Python using the Keras library (2.4.3) and TensorFlow (2.4.1). 
The workflow includes a GUI based on a multidimensional image viewer, Napari (0.4.15), enabling the user to add and remove vesicles.
`\_any other packages required?*`{.green}


The used datasets included a total of 30 tomograms with heterogeneous pixel sizes, defocus and resolution.

1. All 9 tomograms Dataset: partially segmented and used for training (Synaptosome)
2. A single tomogram with the exactly same setup and sample preparation like the train dataset
3. 8 Synaptosome tomograms Dataset:  with ground truth (with an exceeding treatment on the samples)
4. 12 Neuron fully segmented tomograms Dataset: with completely different sample preparation and microscope setup

`\_this is not good place to talk about evalution *`{.green}


#### Deep Model Training with a 3D U-Net

##### Create an Input Voxel Patch

The training set was prepared by splitting the 3D tomographic volume into 32x32x32 `\_voxels??*`{.green} sub volumes and keeping only volumes occupied by a sufficient amount (> 1000 voxels) of binarized vesicle labels.
The obtained sub volumes were randomly divided into ten subsets of the training set, this method is termed k-fold cross-validation in the field of machine learning. 
`\_this is a wrong statment we dont do cross validation just split(fold) data *`{.green}
All of these subsets or "folds" were used as training sets, as an entirely separate set of tomographic subvolumes was used for validation, to avoid overfitting.

`\_are the folds overlapping? are the tomograms normalized any further than the NAD from previous segmentation before feeding it to the deeplearning model? add image from odt??, the 2D slices of the subset are supposed to be 32x32x32, but seem to have a different size... padding?? ---> results*`{.green}

##### 3D U-Net architecture

The previously prepared subsets are fed into the 3D U-Net in batches of 50. `\_cite Ronneberger, what was changed compared to the original U-Net, is there a better publication to cite?*`{.green}
These were passed through the U-Net in a total of 200 epochs.
Batch normalization was applied before Rectified Linear Unit (ReLU) activation `\_was it? cite Ioffe & Szegedy, maybe? [@doi:10.48550/arXiv.1502.03167]*`{.green}.

`\_we do not use deconv layers, instead we upsample (by repeating the data) and then apply a convolution.*`{.green}
`\_as far as I know, nobody uses analysis/expantion path, encoder/decoder is the common and correct term.*`{.green}
The 3D U-Net architecture is composed of a contracting or analysis path!! (convolutional layers), and an expanding or synthesis path (deconvolutional!! layers) (Figure {@fig:unet}).
`\_did we wrote our own U-Net or do we need to quote someones github for the original framework*`{.green}
`\_we used CSBDeep for Convoultion blocks Benoit mentioned it in the introdction we can bring it here but github licence is BSD 3-Clause License whihc it means we dont need to reference *`{.green} 

![**Segmentation Network: U-Net.** Input Size is 32^3 `\_voxels??*`, in each resolution we have two convolution layers followed by batch normalization layer and rectified Linear Units (ReLU) activation function. Intermediate sizes are written on top of arrows, number of convolution filters is written bottom of boxes. Skip connections show concatenation of the features from contracting path (left side of the network) and expansive path (right side of the network).`\_explain different colors, do they correspond with the different steps? for example: red- max pooling 2x2x2? add figure legend?*`{.green} ](images/unet.png){#fig:unet width="10cm"}

`\_what do we use as initial encoder weights and backbone*`{.green} 
`\_code checked: keras- The Glorot uniform initializer, also called Xavier uniform initializer.*`{.green} 
During each layer of the analysis path, the convolution filter consisting of a 3x3x3 kernel, with randomly initialized weights, was moved over all the voxels in each subset twice `\_what do you mean by "twice"?  *`{.green}, each time taking their dot product.
This kernel extracts and enhances the features in different parts of the image.
This is followed by a ReLU function, which can be described as 

$$f(x)=max(0,x)$$

which will output the positive input directly, while setting the negative input to 0.

Between each layer, the voxels were condensed, or down sampled, via a max-pooling step of 2x2x2, in which the maximum value of the 2x2x2 voxel cube is put forth.
With every layer of the U-Net, the input size thereby halves, while the number of channels doubles.

While the analysis path focuses on the identification of the areas of interest, the synthesis part focuses on their localization.
The synthesis path of the U-Net uses the same basic architecture as the analysis path, with a slight variation of using up convolution operation and implementing skip connections, where feature maps of the analysis part are concatenated to the output of the transposed convolutions of the same level. 

`\_code checked:final = Conv3D(n_channel_out, (1,) * n_dim, activation='sigmoid')(unet) *`{.green} 
The sigmoid/Softmax `\_in the image you write Sigmoid but in the text Softmax, which activation function was used?*`{.green} activation function is the last block of the U-Net (Figure {@fig:unet}), it triggers the loss function, which converts the output from the decoder path into a mask, where each voxel is assigned as either vesicle or not-vesicle.
As the segmentation of vesicles can be considered a binary classification task, binary cross-entropy was implemented as a loss function.

$$Loss= -\frac{1}{output  size}\sum_{i=1}^{output size} y_i * log  ŷ_i + (1-y_1) * log  (1-ŷ_1)$$

with the *output size* being the number of scalar values in the model output, *ŷ_1_* being the *i*-th scalar value in the model output and *y_i_* being the corresponding target value.
`\_publication to cite?*`{.green}

To optimize the weights and reduce the loss function during training, the Adam optimizer was used [@doi:10.48550/arXiv.1412.6980].
200 epochs were run until the loss function reached a global minimum.
`\_it's a local minima, we are optimizing a non-convex function with thousands of parameters*`{.green}


##### Mask prediction

The tomograms are large, 3D volumes.
They therefore were split into 32x32x32 patches with a step size of 24 (stride) before the U-Net. 
The small prediction patches, which were the output of the U-Net, were then stitched together to get the final probability mask.

#### Transfer Learning / Neuron Dataset


### Postprocessing


#### Estimating Global Threshold

In electron microscopic images, dense areas of the specimen appear darker, as fewer electrons are able to pass through that area of the sample.
Therefore, the cellular and vesicular membrane, among other features, appear darker than the background.
Binary cross-entropy was utilized to binarize the obtained probability mask. 
To determine the required threshold, several threshold values (between 0.8 and 1.0) were tested and the one that minimized the average of luminance of all marginal voxels was selected.(srounnd of vesicles)
`\_add image from odt??*`{.green}

#### Adaptive Localized Threshold

The global threshold identifies the majority synaptic vesicles.
Some vesicles, however, are more difficult to detect.
This might be, due to high intensity variations within the tomogram, or because the predicted binarized labels are do not match the spherical shape of vesicles. `\_should go to results?*`{.green}

In terms of binarized lables not matching the spherical shape of vesicles, two main classes were identified: vesicles that were in close proximity to another and got connected, and vesicles, which were only partially captured. 
These two classes were then separated from the rightfully identified vesicles by comparing their label sizes and their extent value  (Ratio of pixels in the region to pixels in the total bounding box computed as area / (rows * cols)). `\_write this into a clean formula*`{.green}
In the next step, probability masks of the partially detected vesicles were expanded in an effort to find the correct mask.
The probability masks of the connected vesicles, however, were minimized by searching for a more precise threshold, with the goal of separating the vesicles.


#### Radial Profile

`\_@Benoit?*`{.green}

#### Outlier Removal

The feature space of predicted vesicle labels was defined, containing thickness, membrane density, and estimated radius of a vesicle. `\_@Benoit: after radial profile, we can add the definition of thinness and membrane as well*`{.blue}
To detect outliers in this multivariate space, Mahalanobis Distance (MD) was applied to calculate L2 norm distance on normalized variables using the covariance matrix of observation.
As an additional way to detect outliers, the p-value of MD was calculated, bringing this evaluation setup in iterative form.
If the MD p-value of a specific vesicle was not in a specific margin range (0-10), their radial profile was recalculated, and the label entirely removed if they again failed to pass the margin of the p-value.

#### Radius Estimation (Cross Correlation through Radial Profile)

`\_@Benoit?*`{.green}

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
