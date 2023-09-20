# Persian Question Answering System

## Overview

This repository contains the code and resources for a Persian Question Answering System based on transformer architectures. The model is fine-tuned on an extractive dataset from Persian Wikipedia using [ParsBERT](https://github.com/hooshvare/parsbert) and is hosted on Hugging Face for easy integration into your projects.

- **Model**: [marzinouri/parsbert-finetuned-persianQA](https://huggingface.co/marzinouri/parsbert-finetuned-persianQA)
- **Dataset**: [PersianQA Dataset](https://github.com/sajjjadayobi/PersianQA)

## Best Results
The best results for this Persian Question Answering System were achieved with the following hyperparameters:

- **Batch Size**: 2
- **Learning Rate**: 2e-5
- **Epochs**: 4

These hyperparameters resulted in the following performance metrics:

- **Exact Match**: 42.79
- **F1 Score**: 59.12

It's worth noting that due to limitations in computational resources, larger batch sizes could not be used during the fine-tuning process.

