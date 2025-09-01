---
layout: statement
---

## Introduction to Machine Learning

---

# What is Machine Learning?
<div v-click at="1">

# And how is it related to artificial intelligence?
</div>
<div class="grid grid-cols-[3fr_3fr] gap-15">
<div v-click at="2">
<figure>
  <img src="/mj_car.jpg" style="width: 350px">
  <figcaption style="color:#b3b3b3ff; font-size: 11px; position: absolute;">Images source: Midjourney 6
    </figcaption>
</figure>
</div>

<div v-click at="3">
<div class="grid grid-cols-[3fr_3fr] gap-15">
<div>
<figure>
  <img src="/mj_car_engine.jpg" style="width: 350px">
</figure>
</div>
<div>
<figure>
  <img src="/mj_car_suspension.jpg" style="width: 350px">
</figure>
</div>
</div>
<br>
<div class="grid grid-cols-[3fr_3fr] gap-15">
<div>
<figure>
  <img src="/mj_car_electric.jpg" style="width: 350px">
</figure>
</div>
<div>
<figure>
  <img src="/mj_car_safety.jpg" style="width: 350px">
</figure>
</div>
</div>

</div>
</div>

---

# What is Machine Learning?
<br>
<br>
  <figure>
    <img src="/What_is_ML.drawio.png" style="width: 400px !important;">
  </figure>

---
layout: quote
---

## *"Programming computers to learn from experience should eventually eliminate the need for much of this detailed programming effort."*
<br>
<div style="text-align: right"> Arthur L. Samuel (1959)*</div>

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

##### * Arthur L. Samuel, “Some studies in machine learning using the game of checkers", *IBM Journal of research and development* 3.3 (1959), pp. 210-229


---

## Traditional Programming Paradigm
<br>
<v-click>

```mermaid {scale: 0.75}
stateDiagram
    direction LR
    Input#nbsp;data --> Coder
    Output#nbsp;data --> Code
    Programmer --> Code
    Code --> Computer
    Computer --> Output#nbsp;data
    Output#nbsp;data --> Programmer
```
</v-click>
<br>
<br>
<v-click>

## Machine Learning Paradigm
<br>

```mermaid {scale: 0.75}
stateDiagram
    direction LR
    Input#nbsp;data --> Computer
    Output#nbsp;data --> Computer
    Computer --> Code
```
##### *Machine learning is the field of study that gives computers the ability to learn without being explicitly programmed*
</v-click>

---
layout: quote
---

## *"A computer program is said to learn from experience <span style="color: green">**E**</span> with respect to some class of tasks <span style="color: blue">**T**</span> and performance measure <span style="color: red">**P**</span> if its performance at tasks in <span style="color: blue">**T**</span>, as measured by <span style="color: red">**P**</span>, improves with experience <span style="color: green">**E**</span>."*
<div style="text-align: right"> Tom M. Mitchell  (1997)</div>
<br>

### Consider the task of recognizing handwritten digits

<figure>
  <img src="/digits.png" style="width: 900px !important">
  <figcaption style="color:#b3b3b3ff; font-size: 11px;">Examples of handwritten digits from the MNIST dataset
  </figcaption>
</figure>

