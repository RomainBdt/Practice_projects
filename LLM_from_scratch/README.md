# llm-from-scratch.ipynb
It is a notebook that shows how to train a language model from scratch on the [WikiText](https://huggingface.co/datasets/wikimedia/wikipedia/tree/main/20231101.fr). I chose the French Wikipedia dataset because it is smaller than the English Wikipedia dataset. I mainly used Andrej Karpathy's course [link](https://github.com/karpathy/ng-video-lecture/tree/master) to learn the basics of transformers for NLP tasks. It is funny to see that a model trained from scratch on Wikipedia articles with a  naive character level tokenizer and 454M parameters can generate mostly existing words after a few hours of training.
## Learning Outcomes
- How to build a transformer language model from scratch using PyTorch
- How to train the model
- The importance of the tokenizer in NLP

# tokenizer.ipynb
It is an example notebook that shows how to create a tokenizer from scratch. Again, this notebook is inspired by Andrej Karpathy's course [link](https://github.com/karpathy/minbpe/tree/master).

## Learning Outcomes
- What is a BPE tokenizer
- What is sentencepiece tokenizer
