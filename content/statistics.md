
### Dice of tomographic images of synaptosomes
### Control Dataset Metrics 
|           | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | Average |
|:---------:|:-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|:-----:|
| Deep Mask | 0.72 | 0.84 | 0.82 | 0.83 | 0.79 | 0.76 | 0.78 | 0.81 | 0.82 | 0.80 | **0.797** |
| Global Threshold | 0.72 | 0.87 | 0.86 | 0.76 | 0.75 | 0.78 | 0.84 | 0.85 | 0.77 | 0.86 | **0.806** |
| Adaptive Threshold | 0.73 | 0.88 | 0.86 | 0.76 | 0.75 | 0.79 | 0.84 | 0.85 | 0.77 | 0.86 | **0.809** |
| Radial Profile | 0.77 | 0.91 | 0.90 | 0.90 | 0.85 | 0.82 | 0.86 | 0.88 | 0.89 | 0.89 | **0.867** |
| Outlier Removal | 0.78 | 0.91 | 0.92 | 0.89 | 0.86 | 0.88 | 0.90 | 0.90 | 0.91 | 0.89 | **0.884** |
| TP | 188 | 104 | 128 | 138 | 190 | 102 | 184 | 128 | 132 | 127 | **142.10** |
| FN | 35 | 1 | 0 | 6 | 24 | 2 | 0 | 4 | 3 | 2 | **7.70** |
| FP | 19 | 1 | 2 | 2 | 3 | 7 | 10 | 1 | 3 | 5 | **5.30** |
| F1 | 0.874 | 0.990 | 0.992 | 0.972 | 0.934 | 0.958 | 0.974 | 0.981 | 0.978 | 0.973 | **0.963** |

Dataset 10 is part of the test dataset from control experiment


### Treatment Dataset Metrics
|           | 1 | 2 | 3 | 5 | 6 | 7 | 8 | 10 | Average |
|:---------:|:-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|:-----:|
| Deep Mask | 0.76 | 0.74 | 0.74 | 0.79 | 0.76 | 0.77 | 0.83 | 0.81 | **0.775** |
| Global Threshold | 0.88 | 0.83 | 0.72 | 0.85 | 0.81 | 0.85 | 0.85 | 0.85 | **0.830** |
| Adaptive Threshold | 0.88 | 0.83 | 0.72 | 0.85 | 0.81 | 0.85 | 0.85 | 0.85 | **0.830** |
| Radial Profile | 0.85 | 0.82 | 0.75 | 0.87 | 0.83 | 0.85 | 0.91 | 0.89 | **0.846** |
| Outlier Removal | 0.84 | 0.79 | 0.75 | 0.86 | 0.85 | 0.82 | 0.91 | 0.90 | **0.840** |
| TP | 683 | 117 | 380 | 514 | 355 | 107 | 100 | 75 | **291.38** |
| FN | 16 | 5 | 54 | 21 | 18 | 3 | 0 | 1 | **14.75** |
| FP | 2 | 1 | 22 | 15 | 23 | 7 | 1 | 5 | **9.50** |
| F1 | 0.987 | 0.975 | 0.909 | 0.966 | 0.945 | 0.955 | 0.995 | 0.962 | **0.962** |
### Neuron Dataset Metrics
|           | 73 | 80 | 84 | 102 | 114 | 115 | 116 | 123 | 128 | 132 | 133 | 134 | Average |
|:---------:|:-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|-----:|:-----:|
| Deep Mask | 0.72 | 0.73 | 0.85 | 0.64 | 0.71 | 0.56 | 0.66 | 0.64 | 0.75 | 0.70 | 0.80 | 0.73 | **0.708** |
| Global Threshold | 0.72 | 0.77 | 0.86 | 0.82 | 0.71 | 0.49 | 0.71 | 0.59 | 0.79 | 0.77 | 0.78 | 0.71 | **0.727** |
| Adaptive Threshold | 0.72 | 0.77 | 0.86 | 0.83 | 0.72 | 0.48 | 0.71 | 0.56 | 0.79 | 0.77 | 0.78 | 0.70 | **0.724** |
| Radial Profile | 0.83 | 0.79 | 0.90 | 0.88 | 0.83 | 0.65 | 0.82 | 0.68 | 0.89 | 0.87 | 0.90 | 0.81 | **0.821** |
| Outlier Removal | 0.83 | 0.81 | 0.90 | 0.89 | 0.83 | 0.64 | 0.83 | 0.68 | 0.90 | 0.87 | 0.90 | 0.80 | **0.823** |
| TP | 480 | 101 | 464 | 96 | 115 | 130 | 281 | 59 | 239 | 125 | 498 | 530 | **259.83** |
| FN | 30 | 9 | 17 | 7 | 12 | 33 | 13 | 6 | 9 | 10 | 18 | 99 | **21.92** |
| FP | 39 | 13 | 29 | 2 | 23 | 62 | 44 | 6 | 23 | 17 | 12 | 79 | **29.08** |
| F1 | 0.933 | 0.902 | 0.953 | 0.955 | 0.868 | 0.732 | 0.908 | 0.908 | 0.937 | 0.903 | 0.971 | 0.856 | **0.902** |



