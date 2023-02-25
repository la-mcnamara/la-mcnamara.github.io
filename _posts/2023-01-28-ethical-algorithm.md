---
layout: post
title: "Book Review: The Ethical Algorithm"
date: 2023-01-28
---

I just finished reading The Ethical Algorithm by Michael Kearns and Aaron Roth.

I currently serve as head of the AI Ethics Committee at HCSC. We are forging new ground daily in evaluating a large number of data science projects for bias. I hoped this book would help provide some insight into the practical problems the committee faces, including how to explain the need for bias analysis, how to perform a bias analysis in different scenarios, or be a source I could cite as projects had questions on our methodology. 

I'm not sure I got too much of any of that out of the book, but I did really enjoy reading it. This book is high-level and not mathy. It does a great job of explaining different concepts related to algorithmic fairness.

A main takeaway for the book is that similarly to how computers will only do what you tell them to, algorithms will only optimize for what you tell them to optimize for. If you don't tell them to optimize for fairness, they won't. As anyone who's ever written code will tell you, while the computer will only do what you explicitly said to do, sometimes you tell it to do something you didn't intend. And those bugs can be hard to find! 

Maybe you're now convinced that optimizing for fairness in addition to accuracy (or your preferred metric) is important. The next problem is that you can't optimize for many different goals at once. Your model may need to make some tradeoffs in predictive ability to make it less biased. The authors suggest a Pareto curve for assessing the tradeoffs and finding an appropriate balance of fairness and accuracy. I like this technique and hope to apply it in my work.

I learned about a few other things in addition to algorithmic fairness. The first chapter is about differential privacy, which is not something I previously studied. I now think that differential privacy is pretty cool! The general idea is that you purposely introduce random noise into your data, and that will wash out at a large scale. They gave a survey research example where respondents would be asked a question, and then asked to flip a coin; if heads they give their true answer and if tails a made-up answer. If you poll enough people on the question the true population average will still come out. I think this is a potentially exciting idea to be able to put more data into public use files, which are typically pretty abbreviated. But I also know how hard surveys need to work for each complete, and the idea of introducing false data makes the old survey research part of me shudder.

The chapter about game theory was also interesting - I hear about game theory all the time, in particular it being the root theory behind shap values, but I don't know much about actual game theory. I wouldn't call myself an expert yet but this was a nice introduction.

Finally, the book made an interesting point about human in the loop modeling. The authors suggest that we use algorithms to make decisions at speed and scale, and if you're retaining a human in the process, you're going to slow down that speed and scale and so what's the point of using the algorithm. This is reasoning I come across in my work socializing ethics to projects at work - a team will say that they will retain a human in the loop making the final decision for the algorithm, and the algorithm just helps the human. I don't really buy into this because 1) I agree with the authors, why build the model, and 2) the human is going to be influenced by the algorithm. For the number of times I've heard someone say "my computer doesn't like me" or "this (piece of technology) just does that", I think the inclination of many humans would be that the algorithm knows something they don't, so maybe they should just go with that. And never mind that a reason our models can be susceptible to bias is bias introduced by biased humans in the training data. Human in the loop just doesn't seem like a stopgap to me!

Overall I thought this was a good book and I'd recommend it to anyone interested in a broader treatment of ethics and algorithms.
