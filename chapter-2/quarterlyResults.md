# Quarter as a horizon

I repeat the same exercises, but using quarter as a horizon instead of a month.

## CAPM as a Risk Model

### Pre-formation with Benchmark

| ranks | lm    | Expected Return | Return Vol | Alpha  | MKT   | Idio Vol | R^2   |
| ----- | ----- | --------------- | ---------- | ------ | ----- | -------- | ----- |
| 0     | 0.000 | 3.156           | 9.285      | 2.081  | 1.349 | 6.966    | 0.432 |
| 1     | 0.063 | 1.823           | 4.620      | 0.975  | 0.877 | 2.485    | 0.716 |
| 2     | 0.124 | 1.059           | 3.786      | 0.279  | 0.781 | 1.558    | 0.836 |
| 3     | 0.170 | 0.506           | 4.013      | -0.294 | 0.795 | 1.919    | 0.777 |
| 4     | 0.250 | -0.544          | 5.913      | -1.440 | 0.982 | 3.971    | 0.554 |

| ranks | Alpha  | MKT   | SMB    | HML    | Idio Vol | R^2   |
| ----- | ------ | ----- | ------ | ------ | -------- | ----- |
| 0     | 2.001  | 1.301 | 0.394  | 0.157  | 6.863    | 0.448 |
| 1     | 0.894  | 0.912 | -0.006 | 0.195  | 2.425    | 0.730 |
| 2     | 0.177  | 0.823 | 0.004  | 0.245  | 1.402    | 0.867 |
| 3     | -0.381 | 0.816 | 0.076  | 0.200  | 1.832    | 0.797 |
| 4     | -1.454 | 0.903 | 0.410  | -0.004 | 3.781    | 0.596 |

**Post-formation with Benchmark**

| ranks | lm    | Expected Return | Return Vol | Alpha  | MKT   | Idio Vol | R^2   |
| ----- | ----- | --------------- | ---------- | ------ | ----- | -------- | ----- |
| 0     | 0.000 | 0.546           | 6.828      | -0.429 | 1.111 | 4.643    | 0.533 |
| 1     | 0.063 | 0.850           | 4.460      | 0.009  | 0.880 | 2.079    | 0.782 |
| 2     | 0.124 | 0.948           | 4.094      | 0.113  | 0.852 | 1.541    | 0.859 |
| 3     | 0.170 | 1.028           | 4.411      | 0.155  | 0.908 | 1.763    | 0.841 |
| 4     | 0.250 | 0.912           | 5.770      | -0.054 | 1.086 | 3.134    | 0.706 |

| **ranks** | Alpha  | Mkt   | SMB    | HML    | Idio Vol | R^2   |
| --------- | ------ | ----- | ------ | ------ | -------- | ----- |
| 0         | -0.440 | 1.027 | 0.424  | -0.029 | 4.466    | 0.568 |
| 1         | -0.057 | 0.896 | 0.055  | 0.155  | 2.032    | 0.792 |
| 2         | 0.000  | 0.901 | -0.007 | 0.279  | 1.328    | 0.895 |
| 3         | 0.062  | 0.930 | 0.078  | 0.218  | 1.651    | 0.861 |
| 4         | -0.055 | 1.029 | 0.278  | -0.036 | 3.019    | 0.727 |

**Pre-formation with no Benchmark**

| ranks | lm    | Expected Return | Return Vol | Alpha  | MKT   | Idio Vol | R^2   |
| ----- | ----- | --------------- | ---------- | ------ | ----- | -------- | ----- |
| 0     | 0.000 | 3.826           | 9.164      | 2.727  | 1.338 | 6.866    | 0.435 |
| 1     | 0.063 | 1.937           | 4.659      | 1.093  | 0.857 | 2.714    | 0.669 |
| 2     | 0.124 | 1.102           | 3.772      | 0.330  | 0.762 | 1.679    | 0.807 |
| 3     | 0.170 | 0.524           | 3.821      | -0.255 | 0.760 | 1.825    | 0.779 |
| 4     | 0.251 | -0.485          | 5.627      | -1.355 | 0.930 | 3.829    | 0.545 |

