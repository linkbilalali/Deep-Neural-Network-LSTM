DNNLS Final Assessment

Author: Bilal Ali

## Remarks: 
Isn't that the baseline models already consist of LSTM layers? Please ensure you extend the baseline with relevant models. Would be nice to see the implementation of your extension that address the identified problem of the baseline models.

While the baseline uses a standard LSTM, my extension adds a Tag-Embedding module. This allows the model to 'read' meaningful labels (like objects or actions) alongside the video frames. By fusing these tags with the visual data, the model understands the story's context much better than a baseline that only looks at raw pixels.

### Key Points Simplified:
1. Semantic Context:
The baseline only sees colors and shapes (pixels). My model understands what is happening by using tags like "person" or "running."
2. Feature Fusion:
I added a new layer that blends image data and tag data together before they go into the LSTM. This is the main "extension" of the architecture.
3. Better Grounding:
By linking tags to the story, the model can more accurately predict storytelling scores based on real-world concepts.

## Introduction and Problem Statement
This repository contains my final project for the Deep Neural Networks and Learning Systems (DNNLS) course.
The purpose of this project is to build and extend a baseline deep learning architecture for multi-modal learning using text and vision data.
The project focuses on:

## Data preparation
1. NLP models
2. Vision models
3. A combined storytelling architecture
4. Training routines and evaluation

## The main implementation is provided inside:
MineDNNProject.ipynb

## Project Objectives
Starting from a baseline architecture provided in labs, this project aims to:
1. Prepare and preprocess datasets
2. Implement custom dataset loaders
3. Build text encoders (LSTM based)
4. Build vision encoders (CNN based)
5. Combine both modalities into a unified architecture
6. Train the model for storytelling / score prediction tasks

## Dataset
The project uses data loaded from HuggingFace and locally generated metadata files.
## Main data components:
1. Text sequences
2. Image frame sequences
3. Metadata (CSV file)
4. Synthetic data generation for better training

## Methods
1. Data Preparation
2. Google Drive integration
3. Loading and saving datasets
4. Creating helper functions
5. Dataset splitting (train / validation / test)
6. Creating PyTorch Dataset and DataLoader objects

## Models
1. NLP Models
2. LSTM based text encoder
3. Tokenization using BERT tokenizer
4. Vision Models
5. CNN based image encoder
6. Frame extraction and processing
7. Main Architecture
8. Fusion of text and vision embeddings
9. Joint feature learning

## Training Routines
1. Model initialization
2. Optimizer and loss functions
3. Training loops
4. Validation process
5. Checkpoint saving and loading

### Additional Tasks
1. Story score prediction (temporal + tag embeddings)
2. Synthetic metadata generation
3. Data augmentation experiments

## Results
1. Training and validation losses
2. Model performance comparison
3. Qualitative outputs from model predictions
### (Results are visualized directly inside the notebook)

## Conclusions
 The project successfully demonstrates:
1. Multi-modal deep learning pipeline
2. Integration of NLP and Vision models
3. Stable training process
4. Improved understanding of storytelling architectures

## Future Work
1. Better fusion techniques
2. Transformer based encoders
3. Larger datasets
4. Hyperparameter optimization
5. Human evaluation


