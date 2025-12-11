Optimization Shapes Neural Network Learning: A Controlled Comparison of SGD and Adam
Overview

This repository contains the code and tutorial developed for a university machine learning assignment investigating how optimisation algorithms influence neural network learning. The project demonstrates that optimisation is not a neutral training component: even with identical architectures, data, and initial parameters, different optimisers can lead to distinct convergence dynamics, learned representations, and generalisation behaviour.

The tutorial focuses on a controlled comparison between stochastic gradient descent (SGD) and Adam, highlighting implicit optimisation bias through both quantitative and visual analysis.

All figures and results in the tutorial are fully reproducible using the provided Jupyter Notebook.

Repository Structure
├── notebooks/
│   └── jaseer_ml_code.ipynb
│
├── figures/
│   └── (generated figures – optional)
│
├── tutorial/
│   └── Optimisation_Shapes_Learning.pdf
│
├── README.md
└── LICENSE

Topic Focus

Model: Multilayer Perceptron (MLP)
Core concept: Implicit optimisation bias

The tutorial examines:

how optimisation trajectories differ between SGD and Adam

convergence speed and stability

generalisation performance under identical conditions

parameter norm differences as a proxy for solution geometry

qualitative differences in learned decision boundaries

The study emphasises that optimiser choice is a modelling decision with implications for reproducibility, interpretation, and deployment.

Dataset

A synthetic two-dimensional binary classification dataset is generated using sklearn.datasets.make_moons.

Number of samples: 1,200

Number of features: 2

Classes: 2 (balanced)

The low-dimensional dataset allows direct visualisation of decision boundaries while still requiring nonlinear classification.

Requirements

To run the notebook, Python 3.9 or later is recommended, along with the following packages:

pip install numpy matplotlib scikit-learn tensorflow

How to Run

Clone the repository:

git clone https://github.com/Jasser-ds/machine-learning.git
cd machine learning



Open the Jupyter Notebook:

jupyter notebook optimizer_bias_analysis.ipynb


Run all cells from top to bottom to reproduce:

training and validation loss curves

accuracy comparisons

weight norm analysis

decision boundary visualisations

Experimental Design Notes

Both models use identical architectures

Initial weights are fixed and shared across optimisers

Training data, learning rate, batch size, and number of epochs are identical

The optimiser is the only variable

This design ensures that observed differences arise solely from optimisation dynamics.

Accessibility Considerations

Plots use high-contrast, colour-blind–safe visual styles and include clear labels and titles. Decision boundaries are accompanied by axis annotations, and tables do not rely on colour encoding. The tutorial document uses structured headings to support screen readers.

License

This repository is released under the MIT License. The material may be used, modified, and redistributed with appropriate attribution.
