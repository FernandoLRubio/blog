---
layout: post
title: "Denoising images with Machine Learnig"
date: 2023-12-14
description: Unsupervised fun! # Add post description (optional)
img: denoiser.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Computer Science, Machine Learning]
---

Developed as part of a machine learning course during my master's program.


>[Skip to the live demo](https://fer-lr-mscs-ml.streamlit.app/?ref=fernando.ghost.io)

It has become a character trait of mine to select a hard nearly-out-of-scope 
project for every class I've taken in the last few years and this project was 
no exception.We were asked to plan a project related our hobbies and I chose
 movies, of course.

I wanted to train an AI model to detect what type of camera lens was used based 
solely on the final image. But it turned out to be way more complex than I 
expected; many productions add lens effects in post-production and trying to 
gather enough trustworthy data was a nightmare.

Then, I moved on towards **super resolution**. I was aiming to understand how 
AI upscaling works on modern TV's or [NVIDIA's DLSS](https://en.wikipedia.org/wiki/Deep_learning_super_sampling?ref=fernando.ghost.io). 
And I set the scope to generate a general purpose video upscaler. My teacher 
put a stop to it fast, as I wasn't aware (again) of the size of that endeavour.

We agreed upon super resolution for a limited domain of single images: 
**Human faces**; and I was set to research about deep learning 
[autoencoders](https://en.wikipedia.org/wiki/Autoencoder?ref=fernando.ghost.io#:~:text=An%20autoencoder%20is%20a%20type,data%20from%20the%20encoded%20representation) 
to do so, as the course wouldn't cover them (which was extra risky as we only 
had one session about convolutional neural networks).

As a last minute pivot, I switched the scope into noise reduction. So I could 
add this work into my master's overall project which involves denoising 
multispectral imaging.

So, I developed a pipeline, trained a model and hooked up an interactive demo. 
It turned out pretty well, if I do say so myself.

Here are a **few notes** before sharing the demo:

- I've not modified it since it was presented, the conclusions and any post-work is not included.
- The choice of the model layers was not the goal of the project, so it's pretty generic.
- We concluded that my model learned how to remove gaussian distributed noise and not necessarily how to reconstruct faces.
Which doesn't mean it is wrong, only that I miss-calculated the domain of the training data set.

Anyways, without further a do, here's the link to the demo. 
(If the app is offline it should take about 3 minutes to boot up)

>[Streamlit demo](https://fer-lr-mscs-ml.streamlit.app/?ref=fernando.ghost.io)

---

>btw, if you do look at my code, I know it's horrendous. Like many school 
projects, quality was not the first priority. Don't  this, kids.
