# SkyText

SkyText is a Chinese GPT3 pre-trained large model released by Singularity-AI, which can perform different [tasks](https://openapi.singularity-ai.com/index.html#/examplesIndex) such as chatting, Q&A, and Chinese-English translation. 

![image](https://user-images.githubusercontent.com/120169448/208887507-34db7755-67d6-4807-a43b-ed851c961f8f.png)

#### Hugging Face home pages:
https://huggingface.co/SkyWork/SkyText

https://huggingface.co/SkyWork/SkyTextTiny

#### Here are some show cases:

# Show cases:

For experience and trial, please visit [Singularity-AI-trail](https://openapi.singularity-ai.com/index.html#/tryoutIndex)

### Chat
![image](https://user-images.githubusercontent.com/120169448/208884291-f598368d-951a-4356-967a-f0466f8f069f.png)

### Question and answer
![image](https://user-images.githubusercontent.com/120169448/208884265-55b0cb1c-48a1-4f42-8ea0-6608b5a551af.png)

### Generate recipes：
input——
![image](https://user-images.githubusercontent.com/120169448/208884242-29afcd38-2b8e-451b-9f43-e68b5660f435.png)

output——
![image](https://user-images.githubusercontent.com/120169448/208884206-b58a626e-85de-4c42-81c3-7e4d4c4da634.png)

### Couplet
![image](https://user-images.githubusercontent.com/120169448/208884185-dd2043d3-d868-41fd-a495-a034fac6e35c.png)

# Project Highlights

1. Technical advantage 1: data cleaning of more than 30 processes
   
   With the development of NLP technology, pre-training large models has gradually become one of the core technologies of artificial intelligence. Pre-training large models usually requires a large amount of text for training, and network text naturally becomes the most important source of corpus. The quality of the training corpus undoubtedly directly affects the effect of the model. In order to train a model with outstanding capabilities, Singularity-AI has used more than 30 cleaning processes in data cleaning. Excellence in details, casting excellent model effect.


2. Technical advantage 2: optimized and innovative Chinese coding method for Chinese
   
   In the field of pre-training large models, it has always been dominated by the English community, and the importance of Chinese pre-training large models is self-evident. Unlike English, the Chinese input method（pinyin text) of the Chinese pre-trained large model should obviously be different. According to the characteristics of Chinese, Singularity-AI has optimized and innovated a unique Chinese encoding method, which is more in line with Chinese language habits, and rebuilt a Chinese dictionary that is more conducive to model understanding.



# News of Singularity-AI

- [2022.12.15] [AIGC Press Conference of Singularity-AI](https://live.vhall.com/v3/lives/subscribe/697547540)
  
—————————————————————————————————

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

# 13Billions
model = GPT2LMHeadModel.from_pretrained("SkyWork/SkyText")
tokenizer = AutoTokenizer.from_pretrained("SkyWork/SkyText", trust_remote_code=True)

# or 2.6Billions
model = GPT2LMHeadModel.from_pretrained("SkyWork/SkyTextTiny")
tokenizer = AutoTokenizer.from_pretrained("SkyWork/SkyTextTiny", trust_remote_code=True)

text_generator = TextGenerationPipeline(model, tokenizer, device=0)
input_str = "Today is a "
max_new_tokens = 20
print(text_generator(input_str, max_new_tokens=max_new_tokens, do_sample=True))
```

# License

[MIT License]

# Developer Group
#### Scan the code below with WeChat to join in the developer group
![img_v2_5bed8353-a6e9-4f83-b615-68c2c46c611g](https://user-images.githubusercontent.com/120169448/209296283-6f8b1251-ad01-42f2-8037-a1413cb41d9f.png)


