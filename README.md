# libmpi

[![license](https://img.shields.io/badge/license-Apache-brightgreen.svg?style=flat)](https://github.com/vxfury/libmpi/blob/master/LICENSE)
[![CI Status](https://github.com/vxfury/libmpi/workflows/ci/badge.svg)](https://github.com/vxfury/libmpi/actions)
[![codecov](https://codecov.io/gh/vxfury/libmpi/branch/main/graph/badge.svg?token=5IfLTTEcnF)](https://codecov.io/gh/vxfury/libmpi)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/vxfury/libmpi?color=red&label=release)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/vxfury/libmpi/pulls)

Multiple Precision Integer and Relevant Algorithms, such as Bignum, RSA, DH, ECDH, ECDSA

```
+--------------------------------+---------------------------+--------------------------+--------------------------+
|     operation with options     | average time(nanoseconds) | coefficient of variation | perfermance ratio to ref |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| from-string(ossl)              |        29979.364600       |         0.058321         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| to-string(ossl)                |        2823.028000        |         0.153397         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| from-string(mpi)               |        2084.886000        |         0.048673         |         14.379378        |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| to-string(mpi)                 |         734.442000        |         0.125354         |         3.843773         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| from-octets(ossl)              |         665.761800        |         0.108990         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| to-octets(ossl)                |        1247.823600        |         0.069799         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| from-octets(mpi)               |         217.740600        |         0.159403         |         3.057591         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| to-octets(mpi)                 |         164.840600        |         0.165906         |         7.569880         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| add(ossl)                      |         351.021000        |         0.167208         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| add(mpi)                       |         68.860200         |         0.403310         |         5.097589         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| add-assign(ossl)               |         295.300800        |         0.118000         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| add-assign(mpi)                |         57.500200         |         0.295984         |         5.135648         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sub(ossl)                      |         155.540400        |         0.182649         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sub(mpi)                       |         66.400200         |         0.238013         |         2.342469         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sub-assign(ossl)               |         360.961000        |         0.135903         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sub-assign(mpi)                |         100.920400        |         0.387438         |         3.576690         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| mul(ossl)                      |        11748.813200       |         0.034542         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| mul(mpi)                       |        2180.966200        |         0.090510         |         5.386976         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sqr(ossl)                      |        8368.837288        |         0.063922         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| sqr(mpi)                       |        1224.563600        |         0.192904         |         6.834139         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| div(ossl)                      |        39464.134091       |         0.023083         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| div(mpi)                       |        3873.351000        |         0.035070         |         10.188628        |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| gcd_consttime(ossl)            |      16371789.500000      |         0.078141         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| gcd_consttime(mpi)             |       4944853.936842      |         0.101773         |         3.310874         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| montgomery-exp(ossl)           |      129882686.200000     |         0.017558         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| montgomery-exp-consttime(ossl) |      131193285.800000     |         0.017390         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| montgomery-exp(mpi)            |      11090355.360000      |         0.060182         |         11.711319        |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| montgomery-exp-consttime(mpi)  |      14252012.257143      |         0.028929         |         9.205246         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| generate_prime(ossl)           |     13690634108.000000    |         0.452998         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| is_prime(ossl)                 |      519162246.200000     |         0.031847         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| MUL2(a * 2 = a + a)            |         33.260400         |         0.173412         |         1.000000         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
| MUL2(a * 2 = a << 1)           |         68.940600         |         0.147952         |         0.482450         |
+--------------------------------+---------------------------+--------------------------+--------------------------+
```

