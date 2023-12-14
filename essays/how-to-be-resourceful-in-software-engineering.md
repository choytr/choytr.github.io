---
layout: essay
type: essay
title: "How to be resourceful in software engineering"
# All dates must be YYYY-MM-DD format!
date: 2023-12-10
published: false
labels:
  - Software Engineering
  - Javascript
  - Artificial Intelligence
  - ChatGPT
  - Design Patterns
  - User Interface Frameworks
---

## Resourcefulness in Software Engineering
I learned a lot from ICS 314, Software Engineering I, but by far my biggest takeaway is that one of the most crucial skills you can have as a software engineer is the ability to be resourceful. What I mean by that is how to use the tools around you to write high quality code. This includes how to read documentation, how to dig through forums, and possessing the general knowledge about how to find what you need. It is an intuition, a skill, that you develop as you do more development. It does not matter what programming language you need to write in, or what specific technology you are required to utilize, as depending on the context, you can either gain a lot or very little by completely knowing a specific piece of technology inside out. Regardless, you simply can't learn everything. Now more than ever, knowing how to use the resources around to to do just what you need to is imperative.

My experience in learning software development through ICS 314 was focused on the development of websites. The majority of the semester was spent building up the fundamental skills necessary to build a website using Meteor, a full-stack (provides both front-end and back-end) web application development framework that implements React for the user interface and MongoDB for the database of the application. The last month of the semester was the duration of our final project, which was to build a full Meteor application from scratch. See the [Lendor Vendors project](https://choytr.github.io/projects/lendor-vendors.html) for more details. By the end the development process of the final project, the most important thing I gained was not knowledge about React, MongoDB, or Meteor. It was the ability to look things up.

### The Final Project
Upon starting the final project, very quickly did I realize how little I actually knew. The course had prepared me as best as it could. There was no way you can teach as much information as was needed for this project in such a short span of time. You had to look things up, use the resources available to you, ask for help among your peers, etc. As quickly as I realized that this was the point of the course, to teach you that software development is a LOT of on-the-spot learning, I also realized my incompetence when it came to browsing the web for resources. I did not know the proper terminology for describing the techniques we needed, and I was really bad at deciphering dense documentation.

Over time, however, I did manage to speed up my development process. I got the hang of browsing Stack Overflow threads and coding tutorials to cherry-pick the precise information I needed. But I still felt like I was being very inefficient. Internet surfing can be very time-consuming, so I thought there had to be something I wasn't doing that would boost my productivity tremendously. And there was.

### Artificial Intelligence
Artificial intelligence is an incredible tool programmers can use. In [this essay](https://choytr.github.io/essays/artificial-intelligence-not-code.html), I discuss that, for most of ICS 314, I refrained from using artificial intelligence despite the course actively encouraging the use of it. I had too much pride in myself as a programmer and refused to resort to something that has a reputation for allowing students to cheat in their academics. However, for this final project, I decided to give ChatGPT a try, and it was the best decision I could have made. Hours upon hours of scrounging the internet for answers was immensely simplified and condensed into just a few seconds, as I discovered that one of the best things about ChatGPT is that it is really good at searching the internet and accurately summarizing documentation and internet threads for you- something that is really slow and painful for a human being, but easy for a generative AI like ChatGPT. Thus, it ended up being the perfect tool for me. In the above essay, I list my common use cases of ChatGPT throughout ICS 314.

## Software Engineering Concepts
Moving to the broader context of the entire course of ICS 314, I realize that many of the things I asked ChatGPT to explain or summarize closely tied into the concepts of software engineering that ICS 314 taught me.

### User Interface Frameworks
A big focus of ICS 314 was the use of user interface frameworks. There are many [frameworks](https://choytr.github.io/essays/tools.html) that do similar things very differently, but at their core, they really all just provide different ways of writing HTML. As a software developer, it is your job to know how to use the framework(s) you choose. In my case, it was Twitter Bootstrap and React.

When you get into using a framework, it really feels like you are immersing yourself in a whole way of life. What I think really defines React is its reactivity, and the tools it provides, like hooks, to harness the power of its reactivity. However, I didn't get to a point of proficiency with React by myself. Of course, I used ChatGPT to learn about React features that I would never have known about otherwise.

Then there came a point where the team decided to switch all our buttons from using Bootstrap buttons to using buttons from a library called Material UI (MUI). Initially, switching every button was straight forward, as all we had to do was change a single line of code in each file we had. But then, a slight issue arose when trying to convert a bootstrap dropdown menu into an MUI button. Asking ChatGPT for a solution led me to the discovery of the `as` React property, which was the answer to our problem. We could render a Bootstrap dropdown button "as" an MUI button.


### Design Patterns
Design patterns are reusable solutions to common problems that occur during software development. They are basically templates or guidelines to solve recurring problems in an efficient and maintainable manner. I talk about them in more detail [here](https://choytr.github.io/essays/applying-design-patterns.html).

In the context of the final project, we were implementing a few design patterns without even knowing it, such as the observer, model-view-controller, and React reusable components. In all of these contexts, ChatGPT played a role in providing effective solutions, likely because it has knowledge of design patterns.

## Conclusion
In summary, ChatGPT is a great resource for discovering things about a user interface framework or solutions for applying a specific design pattern across different contexts.