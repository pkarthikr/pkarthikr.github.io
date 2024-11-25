+++
title = "The Fibonacci Sequence"
date = "2020-03-10T16:07:05-08:00"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = ["coding",]
+++

Of late, I’ve been trying to get to the base of how algorithms and mathematics works in general. I’ve wanted to do this for a while because I have an inane fear of Mathematics, and I wanted to face it.

This was also an effort to deep dive into the fundamentals of Computer Science, a topic dear to my heart, but something I’ve ignored for a while. I chanced upon [Teach Yourself CS](https://teachyourselfcs.com/), a good roadmap for getting started with brushing up your CS fundamentals.

As a part of this roadmap, I’ve been solving programs on Project Euler, Hacker Rank and other competitive coding websites. And almost all programs will have a challenge that includes the [Fibonacci Sequence](https://en.wikipedia.org/wiki/Fibonacci_number).

For ex : Here is Project Euler’s 2nd Program

> Each new term in the Fibonacci sequence is generated by adding the previous two terms. By starting with 1 and 2, the first 10 terms will be:
> 
> 1, 2, 3, 5, 8, 13, 21, 34, 55, 89,
> 
> By considering the terms in the Fibonacci sequence whose values do not exceed four million, find the sum of the even-valued terms.

and here’s how I solved it

        i = 0
        j = 1
        sum = 0
        num = 0
        while (num < 4000000):    
             num = i + j    
             i = j    
             j = num    
             if num % 2 == 0:        
             sum = sum + num    
        print("Final Sum is")
        print(sum)
    

If you can overlook my use of the while loop and my amateur Python skills, this looks like a good start. However while working on this program, I went on a rabbit hole, trying to read more about Fibonacci Sequence.

That’s when I stumbled upon the different applications for the sequence. One fun use case is [Planning Poker](https://en.wikipedia.org/wiki/Planning_poker), where participants in a Scrum meeting are given the sequence cards for estimation. But what enchanted me was the fact that the sequence appears in [biological settings](https://en.wikipedia.org/wiki/Fibonacci_number#Nature) as well. For ex: Some flowers are pentagonal because of the arrangement of spirals.

And it also extends into genealogy as well. Bees for that matter.

*   If an egg is laid by an unmated female, it hatches a male or drone bee.
*   If, however, an egg was fertilized by a male, it hatches a female.

And thus, if one were to trace the ancestory of any male bee, he has 1 parent bee, 2 grandparents, 3 great grand parents and so on.

While learning all these facts about how mathematics and nature are interlocked, I chanced upon a Rene Descartes quote

**In my opinion, everything happens in nature in a mathematical way.**

Indeed.