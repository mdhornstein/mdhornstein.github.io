--- 
layout: default_math 
---

Generally, when we think of fine tuning, we think of taking a huge pretrained model and fine tuning it ourselves. But OpenAI provides an API that allows you to fine tune a model purely by submitting additional training data.  

I wonder if OpenAI more heavily weights the training data that you provide. 

### https://beta.openai.com/docs/guides/fine-tuning

* There is an API for fine-tuning, and you pay based on number of tokens in the training data and number of epochs of training. I suppose one epoch is one pass over your training data. 