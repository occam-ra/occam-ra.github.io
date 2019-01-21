---
title: What Is OCCAM?
format: post
---

## What is OCCAM?

OCCAM is software that implements [Reconstructibility Analysis](what-is-reconstructibility-analysis.html). OCCAM combines data mining, machine learning, and statistical analysis in a unique way which lets a user quickly understand the structure of their data, evaluate many possible models, and compare those models under statistical and information-theoretic criteria. Once a model is selected, OCCAM will fit that model to the data, identifying a simplified representation of the data structure that still preserves its essential features, and allow the user to explore and understand variable relationships and make predictions.

### How does it work?

A typical OCCAM workflow might look like this:

* Load some data, specifying search options such as the reference model for comparison, types of models to consider, threshold for statistical significance, and depth of search in the [lattice of structures](https://www.pdx.edu/sysc/sites/www.pdx.edu.sysc/files/overview.pdf)
* Use the search results to quickly compare a list of possible models of the data by their entropy or uncertainty, degrees of freedom, statistical significance, AIC and BIC (information-theoretic criteria which compare models by incorporating both the difference in information content and complexity), prediction accuracy, and other measures. ([Example search output](img/occam-search-example.png))
* Once a model is selected, fit that model to the data, and examine it in detail: dependent and independent variable relationships, possible variable states (and the model's prediction accuracy for each state), prediction rules for each state, statistical significance, and more. ([Example fit output](img/occam-fit-example.png))
* Put this insight to use in making predictions, simplifying complex problems while preserving essential features of the data, and answering your important analytical and research questions.
