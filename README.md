## Sampling
Sampling is a method used to glean insights about a population by analyzing statistics from a representative subset, sparing the need to examine every individual. To tackle an initial dataset imbalance—763 non-fraudulent cases and only 9 fraudulent cases—an oversampling approach was implemented. This involved generating additional instances of the minority class (fraudulent cases) to match the majority class (non-fraudulent cases), resulting in a balanced dataset consolidated into a single data frame.

The following sampling techniques were utilized:

- Simple Random Sampling: Random selection of samples from the population.
- Systematic Sampling: Regular interval selection after a random start.
- Cluster Sampling: Randomly selecting clusters from the population.
- Stratified Sampling: Division of the population into subgroups based on certain criteria.
- Bootstrap Sampling: Resampling with replacement to create multiple samples from the original dataset.

Following the generation of five distinct samples using these techniques, five models were applied to each sample. The accuracies of each model for a given sample are summarized in the following table:

| Sample Technique      | Logistic Regression | SVM        | Naive Bayes      | Decision Trees   | Stochastic Gradient |
|-----------------------|---------------------|------------|------------------|------------------|---------------------|
| Simple Random Sampling| 0.8701              | 0.8831     | 0.7013           | 0.9610           | 0.8701              |
| Systematic Sampling   | 0.9060              | 0.9597     | 0.7383           | 1.0000           | 0.8188              |
| Cluster Sampling      | 0.9612              | 0.9709     | 1.0000           | 1.0000           | 0.9806              |
| Stratified Sampling   | 0.8731              | 0.9478     | 0.7313           | 0.9776           | 0.8806              |
| Bootstrap Sampling    | 0.9250              | 0.9750     | 0.6000           | 0.9625           | 0.9750              |

In above table, each row corresponds to a sampling technique, and each column represent the accuracy achieved by each model applied to the respective sample generated using that respective technique.
<br>
### The RANDOM FOREST outperformed all other models when applied to Stratified Sampling Technique.
