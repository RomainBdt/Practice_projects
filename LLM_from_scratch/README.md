# llm-from-scratch.ipynb
It is a notebook that shows how to train a language model from scratch on the [WikiText](https://huggingface.co/datasets/wikimedia/wikipedia/tree/main/20231101.fr). I chose the French Wikipedia dataset because it is smaller than the English Wikipedia dataset. I mainly used Andrej Karpathy's course [link](https://github.com/karpathy/ng-video-lecture/tree/master) to learn the basics of transformers for NLP tasks. It is funny to see that a model trained from scratch on Wikipedia articles with a  naive character level tokenizer and 0.454M parameters can generate mostly existing words after a few hours of training.
## Learning Outcomes
- How to build a transformer language model from scratch using PyTorch
- How to train the model
- The importance of the tokenizer in NLP

# tokenizer.ipynb
It is an example notebook that shows how to create a tokenizer from scratch. Again, this notebook is inspired by Andrej Karpathy's course [link](https://github.com/karpathy/minbpe/tree/master).

## Learning Outcomes
- What is a BPE tokenizer
- What is sentencepiece tokenizer
- How to create a BPE tokenizer from scratch

# llm-from-scratch-custom-tokenization.ipynb
It is a notebook that combines the previous notebooks to create a language model from scratch coupled with a more advanced technique for tokenization.

## Learning Outcomes
- Increasing the size of the vocabulary increases the size of the model (mainly for this small model because it has only 2 hidden layers). The vocabulary size is now 500 and the model size is 0.5573 M parameters.
- The custom tokenization technique allows to ingest larger context with the same amout of tokens because the tokens can represent more than one character.
- There is no significant improvement in the quality of the generated text. I guess it takes longer to train the model with a vocabulary size being 5 times bigger than the previous one. The eval loss is 1.43 after 72000 steps while it was 1.42 after 73000 steps with the previous model.
- As pre-training requires a lot of computational resources, I do not try to train the model further. I used only the small part of the dataset with a very small model.