# XGBoost

Tree based methods are widely used in different scenarios and industries(e.g. medical detections/recommendation system etc.). Plus in my opinion, the widely used linear regression model, which used to extract alpha return in multi-factors investment, is not obeying the [basic assumptions](https://www.statology.org/linear-regression-assumptions/) and wrongly implemented. Not to mention those techiques to optimize the regression method(eliminate multicollinearity, redictions of dimenstions), these techs are good but are built up based on a wrong fundation.

To replace the method we are using, we are plan to find some machine learning techniques to replace it. Inspired by the reports from [Tianfeng Securities Co., Ltd.](https://www.tfzq.com/) and many competetions results from Kaggle, XGBoost is one of our interest to use. As of its outstanding characteristcs(not only including):
- Able to handle those features which are correlated.
- Multi-processing when calculation optimal division point of features on leaf level.
- No need to pre_process nan values before feeding to model.
- As an ensemble model, it has a strong robustness facing out-sample dataset.

Brief introduction of XGBoost model can be found [here](https://docs.google.com/presentation/d/10F33ASJkZ0YPJAwLp4Frx_RTd07AnEbV/edit?usp=sharing&ouid=118041969453776582937&rtpof=true&sd=true).