| ranks | Alpha  | MKT   | SMB    | HML   | Idio Vol | R^2   |
| ----- | ------ | ----- | ------ | ----- | -------- | ----- |
| 0     | 2.639  | 1.252 | 0.595  | 0.161 | 6.637    | 0.472 |
| 1     | 1.001  | 0.888 | 0.039  | 0.218 | 2.647    | 0.685 |
| 2     | 0.217  | 0.810 | -0.005 | 0.271 | 1.499    | 0.846 |
| 3     | -0.350 | 0.789 | 0.053  | 0.222 | 1.718    | 0.804 |
| 4     | -1.379 | 0.874 | 0.323  | 0.030 | 3.710    | 0.573 |

**Post-formation with no Benchmark**

| ranks | lm    | Expected Return | Return Vol | Alpha  | MKT   | Idio Vol | R^2   |
| ----- | ----- | --------------- | ---------- | ------ | ----- | -------- | ----- |
| 0     | 0.000 | 0.560           | 7.277      | -0.437 | 1.136 | 5.151    | 0.493 |
| 1     | 0.063 | 0.855           | 4.460      | 0.030  | 0.865 | 2.228    | 0.751 |
| 2     | 0.124 | 0.989           | 4.007      | 0.170  | 0.822 | 1.620    | 0.837 |
| 3     | 0.170 | 0.972           | 4.229      | 0.127  | 0.868 | 1.703    | 0.838 |
| 4     | 0.251 | 0.883           | 5.604      | -0.067 | 1.064 | 2.979    | 0.718 |

| ranks | Alpha  | MKT   | SMB    | HML    | Idio Vol | R^2   |
| ----- | ------ | ----- | ------ | ------ | -------- | ----- |
| 0     | -0.439 | 1.015 | 0.590  | -0.073 | 4.831    | 0.554 |
| 1     | -0.029 | 0.871 | 0.090  | 0.133  | 2.187    | 0.760 |
| 2     | 0.072  | 0.868 | -0.021 | 0.246  | 1.463    | 0.867 |
| 3     | 0.030  | 0.899 | 0.046  | 0.234  | 1.575    | 0.862 |
| 4     | -0.087 | 1.024 | 0.231  | 0.019  | 2.901    | 0.733 |

## Fama French as a Risk Model

**Pre-formation with Benchmark**

| ranks | lm    | Expected Return | Return Vol | Alpha  | MKT   | Idio Vol | R^2   |
| ----- | ----- | --------------- | ---------- | ------ | ----- | -------- | ----- |
| 0     | 0.000 | 2.764           | 6.251      | 1.771  | 1.126 | 3.596    | 0.665 |
| 1     | 0.010 | 1.485           | 4.639      | 0.597  | 0.952 | 1.735    | 0.859 |
| 2     | 0.019 | 0.452           | 4.556      | -0.419 | 0.954 | 1.584    | 0.880 |
| 3     | 0.028 | -0.658          | 5.169      | -1.560 | 1.029 | 2.391    | 0.790 |
| 4     | 0.045 | -2.632          | 7.028      | -3.628 | 1.198 | 4.552    | 0.584 |

| ranks | Alpha  | MKT   | SMB   | HML    | Idio Vol | R^2   |
| ----- | ------ | ----- | ----- | ------ | -------- | ----- |
| 0     | 1.713  | 1.131 | 0.095 | 0.132  | 3.570    | 0.670 |
| 1     | 0.495  | 0.987 | 0.038 | 0.240  | 1.604    | 0.880 |
| 2     | -0.505 | 0.959 | 0.154 | 0.192  | 1.442    | 0.901 |
| 3     | -1.612 | 0.991 | 0.291 | 0.099  | 2.228    | 0.817 |
| 4     | -3.607 | 1.063 | 0.613 | -0.102 | 4.148    | 0.655 |

**Post-formation with Benchmark**

| ranks | lm    | Expected Return | Return Vol | Alpha  | MKT   | Idio Vol | R^2   |
| ----- | ----- | --------------- | ---------- | ------ | ----- | -------- | ----- |
| 0     | 0.000 | 0.845           | 4.960      | -0.080 | 1.027 | 1.834    | 0.863 |
| 1     | 0.010 | 1.039           | 4.481      | 0.135  | 0.956 | 1.319    | 0.913 |
| 2     | 0.019 | 1.045           | 4.724      | 0.131  | 0.992 | 1.604    | 0.884 |
| 3     | 0.028 | 1.061           | 5.283      | 0.099  | 1.075 | 2.167    | 0.831 |
| 4     | 0.045 | 0.818           | 6.862      | -0.229 | 1.291 | 3.682    | 0.711 |

