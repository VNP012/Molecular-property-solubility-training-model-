# Molecular-property-solubility-training-model-
Training a model to predict and analyze the solubility of a molecule and reference it to the true solubility. 
Molecular Solubility Predictor

This project demonstrates how to predict the aqueous solubility of small molecules using a deep learning model trained on SMILES strings. It uses the ESOL dataset and a 1D convolutional neural network implemented in TensorFlow/Keras.

What is Solubility and Why It Matters
Solubility is a key physicochemical property that affects how a molecule behaves in biological systems, including:

Drug absorption and bioavailability
Compound formulation in pharmaceutical development
Environmental transport and degradation
Chemical reactivity in lab synthesis
Accurate prediction of solubility from molecular structure is a long-standing challenge in computational chemistry and cheminformatics. Experimental measurements are expensive and time-consuming, so computational models provide a valuable tool for early-stage screening.

How This Project Helps
This model enables rapid, low-cost prediction of molecular solubility using only SMILES strings as input. This has real value in:

Pharmaceutical R&D: Pre-screening drug candidates for solubility before synthesis
Materials science: Designing new molecules or polymers with target solubility profiles
Academic research: Studying how structural features influence solubility
Education: Demonstrating how machine learning models can interpret molecular representations
Method Overview
Dataset: The ESOL dataset contains 1128 drug-like molecules with experimentally measured solubility values.
Representation: Molecules are represented as SMILES strings and tokenized at the character level.
Model: A 1D CNN learns patterns in the token sequences and maps them to continuous solubility values.
Training: The model is trained with mean squared error loss and validated on a held-out split.
Evaluation: Predictions are visualized against ground truth using a scatter plot to assess accuracy.
Model Architecture
Embedding layer: Converts token indices into dense vectors
1D Convolution layer: Captures local patterns in the sequence
GlobalMaxPooling: Aggregates the sequence to a fixed-size vector
Dense layers: Maps the features to a scalar solubility output
Project Outcomes
Achieves low mean absolute error on validation data
Shows strong correlation between predicted and true solubility values
Demonstrates the viability of sequence models for molecular property prediction
Limitations
Limited to the range of molecules and solubility values in ESOL
Model does not explicitly capture 3D structure or stereochemistry
Performance can likely be improved with RNNs, transformers, or GNNs
How to Use This Project
Input a SMILES string of any small molecule
The trained model will output a predicted solubility value
Integrate it into screening pipelines or visualization tools
Future Improvements
Extend to larger datasets like FreeSolv, Lipophilicity, or ChEMBL
Use pre-trained models like ESM or ChemBERTa for richer embeddings
Visualize molecular substructure contributions to solubility
Convert into an interactive web application with Streamlit or Gradio

Note: The code is applicable to Google Colab runtime type CPU and dependancies and python versions installed. The code might need to be changed according to versions or dependancies. 