### Dice statistical values
|                    | Train set | Test set  | Generalization set |
|--------------------|-----------|-----------|--------------------|
| Soft Dice          | 0.80±0.04 | 0.78±0.03 | 0.71±0.08          |
| Global Threshold   | 0.80±0.05 | 0.83±0.05 | 0.73±0.10          |
| Adaptive Threshold | 0.80±0.06 | 0.83±0.05 | 0.72±0.11          |
| Outlier Removal    | 0.88±0.04 | 0.85±0.05 | 0.82±0.08          |
| Radial Profile     | 0.87±0.05 | 0.85±0.05 | 0.82±0.08          |
| N                  | 9         | 9         | 12                 |


### Train Dataset ANOVA Results with Benjamini-Hochberg Correction
| Comparison                          | Original P-Value | Corrected P-Value | Significant |
|-------------------------------------|------------------|-------------------|-------------|
| Soft Dice vs Global Threshold       | 0.842403         | 0.9360            | False       |
| Soft Dice vs Adaptive Threshold     | 0.771617         | 0.9360            | False       |
| Soft Dice vs Radial Profile         | 0.002580         | **0.0083**        | True        |
| Soft Dice vs Outlier Removal        | 0.000322         | **0.0032**        | True        |
| Global Threshold vs Adaptive Threshold | 0.936058      | 0.9361            | False       |
| Global Threshold vs Radial Profile  | 0.013383         | **0.0268**        | True        |
| Global Threshold vs Outlier Removal | 0.002629         | **0.0083**        | True        |
| Adaptive Threshold vs Radial Profile| 0.016572         | **0.0276**        | True        |
| Adaptive Threshold vs Outlier Removal | 0.003329       | **0.0083**        | True        |
| Radial Profile vs Outlier Removal   | 0.442988         | 0.6328            | False       |

### Test Dataset ANOVA Results with Benjamini-Hochberg Correction
| Comparison                          | Original P-Value | Corrected P-Value | Significant |
|-------------------------------------|------------------|-------------------|-------------|
| Soft Dice vs Global Threshold       | 0.011068         | **0.0277**        | True        |
| Soft Dice vs Adaptive Threshold     | 0.010323         | **0.0277**        | True        |
| Soft Dice vs Radial Profile         | 0.001371         | **0.0137**        | True        |
| Soft Dice vs Outlier Removal        | 0.004778         | **0.0239**        | True        |
| Global Threshold vs Adaptive Threshold | 0.936559      | 0.9366            | False       |
| Global Threshold vs Radial Profile  | 0.392195         | 0.7393            | False       |
| Global Threshold vs Outlier Removal | 0.547109         | 0.7522            | False       |
| Adaptive Threshold vs Radial Profile| 0.443555         | 0.7393            | False       |
| Adaptive Threshold vs Outlier Removal | 0.601783       | 0.7522            | False       |
| Radial Profile vs Outlier Removal   | 0.844485         | 0.9366            | False       |

### Generalization Dataset ANOVA Results with Benjamini-Hochberg Correction
| Comparison                          | Original P-Value | Corrected P-Value | Significant |
|-------------------------------------|------------------|-------------------|-------------|
| Soft Dice vs Global Threshold       | 0.604268         | 0.8347            | False       |
| Soft Dice vs Adaptive Threshold     | 0.667768         | 0.8347            | False       |
| Soft Dice vs Radial Profile         | 0.001950         | **0.0097**        | True        |
| Soft Dice vs Outlier Removal        | 0.001816         | **0.0097**        | True        |
| Global Threshold vs Adaptive Threshold | 0.950860      | 0.9509            | False       |
| Global Threshold vs Radial Profile  | 0.021154         | **0.0370**        | True        |
| Global Threshold vs Outlier Removal | 0.019223         | **0.0370**        | True        |
| Adaptive Threshold vs Radial Profile| 0.022216         | **0.0370**        | True        |
| Adaptive Threshold vs Outlier Removal | 0.020209       | **0.0370**        | True        |
| Radial Profile vs Outlier Removal   | 0.936368         | 0.9509            | False       |
