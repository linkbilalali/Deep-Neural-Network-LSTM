## What Does This Project Do?

This project helps AI understand stories better and write improved descriptions of images.

When you give the 4 images from a story, it will:
1. Predict what the 5th image should look like
2. Write a better quality description of that picture

Example:
Input: image 1, image 2, image 3, image 4
Output: image 5 + Description like "A woman is cooking in the kitchen near the stove'

### Our Improved Model:
Added LSTM to understand temporal flow in stories
Added Semantic Tags to identify objects, actions, and locations
Generates more detailed and specific descriptions

### Comparison:
Before: "A person is in a room."
After: "A woman is cooking in the kitchen, standing near the stove while holding a pan."

### What We Used:

**1. LSTM (2 Layers)**
This is an AI technique that remembers sequences
It understands what happened before and what comes after in a story
Example: If Frame 1 shows "person walking", then Frame 5 showing "person sitting" makes logical sense

**2. Semantic Tags (84 Total Tags)**
Objects: person, dog, car, chair, phone (28 tags)
Actions: running, cooking, playing, talking (30 tags) 
Locations: kitchen, park, street, office (26 tags)
These tags tell the AI what is present in each scene

**3. Multi-modal Learning**
Combines Images + Text + Tags for better understanding
Using three types of information makes the AI smarter


## Results in Simple Numbers

Metric | Before | After | Improvement
Text Quality (Perplexity) | 65.61 | 37 | 43 percent better
Text Similarity (BLEU) | 0.0135 | 0.065 | 383 percent better 
Image Quality (SSIM) | 0.155 | 0.246 | 59 percent better

What This Means:
The model now writes much better descriptions
Descriptions are more accurate
Visual predictions are also improved

### Step to run Notebook
1. Open Google Colab at colab.research.google.com
2. Upload the file named final.ipynb
3. Turn on GPU: Go to Runtime, then Change runtime type, select GPU

Training takes 2 to 3 hours (25 epochs)
Runs faster on GPU
You will see progress on screen

### Check Your Results
All results will be saved in your Google Drive in a folder called MineDNN:

MineDNN/
 results/
 comparison_table.xlsx (numbers and statistics)
 loss_curves.png (graphs showing progress)
 visual_samples.png (picture predictions)
 generated_descriptions.txt (text outputs)
 checkpoints/
 best_model.pth (trained model file)

## Output Files

### Excel Files (.xlsx)
training_history.xlsx contains data from each epoch
comparison_table.xlsx shows baseline versus improved comparison

You Get: Numbers, percentages, improvement statistics

### Image Files (.png)
loss_curves.png shows training progress in 6 graphs
visual_samples.png shows image the AI predicted
baseline_vs_improved.png shows bar charts

You Get: Visual charts and sample outputs

### Text Files (.txt)
generated_descriptions.txt contains descriptions written by AI
hypothesis_evaluation.txt contains research results

You Get: Stories and detailed analysis

### Model Files (.pth)
best_model_text.pth is the model with best text quality
checkpoint_epoch_5.pth is a backup saved every 5 epochs

You Get: Trained AI models for future use

## Research Questions We Answered

### Question 1: What Was the Problem?
Answer: The baseline model could not do temporal understanding and semantic grounding properly.

### Question 2: What Is the Solution?
Answer: We added LSTM for temporal understanding and Tag Embeddings for semantic understanding.

### Question 3: What Metrics Do We Use?
Answer: Perplexity and BLEU for text quality, MSE and SSIM for images.

### Question 4: How Did We Process the Data?
Answer: We take 4 frames as input, extract semantic tags, then predict the 5th frame.

### Question 5: What Results Did We Expect?
Answer: 10 to 20 percent improvement in text quality and positive cross-modal similarity.

### Question 6: How Did We Split the Data?
Answer: Video-level split with 80 percent training and 20 percent validation, no data leakage.

## What the we generated

### Input (4 Frames):
Frame 1: Person walking on street
Frame 2: Person approaching building
Frame 3: Person opening door
Frame 4: Person inside room

### Prediction (Frame 5):
Image: Person sitting on chair
Text: "A woman is sitting on a chair in the office, looking at her computer screen."

### What Makes This Good:
Specifies gender (woman)
Details the action (sitting, looking)
Mentions location (office)
Identifies objects (chair, computer)

## Project Goal Summary
Teach model better storytelling

How We Do It:
Temporal understanding using LSTM
Semantic grounding using Tags 
Multi-modal learning combining Images and Text

Results:
Better descriptions
More details included
Higher accuracy overall

## Additional Information

Dataset: StoryReasoning from HuggingFace
Model Type: LSTM-based sequence predictor
Framework: PyTorch
Platform: Google Colab with GPU

## Structure After Training
After the code runs, you will find these files in Google Drive:

MineDNN/
results/
  Analysis_Reports/
    - hypothesis_evaluation.txt
  comparative/
    - comparison_table.xlsx
    - baseline_vs_improved.png
  Generated_Stories/
    - visual_samples.png
    - generated_descriptions.txt
  Performance_Summary/
    - training_history.xlsx
  Visualizations/
    - loss_curves.png
  checkpoints/
   best_model_text.pth
   best_model_overall.pth
   checkpoint_epoch_5.pth
   checkpoint_epoch_10.pth
   checkpoint_epoch_15.pth
   checkpoint_epoch_20.pth
   checkpoint_epoch_25.pth
data/
  config.json
  dataset_info.json
  tag_vocabulary.json
  model_architecture.txt

## What Happens During Training

**Epoch 1 to 5:**
Model learns basic patterns in the data

**Epoch 6 to 15:**
Model improves text quality significantly 

**Epoch 16 to 25:**
Model fine-tunes and achieves best results

The best model is automatically saved based on text quality (lowest perplexity).

