# Similarity Searching and QSAR Model Interpretation in Drug Discovery

# What I have done in this project
## Similarity Searching:
Identifying chemical compounds with similar structures using Tanimoto coefficient and Graph Edit Distance algorithms. 
## QSAR Classification: 
Predicting biological activities of chemicals based on their structure. 
## QSAR Regression:
Estimating toxicity levels of chemicals using Regression models.

# Why I have done this project
## Similarity Searching:
(i) Finds molecules similar to known compounds.

(ii) Helps in drug discovery and creating new chemicals.

(iii) Saves time and resources.
## QSAR Classification:
(i) Classifies the biological activity of compounds.

(ii) Determines if a compound is useful or harmful.

(iii) Guides safer chemical development.
## QSAR Regression:
(i) Predicts chemical toxicity.

(ii) Assesses harm to people, animals, and the environment.

(iii) Identifies dangerous substances early.

# How I have done this project
## Similarity Searching:
(i) Calculated molecular fingerprints.

(ii) Used Tanimoto similarity coefficients to find the top 5 similar drugs for each drug.

(iii) Calculated graph edit distance and found the top 5 similar drugs based on those distances.
## QSAR Classification:
(i) Evaluated Random Forest Classifier and Support Vector Classifier.

(ii) Classified the biological activity of compounds.
## QSAR Regression:
(i) Evaluated Random Forest Regressor and Support Vector Regressor.

(ii) Predicted the toxicity of compounds.

# Some Important Keywords 
## SMILES : Simplified Molecular Input Line Entry Specification

### Formation:
(i) Atoms are represented by their atomic symbols.

(ii) Uppercase symbols denote aliphatic atoms, lowercase denote aromatic atoms.

(iii) Hydrogen atoms are often suppressed.

(iv) Bonds are represented using "=" for double bonds and "#" for triple bonds.

(v) Single and aromatic bonds are not explicitly represented, except in special cases (e.g., non-aromatic single bond in biphenyl uses "-").

(vi) 'Walk' through the structure so all atoms are visited once.

(vii) For rings, break one bond and indicate the ring with an integer on the broken bond's atoms.

(viii) Branch points are indicated with brackets.

(ix) Chirality and geometrical isomerism are included in the notation.

  #### (a) Chirality:
  Use "@" for absolute stereochemistry (e.g., NC@HC(=O)O and NC@@HC(=O)O for alanine stereoisomers).
  #### (b) Geometrical isomerism:
  Use slashes ("/" and "") for E/Z or cis-trans isomerism (e.g., C/C=C/C for trans-butene and C/C=C\C for cis-butene).
### Examples:
Methane(C), Ethane(CC), 2- methyl propane(CC(C)C), Cyclohexane(C1CCCCC1), Benzene(c1ccccc1), Acetic Acid (C(=O)O) etc.

## Molecular Fingerprint:
(i) Helps differentiate one molecule from another.

(ii) Represented as a binary string (contains only 0 and 1).

(iii) '0' indicates absence of a particular substructural fragment.

(iv) '1' indicates presence of a particular substructural fragment.

## Tanimoto Similarity:
Tanimoto coefficient = c/(a+b-c) 

where 'a' represents total number of "1" in molecule A, 'b' represents total number of "1" in molecule B and 'c' represents total number of "1" common to both A and B. The value of the Tanimoto co-efficient ranges from zero to one. A value of one indicates that the molecules have identical fingerprint representations (note that this does not necessarily mean they are identical molecules) and a value of zero indicates that there is no similarity (i.e. there are no bits in common between the two molecules).

## Graph Edit Distance:
### Chemical Similarity:

(i) Chemicals are similar if their structures are similar.

(ii) Graph edit distance (GED) is used as the metric for chemical similarity.
### Graph Edit Distance (GED):

The smallest total number of edits needed to make one graph isomorphic to another.
Edits can involve:
#### Node Insertion:
Adding a new node.
#### Node Deletion: 
Removing an existing node.
#### Node Substitution:
Changing the label or attributes of an existing node.
#### Edge Insertion:
Adding a new edge between two nodes.
#### Edge Deletion:
Removing an existing edge between two nodes.
#### Edge Substitution:
Changing the label or attributes of an existing edge.

# Result
## Molecular Fingerprint Similarity:
![image](https://github.com/user-attachments/assets/f8f4a7eb-1ebe-4316-b285-8dce90e51a1f)
There are 1357 Drugs in my dataset. I have evaluated top 5 similar SMILE for all of them. Here I have shown the top 5 similar SMILE for Hydroxocobalamin only.
### Observation
(i) No single method is best for all molecules.

(ii) Each method focuses on different molecular features (e.g., atom connections, functional groups, 3D shapes). 

(iii) Using multiple fingerprint methods together improves accuracy and reliability of similarity searches.

## Graph Edit Distance Similarity:
![image](https://github.com/user-attachments/assets/1550ec83-2f4c-4a65-baea-1200b7f4b5b1)
There are 1357 Drugs in my dataset. I have evaluated top 5 similar SMILE for all of them. Here I have shown the top 5 similar SMILE for Hydroxocobalamin only.

## QSAR Classification:
![qsar_classification](https://github.com/user-attachments/assets/ea06803f-427f-4ff5-b412-d083a76cc7c6)

## QSAR Regression:
![qsar_regression](https://github.com/user-attachments/assets/44e9239c-01b2-4933-8645-f3da63aeb5af)




