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

## Testing the Model Online

You can easily test the Persian Question Answering System model online using the Hugging Face API. Here's an example of how to do it using Python:

```python
from transformers import pipeline
qa_pipeline = pipeline("question-answering", model="marzinouri/parsbert-finetuned-persianQA")

context = "مطالبه‌ی هویت در فضای مجازی یکی از مسائل مهم و پیچیده‌ای است که به طور متناوب مطرح می‌شود. افراد و سازمان‌ها به دنبال اعتبار و شناخته شدن در فضای مجازی هستند و این امر می‌تواند به وسیله‌ی تولید محتوای ارزشمند، فعالیت‌های اجتماعی و تعامل با دیگران بهبود یابد."

question = "چگونه افراد و سازمان‌ها می‌توانند در فضای مجازی به اعتبار و شناخته شدن دست یابند؟"

answer = qa_pipeline(question=question, context=context)

print("Answer:", answer["answer"])
```
