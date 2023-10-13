# LBO-AC
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
cd LBO-AC
conda create --name LBO-AC --file ./requirements.txt
conda activate GAFSE
jupyter notebook
```

# Reproduction on Bioactivity Prediction
In your jupyter notebook, re-run the corresponding notebook of "GAFSE-HS/GAFSE-HS/1_GAFSE_{Task ID}.ipynb" to reproduce the training process of GAFSE-HS. For example:
```
./LBO-AC/LBO-AC/1_GAFSE_1.ipynb
```
To reproduce the training process of GAFSE-MO on these HS tasks, please re-run the corresponding notebook of "GAFSE-HS/GAFSE-MO/1_GAFSE_{Task ID}.ipynb". For example:
```
./LBO-AC/LBO-AC/3_GAFSE_1.ipynb
```

# Reproduction on Molecular Property Prediction
In your jupyter notebook, re-run the corresponding notebook of "GAFSE-MP/3C_GAFSE_Multi_Tasks_{Small, Medium, Big, Large}.ipynb" to reproduce the training process of GAFSE-MP. For example:
```
./LBO-AC-MP/3C_GAFSE_Multi_Tasks_Small.ipynb
```
To readout the GAFSE-MP performance over all tasks, please re-run the notebook of "GAFSE-MP/3C_Performance_Readout.ipynb":
```
./LBO-AC-MP/3C_Performance_Readout.ipynb
```

# Reproduction on Molecule Optimization
## Reproduce on Molecular Activity 
In your jupyter notebook, re-run the corresponding notebook of "GAFSE-MO/G_AFSE_{Task name}_1/G_AFSE_{Task name}_1.ipynb" to reproduce the training process of GAFSE-MO on molecular activity. For example:
```
./LBO-AC-MO/G_AFSE_IC50_O43614_1/G_AFSE_IC50_O43614_1.ipynb
```
To test trained models, please re-run the corresponding notebook of "GAFSE-MO/G_AFSE_{Task name}_1/G_AFSE_{Task name}_1-Test.ipynb". For example:
```
./LBO-AC-MO/G_AFSE_IC50_O43614_1/G_AFSE_IC50_O43614_1-Test.ipynb
```

## Reproduce on Molecular Property
In your jupyter notebook, re-run the corresponding notebook of "GAFSE-MO/G_ADMET_M,T_C_{Task name}/G_ADMET_M,T_C_{Task name}.ipynb" to reproduce the training process of GAFSE-MO on molecular property. For example:
```
./LBO-AC-MO/G_ADMET_M_C_CYP1A2_inhibitor/G_ADMET_M_C_CYP1A2_inhibitor.ipynb
```
To test trained models, please re-run the corresponding notebook of "GAFSE-MO/G_ADMET_M,T_C_{Task name}/G_ADMET_M,T_C_{Task name}-Test.ipynb". For example:
```
./LBO-AC-MO/G_ADMET_M_C_CYP1A2_inhibitor/G_ADMET_M_C_CYP1A2_inhibitor-Test.ipynb
```

## Reproduce Molecule Optimization on COVID-19
In your jupyter notebook, re-run the notebook of "GAFSE-MO/AID_1706/G_AFSE_AID_1706.ipynb" to reproduce the training process of GAFSE-MO on the COVID-19-related database:
```
./LBO-AC-MO/AID_1706/G_AFSE_AID_1706.ipynb
```
For a quick view of the results, please check "GAFSE-MO/AID_1706/AID_1706_datatable_copy_generated_molecules.csv"

# Tips
- Under the "Data" and "Module" folders are organized data and modules for review. For the convenience of operation, these data and modules are distributed to the "AttentiveFP" and "data" folders in subfolders.
- Some code may need to create an empty "result" folder in the current directory to store the run results.
- The "GRN" and "AFSE" classes imported "from AttentiveFP.AttentiveLayers_Sim_copy" are the most critical modules in this project.
- The "perturb_feature" and "modify_atoms" functions are the most critical functions in this project.
- The "AFSE" imported "from AttentiveFP.AttentiveLayers_Sim_copy" of GAFSE-MP is different from GAFSE-HS.
- The number of epochs for stopping "patience=30" is more suitable for GAFSE-MO, because too much training is not conducive to the optimization of molecules.
- If you encounter any problems reproducing our experiments, please contact me via 1018010514@njupt.edu.cn (or yinym96@qq.com).
