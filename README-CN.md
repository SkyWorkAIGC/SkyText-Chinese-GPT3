# SkyText

SkyText是由奇点智源发布的中文GPT3预训练大模型，可以进行聊天、问答、中英互译等不同的[任务](https://openapi.singularity-ai.com/index.html#/examplesIndex)。
应用这个模型，除了可以实现基本的聊天、对话、你问我答外，还能支持中英文互译、内容续写、对对联、写古诗、生成菜谱、第三人称转述、创建采访问题等多种功能。
![image](https://user-images.githubusercontent.com/120169448/208886238-4c083a21-75be-4368-9f2a-3b80230e04eb.png)

#### Hugging face 模型主页：
https://huggingface.co/SkyWork/SkyText

https://huggingface.co/SkyWork/SkyTextTiny

#### 下面是一些示例：

# 效果示例
体验和试用，请访问[奇点智源API试用](https://openapi.singularity-ai.com/index.html#/tryoutIndex)

### 聊天
![image](https://user-images.githubusercontent.com/120169448/208879009-0aefea8b-2183-4b94-b0d0-0351fe3af0d3.png)

### 问答
![image](https://user-images.githubusercontent.com/120169448/208879023-193723a6-caf9-4ff2-ba01-4c5c017326a8.png)

### 生成菜谱
输入：
![image](https://user-images.githubusercontent.com/120169448/208879071-fe0e87fa-c01d-4edb-8b8a-249e6c2e0b72.png)

输出：
![image](https://user-images.githubusercontent.com/120169448/208879104-3fb89264-5526-4f9f-ace6-508f9a606577.png)

### 对对联
![image](https://user-images.githubusercontent.com/120169448/208879500-4a7d644d-9d0d-4dc4-a6a4-0b21b5c891ac.png)


# 项目亮点

1. 技术优势一 ：30多道流程的数据清洗
   
   随着NLP技术的发展，预训练大模型逐渐成为了人工智能的核心技术之一。预训练大模型通常需要海量的文本来进行训练，网络文本自然成为了最重要的语料来源。而训练语料的质量无疑直接影响着模型的效果。为了训练出能力出众的模型，奇点智源在数据清洗时使用了30多道的清洗流程。精益求精的细节处理，铸造了卓越的模型效果。

2. 技术优势二：针对中文优化创新的中文编码方式
   
   曾经在预训练大模型领域，一直是被英文社区主导着，而中文预训练大模型的重要性不言而喻。不同于英文的拼音文字，中文预训练大模型的中文输入方式显然应该有所不同。奇点智源针对中文的特点，优化创新使用了独特的中文编码方式，更加符合中文的语言习惯，重新构建出更利于模型理解的中文字典。


# 奇点新闻

- [2022.12.15] [昆仑天工AIGC发布会](https://live.vhall.com/v3/lives/subscribe/697547540)
  
——————————————————————————————————

## 依赖

```
推荐
transformers>=4.18.0
```

## 模型使用

```python
# -*- coding: utf-8 -*-
from transformers import GPT2LMHeadModel
from transformers import AutoTokenizer
from transformers import TextGenerationPipeline

# 以 SkyWork/SkyText(13billions) 为例，还有 SkyWork/SkyTextTiny(2.6billions) 可用， 期待使用

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
https://huggingface.co/SkyWork/SkyTextTiny


# 版权许可

[MIT License](LICENSE)

# 加入开发者群
#### 微信扫码加入开发者群
![img_v2_5bed8353-a6e9-4f83-b615-68c2c46c611g](https://user-images.githubusercontent.com/120169448/209296389-52a1147c-5326-4e25-afaf-dfe27fbaaade.png)

