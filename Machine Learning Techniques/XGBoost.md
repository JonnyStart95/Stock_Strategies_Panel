# XGBoost

Tree based methods are widely used in different scenarios and industries(e.g. medical detections/recommendation system etc.). Plus in my opinion, the widely used linear regression model, which used to extract alpha return in multi-factors investment, is not obeying the [basic assumptions](https://www.statology.org/linear-regression-assumptions/) and wrongly implemented. Not to mention those techiques to optimize the regression method(eliminate multicollinearity, redictions of dimenstions), these techs are good but are built up based on a wrong fundation.

To avoid the mistakes we could make as mentioned above, we are plan to find some machine learning techniques to replace it. Inspired by the reports from [Tianfeng Securities Co., Ltd.](https://drive.google.com/drive/folders/10OW5lwLqXhtnalQ7EeqqCZjqiWe_hpvq?usp=sharing) and many competetions results from Kaggle, XGBoost is one of our interest to use. As of its outstanding characteristcs(not only including):
- Able to handle those features which are correlated.
- Multi-processing when calculation optimal division point of features on leaf level.
- No need to pre_process nan values before feeding to model.
- As an ensemble model, it has a strong robustness facing out-sample dataset.

Brief introduction of XGBoost model can be found [here](https://docs.google.com/presentation/d/10F33ASJkZ0YPJAwLp4Frx_RTd07AnEbV/edit?usp=sharing&ouid=118041969453776582937&rtpof=true&sd=true).

The features we used here are mainly financial stats related data, plus some alpha factors we created in previous research section(Investor Preferences/multiply single factors). We would like to keep the copyrights here as not violating the
non-disclosure agreement with AnzhiCapital.

**Feature Selections**: In general, features selections should be adopted to reduce the dimensions of features matrix and avoid noise that those unimportant features could bring. However, we only have around 30 features here where we belive that the marginal profit of using features selection is tiny and cound somehow make use lose the info those factors brought. So we would like to set it as one of the future work as we gain more alpha factors in our database.

**Hyperparameters Tuning**: 5-fold CV are used here to explore what exactly the best hyperparameters are in the training process, whereas, we find out that XGBoost are not that sensitive to the change of hyperparameters, the most two important hyperparameters as we found are the depth of tree and learning rate. This situation also correspond to our assumption that XGBoost/Random Forest are more robust than other machine learning techniques. This is really import when out scenarios is financial market, since the stock market is dynamic and the internal regulation of it is changing all the time, unlike recommendation system and fraud detections.
