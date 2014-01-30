<<<<<<< HEAD
<<<<<<< HEAD
<<<<<<< HEAD
=======
>>>>>>> 632060c... fixing stupidness
---
layout: default
title: Blog Post
type: post
category: iplayer
author: Johnson Cheng
---
<<<<<<< HEAD

=======
>>>>>>> d241606... First draft of the first post of the blog.
=======
----
 -layout: default
 -title: Blog Post
 -type: post
 -category: iplayer
 -author: Johnson Cheng
 ----
=======
>>>>>>> 632060c... fixing stupidness

>>>>>>> 25e249a... adding the metadata
# Problem

BBC Future Media is a big and distributed organisation. This is cool because we produce a lot of awesome stuff online, but it's complex because at any given time there are lots of teams working on different projects, and sometimes, it can be difficult to make sure that every team is building things in the most optimal, secure, scalable, and robust way. 

Historically this problem is solved by the various "Technical Approval Groups" (TAG) or "Design Authority" (DA) we have internally. These TAG or DA meetings generally consist of technical architects or engineering managers from different teams getting together to review different projects from different teams on a regular basis, by going through the technical architecture, technology choice, caching strategy, resilience models, etc. Often times these groups also maintain sets of "technical policies" which are used to measure how good the proposed projects are. Occassionally bad apples get through, but in general these meetings are quite effective in **making sure bad stuff don't get through to Production**. 

Unfortunately, these meetings have a few shortcomings:

1. These meetings are a [negative reinforcement](http://en.wikipedia.org/wiki/Reinforcement#Reinforcement), and does very little to **encourage the engineering teams to make better designs** as time goes on;
2. Since it's effectively a "gate" the teams must go through whenever they want to ship something, it's common for project managers to treat these forums as a tickbox exercise towards the end of a project, rather than **an ongoing forum to discuss technical designs**.
3. The forum is ultimately bottlenecked by the few selected people that attend it. This can sometimes give the impression that technical architecture decisions are made in a vacuum by people who are not writing code daily, and therefore can have the risk of being removed from the **latest trends in best practices and patterns**.

# Solution

To summarise, we want something that can

1. Encourage engineering teams to make better designs;
2. Foster an ongoing discussion around technical designs;
3. Keep the organisation up-to-date with the latest trends in best practices and design patterns.

**The blog you are reading now is the solution we've come up with**. The idea is simple: an engineering-focused blog that allows anyone in the engineering team to capture good engineering designs and best practices, using concrete solutions they've come up with in order to solve real problems as examples. Then hopefully these blog articles would also spark further dialogues in the comment section, so everyone can participate in the discussion.

We want the process to be as democratic as possible, but we also want the signal-to-noise ratio to stay high. A peer review process is a good way to accomplish this. Many teams in the organisation are using Github as a way to facilitate good code reviews (there is actually an upcoming blog about this exact topic!) - so we thought we could apply that model for this blog as well. Here's how anyone can write an entry in this blog:

1. [Fork this github repo](https://help.github.com/articles/fork-a-repo): ``https://github.com/bbc/bbc.github.io``
2. [Create a branch](https://github.com/blog/1377-create-and-delete-branches) to get your blogger hat on.
3. Write a blog entry in Markdown. The bare minimum format requirement is that you must have the following sections:

  | section | contains      |
  |---------|---------------|
  | Problem | State the problem you are solving |
  | Solution | State the solution you came up with |
  | Validation | Prove your solution actually solves the stated problem, effectively. If your problem was a performance or scalability one, graphs and stats would be useful and essential. If your problem was a code quality issue, then static analysis of your code would be a good thing to capture. In certain cases, you may not have enough evidence to prove your case sufficiently yet, but you can point to examples outside of the BBC on how similar solutions have solved similar problems. |
  | Patterns | What are the lessons learned? What generic and useful patterns have you learned from this solution that can be applied to other similar class of problems elsewhere? |
  
4. Commit your awesome blog entry into this directory: ``https://github.com/<you>/BBC.github.io/tree/<branch>/_drafts``
5. [Submit a pull request](https://help.github.com/articles/creating-a-pull-request).
6. A set of tech blog moderators ([yours truly](https://github.com/johnsoncheng), for example) will review it and comment on it. The comments can range from spelling and grammatical errors, to getting more details on a particular aspect of your solution. Don't think of this as censorship, but as quality check (similar to a code review). Moderatorship can be earned if  you contribute to the blog enough times.
7. Once all comments are addressed and everyone's happy as clams, a moderator can then merge it and publish it.
8. Fame and profit for you!!!

# Validation

I've tried hard to follow the format for this post, to bootstrap the process. This section is a bit tricky though, as I bviously don't know yet how well this solution will solve the problem I've outlined above. What I can do though is point to plenty of other organisations that have a prolific engineering blog, and correlate how good they are perceived in the tech world:
- Github: https://github.com/blog/category/engineering
- Etsy: http://codeascraft.com/
- Twitter: https://blog.twitter.com/engineering
- Facebook: https://code.facebook.com/posts/
- Netflix: http://techblog.netflix.com/

It seems pretty self-evident that awesome engineering companies have awesome engineering blogs.

# Patterns

This blog post is a bit of an exception, in that, the problem stated here is not purely a technical one. Instead, these are organisational problems, and this is, more or less, an organisational solution. I think there are a few clear patterns that I can see that would apply to this class of problems:

1. Transparency. Engineers tend to be people who want to see what goes on inside the box, or as the brits would say, under the bonnet. We like this because by knowing what's going on, we can fix issues, optimise it and make it work better. (This is also obviously why engineers love open source software) By bringing the technical discussions from a meeting room with a handful of people to a blog anyone in the organisation can read, engineers from every team can look at the process of "making our engineering better" transparently, and find ways to make it better.

2. Democratisation and crowdsourcing. This is an extension of Transparency. If we just make a blog for every engineer to see, but still let only a handful of people write posts, it's difficult to envisage engineers actively participating in the discussion, nor be fully bought-into the content. By making it possible for everyone to contribute, we can potentially get a lot more content, and also a lot more buy-in.

3. Apply engineering patterns to organisational problems *sometimes* works great. Specifically, using Github Pull Requests as a mechanism to moderate blog entries makes intuitive sense, and creates a convenient analogy to this peer review process. What other engineering solutions can we apply to organisational problems? [Continuous Delivery as a way to organise teams](https://t.co/rGOTKBu0S2)? 

