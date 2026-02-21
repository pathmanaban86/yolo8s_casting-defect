# Comparative Analysis of YOLO Architectures for Casting Defect Detection

Repository for the manuscript:
**"Comparative analysis of YOLO architectures for automated casting defect 
detection in industrial quality control"**  
*Discover Mechanical Engineering* (under review)

## Repository Contents

| File | Description |
|------|-------------|
| `data/image_subset_list.csv` | Filenames of all 1,300 images used in experiments, with split assignment (train/val) and class labels |
| `configs/data.yaml` | Dataset configuration file for YOLO training |
| `notebooks/training_experiment.ipynb` | Google Colab notebook reproducing all main experiments |
| `scripts/train.py` | Training script for YOLOv5s, YOLOv8s, and YOLO11s |
| `scripts/evaluate.py` | Evaluation script generating Table 3, Table 5 metrics |
| `scripts/learning_curve.py` | Learning curve experiment (Section 4.1.3) |
| `results/learning_curve_results.csv` | Numerical results from learning curve analysis |

## Dataset

The full dataset is publicly available on Kaggle:  
https://www.kaggle.com/datasets/ravirajsinh45/real-life-industrial-dataset-of-casting-product

Download the dataset, then use `data/image_subset_list.csv` to 
select the exact 1,300 images used in this study.

## Requirements
```
ultralytics>=8.0.0
torch>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
pyyaml>=6.0
```

## Reproducing Results

1. Download dataset from Kaggle
2. Filter images using `data/image_subset_list.csv`
3. Open `notebooks/training_experiment.ipynb` in Google Colab
4. Set runtime to GPU (T4 recommended)
5. Run all cells

**Random seed:** 42 (applied to all stochastic operations)  
**Hardware:** NVIDIA Tesla T4 GPU  
**Training:** 80 epochs, batch size 16, Adam optimizer

## Citation

[To be added upon acceptance]
