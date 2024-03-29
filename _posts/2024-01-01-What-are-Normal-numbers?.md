---
title: 'What are Normal Numbers?'
date: 2024-01-01
permalink: /posts/2024/01/blog-post-1/
tags:
  - Numbers
  - Randomness 
  - Normality 
---



I suppose almost everybody would agree that at some point in life, they have been thoroughly fascinated by numbers—specifically, a particular set of numbers. It starts with primes, naturally the most enigmatic set, with no correlation whatsoever to each other. Those who pursue higher education will stumble upon algebraic and transcendental numbers. But once you get past these sets of numbers, there is a vast category, probably encompassing almost all the numbers in the real line, known as normal numbers.

Why do we use the term 'normal' in mathematics when talking about numbers? In math, 'normal' is ubiquitous, appearing in various contexts such as normal vectors, normal lines, normal spaces, and normal distributions. When it comes to numbers, we call a number $x$ normal (written as $0.a_1a_2a_3\ldots$) if a string of $k$ digits shows up just as much as any other string of $k$ digits.

Let's clarify a bit. We're only interested in numbers after the decimal point, and by 'frequency,' you can think of it as being equally likely. For example, '1' should show up as often as '2', '3', '4', '5', '6', '7', '8', '9', and '0.' The same rule applies to something like '666' which should appear as often as any other 3-digit number.

#####  Rigorous definition
>Let $x$ be a number, Let s be a string of $k$ digits , let $N_x(s,n)$ denote the number of times s appears in the first n digit of $x$ then $x$ is normal iff

$$ lim_{n \rightarrow \infty} \frac{N_x(s,n)}{n} = \frac{1}{10^k} \nonumber$$

More natural question is to ask for an example. That's exactly what an undergraduate at Cambridge asked back in 1933, and he actually came up with one. It's now called the `Champernowne Constant` named after its creator, D.G. Champernowne.

$$ 0.1234567891011121314151617181920\ldots \nonumber$$ 

This is a bit out there, isn't it? You take all the natural numbers and concatenate them together. Surprisingly, every one-digit number appears roughly one-tenth of the time. My phone number, your phone number, and almost everybody's phone number appear as frequently as any other. Moreover, every word can be written as a string of numbers. In this way, everybody's biography is inside this number. For instance, both Henry VI (part 2) and Romeo and Juliet are encoded within the same number, as they have roughly the same number of words, ensuring they appear with equal frequency. 

Is this the only example? No, there are a handful of examples. Another famous one is the `Copeland–Erdős constant`

$$ 0.235711131719232931374143\ldots \nonumber$$

My first thought was that this has to be wrong. The same properties that Champernowne Constant had is can be said about this number. Prime numbers are not dense in natural numbers. How can this work? Well, Copeland and Erdős proved it works using something called $\(\epsilon,k\) - normal$ property. 

This is all fascinating; we can construct numbers, but can we take the numbers we already know and declare that one or more of them are normal? We have a plethora of irrational numbers. The short answer is **NO**.

Look at $\pi$ for example; we have calculated this number to trillions of digits, and there are [websites](https://www.atractor.pt/fromPI/PIalphasearch-_en.html) where you can go and check whether your name is in it or not. So far, empirically, it seems to be a normal number, but we have not proven it outright.

Simultaneously random and not, constructing normal numbers can be as simple as rolling a 10-sided die infinitely many times and concatenating the digits. The magic of this intersection between order and randomness within mathematics is truly captivating. 

As I reflect on this exploration, I'm left with numerous questions and an eagerness to uncover more hidden patterns within the vast landscape of numbers. How do these mathematical concepts resonate with your understanding of randomness? What other mysteries might lie waiting to be revealed?

Thank you all for your constant support, and I look forward to continuing this journey of mathematical discovery together."
**CHEERS**

## Epilogue 

* This is completely talked with respect to base 10, there is normality in other bases as well.
* I do wish to talk about how random in mathematics is very different from how we perceive in real life.
* The density of prime numbers is also another topic
* References
  * Champernowne, D.G. (1933), The Construction of Decimals Normal in the Scale of Ten. Journal of the London Mathematical Society, s1-8: 254-260. [https://doi.org/10.1112/jlms/s1-8.4.254](https://doi.org/10.1112/jlms/s1-8.4.254).
  * [A thesis by a G. Pomstra from university of groningen](https://fse.studenttheses.ub.rug.nl/17907/1/The%20Constant%20of%20Champernowne.pdf)
  * [The Abnormality of Normal Numbers by Dr.Joseph Vandehey ](https://www.youtube.com/watch?v=G3MwnMo7tio&t=2216s)
  * [All the Numbers - Numberphile](https://www.youtube.com/watch?v=5TkIe60y2GI)
