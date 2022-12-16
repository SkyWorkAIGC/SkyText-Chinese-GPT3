# SkyText

SkyText是由奇点智源发布的中文GPT3预训练大模型，可以进行聊天、问答、中英互译等不同的[任务](https://openapi.singularity-ai.com/index.html#/examplesIndex)。SkyText则是中文GPT3预训练模型的开源项目。


## 项目亮点

1. 技术优势一 ：30多道流程的数据清洗
   
   随着NLP技术的发展，预训练大模型逐渐成为了人工智能的核心技术之一。预训练大模型通常需要海量的文本来进行训练，网络文本自然成为了最重要的语料来源。而训练语料的质量无疑直接影响着模型的效果。为了训练出能力出众的模型，奇点智源在数据清洗时使用了30多道的清洗流程。精益求精的细节处理，铸造了卓越的模型效果。

2. 技术优势二：针对中文优化创新的中文编码方式
   
   曾经在预训练大模型领域，一直是被英文社区主导着，而中文预训练大模型的重要性不言而喻。不同于英文的拼音文字，中文预训练大模型的中文输入方式显然应该有所不同。奇点智源针对中文的特点，优化创新使用了独特的中文编码方式，更加符合中文的语言习惯，重新构建出更利于模型理解的中文字典。



# 奇点新闻

- [2022.12.15] [昆仑天工AIGC发布会](https://live.vhall.com/v3/lives/subscribe/697547540)
  
  

## 依赖

```
推荐
transformers>=4.16.0
```

## 模型使用

```python
# -*- coding: utf-8 -*-
from transformers import GPT2LMHeadModel
from transformers import AutoTokenizer
from transformers import TextGenerationPipeline

# 以 SkyWork/SkyText(13billions) 为例，还有 SkyWork/SkyTextJunior(2.6billions) 可用， 期待使用

model = GPT2LMHeadModel.from_pretrained("SkyWork/SkyText")
tokenizer = AutoTokenizer.from_pretrained("SkyWork/SkyText", trust_remote_code=True)
text_generator = TextGenerationPipeline(model, tokenizer, device=0)
input_str = "今天是个好天气"
max_new_tokens = 20
print(text_generator(input_str, max_new_tokens=max_new_tokens, do_sample=True)) 
```


## huggingface模型主页
一百四十亿参数模型
https://huggingface.co/SkyWork/SkyText
三十亿参数模型
https://huggingface.co/SkyWork/SkyTextJunior


# 版权许可

[MIT License](LICENSE)
