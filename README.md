
# Conditionally conjugate variational Bayes in logistic models


This repository is associated with the article [Durante and Rigon (2018). *Conditionally conjugate variational Bayes in logistic models*](https://arxiv.org/abs/1711.06999), and provides detailed materials to implement the different algorithms derived in the paper along with some quantitative assessments of such computational routines. 

The core functions of our implementations are made available in the file [`logistic.R`](https://github.com/tommasorigon/logisticVB/blob/master/logistic.R), which can be downloaded from this repository. These codes allow the implementation of the algorithms derived in the paper. Such routines cover **CAVI** and **SVI** for approximate Bayesian logistic regression, along with classical **ML estimation via EM**. In addition, we provide two tutorials aimed at fully reproducing our results. More specifically:

- [`vb_logistic_tutorial.md`](https://github.com/tommasorigon/logisticVB/blob/master/vb_logistic_tutorial.md). In this tutorial, we empirically compare the CAVI and the SVI algorithms on a simulated dataset. We show that CAVI and SVI provide similar approximations, which additionally concentrate around the truth as the sample size increases. **This empirical study is discussed in Section 3 of our article.**
- [`em_logistic_tutorial.md`](https://github.com/tommasorigon/logisticVB/blob/master/em_logistic_tutorial.md). In this tutorial, we show that the Newton-Raphson algorithm for maximum likelihood estimation of logistic coefficients can diverge in some scenarios, even if the MLE is well defined. We also compare empirically the convergence rates of the EM algorithm based on Pòlya-gamma data augmentation and the MM algorithm of [Böhning and Lindsay (1988)](https://link.springer.com/article/10.1007/BF00049423). We show that the EM is more efficient than MM in terms of iterations to reach convergence. This result confirms **Proposition 1 in the Appendix of our article**.
