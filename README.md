# Predicting DNA Type and Taxon from Codon and Amino Acid Frequencies

## Background

Nucleotides encode amino acids in blocks of three, called codons.  The four distinct nucleotides produce 64 possible codons, which do not occur with equal frequency; this is codon usage bias.

A preprint paper - ['Codon usage bias levels predict taxonomic identity and genetic composition'](https://www.biorxiv.org/content/10.1101/2020.10.26.356295v1.full) - applied various ML models to predict taxon and DNA type from codon frequencies.  This project repeats this work, and extends it by also using amino acid frequencies as predictors.

Data from this study were made freely available at http://archive.ics.uci.edu/ml/datasets/Codon+usage.  These data were [wrangled](/Capstone%202%20Data%20Wrangling%20v%201.ipynb) and [preprocessed](/Capstone%202%20Pre-Processing.ipynb) to remove sparse categories and encode amino acid frequencies.

## Exploratory Data Analysis

Some [EDA](/Capstone%202%20EDA%20v1.ipynb) tended to confirm the reliability of the data, and demonstrated significant correlations between both codon and amino frequencies and outcomes.  A quick perusal also shows that there's plenty of variation across categories for these frequencies.

## Models

Five families of [models](/Capstone%202%20Modeling.ipynb) were applied:  k-Nearest Neighbors, Random Forest, eXtreme Gradiant Boosting, Multi-Layer Perceptron neural net classifer, and Naive Bayes.  Each of these was optimized to some extent; for the more sophisticated models, which have larger hyperparameter spaces, Hyperopt was used. 

## Conclusions

The assumption that DNA type and taxonomic category could be predicted using amino acid frequencies was confirmed. Strangely, this didn't provide any computational savings, even neglecting the preprocessing time.  Overall, the best model was the MLP classifier.  [Results](/Capstone%202%20Results.ipynb) are discussed in detail in the [documentation](/capstone%202%20documentation.pdf) and [PowerPoint presentation](/capstone%202%20presentation.pptx).

Much thanks to my advisor, Jeremy Cunningham, for his patience and assistance.




