# HardnessMapDesign

Code for "Deep Learning Virtual Indenter Maps Nanoscale Hardness Rapidly, Non-destructively, Revealing Mechanism, and Enhancing Bioinspired Design"

Reference: A.J. Lew, C.A. Stifler, A. Cantamessa, A. Tits, D. Ruffoni, P.U.P.A. Gilbert, M.J. Buehler, Deep Learning Virtual Indenter Maps Nanoscale Hardness Rapidly, Non-destructively, Revealing Mechanism, and Enhancing Bioinspired Design, Matter, 2023

1.) Setup environment with: conda env create -f environment.yml

2.) Generate labeled, formatted dataset from original PIC images and hardness values with ‘HardnessDesign-DatasetCreation.ipynb’. 

3.) Train deep residual neural network model on image regression task with ‘HardnessDesign-ResNetTraining.ipynb’. A sample pretrained model is provided in ‘data/models/res_cnn_03_11_18_54/saved_model.pb’.

4.) The trained deep residual neural network model can be used as a surrogate Virtual Indenter to generate a hardness map of a given structure, with “HardnessDesign-Indenter.ipynb’.

5.) Insights into Virtual Indenter predictions in terms of filter maximization and structure saliency can be visualized with ‘HardnessDesign-Visualization.ipynb’ and ‘HardnessDesign-Saliency.ipynb’, respectively.

6.) Train generative model on PIC images, using https://github.com/NVlabs/stylegan2  

7.) Generate bioinspired structures that meet prescribed target hardness values with ‘HardnessDesign-GeneticAlgorithm.ipynb’

8.) As a control verification, “HardnessDesign-IndentorControl.ipynb” demonstrates that predicted hardness values are indeed tied to the specific morphology of generated structures, not simpler features such as average orientation or frequency distribution of orientations within the structure. 
