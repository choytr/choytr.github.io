---
layout: essay
type: essay
title: "The intricacies of internet literacy"
# All dates must be YYYY-MM-DD format!
date: 2023-09-05
published: true
labels:
  - Stack Overflow
  - Internet Literacy
  - Questions
---


The concept of internet literacy refers to one's ability to utilize the internet effectively in order to gain information or fulfil one's objectives. The internet is a vast place with an over-abundance of information, but in order to use it well, you must know where and how to look for answers. It is ultimately your own fault for not knowing how to find the answer you are looking for, or whether or not your problems are even solvable through the internet. However, in some cases your own shortcomings will not only affect you. If you choose to approach a forum and use a discussion thread, you are choosing to consume the time and efforts of other living, breathing humans. Poorly asking a question in such forums will not only result in you getting ignored, but it will also waste the valuable time of the people who chose to spare you their time to attempt to comprehend and formulate an answer for you. Here, we take a look at two threads that represent some features of a horribly formulated question post, and an amazing one.

## The Bad Thread

In this [Stack Overflow thread](https://stackoverflow.com/questions/77049706/create-custom-tab-bar-in-flutter), the title, which reads "Create custom tab bar in flutter," does not read like a technical problem whatsoever. In fact, it does not even look like a problem; it looks like the title for a tutorial article on tab bars in Flutter. Titles are the first thing that any forum browser will see. They are the first impression to a question among the sea of countless queries that pop up every single minute. If, in the very first few words, you cannot convey the issue you are having clearly, it will almost always be ignored.

However, this is a secondary priority to simply having a quality problem to post to a forum, and this thread fails to accomplish even that. A good forum discussion or support post topic would not be so vague or overly-complicated for the forum's users to have an easier time answering. In this case, from the body of the post it appears this post was made to ask how to create a custom tab bar in Flutter. Two screenshots are provided, one presumably of a desired outcome, and the other... showcases the poster's abilities? A question like this asking for an entire tutorial on how to design and create an entire user-interfacce is way too vague and encompasses too many aspects for anyone to spend a reasonable amount of time asking. Instead, the poster's time would have been much more well-spent even attempting to start creating their desired interface, and later create a forum post once they discover a specific issue during development.

There is also an unbelievably giant block of code with zero explanation at the end of the post. Assuming it is the code for the tab bar they are developng, it is way too long and complex for any single person to comprehend, not to mention the lack of explanation for its existence. Is there something to debug? Is there something wrong with the code? Are they looking for suggestions to make it cleaner?

As a result of the original poster's ill-preparation and horrendous lack of thought in formulating their post, zero answers have been contributed.

## The Good Thread

In stark contrast, [this thread](https://stackoverflow.com/questions/77042490/github-page-url-not-being-github-io-repo-about-but-github-io-about-instead) is formatted excellently. Following a concise 'object-deviation' format, a glance at the self-explanatory title "Github Page url not being github.io/repo/about but github.io/about instead" is all it takes to understand the problem at hand.

Details of the topic at hand have been explained clearly. With the line:
```
What I have right now is: user.github.io/about
```
their symptoms were given, and the next line:
```
What I want is: user.github.io/portfolio-web/about
```
a desired outcome was stated simply and concisely.

Immediately after, a code sample was presented: 
```
<Routes>
  <Route exact path="/" element={<Home />} />
  <Route path="/about" element={<AboutMe />} />
  <Route path="/contact" element={<Contact />} />
  <Route path="*" element={<NotFound />} />
</Routes>
```
making it even easier for passerbys to potentially diagnose the problem.

In addition, its topic was obviously something the original poster had contemplated and attempted to solve on their own. Having explained that they had attempted to do their own research to solve the problem themselves, new users reading their post will understand that they could use some help to push them in the right direction and will be more willing to contribute an answer. 

This well-thought out forum post netted a meaningful answer from a user that led to a discussion between the two further diagnosing the issue, eventually leading to a solution.

## Conclusion

Today, the world almost completely revolves around the internet. If you are unable to use the vast resources available on the internet, you will be left behind in the dust. To avoid this and to become successful in life, you must be competent at using the internet, and have internet literacy. As demonstrated by the two example threads provided above, preparation and thoughtfulness in forum posts are just one way to garner good information and support, and in contrast, a monkey-brained post will net you absolutely no results in the best case.
