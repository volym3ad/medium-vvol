
# System Design Guide



System Design is quite interesting topic to talk about. Wherever you work as an IT Engineer it’s unavoidable for you to face with system design. By having hundreds of thousands examples of running projects we can outline some best practices when it comes to building tech systems. Ever since I’ve first heard about system design I’ve realized that this is really worth studying. Now I want to share my notes I’ve accumulated during my investigation and practice.

## Know your enemy

This quote came from “The Art of War” written by Sun Tzu more that two centuries ago. But it’s still valid even in IT sphere. When you start working on project, first thing you should do is to find out what it consist of.

But that’s only the beginning. We all know that same product can be done via dozens of methods. Here is where your knowledge is needed. You should understand the pros and cons of each approach, method or technology. Only then you can determine what will fit better in specific case.

Of course this goal can be reached only by combining both theory and practice. The harder you work, the faster you can become pro you want to be. It’s inevitable!

## It’s not always about technology

With such variety of technologies it’s easy to get lost) You simply do not know where to start from. I’m facing this every day! Every week, every day or sometimes every hour new technologies, new versions of existing ones arise. Right question here is — how can I choose?

My opinion is: “Don’t be fooled by hype, experiment by yourself”! Before using technology in production you need setup it in dev/stg environment, run bunch of tests and only then to move on. This will led us to one more rule to follow: if you’re not sure about technology, do not use it.

Remember that one “magic” technology won’t solve all your problems. It’s a set of architectural patterns, hard decisions and trade-offs that run your business.

## The less complicated, the better

After you get familiar with pool of technologies and their usage, it’s time for you to discover another rule. You should always make your system as easy as it can be. Try to build with the following in mind: “I build it now and it will be my task to support it in future” or even like this “Will I understand what’s going on here after 6 months timeout?”.

Keep in mind that everything is a trade-off. But maintaining the right balance between complexity and productivity of your system is what you must remember all the time.

## Set strict service API contracts

I found great article describing why we should care about API contracts — [https://blog.apisyouwonthate.com/guessing-api-contracts-ac1b7eaebced](https://blog.apisyouwonthate.com/guessing-api-contracts-ac1b7eaebced). Also what if I told you that API should be built with 3 principles:

* predictable response

* understandable response

* reasonable response

The behavior of your service must be expected. Are you sure you’ll always get a predictable response in case of dependency failure? Won’t failure in your service cascade to dependent services? Does your service error responses looks reasonable? Don’t you violate contract somehow? Why you should care about service tiers? This is just a few questions that can help you in creating API contract.

## Avoid SPOF

SPOF stands for Single Point Of Failure. If you want your system to be highly available, you must eliminate any SPOF in your system. It refers to both infrastructure and software aspects. Can you allow yourself to lose a node, sustain network latency? Or would your application be working even if one service went down? Anyway this task requires efforts of whole team.

## Be paranoid O_o

All systems and especially complicated ones are full of risks. These risks must be identified, managed and mitigated. Moreover risks should be regularly reviewed. This is very important topic and must not be overlooked. Create risk matrix, brainstorm it, set mitigation plan — these definitely help you and your team sleep at night =P

## Consult with your colleagues

You can see from the text above that I emphasize on team value. Important to remember — system design require a combination of both hard and soft skills. If you’re not working alone, all system design decisions should be decided collectively with your team. There is a proverb: “Two heads are better than one”.

## Do not stop learning

I guess it’s obvious so won’t stop here. One thing I’ll add is the useful info at the end of article.

## Share your knowledge with others

By sharing your knowledge you gain more karma! However, it’s only one side of coin. The other is that explaining will help you to structure gained knowledge and boost soft skills as well. In my case it helped me to be more patient =)

## **List of github stars that helped me a lot:**

* [https://github.com/donnemartin/system-design-primer](https://github.com/donnemartin/system-design-primer)

* [https://github.com/binhnguyennus/awesome-scalability](https://github.com/binhnguyennus/awesome-scalability)

* [https://github.com/kilimchoi/engineering-blogs](https://github.com/kilimchoi/engineering-blogs)

* [https://github.com/mspnp/performance-optimization](https://github.com/mspnp/performance-optimization)

* [https://github.com/danluu/post-mortems](https://github.com/danluu/post-mortems)

* [https://github.com/Mykolaichenko/devopsfactors](https://github.com/Mykolaichenko/devopsfactors) (*it’s in russian*)

### Plus some sec stuff:

* [https://github.com/FallibleInc/security-guide-for-developers](https://github.com/FallibleInc/security-guide-for-developers)

* [https://github.com/forter/security-101-for-saas-startups](https://github.com/forter/security-101-for-saas-startups)
