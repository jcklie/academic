---
title: "Yangtao - Our entry for the 2019 International Collegiate Competition for Brain-inspired Computing"
date: 2019-11-05
tags: ["Personal", "China", "Mandarin", "Programming"]
---

## Introduction

In October, I participated together with a friend in the [2019 International Collegiate Competition for Brain-inspired Computing](https://contest.cbicr.org/) organized by Tsinghua University. The task was to 
develop an AI system that is brain-inspired, that is inspired by how the human brain works. From the website:

> In this contest, we generalize brain-inspired computing a little bit to a wider range of works reflecting the
> integration of neuroscience and computer science on problems relevant to general intelligence. The embodiment 
> can be theories, algorithms, hardware, software, application, etc. We decompose the big topic into several
> sub-topics including Perception, Cognition, Computation and Decision making. We also set Education topic to 
> promote a better educational system based on our knowledge of brain development and AI strategies.

The friend LanLan is Chinese exchange student I met in Germany and made friends. She told me that this contest exists and that we should participate. She is already back to China and continues her studies at Tsinghua University. As the task was related to AI, the price money was quite high and it was a chance to go to visit China, Tsinghua University and friends I have in Beijing, we decided to join forces and work on the task.

We brain-stormed for quite a while what our entry could be. It was difficult to find a topic for several reasons: first, my main area is Natural Language Processing. While I have experience in general Machine Learning and AI, I do not have worked in brain-inspired computing. Second, my teammate studies Automotive Engineering and does not have an extensive ML/AI and Computer Science background. Third, I was very busy as always writing papers.

Our first idea was to develop a system that prevents motion sickness while traveling in cars in trains by using a VR headset that shows an interactive video based on how the car works. Sadly, this topic was already [thought up by a German start-up](https://www.holoride.com/) whose solution also looks quite nice. We both were interested in doing something with Virtual or Augmented Reality. As I love learning Chinese and struggle with learning Chinese characters (Hanzi), we had the idea to aid learners with an engaging smartphone app. We base the learning approach in the app on our understanding how the brain best works.

My Chinese surname is Yang (杨) and the surname of my friend is Tao (陶), so we combined their pronunciations. The result is Yangtao - Chinese for star fruit (杨桃) - which is how we named our app.

{{< figure src="yangtao_logo.png" lightbox="true" title="The logo of our app Yangtao." >}}

## Motivation

Chinese characters are an essential part of the Chinese language and culture. They are an integral part of becoming proficient in Mandarin. Learning even only the most common 2000-3000 characters is an arduous task that requires many hours of study. To support students, we implemented an augmented reality smart phone app for interacting with Chinese characters. 

When pointing the smart phone camera to a single character, we identify the character with machine learning and show its 3D representation above it. Its etymology, decomposition and mnemonic can be looked up. We use the knowledge about how the brain works and learns so that our users can better and more efficiently remember all the Hanzi. This is done by e.g. teaching character decompositions **六書**, showing the decomposition in the 3D view or helping users coming up with mnemonics to connect Hanzi parts to a story.

<center>
{{< gallery album="yangtao-screenshots_ar" >}}
</center>

The learning process implemented in Yangtao relies on the Dual Coding Theory of Reading and Writing which states that the brain best remembers if the item to remember, in this case Hanzi, is associated with as many different cues as possible. Therefore, we present the users with visual cues (the 3D Hanzi), audio cues (the pronunciation) and the logic behind the Hanzi (its decomposition, etymology and kind of formation). A mnemonic for **休** could be e.g. a man leaning on a tree to rest, which is arguably easier to remember than learning its meaning by rote. 

<center>
{{< gallery album="yangtao-screenshots_app" >}}
</center>

We created a video that showcases our app:

<div style="margin: 1em">
{{< youtube 3IBDXE0ZM14 >}}
</div>

For more information about the project, please have a look at our poster:

<center>
{{< gallery album="yangtao-poster" >}}

{{% staticref "files/0048-Yangtao-TUD_THU-Poster.pdf" "newtab" %}}Download poster as PDF{{% /staticref %}}
</center>

## The app development

The [first app prototype is available for Android](https://github.com/jcklie/iccbc-2019) and uses [Google ARCore](https://developers.google.com/ar) for the Augmented Reality, [Sceneform](https://developers.google.com/ar/develop/java/sceneform) for displaying 3D models with ARCore and [tflite](https://www.tensorflow.org/lite) for running the machine learning model. 

The character recognition itself uses a feed-forward neural network that is fed with HOG (Histogram of oriented gradients) features from filtered camera images. We train on the [SCUT SPCCI dataset](http://www.hcii-lab.net/data/scutspcci/download.html) which contains Hanzi rendered from a wide variety of fonts. We chose this approach because it is simple, works, does not need much data and is fast enough to run in real time. While we also experimented with using CNN, especially MobileNets, they did not perform well enough for us to justify the increase in training and inference time.

We ask the user to focus the camera at the character they want to scan, therefore we can perform object classification and do not need to detect where the actual character is. It worked surprisingly well for printed characters, we also successfully scanned characters written by a brush.

The prototype supports 250 selected characters. In the next iteration, we want to add online learning/lifelong learning capabilities so that the character recognition is  improved by user feedback if it was wrong, adapting the app to the users’ environment. This is similar to how the brain continually learns and adjusts.

The character 3D models itself are generated from SVGs created by the [MakeMeAHanzi](https://github.com/skishore/makemeahanzi) project. We used the Blender Python API to turn them into 3D.

## The contest

The contest was organized in two rounds. In the first round, we had to prepare a write-up of our project, presentation slides and - if possible - a video until the 15th of September 2019. The first 32 were then awarded prize money, the top 16 were invited to actually participate in the live event in Tsinghua University, Beijing, China.

One week after we submitted our entry, we were notified that we are in the top 16! The organizers also sponsored the flight and the hotel, therefore I was very happy to have made it that far and to travel again to China. The jury remarked that our entry should be more brain-inspired though and that we still should use the time left to polish it.

The competition was scheduled on a weekend in mid of October. In preparation, I applied for the visa, bought the flights and we improved our app, video and narrative of the app to make it more fitting. Getting the visa turned out to be a bit annoying, as there was not much time between the acceptance notification, getting an invitation letter, an appointment with the visa centre and the actual flight. It managed to be done in time, but just because I paid express fees for the visa and express delivery for my passport.

We were then asked to prepare many deliverables for the finals: posters, updated slides, a video of our team introducing themselves, a video that is played before we enter the stage for the presentation, a video of our app, more documentation, reimbursement forms and so on. We spent lots of time on the videos and poster, some of these were not used at the end or cut very short.

I first wanted to stay longer in Beijing after the competition, but the competition was only allowed to reimburse flights that are around the competition date (understandably). As I was writing a paper during that time, I decided to just stay there for the weekend. I flew on Thursday night and left on Monday noon.

### Day 0

I flew on Thursday night before the competition weekend. The flight itself was not so interesting. The last times I was in China, I always had to change planes there because I did not travel to large cities but to smaller ones (Dalian and Kunming). Therefore, it was a nice treat to not have to do that. On Friday in Beijing, my friend picked me up from the airport. She had ordered the Chinese version of Uber Black with a private driver. The airport, hotel and Tsinghua University are both in Northern Beijing, therefore, it was all very close. I was very happy to see LanLan again after a year or more.

The hotel was a large Holiday Inn which targets upper class business travellers. I really liked it. We went to my room, I slept as I was weary from the travel and LanLan studied a bit. After that, we went to the Tsinghua campus which was just 10 minutes by foot from the hotel. Before I went there, I did not realize that Tsinghua is like its own city. It has a wall around with manned gates, its own street network, sport courts, cinemas, student housing, supermarkets, cafeterias and so on. As a student, you do not need to leave campus. The institute buildings are equally impressive. Everything is very modern and organized. It feels like one building there is as large as my whole university campus. You need a bike to get around, walking would be too slow.

LanLan showed me around the campus, we went to the supermarket there where I bought gifts and snacks. We then headed to a coffee shop  to prepare our presentation. After that, we went off campus to a very nice all-you-can-eat vegetarian buffet restaurant. We talked a lot and ate a lot, it was very delicious and not expensive for Beijing. As it was already late then, LanLan went to her room and I managed to find my hotel without mobile internet.

<center>
{{< gallery album="yangtao-day0" >}}
</center>

### Day 1

During check-in on the day before, LanLan asked the staff whether she can also eat breakfast in the hotel, as the room was booked for two people. They said yes, so she came to the hotel every morning just for the breakfast. It was really worth it. One could choose between continental, American, British and Chinese breakfast buffet. I love eating fries, hash brownies, pastries, cheese plate and toast in the morning! There are cooks which prepare the food just in time and fresh. It was a good start into a new day.

Then we went to the building where the competition was held. We checked in with the organizers, were given some merchandise and went to the lecture hall. On the first day, the program consisted of presentations by the organizers in the morning and in the afternoon poster session of the competitors .

Most of the participants were Chinese, I was one of the few foreigners. The organizers asked me whether I want a ear piece for simultaneous live translation and I declined. I wanted to see whether my Mandarin was good enough. It was for the most part ok. Then, the introduction started followed by quite interesting talks of several professors working in brain-inspired computing. While I work in machine learning, that is not my field of expertise. I always feel that listening to talks in fields your are not familiar with is very insightful and gives you a completely different view on something. That is also was happened. The talks were in Chinese, I got most of it but had struggle to understand some technical terms.

After the talks, each group was asked for a short interview. We first chatted with the moderator on Chinese and then were taped speaking English.

During lunch, another friend of mine which I met in Germany and now lives in Beijing also came by. We exchanged gifts and the newest gossip. It was nice to have the chance to see her again. We then prepared for the poster session and demo of our app. I brought a second smart phone which just runs the app for that, printed some large Hanzi to scan and also brought a calligraphy set a good friend gifted me. It uses a brush and water on a special paper which gets black if it gets wet and turns blank again on drying. 

We presented our poster to the visitors, jury and fellow participants. I gave demos mostly in Mandarin and it worked reasonably well. Many people were interested in our app, but some of the jury members just quickly had a look and then went to other posters. I assume it was because our entry was not brain-inspired enough (although we created an entry according to the call for participation in the education category).

In the end, it was a really long day after the flight and jetlag. I was happy when the poster session was over and quickly went back to my hotel and fell asleep.

<center>
{{< gallery album="yangtao-day1" >}}
</center>

### Day 2

Sunday, the second and last day of the competition again started with a very nice breakfast in my hotel. Then, back in Tsinghua, it was time for the final presentations of each group. Every group had to present their work and was afterwards questioned by the jury. The other participants were really good, many of them studied brain-inspired computing, work a long time in the field or are even doing a related PhD. 

I was still tired from the jetlag so it was sometimes difficult to follow. Most of the talks were in Mandarin and I did not get too much from them as I lacked the technical vocabulary and did not understand their topic too well. I should have taken the translator. Many works were about spiked neural networks which I never used before. It will be interesting to see practical applications using these!

Our talk was scheduled to be one of the last in the afternoon. I was really nervous, especially for the questions of the jury as they seemed not so interested in our topic the day before. When we presented, I managed to contain this thought and and we got it done. The questions were ok, but we still had lots of time at the end which was a bit awkward. I was very happy when it was over.

Finally, the last few teams presented and the jury went outside to discuss the final ranking. They took a long time to decide, much more than what was allotted in the schedule. I did not expect to be ranked high, so I tried to calm down and lower my expectations. In the end, we were called 11th place out of 16 in the finals and over 200 participants in total. While I would of course loved to be better, I am in hindsight satisfied with the result. We were invited to the finals, not called last, participated with a topic that was not a perfect fit and competed with groups who do a PhD in this area.

After the award ceremony was a party which we did not participate in. The room mate and best friend of LanLan came by and I was introduced. She studies art in Tsinghua, is very talented and nice. She showed me some of her drawings. We went to the supermarket to shop and learn for a bit, we planned my departure and later I went to the hotel.

<center>
{{< gallery album="yangtao-day2" >}}
</center>

### Day 3

The last day of my stay in Beijing was a Monday. After the breakfast, LanLan had to attend classes so I went back to my room, packed and checked out. We agreed that we go to lunch together and then her friend takes me with her electro scooter to the shuttle bus. 

There are many cafeteria in Tsinghua, the one we went there was really good and really cheap. I wish the same was true for my university. I did not want to leave Tsinghua but I had to. We went to the bus and said farewell. I hope I will have the chance to go back! 

{{< figure src="day3_mensa.jpg" lightbox="true" >}}

The bus took its time and I feared that I arrive late, Beijing has many cars and traffic jams. I arrived in time, but then the plane got late so I almost missed my connecting flight in Chengdu. In the end, I made it but it was very stressful. I arrived in Germany on Tuesday morning and just started to work a bit from home. Flying back from China never causes me jetlag. It was good to be back but I miss China.

### Conclusion

It was an incredible experience to go do Tsinghua, one of the best universities in the world and the best in China. I wish I could have studied there. There are many exchange students, but it is too late for me now doing a PhD to do an exchange. I really envy them and wonder how good their Mandarin is.

The competition was very well organized, better than some conference I know. The food was good, there were many refreshment during breaks. It was a bit tiring though to fly to China just for weekend. Getting the visa as well as preparing all the deliverables was a bit stressful.

Our competition entry was not so brain inspired. I knew that would cause a problem beforehand, but we still made it to the finals and won some cash. It was difficult to find another topic as brain-inspired computing is not my field of expertise.

The app development itself was ok, ARCore and Sceneform are not used so widely therefore I had some trouble with it. But in the end, we created a prototype that worked well when actual users used it. We used Tensorflow and OpenCV on a smartphone, which is also kind of cool.

It was overall a great experience, I learned many new things and I am happy that LanLan talked me into participating. I had the chance to see friends that I had not seen in a long while.

## Acknowledgements

We want to thank the ICCBC 2020 organizers for inviting us and covering my expenses. We used the following resources from third parties:

1. We use SVG and dictionary from [MakeMeAHanzi](https://github.com/skishore/makemeahanzi)
2. We use the SCUT-SPCCI Hanzi images created by the [Group of Lianwen Jin of South China
University of Technology](http://www.hcii-lab.net/data/scutspcci/download.html) as training data for the character classifier
3. We use [The dictionary Etymological Dictionary of Han/Chinese Characters by Lawrence J. Howell](http://nihongo.monash.edu/Etymological_Dictionary_of_Han_Chinese_Characters.pdf)