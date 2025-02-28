# **Causal Inference on UCI Census Income Dataset**

## **Overview**
This project applies **causal inference techniques** to the **UCI Census Income Dataset** to estimate whether **graduate education increases the probability of earning more than $50K per year**. The analysis leverages **causal discovery, propensity score matching, regression-based causal estimation, and meta-learning techniques** to derive robust insights.

## **Key Objectives**
- Identify **causal relationships** between **education level and income**.
- Estimate the **causal effect of having a graduate degree on income**.
- Compare different causal inference techniques:
  - **Causal Discovery Methods**: PC, GES, GIES, LiNGAM
  - **DoWhy-based causal modeling**
  - **Propensity Score Matching, Stratification, and Weighting**
  - **Regression-based causal effect estimation**: Linear Regression, Double ML, X-Learner
  - **Meta-learners**: T-Learner using Random Forest

## **Methodologies**

### **1️⃣ Causal Discovery**
- Used **Graph Lasso** to estimate the skeleton of the causal graph.
- Applied **PC, GES, GIES, and LiNGAM** methods to infer causal relationships.
- Visualized **causal graphs** to understand dependency structures.

### **2️⃣ DoWhy-based Causal Inference**
- Defined a **causal model** with:
  - **Treatment**: Graduate degree
  - **Outcome**: Income > $50K
  - **Confounder**: Age
- Used **graphical representations** to validate causal assumptions.
- Estimated causal effects using **backdoor adjustment** and **metalearners**.

### **3️⃣ Propensity Score Matching (PSM)**
- Implemented **three different propensity score methods**:
  - **Matching**: Finding individuals with similar propensity scores.
  - **Stratification**: Dividing samples into strata based on scores.
  - **Weighting**: Adjusting for treatment assignment probability.
- Compared the **Average Treatment Effect (ATE)** across methods.

### **4️⃣ Regression-based Causal Effect Estimation**
- Applied **Linear Regression** to estimate causal effects.
- Used **Double Machine Learning (DML)** for **robust estimation**.
- Implemented **X-Learner** with **Decision Trees** to capture heterogeneous treatment effects.

## **Key Findings**
✅ **Graduate education has a statistically significant positive impact on income.**  
✅ **Different causal methods yield varying effect sizes,** but the overall direction remains consistent.  
✅ **Machine learning-based methods (DML, X-Learner) provide more flexible and robust estimates** than traditional regression.  
✅ **Propensity score methods reduce bias**, but require careful selection of confounders.  

## **Tools & Technologies**
- **Programming Language:** Python
- **Libraries:** `DoWhy`, `EconML`, `CausalDiscoveryToolbox`, `Scikit-Learn`, `Matplotlib`
- **Graph-based Causal Discovery:** PC, GES, GIES, LiNGAM
- **Propensity Score Methods:** Matching, Stratification, Weighting
- **Machine Learning-based Causal Estimation:** Meta-Learners, Double ML

## **Conclusion**
This project showcases **how causal inference techniques can estimate treatment effects** from observational data. By applying multiple methodologies, we derive **robust insights** into the role of education in determining income levels.

---


### **📊 Results & Visualizations**
Sample causal graph (Generated using PC Algorithm):

![Causal Graph](./images/causal_graph.png)  

---

### **🔗 References**
- UCI Census Income Dataset: [https://archive.ics.uci.edu/ml/datasets/census+income](https://archive.ics.uci.edu/ml/datasets/census+income)
- DoWhy Library: [https://microsoft.github.io/dowhy/](https://microsoft.github.io/dowhy/)
- EconML Library: [https://econml.azurewebsites.net/](https://econml.azurewebsites.net/)
- Causal Discovery Toolbox: [https://fentechsolutions.github.io/CausalDiscoveryToolbox/html/index.html](https://fentechsolutions.github.io/CausalDiscoveryToolbox/html/index.html)

---

