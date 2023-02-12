---
layout: post
title: "Reddit Bot"
---

[Github Link](https://github.com/ammarj0987/Tl-dr-Reddit-Bot)

Technologies used: Python, PRAW, Reddit, openAI, hugging face

This is a reddit bot that summarizes long posts into a few sentences so that the users do not have to read the full post. 

I use [PRAW](https://praw.readthedocs.io/en/stable/#) to navigate reddit and reddit API to create an account that can access posts and reply to them. For the backend, I use trained machine learning models to summarize the posts. Then I process those responses and turn them into clean replies. Then I again use PRAW and Reddit API to reply to the post with a summary of it.

Learn more about the machine learning models used to summarize text:

[openAI](https://openai.com/api/)

[philschmid/bart-large-cnn-samsum](https://huggingface.co/philschmid/bart-large-cnn-samsum)