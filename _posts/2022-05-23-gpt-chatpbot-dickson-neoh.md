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

Now we will follow the steps in this YouTube video to create a Telegram bot: 
<iframe width="560" height="315" src="https://www.youtube.com/embed/aNmRNjME6mE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



## Step 2: Install a Python library for the bot 

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">🐍 Python Telegram Bot<br><br>Next, install a Telegram bot wrapper library👉python-telegram-bot (PTB).<br><br>Now, we can code our bot using Python!<a href="https://t.co/6MLC2kmxCB">https://t.co/6MLC2kmxCB</a></p>&mdash; Dickson Neoh 🚀 (@dicksonneoh7) <a href="https://twitter.com/dicksonneoh7/status/1527512984360087553?ref_src=twsrc%5Etfw">May 20, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>




