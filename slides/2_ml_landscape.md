# Machine Learning Landscape

<div>
<br>
<figure>
  <img src="/ml_problems.png" style="width: 580px !important">
</figure>   
</div>

---

# Supervised Learning and Unsupervised Learning

* **Supervised learning**: each observation is accompanied by answers (labels), $y$
* We want to correlate:
  * rows of observations, $x_i$, with their predictions, $y_i$<br>
or<br>
  * feature columns, $X_i$, with the response column

* **Unsupervised learning**: without responses (labels)
  * We are looking for correlations between
    * feature columns, $X_i$
      * We group similar features together (PCA, NMF, Gaussian Mixture)
    * rows of observations, $x_i$ with $x_j$
      * Group similar observations (kMeans, DBScan, HAC)

---

# Supervised Learning
### Regression and classification tasks
<br>
<div class="grid grid-cols-[3fr_3fr] gap-15]">
<div>

<figure>
  <br>
  <img src="/ex_regression.png" style="width: 300px !important">
</figure> 
</div>
<div>
  <br>
<figure>
  <img src="/ex_classification.png" style="width: 300px !important">
  <figcaption style="color:#b3b3b3ff; font-size: 11px;">Источник изображений:<br> <a href="https://github.com/rasbt/python-machine-learning-book-2nd-edition">S.Raschka, V. Mirjalili: Python Machine Learning, 2nd Ed.</a>
  </figcaption>
</figure> 
</div>
</div>

---

# Regression and Classification Tasks

* **Categorical** variables take values in $k$ classes (categories)
  * If such variables are **ordinal**, then this can be used
* Often we can move from one task to another

<div>
<br>
<figure>
  <img src="/reg_vs_class.png" style="width: 570px !important">
</figure>   
</div>

---

# Unsupervised Learning
### Clustering and dimensionality reduction tasks
<br>
<br>
<div class="grid grid-cols-[3fr_5fr] gap-15]">
<div>

<figure>
  <br>
  <img src="/ex_unsupervised.png" style="width: 250px !important">
</figure> 
</div>
<div>
  <br>
<figure>
  <img src="/ex_unsupervised_dim_reduction.png" style="width: 600px !important">
  <figcaption style="color:#b3b3b3ff; font-size: 11px;">Images source:<br> <a href="https://github.com/rasbt/python-machine-learning-book-2nd-edition">S.Raschka, V. Mirjalili: Python Machine Learning, 2nd Ed.</a>
  </figcaption>
</figure> 
</div>
</div>

---

# Key Factors for Model Selection

### So, there are many models and many types of problems, and there is [no such thing as a free lunch](https://en.wikipedia.org/wiki/No_free_lunch_theorem)<br><br>

### So how do we choose the best one for our specific task?<br><br>

### There are several key choices/trade-offs to be made:
* Parametric or nonparametric model
* Customizable or interpretable model
  * Prediction or inference tasks, respectively
* Low bias or low variance model?

---

# Parametric Models

### Use functions with a **finite** number of parameters

* Step 1: **Fix the family** of parametric models $\mathcal{F}$
  * We also determine the dimension of the parameter space
* Step 2: **Fit the model** to the training observations
  * That is, estimate the model parameters (using least squares, gradient descent, etc.)
<br>

#### Ex.:
* Let's take **logistic regression** with $p+1$ parameters<br>
$$\log\bigg(\frac{p(X)}{1 - p(X)}\bigg) = \beta_0 + \beta_1 X$$

* Let's estimate the regression coefficients $\beta$ using<br> [the maximum likelihood method](https://en.wikipedia.org/wiki/Maximum_likelihood_estimation): $\ell(\beta_0, \beta_1) = \prod\limits_{i:y_i=1} p(x_i) \prod\limits_{j:y_j=1} (1 - p(x_j))$

---

# Parametric models

### Properties of parametric models:

* A **overfitted** model memorizes noise in training observations and cannot generalize new observations well
  * Works well on training data, but poorly on new (test) data

* An **under-trained** model cannot reflect the main relationships in the data
  * Performs poorly on training and new data

* Complex models (e.g., decision trees or neural networks) tend to overfit if they are not controlled and regularization is not used

---

# Nonparametric Models

* We do not select a family of functions
* Such models **do not have** training parameters, or their number is **variable**
  * **Hyperparameters** (not trained) are still available to the researcher
<div class="grid grid-cols-[5fr_3fr] gap-9]">
<div>

* Can produce smooth functions
  * Their smoothness can be controlled
</div>
<div>
<br>
<figure>
  <img src="/ISLP_figure_2.6.png" style="width: 420px !important">
</figure>   
</div>
</div>

---

# Nonparametric Models: Examples

* k-nearest neighbors classifier (**kNN**)
* Histogram defining the density distribution function
* Kernel density estimation (**KDE**)
* Support vector machine (**SVM**)
* Nonparametric logistic regression

<div class="grid grid-cols-[5fr_5fr] gap-9]">
<div>
<br>
<figure>
  <img src="/non-param_1.png" style="width: 290px !important">
</figure> 
</div>
<div>
<br>
<figure>
  <img src="/non-param_2.png" style="width: 290px !important">
</figure>   
</div>
</div>

---

# Nonparametric Models and Inductive Biases

### Nonparametric models seem like the best idea — why can't we use them everywhere?

* It's because they still have some assumptions about the data, or **inductive bias**

* In **parametric** models, we make **explicit** assumptions about the true value of $f$

* In **nonparametric** models, we make **implicit** assumptions

---

# Flexibility vs Interpretability

<br>
<br>
<div>
<figure>
  <img src="/int_vs_flex.png" style="width: 430px !important">
</figure>   
</div>
