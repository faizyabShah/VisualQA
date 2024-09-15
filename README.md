# Visual Question Answering System using VizWiz Dataset

## Overview
This project aims to develop a Visual Question Answering (VQA) system to assist visually impaired individuals. The system leverages deep learning models trained on the VizWiz dataset to interpret visual content and provide contextually appropriate responses to users' queries.

## Dataset
The VizWiz dataset is used for training and validation. It includes:
- **Training Set**: 20,523 image/question pairs and 205,230 answer/answer confidence pairs.
- **Validation Set**: 4,319 image/question pairs and 43,190 answer/answer confidence pairs.
- **Annotations**: Each image is associated with a question and ten crowd-sourced answers, categorized into types like unanswerable, number, color, and other.

## Model Architecture
The model is designed for VQA tasks, taking in an image and a related question as inputs. These inputs are encoded using the CLIP model and processed through various layers to predict three outputs: Answerability, Answer Type, and the Actual Answer.
![image](https://github.com/user-attachments/assets/6975df9e-e96e-453f-abb4-30b07060908d)


### Key Components
- **CLIP Image Encoder**: Converts images into fixed-size tensors by extracting visual features.
- **CLIP Text Encoder**: Transforms text into fixed-size tensors by capturing semantic meaning.
- **Answerability Prediction**: Predicts whether the question is answerable.
- **Answer Type Prediction**: Categorizes the answer into types like unanswerable, number, color, or other.
- **Final Answer Prediction**: Combines features to produce the final answer to the input question.

## Training
The model was trained with the following parameters:
- **Epochs**: 50
- **Learning Rate**: 0.0005
- **Optimizer**: Adam
- **Loss Functions**: Cross Entropy Loss for answer type and answer prediction, Binary Cross Entropy Loss for answerability prediction.

## Results
- **Test Accuracy**: 52.2%
- **VizWiz Accuracy**: 68%

## Conclusion
The project demonstrates the potential of deep learning models in addressing real-world VQA tasks. Despite challenges posed by unanswerable and conversational questions, the model achieved reasonable accuracy, aligning well with human judgment.

## Contributors
- Faizyab Ali Shah (fshah.bscs21seecs@seecs.edu.pk)
- Manahil Ahmad (mahmad.bscs21seecs@seecs.edu.pk)

## References
- [VizWiz Dataset](https://www.kaggle.com/datasets/lhanhsin/vizwiz)
- [CLIP Model](https://github.com/openai/CLIP)
