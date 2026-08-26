# Diabetic-Retinopathy-CNN-Transformer-Comparison
This repository contains the implementation and experimental code associated with the comparative evaluation of convolutional neural network (CNN)-based and transformer-based deep learning architectures for five-class diabetic retinopathy (DR) grading using the APTOS 2019 retinal fundus image dataset.

## Models

Six ImageNet-pretrained deep learning architectures were evaluated:

### CNN-Based Models
- ResNet50
- EfficientNet-B0
- MobileNetV2

### Transformer-Based Models
- Vision Transformer (ViT)
- Swin-Tiny
- Swin Transformer

The models were implemented using PyTorch and the TIMM library and were fully fine-tuned on the APTOS 2019 dataset.

## Dataset

The experiments were conducted using the APTOS 2019 Blindness Detection dataset for five-class diabetic retinopathy grading.

" The five DR severity grades are:

- No DR
- Mild DR
- Moderate DR
- Severe DR
- Proliferative DR"

The dataset used in the experiments was obtained from the publicly available APTOS 2019 Kaggle repository described in the associated manuscript.

## Experimental Setup

All evaluated architectures were trained under a consistent experimental configuration to enable controlled comparison across models.

The main training configuration included:

- Input image size: 224 × 224
- Optimizer: AdamW
- Learning rate: 1 × 10⁻⁴
- Weight decay: 1 × 10⁻⁴
- Batch size: 32
- Maximum epochs: 20
- Early stopping patience: 6
- Loss function: Weighted Cross-Entropy Loss
- Sampling strategy: WeightedRandomSampler

Each model was independently trained and evaluated across five runs using different random seeds. Classification performance was reported as mean ± standard deviation across the five runs.

## Evaluation

Model performance was evaluated using multiple complementary measures, including:

- Accuracy
- Precision
- Recall
- F1-score
- Area Under the ROC Curve (AUC-ROC)
- Quadratic Weighted Kappa (QWK)
- Per-class performance
- Model complexity
- Inference latency

Class-specific 95% confidence intervals were additionally estimated using bootstrap resampling for the per-class analysis.

## Repository Contents

The repository contains separate Jupyter/Google Colab notebooks for the evaluated deep learning architectures. The notebooks include the main preprocessing, training, validation, testing, and performance evaluation procedures used in the study.

## Implementation Environment

The experiments were implemented in Python using:

- PyTorch
- Torchvision
- TIMM
- Scikit-learn
- Matplotlib
- Pillow
- NumPy

The experiments reported in the study were conducted using Google Colab Pro+ with NVIDIA A100 GPU acceleration.

## Reproducibility

Different random seeds were used for the five independent experimental runs, while the random states for Python, NumPy, and PyTorch were controlled within each run.

The exact TIMM model identifiers and complete experimental configuration are documented in the associated manuscript and implemented in the corresponding model notebooks.

## Citation

If you use this code in your research, please cite the associated article.

Citation information will be added following publication.

## License

This repository is provided for academic and research purposes.
