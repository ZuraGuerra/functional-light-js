# Functional-Light JavaScript
# Chapter 1: Why Functional Programming?

> Functional programmer: (noun) One who names variables "x", names functions "f", and names code patterns "zygohistomorphic prepromorphism"
>
> James Iry ‏@jamesiry 5/13/15
>
> https://twitter.com/jamesiry/status/598547781515485184

Functional Programming (FP) is not a new concept by any means. It's been around almost as long as any programming has been around. I don't know if it's fair to say, but it sure hasn't seemed like as mainstream of a concept in the overall developer world until perhaps the last few years. I think FP has more been the realm of academics.

But that's all changing. There's a groundswell of interest growing around FP, not just at the languages level but even in libraries and frameworks. You very well might be reading this text because you've finally realized FP is something you can't ignore any longer. Or maybe you're like me and you've tried to learn FP many times before but struggled to wade through all the terms or mathematical notation.

Whatever your reason for reading this book, welcome to the party!

## Confidence

I have a very simple premise that sort of underlies everything I do as a teacher of software development (in JavaScript): code that you cannot trust is code that you do not understand. And furthermore, if you cannot trust or understand your code, then you can have no confidence whatsoever that the code you write is suitable to the task. You run the program and cross your fingers.

What do I mean by trust? I mean that you can verify, by reading, not just running, that you understand what a piece of code *will* do, not just relying on what it *should* do. Perhaps more often than we should, we tend to rely on verification of our program's correctness by running test suites. I don't mean to suggest tests are bad. But I do think we should aspire to be able to understand our code well enough that we know the test suite will pass before it runs.

I believe the techniques that form the foundation of FP are designed from the mindset of having far more confidence over our programs just by reading them. Someone who understands FP, and who diligently uses it in their programs, will write code that they can read and verify, by the principles they have already proven to be true, that the program will do what they want.

It is my hope that you will begin to develop more confidence in the code you write, and that these functional-light programming principles will be carry you in that direction.

## Communication

Why is functional programming important? To answer that, we need to take a bigger step back and talk about why programming is important?

It may surprise you to hear this, but I don't believe that code primarily exists to instruct the computer. As a matter of fact, I think the fact that code does instruct the computer is almost a happy accident.

I believe very deeply that the vastly more important role of code is a means of communication with other human beings.

You probably know by experience that an awful lot of your time spent "coding" is actually spent reading existing code. Very few of us are so privileged as to spend all or most of our time simply banging out all new code and never dealing with code that others (or our past selves) wrote.

Did you know that researchers who've studied this topic say that we spend 70% of our "maintaining code" time just reading it to understand it? I find that shocking. 70%. No wonder the global average for a programmer's lines of code written per day is around 5. We spent the other 7 hours and 30 minutes of the day just reading the code to figure out where those 5 lines should go!

I think we should pay a lot -- a LOT! -- more of our time focusing on the readability of our code. Like, a lot more. And by the way, readability is not about least number of characters. Readability is actually most affected by familiarity (yes, that's been studied, too).

So, if we are going to spend more time concerned with making code that will be more readable and understandable, FP turns out to be a really handy pattern in that effort. The principles of FP are well established, deeply studied and vetted, and provably verifiable.

If we use FP principles, I believe we will create code that is easier to reason about, because once we know these principles, they will be recognizable and familiar in the code, meaning we'll spend less time figuring that part out when we read a piece of code. Our focus will be spent on how all the well-known, established lego pieces are assembled, not on what those lego pieces mean.

I think FP is one of the most useful tools for writing readable code. *That* is why it's so important.

## Take

We're going to approach FP from the ground up, and uncover the basic foundational principles that I believe formal FPers would admit are the scaffolding for everything they do. But for the most part we'll stay arms length away from most of the intimidating terminology or mathematical notation that can so easily frustrate learners.

I believe it's less important what you call something and more important that you understand what it is and how it works. That's not to say there's no importance to shared terminology -- it undoubtedly eases communication among seasoned professionals. But for the learner, I find it can be somewhat distracting.

So I hope this book can focus more on the base concepts and less on the fancy terminology. That's not to say there won't be terminology; there will be. But don't get too wrapped up in the fancier words. Look beyond them to the ideas. That's what this book is trying to be about.

I call the less formal practice herein "Functional-Light Programming" because I think where the formalism of true FP suffers is that it can be quite overwhelming if you're not already used to formal thought. I'm not just guessing; this is my own personal story. Even after teaching FP and writing this book, I can still say that the formalism of terms and notation in FP is very, very diffcult for me to process. I've tried, and tried, and I can't seem to get past much of it.

I know many FPers who believe that the formalism itself helps learning. But I personally think there's a very definite cliff where that only becomes true once you reach a certain comfort with the formalism. If you happen to already have a math background or even some flavors of CS experience, this may come more naturally to you. But some of us don't, and no matter how hard we try, the formalism keeps getting in the way.

So this book aims to introduce the concepts that I believe FP is built on, but come at it by easing you up the cliff rather than throwing you straight at it to figure out how to climb as you go.

## Resources

I have drawn on a great many different resources to be able to compose this text. I believe you too may benefit from them, so I wanted to take a moment to talk about them.

### Books

Some FP-JavaScript books that you should definitely read:

* [Professor Frisbee's Mostly Adequate Guide to Functional Programming](https://drboolean.gitbooks.io/mostly-adequate-guide/content/ch1.html) by [Brian Lonsdorf](https://twitter.com/drboolean)
* [JavaScript Allongé](https://leanpub.com/javascript-allonge) by [Reg Braithwaite](https://twitter.com/raganwald)
* [Functional JavaScript](http://shop.oreilly.com/product/0636920028857.do) by [Michael Fogus](https://twitter.com/fogus)

### Blogs/Sites

Some other blogs/authors/content you should check out:

* [Fun Fun Function Videos](https://www.youtube.com/watch?v=BMUiFMZr7vk) by [Mattias P Johansson](https://twitter.com/mpjme)
* [Awesome FP JS](https://github.com/stoeffel/awesome-fp-js)
* [Kris Jenkins](http://blog.jenkster.com/2015/12/what-is-functional-programming.html)
* [Eric Elliott](https://medium.com/@_ericelliott)
* [James A Forbes](https://james-forbes.com/)
* [James Longster](https://github.com/jlongster)
* [André Staltz](http://staltz.com/)
* [Functional Programming Jargon](https://github.com/hemanth/functional-programming-jargon#functional-programming-jargon)

### Libraries

This book is not going to use libraries for any of its code. Each operation that we discover, we'll derive how to implement it in standalone, plain ol' JavaScript. However, as you begin to build more of your code with FP, you'll quickly want to turn to a library to provide optimized and highly audited versions of these operations.

By the way, you'll want to make sure you check the documentation for the library functions you use to make sure you know how they work. There will be a lot of similarities in many of them to the code we build on in this text, but there will undoubtedly be some differences.

There are a bunch of different libraries that adopt FP into JavaScript. Here are a few popular ones you should start your exploration with:

* [Ramda](http://ramdajs.com)
* [lodash/fp](https://github.com/lodash/lodash/wiki/FP-Guide)
* [functional.js](http://functionaljs.com/)
* [Immutable.js](https://github.com/facebook/immutable-js)

## Summary

This is Functional-Light JavaScript (FLP). The goal is to learn to communicate with our code but not suffocate under mountains of notation or terminology to get there. Welcome to the party!