## Understanding the Results

### Perplexity (Text Quality)
Measures how well the model predicts text
Lower numbers are better
Goes from 65 to 37 (big improvement)

### BLEU (Text Accuracy)
Compares generated text to actual text
Higher numbers are better
Goes from 0.01 to 0.06 (big improvement)

### SSIM (Image Quality)
Measures structural similarity of images
Higher numbers are better 
Goes from 0.15 to 0.24 (good improvement)

## Important Notes

1. All files are automatically saved to Google Drive
2. Training progress is shown on screen
3. You can stop and resume training using checkpoints
4. GPU makes training much faster than CPU
5. Results are organized in separate folders for easy access

# Daily Update: 2025-12-17 - Log ID 32100
# Daily Update: 2025-12-17 - Log ID 14332
# Daily Update: 2025-12-17 - Log ID 507
# Daily Update: 2025-12-18 - Log ID 12977
# Daily Update: 2025-12-18 - Log ID 30192
# Daily Update: 2025-12-19 - Log ID 7397
# Daily Update: 2025-12-19 - Log ID 20856
# Daily Update: 2025-12-20 - Log ID 11773
# Daily Update: 2025-12-20 - Log ID 25731
# Daily Update: 2025-12-21 - Log ID 12414
# Daily Update: 2025-12-21 - Log ID 28820
# Daily Update: 2025-12-22 - Log ID 14033
# Daily Update: 2025-12-22 - Log ID 2615
# Daily Update: 2025-12-22 - Log ID 28390
# Daily Update: 2025-12-23 - Log ID 14234
# Daily Update: 2025-12-24 - Log ID 29297
# Daily Update: 2025-12-26 - Log ID 10374
# Daily Update: 2025-12-26 - Log ID 16956
# Daily Update: 2025-12-26 - Log ID 2374
# Daily Update: 2025-12-26 - Log ID 19128
# Daily Update: 2025-12-27 - Log ID 11820
# Daily Update: 2025-12-28 - Log ID 24017
# Daily Update: 2025-12-28 - Log ID 16025
# Daily Update: 2026-01-01 - Log ID 32588
# Daily Update: 2026-01-02 - Log ID 25970
# Daily Update: 2026-01-02 - Log ID 25159
# Daily Update: 2026-01-03 - Log ID 3745
# Daily Update: 2026-01-03 - Log ID 14750
# Daily Update: 2026-01-03 - Log ID 6519
# Daily Update: 2026-01-05 - Log ID 15928
# Daily Update: 2026-01-05 - Log ID 8524
# Daily Update: 2026-01-06 - Log ID 10587
# Daily Update: 2026-01-07 - Log ID 3609
# Daily Update: 2026-01-09 - Log ID 3560
# Daily Update: 2026-01-10 - Log ID 18526
# Daily Update: 2025-12-16 - Log ID 28200
# Daily Update: 2025-12-17 - Log ID 11509
# Daily Update: 2025-12-18 - Log ID 9048
# Daily Update: 2025-12-18 - Log ID 12538
# Daily Update: 2025-12-18 - Log ID 21245
# Daily Update: 2025-12-19 - Log ID 4360
# Daily Update: 2025-12-19 - Log ID 8713
# Daily Update: 2025-12-19 - Log ID 15983
# Daily Update: 2025-12-21 - Log ID 17175
# Daily Update: 2025-12-21 - Log ID 21911
# Daily Update: 2025-12-22 - Log ID 25892
# Daily Update: 2025-12-23 - Log ID 6213
# Daily Update: 2025-12-23 - Log ID 21816
# Daily Update: 2025-12-24 - Log ID 47
# Daily Update: 2025-12-25 - Log ID 22640
# Daily Update: 2025-12-26 - Log ID 6622
# Daily Update: 2025-12-26 - Log ID 3458
# Daily Update: 2025-12-27 - Log ID 32023
# Daily Update: 2025-12-27 - Log ID 19892
# Daily Update: 2025-12-29 - Log ID 16437
# Daily Update: 2025-12-31 - Log ID 24412
# Daily Update: 2025-12-31 - Log ID 19601
# Daily Update: 2025-12-31 - Log ID 11285
# Daily Update: 2025-12-31 - Log ID 24081
# Daily Update: 2026-01-01 - Log ID 22381
# Daily Update: 2026-01-03 - Log ID 29381
# Daily Update: 2026-01-04 - Log ID 25862
# Daily Update: 2026-01-04 - Log ID 644
# Daily Update: 2026-01-04 - Log ID 27067
# Daily Update: 2026-01-04 - Log ID 21397
# Daily Update: 2026-01-06 - Log ID 13858
# Daily Update: 2026-01-07 - Log ID 25429
# Daily Update: 2026-01-07 - Log ID 29478
# Daily Update: 2026-01-07 - Log ID 23497
# Daily Update: 2026-01-08 - Log ID 26983
# Daily Update: 2026-01-08 - Log ID 15962
# Daily Update: 2026-01-10 - Log ID 8045
# Dev Log: 2025-12-18 revision 3
# Dev Log: 2025-12-18 revision 6
# Dev Log: 2025-12-21 revision 3
# Dev Log: 2025-12-23 revision 2
# Dev Log: 2025-12-23 revision 4
# Dev Log: 2025-12-24 revision 1
# Dev Log: 2025-12-24 revision 2
# Dev Log: 2025-12-24 revision 3
# Dev Log: 2025-12-25 revision 1
# Dev Log: 2025-12-26 revision 1
# Dev Log: 2025-12-26 revision 7
# Dev Log: 2025-12-27 revision 2
# Dev Log: 2025-12-27 revision 3
# Dev Log: 2025-12-27 revision 4
# Dev Log: 2025-12-29 revision 4