| ranks | Alpha  | MKT   | SMB    | HML    | Idio Vol | R^2   |
| ----- | ------ | ----- | ------ | ------ | -------- | ----- |
| 0     | -0.055 | 1.018 | -0.005 | -0.062 | 1.826    | 0.864 |
| 1     | 0.064  | 0.995 | -0.045 | 0.181  | 1.205    | 0.927 |
| 2     | 0.029  | 1.016 | 0.091  | 0.240  | 1.451    | 0.905 |
| 3     | 0.014  | 1.056 | 0.266  | 0.174  | 1.985    | 0.858 |
| 4     | -0.301 | 1.199 | 0.590  | 0.100  | 3.248    | 0.775 |

**Pre-formation with no Benchmark**

(Really strange results. Need to do a few analyses here. Why are the betas so low for realized returns???)

| ranks | lm    | #Stocks | Expected Return | Return Vol | Alpha  | MKT   | Idio Vol | R^2   |
| ----- | ----- | ------- | --------------- | ---------- | ------ | ----- | -------- | ----- |
| 0     | 0.000 | 1133    | 4.302           | 6.056      | 3.484  | 0.718 | 5.051    | 0.291 |
| 1     | 0.014 | 946     | 2.262           | 4.076      | 1.463  | 0.735 | 2.376    | 0.660 |
| 2     | 0.030 | 945     | 1.321           | 4.410      | 0.454  | 0.903 | 1.746    | 0.844 |
| 3     | 0.046 | 945     | 0.360           | 5.449      | -0.631 | 1.135 | 2.008    | 0.866 |
| 4     | 0.076 | 945     | -1.424          | 7.765      | -2.608 | 1.501 | 3.860    | 0.754 |

| ranks | Alpha  | MKT   | SMB   | HML    | Idio Vol | R^2   |
| ----- | ------ | ----- | ----- | ------ | -------- | ----- |
| 0     | 3.355  | 0.721 | 0.247 | 0.287  | 4.949    | 0.319 |
| 1     | 1.338  | 0.763 | 0.121 | 0.289  | 2.225    | 0.702 |
| 2     | 0.344  | 0.935 | 0.069 | 0.259  | 1.590    | 0.871 |
| 3     | -0.712 | 1.132 | 0.176 | 0.179  | 1.894    | 0.881 |
| 4     | -2.622 | 1.419 | 0.424 | -0.003 | 3.649    | 0.780 |

**Post-formation with no Benchmark**

| pq   | lm    | #Stocks | Expected Return | Return Vol | Alpha  | MKT   | Idio Vol | R^2   |
| ---- | ----- | ------- | --------------- | ---------- | ------ | ----- | -------- | ----- |
| 0    | 0.000 | 1138    | 0.733           | 5.280      | -0.120 | 0.899 | 3.404    | 0.582 |
| 1    | 0.014 | 951     | 0.948           | 4.002      | 0.142  | 0.802 | 1.795    | 0.800 |
| 2    | 0.030 | 950     | 1.075           | 4.371      | 0.194  | 0.929 | 1.353    | 0.904 |
| 3    | 0.046 | 950     | 0.973           | 5.338      | -0.011 | 1.122 | 1.742    | 0.892 |
| 4    | 0.076 | 950     | 0.866           | 7.192      | -0.269 | 1.443 | 3.156    | 0.807 |

| ranks | Alpha  | MKT   | SMB    | HML    | Idio Vol | R^2   |
| ----- | ------ | ----- | ------ | ------ | -------- | ----- |
| 0     | -0.137 | 0.860 | 0.219  | 0.013  | 3.342    | 0.597 |
| 1     | 0.092  | 0.825 | -0.010 | 0.126  | 1.759    | 0.807 |
| 2     | 0.133  | 0.959 | -0.021 | 0.152  | 1.281    | 0.914 |
| 3     | -0.050 | 1.125 | 0.068  | 0.088  | 1.717    | 0.896 |
| 4     | -0.280 | 1.401 | 0.225  | -0.002 | 3.084    | 0.816 |