---
title: "2019 International Collegiate Competition for Brain-inspired Computing"
date: 2020-01-05
draft: true
---

## Introduction

In October, I participated together with a friend in the [2019 International Collegiate Competition for Brain-inspired Computing](https://contest.cbicr.org/) organized by Tsinghua University. The task was to 
develop an AI system that is brain-inspired, that is inspired by how the human brain works. From the website:

> In this contest, we generalize brain-inspired computing a little bit to a wider range of works reflecting the
> integration of neuroscience and computer science on problems relevant to general intelligence. The embodiment 
> can be theories, algorithms, hardware, software, application, etc. We decompose the big topic into several
> sub-topics including Perception, Cognition, Computation and Decision making. We also set Education topic to 
> promote a better educational system based on our knowledge of brain development and AI strategies.

I was told by a Chinese exchange student I met in Germany and made friends with that this contest exists. She is already back to China and continues her studies at Tsinghua University. As the task was related to AI, the price money was quite high and it was a chance to go to visit China, Tsinghua University and friends I have in Beijing, we decided to join forces and work on the task.

We brain-stormed for quite a while what our entry could be. It was difficult to find a topic for several reasons: first, my main area is Natural Language Processing. While I have experience in general Machine Learning and AI, I do not have worked in brain-inspired computing. Second, my teammate studies Automotive Engineering and does not have an extensive ML/AI and Computer Science background. Third, I was very busy as always writing papers.

Our first idea was to develop a system that prevents motion sickness while traveling in cars in trains by using a VR headset that shows an interactive video based on how the car works. Sadly, this topic was already [thought up by a German start-up](https://www.holoride.com/) whose solution also looks quite nice. We both were interested in doing something with Virtual or Augmented Reality. As I love learning Chinese and struggle with learning Chinese characters (Hanzi), we had the idea to aid learners with an engaging smartphone app called Yangtao. We base our learning on our understanding how the brain best works.

## Motivation

Chinese characters are an essential part of the Chinese language and culture. They are an integral part of becoming proficient in Mandarin. Learning even only the most common 2000-3000 characters is an arduous task that requires many hours of study. To support students, we implemented an augmented reality smart phone app for interacting with Chinese characters. 
When pointing the smart phone camera to a single character, we identify the character with machine learning and show its 3D representation above it. Its etymology, decomposition and mnemonic can be looked up. We use the knowledge about how the brain works and learns so that our users can better and more efficiently remember all the Hanzi. This is done by e.g. teaching character decompositions **六書**, showing the decomposition in the 3D view or helping users coming up with mnemonics to connect Hanzi parts to a story.

The learning process implemented in Yangtao relies on the Dual Coding Theory of Reading and Writing which states that the brain best remembers if the item to remember, in this case Hanzi, is associated with as many different cues as possible. Therefore, we present the users with visual cues (the 3D Hanzi), audio cues (the pronunciation) and the logic behind the Hanzi (its decomposition, etymology and kind of formation). A mnemonic for **休** could be e.g. a man leaning on a tree to rest, which is arguably easier to remember than learning its meaning by rote. 

<center>

| [![Yangtao: AR App for Interactively Learning and Exploring Chinese Characters](http://img.youtube.com/vi/3IBDXE0ZM14/0.jpg)](http://www.youtube.com/watch?v=3IBDXE0ZM14 "Yangtao: AR App for Interactively Learning and Exploring Chinese Characters")  |
| :--: | 
| [Watch me on Youtube](https://youtu.be/3IBDXE0ZM14) |

</center>

## The app development

The first app prototype is available for Android and uses Google ARCore, Sceneform and tflite. The character recognition itself uses a feed-forward neural network that is fed with HOG (Histogram of oriented gradients) features from filtered camera images. 

The prototype supports 250 selected characters. In the next iteration, we want to add online learning/lifelong learning capabilities so that the character recognition is  improved by user feedback if it was wrong, adapting the app to the users’ environment. This is similar to how the brain continually learns and adjusts.

## The contest

The contest was organized in three rounds

Lots of deliverables, some were not used at the end

Qinghua was really nice