# PRUNE AND TELL: ViT vs ConvNeXt in Image Captioning with Token Pruning
Project Description
This project explores the development of efficient image captioning models by comparing Vision Transformer (ViT) and ConvNeXt architectures. A key focus is the integration of token pruning to enhance computational efficiency without significantly sacrificing captioning accuracy. The research aims to contribute to the field of vision-language models, particularly for applications requiring real-time processing or deployment on resource-constrained edge devices.

## Key Features
Dual Backbone Evaluation: Comparative analysis of ViT and ConvNeXt as image encoders for image captioning.

- Token Pruning Integration: Implementation and evaluation of token pruning as a strategy to optimize computational resources.

- High Accuracy: Achieved training accuracies consistently above 99.7% for both architectures.

- Efficient Convergence: Demonstrated rapid and stable convergence of training loss and accuracy.

- Real-World Generalization: Validated model performance on diverse, unseen real-world images.

- Interpretability: Utilized attention map analysis to understand model focus and decision-making.

## Methodology Highlights
The project leverages a robust framework for image captioning, comprising:

- Image Encoder: ViT or ConvNeXt for extracting visual features.

- Projection Layer: To align visual and textual feature dimensions.

- Tokenization & Positional Embedding: For processing ground truth captions.

- Masking Mechanisms: Padding and Subsequent masks for effective training.

- Transformer Decoder: With cross-attention and integrated token pruning for caption generation.

Training was conducted on the COCO image captioning dataset (14GB). A 30% prune ratio was applied, which notably allowed for a significantly larger batch_size (128 vs. 48 without pruning) on a single RTX 4090 GPU, showcasing the efficiency gains.

## Performance Summary
Both ViT and ConvNeXt backbones achieved remarkable performance:

- ViT Backbone Accuracy: Approximately 99.8%

- ConvNeXt Backbone Accuracy: Approximately 99.7%

The models exhibited rapid convergence, with training loss stabilizing near zero and accuracy saturating at near-perfect levels within the initial epochs. Qualitative assessments through real-world testing confirmed the models' ability to generate coherent and contextually relevant captions for novel images. Attention map visualizations further demonstrated that the models effectively focused on salient visual regions, maintaining interpretability despite token pruning.