Where:
* Experience <span style="color: green">**E**</span>: [MNIST](https://en.wikipedia.org/wiki/MNIST_database) dataset
* Task <span style="color: blue">**T**</span>: digit classification in images
* Мера качества <span style="color: red">**P**</span>: fraction of correctly classified images

---
zoom: 1.05
---

# Connection between ML and Mathematics
<v-clicks depth="3">

- **Mathematical statistics and probability theory**
  - Uncertainty estimation, representation of noisy data

- **Linear algebra**
  - Compact representation of linear data transformations
  - Dimension reduction methods

- **Other areas of mathematics**
  - Properties of functions, optimization theory, convergence and approximation guarantees

- In addition, **knowledge of the subject area** of machine learning application is required.
  - Physics, linguistics, geology, genetics, medicine, etc.

</v-clicks>

---

# Why do we need math in machine learning?
<br>
<v-clicks>

### Suppose your model shows $81\%$ accuracy
<br>

### <span style="color:#FA9370">Now what?</span>

* Is this good/bad, useful/useless?
* Can it be improved?
* If so, to what extent?
<br>
<br>

### Machine learning and statistical theory provide answers to these questions
</v-clicks>

---

# Why do we need Math in Machine Learning?

### Mathematics helps:

<v-clicks depth="2">

* To choose:
  * **the right algorithm** for solving a problem
  * **the best hyperparameters**
  * **validation** (verification) strategies for a model

* Recognize and eliminate **underfitting** and **overfitting**

* **Eliminate problems** with poor and ambiguous results

* Assess forecast uncertainty

* **Optimize algorithms** and build effective program code
  * Models must be (economically) viable
</v-clicks>

<v-click>

#### <span style="color:#FA9370">Every decision you make in machine learning requires understanding</span>
</v-click>

---

# What is Machine Learning?
<br>
<br>
<br>
<br>

## Machine learning is a set of methods<br><br> for finding <span v-mark="{ at: 2, color: 'orange', type: 'box' }">**unknown functions**</span> from observations

---

# Selection of Unknown Functions

<div class="grid grid-cols-[3fr_2fr] gap-15">

<div>

* Need to match the appropriate function to the observed data
* Problems:
  * There are infinitely many such functions
  * Which one is the “right” one?
  * It is often impossible to manually search the data
    * Millions of observations
    * Thousands of features

<br>

#### The problems to which machine learning is applied<br> <span v-mark="{ at: 1, color: 'orange', type: 'underline' }">do not have</span> a "correct" solution
<br>
<div style="color:#b3b3b3ff; font-size: 12px">Image source: <a href="https://xkcd.com/2048/">https://xkcd.com/2048</a></div>
</div>
<div>
<figure>
  <img src="/curve_fitting_2x.png" style="width: 280px !important;">
</figure>
</div>
</div>

<!--
Machine learning is nothing more than fitting the right function to the observed data.
But, come on! There are infinitely many such functions. In the comic on the right, the red lines show 12 functions describing the same data. How different they are! Which one should you choose? Often manual selection of functions is not possible.

An interesting consequence of all this is that problems to which machine learning is applied often have no correct or reference solution.
-->

---

# Even 2D functions can be complicated

<figure>
  <img src="/wireframe-mesh-surface-d-illustration-127415228.jpg" style="width: 660px !important; position:relative; left: -20px">
  <figcaption style="color:#b3b3b3ff; font-size: 11px; float: left;"><span>Image source: <a href="https://www.dreamstime.com/wireframe-mesh-surface-d-illustration-image127415228">https://dreamstime.com/wireframe-mesh-surface-d-illustration-image127415228</a></span>
    </figcaption>
</figure>

---

# Example of Machine Learning Task

<br>
<div class="grid grid-cols-[3fr_3fr] gap-5]">
<div>
<figure>
  <img src="/mj_sales_dataset.jpg" style="width: 350px">
  <figcaption style="color:#b3b3b3ff; font-size: 11px; position: absolute;">Image source: Midjourney 6
    </figcaption>
</figure>
</div>
<div>

### [Advertising](https://www.statlearning.com/s/Advertising.csv) dataset
<br>

### **Goal** - increase sales of a certain product depending on the advertising budget
</div>
</div>
---

# Example of Machine Learning Task

### **Goal** - to increase sales of a certain product

* We have a budget for advertising on television, radio, and in newspapers (indicators)
* It is necessary to determine the relationship between the advertising budget and sales
* Which indicator has the strongest influence on the target variable?
<div class="grid grid-cols-[5fr_3fr] gap-5]">
<div>

* How should the budget be allocated<br>
to increase sales?<br>

<figure>
  <br>
  <img src="/stat_learning_example_1.png" style="width: 380px !important">
</figure> 
</div>
<div>
  <figure>
    <img src="/stat_learning_example_2.png" style="width: 300px !important">
  </figure>   
</div>
</div>

---

# What is Machine Learning?

### In general:
<v-clicks depth="2">

* Let $X$ be a **data matrix** with $N$ observations (points, cases)<br> and $p$ features (predictors, features):
$$X = [X_1, X_2, ..., X_p] \in \R^{N \times p}$$

* Let $Y$ be a vector of **answers** with $N$ corresponding labels: $Y \in \R^N$

* We want to find a **fixed** but **unknown** function $f$:
$$Y = f(X) + \varepsilon$$

* Where $\varepsilon$ is an **independent** random variable with the following properties:
$$\varepsilon \perp\!\!\!\!\perp X_i, ~~ \mathbb{E} \varepsilon = 0, ~~ \mathbb{V} \varepsilon < \infty$$

</v-clicks>

---

# Why to Estimate $f$?

<v-clicks depth="3">

<div class="grid grid-cols-[2fr_1fr] gap-1">

<div>

* Prediction
  * $\hat{f}$ is an uninterpretable **black box**
  * We are looking for the best **predictions** for the available $X$
  * The goal is to reduce **avoidable** error
</div>
<div>
  <figure>
    <img src="/black_box.jpg" style="width: 150px !important">
  </figure>
</div>
</div>

<div class="grid grid-cols-[2fr_1fr] gap-1">

<div>

* Inference
  * $\hat{f}$ is an interpretable **white box**
  * We want to:
    * understand how **sensitive** $Y$ is to changes in $X$
    * find **important** features
    * determine whether $f$ is a **linear** or more complex function
      * Linear models are easier to interpret
</div>
<div>
  <figure>
    <img src="/white_box.jpg" style="width: 150px !important">
  </figure>
</div>
</div>
</v-clicks>

---

# How to Estimate $f$?

* Most machine learning methods estimate $\hat{f}$<br> from **training observations** $(x_i^\prime, y_i^\prime) \in \R^{p+1}$
  * $x_i^\prime$ - $i$-th vector of feature values

<div>
  <br>
<figure>
  <img src="/data_matrix_2.png" style="width: 600px !important">
</figure>   
</div>

---

# How we Estimate Errors?

<v-clicks>

* In **regression** problems (i.e., where $Y$ is a continuous variable), we use the square of the difference (or **mean square error**, $MSE$):
$$\mathcal{L}_{MSE} (y, f(X)) \overset{\Delta}{=} \big(y - f(X)\big)^2$$

* In **classification** problems (i.e., where $Y$ is a categorical variable),<br> we use **Accuracy** (or **error rate**, or **loss** $0-1$):
$$\mathcal{L}_{acc} (y, f(X)) \overset{\Delta}{=} I\big(f(X) \neq Y \big)$$

* In both cases, we average the errors across all observations, assuming that they are **i.i.d.**<br> (= independent and identically distributed):<br>
$~~~~~~~~~~~~~~~~~~~~~~~~~~\mathcal{L} (D, f) \overset{\Delta}{=} \mathbb{E}_{(X,y) \sim D} \mathcal{L}\big(y, f(X)\big) \approx \frac{1}{N}\sum\limits_{i=1}^N \mathcal{L}\big(y_i, f(X_i)\big)$
</v-clicks>

---

# Reducible and Irreducible Errors

* Often, $f \in \mathcal{F}$, a certain **family** (**class**) of functions
* $\mathcal{F}$ can be constant, stepwise, linear, quadratic, ...
<div class="grid grid-cols-[5fr_3fr] gap-9]">
<div>

* The choice of $\mathcal{F}$ determines the **eliminable** error.
  * Example: $\hat{f}_{\mathrm{step}}$ produces larger errors than $\hat{f}_{\mathrm{linear}}$.
  * Example: $\hat{f}_{\mathrm{linear}}$ produces larger errors than $f$.

* **Irreducible** error (**noise**) $\varepsilon$ arises due to:
  * omitted variables
  * measurement errors
  * ...
</div>
<div>
  <br>
<figure>
  <img src="/ISLP_figure_2.2_step.png" style="width: 300px !important">
</figure>   
</div>
</div>

---

# Error Decomposition

* If we assume fixed  $\hat{f}$ and $X$, then for $\hat{Y} := \hat{f}(X)$, the mean square error will be:<br><br>
$\mathbb{E}\big[Y - \hat{Y}\big]^2 = \mathbb{E}\big[f(X) + \varepsilon - \hat{f}(X)\big]^2 =
\color{grey}\underbrace{\color{green} \big[f(X) - \hat{f}(X) \big]^2}_{\mathrm{reducible~error}}
\color{#006}{~~~~~~+~}
\color{grey}\underbrace{\color{red} \mathbb{V}\varepsilon}_{\mathrm{irreducible~error}}$<br>

<br>

* Where $Y$ is a random variable, since it is a linear combination of random variables $\varepsilon$
  * $\mathbb{E}$ is expressed as a probability density function $Y$ (or $\varepsilon$)
  * $\mathbb{V}\varepsilon$ is the variance of $\varepsilon$

---

# Example of a Machine Learning Task
### **Goal**: to find the relationship between income and length of education
<br>
<div class="grid grid-cols-[5fr_5fr] gap-5]">
<div v-click>
<figure>
  <img src="/ISLP_figure_2.2_left.png" style="width: 320px !important">
</figure> 
</div>
<div v-click>
<figure>
  <img src="/ISLP_figure_2.2_right.png" style="width: 320px !important">
</figure>   
</div>
</div>

---

# Example of a Machine Learning Task
### **Цель**: find the relationship between income and length of education and seniority
<br>
<div class="grid grid-cols-[5fr_5fr] gap-5]">
<div v-click>
<figure>
  <img src="/ISLP_figure_2.3.png" style="width: 320px !important">
</figure> 
</div>
<div v-click>
<figure>
  <img src="/ISLP_figure_2.4.png" style="width: 320px !important">
</figure>   
</div>
</div>
<br>
<v-clicks>

* The process of evaluating $f$ is called **model fitting**
* To evaluate the quality of training, the **residual** $r(x) = y - f(x)$ is used
</v-clicks>