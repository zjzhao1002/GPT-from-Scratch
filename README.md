# GPT-from-Scratch
A small GPT language model is built from scratch by using PyTorch.
This model is developed by following [Andrej Karpathy's video](https://www.youtube.com/watch?v=kCc8FmEb1nY) and [Imad Saddik's video](https://www.youtube.com/watch?v=9Ge0sMm65jo&t=11900s), 
but the tokenizer is replaced by the [sentencepiece](https://github.com/google/sentencepiece).

The base model is trained by 500 articles from wikipedia, which are taken from [Huggingface](https://huggingface.co/datasets/wikimedia/wikipedia). 
This small model has 13 Million parameters. 
After pre-training, this model can generate some English text. 

To make the model more useable, I also perform the fine tuning. 
The fine tuning dataset is a [Fact Q&A](https://huggingface.co/datasets/rubenroy/GammaCorpus-Fact-QA-450k) dataset. 
It provides some short questions and answers. 
Two methods for fine tuning are applied:
* Supervised Fine Tuning (SFT)
* Parameter Efficient Fine Tuning (PEFT)

After fine tuning, this model can only generate some weird answers to input questions.
We need more computing resouce and data to improve this model.
