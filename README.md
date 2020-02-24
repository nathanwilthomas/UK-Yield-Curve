# PCA Decomposition on the UK yield curve

Principal Components aims to reduce the dimensionality of a dataset; by finding the least amount of variables that explain the largest proportion of the data. It does this by transforming the data from a correlation matrix (more commonly used on financial data than a covariance matrix), onto a subspace with less dimensions, where all explanatory variables are orthogonal (perpendicular) to each other, i.e there is no multicollinearity. These are <b>statistical properties</b> and do not necesarrily have an economic interpretation.

For this analysis I will use the 10-year-yield for the US and UK to see if we can fiind an estimate for the long-term interest rate/term premium. It is commonly know that:

<b>PC1:</b> constant ~ long term interest rate ~ R*

<b>PC2:</b> slope ~ term premia

<b>PC3:</b> curvature

To read about this in more detail, read the PCA section of <i>"Market Risk Analysis II, Practical Financial Econometrics- Carol Alexander"</i>.

There is also a good paper here which uses PCA and macroeconomic variables: https://pdfs.semanticscholar.org/8736/5855217edbc53e5e29c5c5872db7efb907cc.pdf

In this code I perform PCA manually, but there is a module in scikit-learn which speeds up the process:

https://github.com/scikit-learn/scikit-learn/blob/b194674c4/sklearn/decomposition/_pca.py#L104

A bit more detail on how to do PCA in Python: http://sebastianraschka.com/Articles/2015_pca_in_3_steps.html
