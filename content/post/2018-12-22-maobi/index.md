---
title: "maobi - Learning to write Hanzi in Anki"
date: 2018-12-22
tags: ["anki", "Mandarin", "programming"]
---

For over three years now, I learn Mandarin after lectures or after work. To stay motivated, I take the HSK Chinese proficiency exams. In November, I took HSK 4. While my scores were high in listening and reading, my writing score was pretty low (I am still a bit sad about it). To be honest, that was not too much of a surprise, as I up to then skipped writing practice. Therefore, I felt that I need to practice more writing Hanzi.

Because I like programming, I created *máobĭ* (毛笔), an [Anki](https://apps.ankiweb.net/) add-on that allows you to have cards with Hanzi writing quizzes. Have a look:

<img src="https://raw.githubusercontent.com/jcklie/anki-maobi/master/img/maobi.gif" class="img-responsive center-block">

Learning Chinese is difficult, remembering what you have learned even more so. I heavily rely on Anki to review my vocabulary. It has changed my study life and made it possible for me to remember all the words, characters, chengyu, sentences and pass my university exams.

While Anki itself is good to remember the meaning of words and characters, I found it difficult to use for remembering writing Hanzi. There is the possiblity of using [AnkiDroid](https://github.com/ankidroid/Anki-Android) and the built-in whiteboard or defining a workflow as described in a [blog entry of EastAsiaStudent](https://eastasiastudent.net/study/skritter-functionality-for-free/). I tried it, but I did not like it too much.

A paid alternative that I used heavily in the past is [Skritter](https://skritter.com/). Right now, I really dislike the Version 2, their update policy and the bugs in the scheduling. It also is really unresponsive, making me wasting (lots of!) time by just waiting for the app. A contender of Skritter for mobile is [Inkstone](https://www.skishore.me/inkstone/), but I did not get warm with that either. 

Another aspect is that I personally do not like to use many different programs and tools to collect vocabulary. Therefore, I built *maobi* to remember writing Hanzi within *Anki*. Now, I have all my learning progress in one tool!

*maobi* is open-source and MIT licensed. You can find the code on [Github](https://github.com/jcklie/anki-maobi).

## Quickstart

1. Install the addon via the code found on the [maobi Anki page](https://ankiweb.net/shared/info/931477147). (Chinese characters)
2. Download and import the [example deck](https://github.com/jcklie/anki-maobi/blob/master/data/Maobi.apkg).
3. Restart Anki.
4. Open the deck and start writing!

## Disclaimer

*maobi* is still early in development. I use it daily, but your mileage may vary. If you encounter bugs or miss features, please send me a mail to <blog@mrklie.com> or open an issue in the [Github repository](https://github.com/jcklie/anki-maobi/issues).

## Acknowledgements

I did not design the writing component, it comes from the awesome [Hanzi Writer](https://github.com/chanind/hanzi-writer) JavaScript library. Without it, this would not be possible. *maobi* merely bundles it with Anki. Please visit the *Hanzi Writer* website and look how nice it looks! 

The Chinese character and stroke order data used by *Hanzi Writer* is derived from [Make me a Hanzi](https://github.com/skishore/makemeahanzi). The data can be found in the [Hanzi Writer Data](https://github.com/chanind/hanzi-writer-data) repo.