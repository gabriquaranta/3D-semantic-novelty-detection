# 3D Semantic Novelty Detection

The code and paper result have been developed in collaboration with [George Florin Eftime](https://github.com/geoxRegex) and [Giulio Maselli](https://github.com/giuliomsl).

The project centers on 3D semantic novelty detection, aiming to differentiate whether a given data sample belongs to a predefined nominal distribution of known semantic classes.

Traditional machine learning models often assume that training and test data stem from the same distribution, which may not hold true in real-world scenarios characterized by distributional shifts. These shifts can involve new object categories or data from new domains, leading to out-of-distribution (OOD) data that pose risks, particularly for autonomous agents like self-driving cars. Developing robust models capable of effectively discriminating among known classes while detecting unknown categories is essential yet challenging.

The research conducted in "3DOS: Towards 3D Open Set Learning" enables us to assess the performance of different models and backbones in this context, offering a comprehensive analysis of their effectiveness when confronted with data falling outside the training distribution. The benchmark includes tracks for Synthetic, Real to Real, and Synthetic to Real scenarios, mimicking real-world deployment conditions.

Leveraging the 3DOS benchmark, particularly in the Synthetic to Real scenario, where nominal data samples are synthetic (CAD model-derived) and test samples are real-world point clouds from sensor scans, the objective is to distinguish between in-distribution (known semantic classes) and out-of-distribution (unknown) samples.

In this project, our focus is on a subset of this benchmark, specifically the Synthetic to Real Scenario. We re-evaluate the behavior of two backbones, DGCNN and PointNet, in this track. Additionally, we conduct failure case analysis for DGCNN and explore the performance of a pre-trained model, OpenShape, leveraging its large scale to extract feature representations of both nominal and test data distributions.

## How to run our code

Four notebooks are available to run the code, each can be run indipendentely to obtain the results. The notebooks are the following:

1. `dgcnn_baselines.ipynb`: This notebook contains the code to train and evaluate the DGCNN model on the 3DOS benchmark.

2. `pointnet_baselines.ipynb`: This notebook contains the code to train and evaluate the PointNet model on the 3DOS benchmark.

3. `openshape.ipynb`: This notebook contains the code to evaluate the OpenShape model on the 3DOS benchmark.

4. `dgcnn_sr2_failcases.ipynb`: This notebook contains the code to conduct failure case analysis for the DGCNN model.
