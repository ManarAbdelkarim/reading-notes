# Dunder Methods

## What Are Dunder Methods?

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

- As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”

![](https://miro.medium.com/max/3220/1*g6LbGqMogPuFiHojMmSFTw.png)

- These “dunders” or “special methods” in Python are also sometimes called “magic methods.

- Dunder methods let you emulate the behavior of built-in types

- Object Initialization: __init__ :

   - Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder

- __repr__ : The “official” string representation of an object. This is how you would make an object of the class. The goal of__repr__is to be unambiguous.

- __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

- Callable Python Objects: __call__ : You can make an object callable like a regular function by adding the __call__ dunder method

# Basic Statistics in Python — Probability

## what is probability?
Probability is the branch of mathematics concerning numerical descriptions of how likely an event is to occur, or how likely it is that a proposition is true.

The probability of an event is a number between 0 and 1, where, roughly speaking, 0 indicates impossibility of the event and 1 indicates certainty.

![](https://lh3.googleusercontent.com/proxy/LtE9ia6lHJC0X5n-W6lNr3Xc3wkz1-AhuVN1APwHvL9P6if4Ee7y-pGdXwuQKy6JmskcbpbTc4cSmyXE1o0LzygYFBqvuwjDmOhVNOvzWrUzvht4cBfg__4JQDW9zQWqwvOM)

- At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?” An event is some outcome of interest. To calculate the chance of an event happening, we also need to consider all the other events that can occur.

- The quintessential representation of probability is the humble coin toss. In a coin toss the only events that can happen are:

- Flipping a heads
- Flipping a tails

```
These two events form the sample space, the set of all possible events that can happen. To calculate the probability of an event occurring, we count how many times are event of interest can occur (say flipping heads) and dividing it by the sample space.
```

We started with descriptive statistics and then connected them to probability. From probability, we developed a way to quantitatively show if two groups come from the same distribution. In this case, we compared two wine recommendations and found that they most likely do not come from the same score distribution. In other words, one wine type is most likely better than the other one.

Statistics doesn’t have to be a field relegated to just statisticians. As a data scientist, having an intuitive understanding on common statistical measures represent will give you an edge on developing your own theories and the ability to subsequently test these theories.

We barely scratched the surface of inferential statistics here, but the same general ideas here will help guide your intuition in your statistical journey.

Our article discussed the advantages of the normal distribution, but statisticians have also developed techniques to adjust for distributions that aren’t normal.