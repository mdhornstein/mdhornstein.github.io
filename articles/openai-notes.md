
--- 
layout: default_math 
--- 

## OpenAI Tutorial/Guide 

## Notes on Open AI website 

### https://beta.openai.com/docs/guides/fine-tuning


### https://openai.com/api/pricing/
Here are some salient points from the article: 
* Open AI offers the following services 
    * Image generation 
    * Language generation 
    * Fine-tuning 
    * Embedding 
* You pay for tokens, not directly for requests. Therefore, you have to understand the relationship between tokens and requests. 
* "1,000 tokens is about 750 words" 

Thoughts on their pricing model: 
* There are a number of companies that charge for usage, for example: 
    * Snowflake charges for computation and storage
    * OpenAI charges based on number of tokens 
    * AWS Lambda charges for memory and compute time 

### https://beta.openai.com/docs/guides/safety-best-practices?lang=python
Here are some salient points to remember: 
* It is safer to require users to log in (e.g. through social media sites). You can pass the user ID in the API call to OpenAI, and OpenAI will help you identify policy-violating users. 
* If you do not require users to log in, you can still track session id. 
* Rate limits help prevent abuse of your app. 
* Test your model/app on adversarial inputs. 
    * Todo: read more about adversarial inputs and safeguarding models against adversarial inputs. 