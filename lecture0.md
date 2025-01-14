class: middle, center, title-slide

# Deep Learning

Lecture 0: Introduction

<br><br>
Prof. Gilles Louppe<br>
[g.louppe@uliege.be](mailto:g.louppe@uliege.be)

---

# Today

- Course outline
- Introduction to deep learning
- Fundamentals of machine learning

---

# Outline

- Lecture 1: Fundamentals of machine learning
- Lecture 2: Multi-layer perceptron
- Lecture 3: Automatic differentiation
- Lecture 4: Training neural networks
- Lecture 5: Convolutional neural networks
- Lecture 6: Computer vision
- Lecture 7: Attention and transformer networks
- Lecture 8: GPT
- Lecture 9: Graph neural networks
- Lecture 10: Uncertainty
- Lecture 11: Auto-encoders and variational auto-encoders
- Lecture 12: Score-based diffusion models

---

class: middle

.center.width-60[![](figures/lec0/map.png)]

---

class: middle

## My mission

By the end of this course, you will have a strong and comprehensive understanding of deep learning. 

You will learn how to design deep neural networks for various advanced probabilistic inference tasks and how to train them.

The models covered in this course have broad applications in artificial intelligence, engineering, and science.

---

class: middle

# Why learning?

---

class: middle, center

.width-100[![](figures/lec0/mushrooms.png)]

What do you see?

???

.italic[How do you do that?]

---

class: middle

.center[
.width-70[![](figures/lec0/dog1.jpg)]

Sheepdog or mop?
]

