# SkyText

SkyText is a Chinese GPT3 pre-trained large model released by Singularity-AI, which can perform different [tasks](https://openapi.singularity-ai.com/index.html#/examplesIndex) such as chatting, Q&A, and Chinese-English translation. SkyText is an open source project of the Chinese GPT3 pre-training model.


## Project Highlights

1. Technical advantage 1: data cleaning of more than 30 processes
   
   With the development of NLP technology, pre-training large models has gradually become one of the core technologies of artificial intelligence. Pre-training large models usually requires a large amount of text for training, and network text naturally becomes the most important source of corpus. The quality of the training corpus undoubtedly directly affects the effect of the model. In order to train a model with outstanding capabilities, Singularity-AI has used more than 30 cleaning processes in data cleaning. Excellence in details, casting excellent model effect.


2. Technical advantage 2: optimized and innovative Chinese coding method for Chinese
   
   In the field of pre-training large models, it has always been dominated by the English community, and the importance of Chinese pre-training large models is self-evident. Unlike English, the Chinese input method（pinyin text) of the Chinese pre-trained large model should obviously be different. According to the characteristics of Chinese, Singularity-AI has optimized and innovated a unique Chinese encoding method, which is more in line with Chinese language habits, and rebuilt a Chinese dictionary that is more conducive to model understanding.



# News of Singularity-AI

- [2022.12.15] [AIGC Press Conference of Singularity-AI](https://live.vhall.com/v3/lives/subscribe/697547540)
  
  

## Installation

```
Recommand
transformers>=4.18.0
```

## Model Usage

```python
# -*- coding: utf-8 -*-
from transformers import GPT2LMHeadModel
from transformers import AutoTokenizer
from transformers import TextGenerationPipeline

model = GPT2LMHeadModel.from_pretrained("SkyWork/SkyTextTiny")
tokenizer = AutoTokenizer.from_pretrained("SkyWork/SkyTextTiny", trust_remote_code=True)
text_generator = TextGenerationPipeline(model, tokenizer, device=0)
input_str = "Today is a "
max_new_tokens = 20
print(text_generator(input_str, max_new_tokens=max_new_tokens, do_sample=True))
```

# License

[MIT License]
