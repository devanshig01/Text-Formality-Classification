# Text-Formality-Classification (Fine-Tuning DeBerta)

This project is based from the following paper: https://arxiv.org/pdf/2204.08975. This paper by Dementieva et al. (2023), discuses and evaluates various methods to detect formality across text in different languages. The paper utilizes various transformer based and BERT-based models and report the findings of which models have the highest accuracy in detecting text formality by leveraging the GYAFC corpus dataset.

Taking this paper a step further, the main aim was to improve contextual understanding by developing a formality score scale of 0 to 1 and making further accurate sentence predictions. More detail in the Jupyter Notebook.

## Models Investigated and F1 scores:

- BiLSTM (Baseline model): 77.9%
- DeBerta: 93.7%
- Bert (uncased): 88.4%
- Simple CNN: 79.9%


Since DeBerta has the highest f1 score, we use that trained model to develop formality scores. Here are some examples:

<img width="1076" alt="Screenshot 2024-06-05 at 9 38 07 AM" src="https://github.com/devanshig01/Text-Formality-Classification/assets/68164303/81fc553c-d852-426e-8e86-9c3d5b2e2721">

## Brief Aside

The investigation is not without its limitations, the formality score combines the model's confidence score to get predictions. Despite the accuracy in determining whether a piece of text is formal/informal, there could be multiple other different factors apart from the confidence that causes high or low probabilities when determining formality. For example, if a sentence in the training dataset is very similar to a sentence in the testing dataset, then the confidence score and thus the probability is bound to be higher regardless of the fact if that test sentence has a high degree of formality. 

This implementation was performed because there is currently no large-scale or small-scale datasetthat actually measures such a degree of formality.Perhaps in the future, work could be done to com-
pile such a dataset, which could further a huge amount of research much like (Rao and Tetreault, 2018) did. Perhaps, another way to collect data could be to scrape from certain domains we know to have a certain degree of formality like (Naous et al., 2023). For example, a sentence from an academic paper could have the maximum formality score of 1 but an SMS text to a close friend could be 0. However, albeit naive, it is for sure  that the current implementation will still prove to be a strong basis for measuring formality in the future.
