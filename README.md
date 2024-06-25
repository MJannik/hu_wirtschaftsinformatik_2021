**Asymmetric error costs in regression models**

A vast amount of data is collected and processed to provide better support for decision-making in industries, such as finance, marketing, retail and medicine. The major problem with real-world data mining applications lies within the traditional minimization of prediction errors, which assumes equal over- and underprediction costs. This assumption generally does not hold in practice. In a binary classification problem, incorrectly predicting a fraudulent transaction as “non-fraud” leads to higher costs than predicting a legitimate transaction as “fraud”. In a regression problem, underestimating the resale price of a pre-owned car is associated with opportunity cost of lost sales, whereas systematic overestimation can significantly reduce revenue and increase expenses, leading to business bankruptcy. On an individual level, we perceive being 20 minutes late for an exam worse than arriving 20 minutes early.

In machine learning (ML) loss (or, strictly speaking, cost) functions are used for evaluating how well the model predicts the expected outcome using a given set of values. A cost function takes in the model’s parameters and returns the costs as a scalar value, which helps to determine the best candidate for a solution (Brownlee and Machine Learning Mastery, 2019). It must therefore reflect the difference in costs associated with each type of prediction error. 

In order to obtain a better fit between modelling and decision objectives, several efforts have been made to circumvent the restrictions imposed by symmetric loss functions. Some researchers have focused on designing new forms of loss functions that are more capable of accounting for the cost imbalance. The examples of proposed functions include LLC (asymmetric linear) loss, QQC (asymmetric quadratic) loss and LEC (linear on one side and exponential on the other) loss designed by Varian (1975). More recently, other researchers introduced an alternative approach to cost-sensitive regression – post hoc tuning. In comparison to other approaches, which incorporate asymmetric costs during model training, the post hoc process is performed after the model has already been trained. 

In this article, we want to take a closer look at the post hoc tuning method offered by Bansal et al. in 2008 for regular regression models. We minimize average misprediction cost (AMC) under asymmetric loss for linear regression model post hoc by adjusting the prediction by a certain amount provided by the markdown algorithm. Our experiments are consistent with previous results demonstrated by Bansal et al. in 2008. We achieve a significant reduction of the AMC of models learned with linear regression as a base method using LLC and QQC loss functions. Our experiments also support the claim that “the degree of cost reduction increases as the difference between the unit costs of the two types of errors (overprediction and underprediction) increases“ (Bansal et al. 2008) as demonstrated in Section 5.  

The objectives of this reserach are threefold: (i) to give an overview of the previous research on the topic of cost-sensitive regression problems; (ii) to test an algorithm (Bansal et al, 2008) for tuning the regression model post hoc in the context of the “UK Used Car” data set; and (iii) to derive the potential of this approach for real-world applications.
