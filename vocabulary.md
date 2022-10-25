# Alphabetical Listing
**bias:** error introduced by approximating a complicated model by a simpler one

**classification:**	problems with a qualitative (or categorical) response

**error:**  difference in observed response compared to predicted response

**flexibility:**  ability for model to fit the data

**interpretability:** ability to make specific inference in regard to data and model

**MSE:**  one measure of measuring model error; mean squared error

**non-parametric model:** does not assume a specific form of relationship

**parametric model:** assumes a specific form of relationship

**quantitative variable:**	takes on a numerical value (e.g. age, height, income)

**qualitative variable:** takes on a value of one of K different classes or categories

**regression:**	problems with a quantitative response

**statistical learning:** a set of tools for understanding data

**training dataset:** set of data used to estimate f

**test dataset:** hold out set used to estimate model performance

**variance:** the amount our prediction changes from one training set to another


# Topical Listing
## Statistical Learning Overview
**statistical learning:** a set of tools for understanding data

**interpretability:** ability to make specific inference in regard to data and model

**quantitative variable:**	takes on a numerical value (e.g. age, height, income)

**qualitative variable:** takes on a value of one of K different classes or categories


## Types of Approaches and Related Terms
**parametric model:** assumes a specific form of relationship

**non-parametric model:** does not assume a specific form of relationship

**classification:**	problems with a qualitative (or categorical) response

**regression:**	problems with a quantitative response

**method of least squares:** approach to estimate coefficients in linear regression model that minimizes the RSS

**logistic regression:** we use the logistic function to model Pr(Y=1|X) as the 'response'. We choose coefficients using maximum likelihood

**linear discriminant analysis (LDA):** a way of estimating the distribution of $X$ in $k$ categories, and the likelihood of those categories.

**quadratic distriminant analysis (QDA):** like LDA, but assumes each class has its own covariance matrix for predictors, $X$.

**K-nearest neighbors regression or classification:** assigns the class or value as the average of the *K* nearest neighbors.

**step-wise selection:** approaches for feature selection; can include forward selection and backward selection.

**least absolute shrinkage and selection operator (LASSO):** Introduces an L1 penalty to shrink coefficients from the least squares approach towards zero. Can perform feature selection by shrinking some coefficients to exactly zero. $$RSS + \lambda\Sigma_{j=1}^{p}|\beta_j|$$

**ridge regression:** Introduces an L2 penalty to shrink coefficients from the least squares approach towards zero.
$$RSS + \lambda\Sigma_{j=1}^{p}\beta_j^2$$

**elastic net:** Mix of ridge and LASSO. Combines L1 and L2 penalty.
$$RSS + \lambda\Sigma_{j=1}^{p}|\beta_j| + \lambda\Sigma_{j=1}^{p}\beta_j^2$$

**polynomial regression:** introduces non-linearity in the relationship between a predictor and response (globally) by including transformation of predictors raised to a power.

**step functions**: split the predictor space into bins, and then assign a constant value for observation in each bin.

**regression spline**: split the predictor space into $k$ bins, and fit $k$ polynomial regression models, one for each bin.

**natural spline:** a spline with additional constraints (function must be linear at the boundaries). Reduces variance at the boundaries.

**smoothing spline**: the more elegant approach :). Uses Loss + Penalty formulation to 'smooth' a regression spline with knots at every observation. 

## Training and Related Terms
**training dataset:** set of data used to estimate f

**test dataset:** hold out set used to estimate model performance

**curse of dimensionality:** with increasing number of predictors, the distance between observations in predictor space increases exponentially

**validation set approach:** split data into two sets: training and validation set

**leave-one-out cross-validation (LOOCV):** leave out one observation as the validation set, and use the rest of the observations to train the model. Do this *n* times, and then average the results of the left out sets.

**$k$-fold cross-validation:** split the dataset into *k* folds, then use *k* - 1 folds for training and the remaining fold for testing. Repeat for the remaining folds.

**Bootstrap:** A resampling approach to estimate error associated with a parameter of interest or a model. Can resample (with replacement) to create multiple 'bootstrap' datasets.

## Measuring Error
**error:**  difference in observed response compared to predicted response

**MSE:**  one measure of measuring model error; mean squared error; ((1/n) * SUM(ySubI - fHat(xSubI))^2)

**variance:** the amount our prediction changes from one training set to another

**bias:** error introduced by approximating a complicated model by a simpler one

**flexibility:**  ability for model to fit the data

**residual:** difference in observed and predicted response

**Residual Sum of Squares:** sum of squared residuals across observations in dataset

**Residual Standard Error:** average amount the response will deviate from the true regression line

**$R^2$:** proportion of variability explained by f(X)

## Assumptions
**collinearity:** when there exists a linear relationship between two predictors


