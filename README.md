# OLB-AC
Reproducing of the paper entitled "OLB-AC: Towards Optimizing Ligand Bioactivities Through Deep Graph Learning and Activity Cliffs" (Under Review)

- All rights reserved by Yueming Yin, Email: 1018010514@njupt.edu.cn (or yueming.yin@ntu.edu.sg).

# Environment
- Python 3.6.13
- Pytorch 1.10.2 (Up to your CUDA version)
- RDKit 2020.09.1.0
- Jupyter
- Tensorboard
- Tensorboardx
- Seaborn
- Matplotlib
- Scikit-learn

# Installation
For a quick installation, please enter the following command in your terminal:
```
cd OLB-AC
conda create --name OLB-AC --file ./requirements.txt
conda activate OLB-AC
jupyter notebook
```

# Reproduction on Ligand Bioactivity Optimization
In your jupyter notebook, re-run the corresponding notebook of "OLB-AC-Optimization/Bioactivity/G_OLB-AC_{Task name}_1/G_OLB-AC_{Task name}_1.ipynb" to reproduce the training process of OLB-AC on ligand bioactivity optimization. For example:
```
./OLB-AC-Optimization/Bioactivity/G_OLB-AC_IC50_O43614_1/G_OLB-AC_IC50_O43614_1.ipynb
```
To test trained models, please re-run the corresponding notebook of "OLB-AC-Optimization/Bioactivity/G_OLB-AC_{Task name}_1/G_OLB-AC_{Task name}_1-Test.ipynb". For example:
```
./OLB-AC-Optimization/Bioactivity/G_OLB-AC_IC50_O43614_1/G_OLB-AC_IC50_O43614_1-Test.ipynb
```

# Reproduce on Ligand Inhibitory Efficacy Optimization
In your jupyter notebook, re-run the corresponding notebook of "OLB-AC-Optimization/Inhibitory-Efficacy/G_ADMET_M_C_{Task name}/G_ADMET_M_C_{Task name}.ipynb" to reproduce the training process of OLB-AC on ligand inhibitory efficacy optimization. For example:
```
./OLB-AC-Optimization/Inhibitory-Efficacy/G_ADMET_M_C_CYP1A2_inhibitor/G_ADMET_M_C_CYP1A2_inhibitor.ipynb
```
To test trained models, please re-run the corresponding notebook of "LBO-AC-Optimization/Inhibitory-Efficacy/G_ADMET_M,T_C_{Task name}/G_ADMET_M,T_C_{Task name}-Test.ipynb". For example:
```
./OLB-AC-Optimization/Inhibitory-Efficacy/G_ADMET_M_C_CYP1A2_inhibitor/G_ADMET_M_C_CYP1A2_inhibitor-Test.ipynb
```

# Reproduce on Ligand Toxicity Reduction
In your jupyter notebook, re-run the corresponding notebook of "OLB-AC-Optimization/Toxicity/G_ADMET_T_C_{Task name}/G_ADMET_T_C_{Task name}.ipynb" to reproduce the training process of OLB-AC on ligand toxicity reduction. For example:
```
./OLB-AC-Optimization/Toxicity/G_ADMET_T_C_Ames/G_ADMET_T_C_Ames.ipynb
```
To test trained models, please re-run the corresponding notebook of "LBO-AC-Optimization/Toxicity/G_ADMET_M,T_C_{Task name}/G_ADMET_M,T_C_{Task name}-Test.ipynb". For example:
```
./OLB-AC-Optimization/Toxicity/G_ADMET_T_C_Ames/G_ADMET_T_C_Ames-Test.ipynb
```

# Reproduction on Ligand Bioactivity Prediction
In your jupyter notebook, please re-run the corresponding notebook of "OLB-AC-Prediction/0_OLB-AC_{Task ID}.ipynb". For example:
```
./OLB-AC-Prediction/0_OLB-AC_1.ipynb
```

# Reproduction on Matched Molecular Pair (MMP) Baselines
In your jupyter notebook, please re-run the notebook of "Baselines/MMPDB.ipynb". For example:
```
./Baselines/MMPDB.ipynb
```

# Tips
- Under the "Data" and "Module" folders are organized data and modules for review. For the convenience of operation, these data and modules are distributed to the "AttentiveFP" and "data" folders in subfolders.
- Some code may need to create an empty "result" folder in the current directory to store the run results.
- The "GRN" and "AFSE" classes imported "from AttentiveFP.AttentiveLayers_Sim_copy" are the most critical modules in this project.
- The "perturb_feature" and "modify_atoms" functions are the most critical functions in this project.
- If you encounter any problems reproducing our experiments, please contact me via 1018010514@njupt.edu.cn (or yueming.yin@ntu.edu.sg).
