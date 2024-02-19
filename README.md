Problem Statement:

Based on specific factors, the effectiveness of each medicine
in preventing protein development is evaluated. In this experiment, we employed the Inhibitory Concentration (IC 50)
value as a marker for analyzing the bioactivity of a specific
medicine. The IC 50 value is a quantitative measure of how
much a drug is needed to block a given biological process
(in this case, multiplication of the EGFR protein) by 50percent. To obtain the canonical notation of a drug’s molecular
formulae, we use the ChEMBL dataset, a chemical library of
bioactivity molecules.
The EGFR constantly ”grows” in cases of lung cancer that
tests positive for the EFGR gene due to a gene mutation or
malfunction. As a result, cells proliferate out of control the
root of which is cancer. Chemotherapy is one of the best
ways to treat cancer, but it also has some negative effects,
like fatigue, hair loss, and changes in appetite. Therefore,
many medications are being investigated to see if they can
prevent the EGFR protein from proliferating as an alternative
to chemotherapy.
Feature selection helps to reduce the dimensionality of the
problem, making it easier to work with, and can improve the
performance and generalisation ability of machine learning
models by reducing the risk of overfitting. In this case there
are a lot of features which determine the specifications of a
particular molecule which makes it difficult to predict which
characteristic might affect a cell from cancer. It plays an important tool for improving the efficiency and effectiveness of
machine learning models, especially in problems with highdimensional input data. Training models on all the available
characteristics may be computationally expensive and timeconsuming when working with high-dimensional data. We
may decrease the computational demands and increase the effectiveness of model training by just choosing the most crucial
characteristics. Even when some data is absent, we can still
provide good predictions by choosing the most useful characteristics. A lot of data is present in the world regarding the
particular protein molecule present in every species of living
organisms. It is quite difficult to extract the required targeted
molecule which might affect the living being’s conditions of
survival.



The methodology for this project was divided into four parts:-
1. Collection of Data.
2. Exploratory Data Analysis.
3. Calculating Molecular Fingerprints.
4. Model construction and feature engineering.
A] The data gathering method begins with a search for
’EGFR’ molecules in the ’Chembl’ database. EGFR (epidermal growth factor receptor) is a protein that plays an important
role in the regulation of cell growth and division. Mutations
in EGFR are associated with a variety of cancers.
B] The data is then selected where standard type is IC50.
IC50 is a commonly used measure of the potency of a drug
compound, and it represents the concentration at which the
compound inhibits 50% of the target protein’s activity. Therefore, IC50 values are useful for determining the efficacy of a
drug compound in inhibiting a specific target protein.
C] Predictors such as molecular weight, molecular LogP
value, Number of Hydrogen bone donors and number of hydrogen bone acceptors is calculated from the Lipsinki package.
Usefulness of these predictors:
1. 500 Daltons as the molecular weight (MolWt) to ensure that
the molecule is small enough to be absorbed and distributed
in the body.
2. A partition coefficient (MolLogP) of 5 or less to ensure that
the molecule has appropriate lipophilicity and hydrophilicity
to cross cell membranes.
3. 5 or fewer hydrogen bond donors (NumHDonors) to avoid
excessive hydrogen bonding, which can lead to poor permeability.
4. 10 or fewer hydrogen bond acceptors (NumHAcceptors)
to avoid excessive hydrogen bonding, which can lead to poor
permeability.
D] After calculating the above, pIC50 is calculated. The
function pIC50() converts the IC50 values in the input dataframe
to pIC50 values (negative log of the molar IC50 concentration), and adds the resulting pIC50 values as a new column
to the input dataframe. The standard-value-norm column is
used as input to the pIC50() function, which is created in the
norm-value() function by replacing any IC50 values greater
than 100000000 with 100000000.
E] The next phase involves the conversion of the canonical
formula into its corresponding molecular fingerprint with the
help of the other descriptors.
F] The program standardizes the data by removing any
extraneous salts or chemical components from the molecule.
G] The algorithms and methods we are looking forward to
implement use are Logistic Regression, Ada-Boost Regressor,
Bagging Regressor and Random Forest Regressor.
Our project aims to compare the methods and best models
out there to to predict the efficiency of a therapy in preventing
the development of cancer cells caused by a deficiency in
EGFR protein.
