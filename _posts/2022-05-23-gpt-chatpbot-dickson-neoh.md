--- 
layout: default 
author: Michael Hornstein
--- 

I will "liveblog" my experience following Dickson Neoh's guide to deploying GPT-J in a chatbot. 

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Deploying GPT-like language models on a chatbot is tricky.<br><br>You might wonder<br>• How to access the model?<br>• Where to host the bot?<br><br>In this 🧵I walk you through how easily I deployed a GPT-J-6B model by <a href="https://twitter.com/hashtag/EleutherAI?src=hash&amp;ref_src=twsrc%5Etfw">#EleutherAI</a> on a <a href="https://twitter.com/hashtag/Telegram?src=hash&amp;ref_src=twsrc%5Etfw">#Telegram</a> bot with <a href="https://twitter.com/huggingface?ref_src=twsrc%5Etfw">@huggingface</a> and <a href="https://twitter.com/Gradio?ref_src=twsrc%5Etfw">@Gradio</a>.<br><br>For FREE 🚀 <a href="https://t.co/z0uvnxksWt">pic.twitter.com/z0uvnxksWt</a></p>&mdash; Dickson Neoh 🚀 (@dicksonneoh7) <a href="https://twitter.com/dicksonneoh7/status/1527512946603020288?ref_src=twsrc%5Etfw">May 20, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## Step 1: Set up a Telegram bot. 

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">🤖Token From the BotFather<br><br>To create a bot, you must have a Telegram account.<br><br>Next, get a TOKEN from the BotFather. This TOKEN allows you to access the bot.<br><br>Keep this TOKEN private🤫. Anyone with this TOKEN can access your bot.<a href="https://t.co/9VWBkoKX8l">https://t.co/9VWBkoKX8l</a></p>&mdash; Dickson Neoh 🚀 (@dicksonneoh7) <a href="https://twitter.com/dicksonneoh7/status/1527512982078443520?ref_src=twsrc%5Etfw">May 20, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

I have not heard of Telegram. Let's look it up ... 
https://telegram.org/faq#q-what-is-telegram-what-do-i-do-here
* Telegram is a messaging app. 
* "Telegram's API and code is open, and developers are welcome to create their own Telegram apps. We also have a Bot API, a platform for developers that allows anyone to easily build specialized tools for Telegram, integrate any services, and even accept payments from users around the world." 

I need a Telegram account, so let's create one... I signed up for Telegram on Android. 

Now we will follow the steps in this YouTube video to create a Telegram bot: 
<iframe width="560" height="315" src="https://www.youtube.com/embed/aNmRNjME6mE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Here are my notes: 
* BotFather is a Telegram account used to create bots. 

Here are some additional notes from the Telegram reference on bots, (https://core.telegram.org/bots).
* "Use the `/newbot` command to create a new bot. The BotFather will ask you for a name and username, then generate an authentication token for your new bot." 
  * What name should I use? I chose "GPT Neoh Tutorial" 
  * What username should I use? gpt_tutorial_from_neoh_bot
    * The username must end in `bot`. 
* The token is used to "authorize the bot and send requests to the Bot API." 
  * I am not posting the token here, to protect my security. 

The bot API is defined here: https://core.telegram.org/bots/api
* An API request is a URL of this form: https://api.telegram.org/bot<token>/METHOD_NAME

* The API includes methods to read input from users and to send responses to users.  


How is a bot different from a traditional web app? For both a bot and a web app, users send requests and receive responses. But for a bot, the interface is different. Users send requests through a chat interface. Furthermore, there is real time communication. 

## Step 2: Install a Python library for the bot 

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">🐍 Python Telegram Bot<br><br>Next, install a Telegram bot wrapper library👉python-telegram-bot (PTB).<br><br>Now, we can code our bot using Python!<a href="https://t.co/6MLC2kmxCB">https://t.co/6MLC2kmxCB</a></p>&mdash; Dickson Neoh 🚀 (@dicksonneoh7) <a href="https://twitter.com/dicksonneoh7/status/1527512984360087553?ref_src=twsrc%5Etfw">May 20, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


## Hugging Face Spaces

* Lets you host machine learning apps. 
* Two SDKs: Streamlit and Gradio
    * Gradio provides an interface for running ML models
    * Streamlit is for more general apps
* Code is stored in a Git repo
* Spaces relies on GitHub actions, so we need to read about GitHub actions

Hugging Face provides a space that makes it easier for you to create your own spaces.
(https://huggingface.co/spaces/farukozderim/Model-Comparator-Space-Builder)

## GitHub Actions
(https://github.com/features/actions)

(https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions)
* A workflow is an automated process
* You can define a workflow with a yaml file
* A workflow can run based on any of these conditions:
    * Some event occurs that triggers the workflow
    * Trigger manually
    * Trigger at a predefined time
* A workflow contains jobs, which executive on the same virtual machine, which means they can share data