.footnote[Credits: [Karen Zack](https://twitter.com/teenybiscuit), 2016.]

---

class: middle

.center[
.width-70[![](figures/lec0/dog2.jpg)]

Chihuahua or muffin?
]

.footnote[Credits: [Karen Zack](https://twitter.com/teenybiscuit). 2016.]

---

class: middle

The (human) brain is so good at interpreting visual information that the gap between raw
data and its semantic interpretation is difficult to assess intuitively.

<br>
.center[
![](figures/lec0/mushroom-small.png)

This is a mushroom.
]

---

class: middle, center

.width-70[![](figures/lec0/mushroom-big.png)]

This is a mushroom.

---

class: middle, center

.width-30[![](figures/lec0/mushroom-rgb0.png)] +
.width-30[![](figures/lec0/mushroom-rgb1.png)] +
.width-30[![](figures/lec0/mushroom-rgb2.png)]


This is a mushroom.

---

class: middle, center

.width-80[![](figures/lec0/mushroom-small-nb.png)]

This is a mushroom.

---

class: middle, center

Writing a computer program that sees?

---

class: middle

.center.width-60[![](figures/lec0/cat1.png)]

---

count: false

.center.width-60[![](figures/lec0/cat2.png)]

---

count: false
class: middle
background-image: url(figures/lec0/cat3.png)
background-size: cover

---

count: false
class: middle
background-image: url(figures/lec0/cat4.png)
background-size: cover

---

class: middle

To extract semantic information, we need models with high complexity .bold[that cannot be manually designed]. 

However, we can write a program that learns the task of extracting semantic information.

---

class: middle, black-slide

.center.width-70[![](figures/lec0/console.jpg)]

The .bold[machine learning approach] consists in:
- defining a parametric model
- optimizing its parameters, by "making it work" on the training data.

---

class: middle

# The deep learning revolution

---

class: middle

Deep learning .bold[scales up] the statistical and machine learning approaches by
- using larger models known as neural networks,
- training on larger datasets,
- using more compute resources.

.grid[
.kol-3-4.width-70.center[![](./figures/lec0/mlp.png)]
.kol-1-4.width-90.center[![](./figures/lec0/imagenet.jpeg)<br>![](./figures/lec0/titan.jpg)]
]

???

[Talk about the slide first.]

Scaling up the statistical and machine learning approaches by brute force in these three dimensions has been key to the success of deep learning.

---

class: middle, center, black-slide

.center[
<video loop controls preload="auto" height="500" width="600">
  <source src="./figures/lec0/yann-dl.mp4" type="video/mp4">
</video>
]

---

class: middle

Specialized neural networks can be trained achieve super-human performance on many complex tasks that were previously thought to be out of reach for machines.

.width-100[![](./figures/lec0/tasks-1.png)]

.width-100[![](./figures/lec0/tasks-2.png)]

.center[(Top) Scene understanding, pose estimation, geometric reasoning.<br>
(Bottom) Planning, Image captioning, Question answering.]

.footnote[Credits: François Fleuret, 2023.]

???

Following this approach, deep learning has been successful in tasks that were previously considered hard for computers, such as understanding images, speech, or text.

In particular, specialized neural networks can be trained to solve a large variety of problems, from scene understanding to geometric reasoning, from planning to question answering.

While these problems can be perceived as artificial and not really important in their own right, they actually form a set of primitive tasks that are found in many domains of application. 

---

class: middle

Neural networks form .bold[primitives] that can be transferred to many domains. 

.grid[
.kol-1-3.center.width-100[![](./figures/lec0/cytomine2.png)]
.kol-1-3.center.width-80[![](./figures/lec0/mri.jpg)]
.kol-1-3.center.width-80[![](./figures/lec0/melanoma.jpg)]
]
.width-100[![](./figures/lec0/sbi-cardio.png)]

.center[(Top) Analysis of histological slides, denoising of MRI images, nevus detection.<br>
(Bottom) Whole-body hemodynamics reconstruction from PPG signals.]

???

For example, in health and medicine, the same specialized neural networks that are used to annotate scenes can be used to analyze biomedical images, such as histological slides.

Specialized neural networks can also be used to denoise MRI images, to detect nevus, or to reconstruct whole-body hemodynamics from PPG signals, if some of you have an Apple Watch.

As a matter of fact, the adoption of AI and deep learning in health and medicine has been growing steadily over the past decade, with many applications in medical imaging, genomics, and many more. 

These applications however, are often deeply embedded in the tools used by healthcare professionals, and are not always visible to the public.

---

class: middle, center, black-slide

<iframe width="600" height="450" src="https://www.youtube.com/embed/oYUcl_cqKcs" frameborder="0" allowfullscreen></iframe>

Object detection, pose estimation, segmentation (Meta AI, 2023)

---

class: middle, center, black-slide

<iframe width="600" height="450" src="https://www.youtube.com/embed/hA_-MkU0Nfw" frameborder="0" allowfullscreen></iframe>

Building autonomous cars (Waymo, 2022)

---

class: middle, black-slide, center

<iframe width="600" height="450" src="https://www.youtube.com/embed/zrcxLZmOyNA" frameborder="0" allowfullscreen></iframe>

Powering the future of clean energy (NVIDIA, 2023)

---

class: middle, black-slide, center

<iframe width="600" height="450" src="https://www.youtube.com/embed/AbdVsi1VjQY" frameborder="0" allowfullscreen></iframe>

How AI is advancing medicine (Google, 2023)

---

class: middle

.grid[
.kol-2-5.center.width-100[![](./figures/lec0/transformer.svg)]
.kol-3-5.center.width-100[<br>![](./figures/lec0/scaling.png)]
]

## From large to enormous

Scaling up further to gigantic models, datasets, and compute resources keeps pushing the boundaries of what is possible, .bold[with no sign of slowing down].

???

Meanwhile, research in deep learning has continued at a fast pace, with the development of new models, new algorithms, and new applications.

One of the most important developments in recent years has been the introduction of the transformer architecture.

This architecture has been key to scaling up the size of our models and the amount of data we can use to train them. Today, the largest models count up to hundreds of billions of parameters, and are trained on datasets with hundreds of terabytes of data.

To our surprise, these gigantic models keep pushing the boundaries of what is possible, with no sign of slowing down. Make them bigger, train them on more data, and they keep getting better.

---

class: middle, center
background-color: #343541

<video src="./figures/lec0/chatgpt.webm" controls loop muted width=640 height=640></video>

???

The pinnacle of this scaling up has been the development of conversational and generative AI systems. The most famous and successful example being of course OpenAI's ChatGPT.

[play video]

These systems are trained to generate human-like text, and can be used to answer questions, write stories, or even have a conversation with a human.

For example, here is a short conversation with ChatGPT about hematology and what I should know about it, as a non-professional.

These systems keep getting better, the pace of progress is really fast and impressive. For example, the latest versions of those systems are multi-modal, meaning that they can generate not only text, but also images and sounds.

---

class: middle, center

.center.width-50[![](./figures/lec0/medpalm2.gif)]

.center[Med-PaLM 2 (Google) is a large language model tuned for the medical domain. It reaches 85%+ accuracy on US Medical Licensing Examination-style questions.] 

???

What makes these AI systems really different is that they offer a new interface. AI is no longer embedded in tools but in direct contact with us, humans.

For example, Med-PaLM 2 is a large language model tuned for the medical domain. It can be interacted with using natural language, as if you were talking to a medical expert. You do not need to know how to write code or how to define these mathematical models. You just ask a question, and it will give you an answer.

---

class: middle, center

Deep learning can also .bold[solve problems that no one could solve before].

???

Beyond the basic work that can be automated, the most exciting applications of AI, at least for the scientist in me, is the fact that deep learning can also be used to solve problems that no one could solve before. To make discoveries. 

I have many examples in mind, but I will only mention a few today, to give you a sense of what is possible. I will focus on health and medicine, but the same is true in many other domains.

---

class: middle

## AlphaFold: From a sequence of amino acids to a 3D structure

.grid[
.kol-2-3.center.width-100[![](./figures/lec0/alphafold-nature.png)]
.kol-1-3.center.width-100[![](./figures/lec0/alphafold-prediction.gif)]
]

???

The first example is AlphaFold, a neural network based on the trasnformer architecture that can predict the 3D structure of a protein from its amino acid sequence.

This problem is important because the 3D structure of a protein determines its function, and understanding protein function is key to understanding biology and designing new drugs.

However, determining the 3D structure of a protein experimentally is difficult and expensive, taking up to months just to solve a single structure. 

AlphaFold has been a breakthrough in this area, and has been able to predict the 3D structure of proteins with high accuracy, in just a couple of minutes for the longest sequences.

---

class: middle, black-slide, center

<iframe width="600" height="450" src="https://www.youtube.com/embed/gg7WjuFs8F4" frameborder="0" allowfullscreen></iframe>

AI for Science (Deepmind, AlphaFold, 2020)

---

class: middle

## Drug discovery with graph neural networks

.center.width-80[![](./figures/lec0/cell.png)]

???

A second example is the use of graph neural networks to discover new drugs.

Discovering new drugs is a complex and expensive search problem, where the goal is to find molecules that will bind to a target protein and modulate its function. Unfortunately, this problem is difficult for two reasons:
- first, the search space is huge -- the space all possible pharmacologically active molecules is estimated to be in the order of 10^60 molecules.
- second, the binding of a molecule to a protein is a complex process that is difficult to model. Laboratory experiments are necessary to evaluate the binding of a molecule to a protein, and these experiments are expensive and time-consuming.

Graph neural networks have been a breakthrough in this area, and have been able to predict the properties of molecules with high accuracy. 

In a sense, they can serve as a virtual laboratory that can be used to pre-screen millions of molecules in a matter of hours, thereby reducing the laboratory work to only the most promising candidates.

---

class: middle

## Predicting cardiovascular risks from retinal images

.grid[
.kol-1-2.center.width-100[![](./figures/lec0/retina1.jpg)]
.kol-1-2.center.width-100[![](./figures/lec0/retina2.png)]
]

???

Finally, a third example is the use of deep learning to predict cardiovascular risks from retinal images.

As I understand it, predicting cardiovascular risks and other factors from retinal fundus photographs was previously considered impossible because no relevant features were believed to be visible in these images. However, a few years ago, a team of researchers from Google showed that it was possible to predict cardiovascular risks from retinal images with high accuracy, using a deep neural network.

Not only this is interesting from a medical perspective, but it also points to the fact that deep neural networks can be used to make discoveries in unexpected places, because of their ability to pick up complex and latent patterns from data that are difficult to understand for humans.

---

class: middle

.center.circle.width-30[![](figures/lec0/bishop.jpg)]

.italic[For the last forty years we have programmed computers; for the next forty years we will train them.]

.pull-right[Chris Bishop, 2020.]

---

class: end-slide, center
count: false

The end.
