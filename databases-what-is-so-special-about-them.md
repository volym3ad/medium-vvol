
# Databases : What is so special about them?



Learning databases for almost 3 years I still have no confidence in my knowledge… Moreover, I see that most SWEs and even Ops staff do not know how databases work. No matter is it relational or not engineers are trying to concentrate on software development itself leaving DB stuff at low priority.

And then team has 2 options: either to move all their DBs to 3rd party providers or hire DBRE. But hiring DBRE won’t solve all your problems as well as making someone care about store. Your team should know “what databases are made of” by creating solid knowledge sharing and defined rump up for newbies.

This article is aimed to emphasize on database importance and give you some main points when it comes to dealing with databases.

## **What should you start with?**

I think you should start with understanding SLOs of your project/company. What are availability, scalability, latency, durabilty, portability, throughput, safety in terms of database and what impact they have? How to monitor all those stuff? What is the difference between relational and non-relational models, normalized and denormalized data, cloud and on-premise stores? What Is MTTR, MTTF, and MTBF? etc.

The most important thing to realize is that everything is a trade-off. You can’t sharp one thing without sacrificing another. You must evaluate risks combined with each decision. I know it may sound weird but it’s true.

Observability and monitoring should be your best friends in learning databases. They should come in parallel with knowledge absorbing no matter how tough it could be. You’ll be grateful for this after all.

If you’re using/plan to use bare-metal data store be sure to get acquainted with OS and filesystem internals. Have you heard about RAID? -_-

## **Ok, what’s next?**

Next you need to discover what ACID, BASE and CAP theorem means. What forms of normalization exist? Maybe it’s time to learn SQL.

Find out how data is stored on disk after query is performed. How system parse query and decide where to store it? How can you influence on that? What could you do to bleed DB dry? Why should I care about quorum in distributed systems? It varies strongly from DBMS you’re working on. As it says, the sky is the limit :)

## **Phase II. Getting serious**

Look at indexes, MVCC, shared and exclusive locks, concurrency, conflict resolution and versioning.

Practice with backups, replication (single- and multi-leader, master-slave and master-master, read vs write replicas), sharding, automatic failover/DR. Learn about different system design/architecture patterns (database proxies, connection pools, async jobs etc).

And do not forget about testing. There is nothing worse than having untested backup. You ought to create special pipeline to validate data is ok before, during and after deployment (all the time I mean). It applies also to post-commit, schema, integration, acceptance, downstream, operational and load testing. Of course doing aforementioned things in automated way.

## **Finally, domain-specific knowledge**

Here I’ll nominate security, release management, reliability of your system. Are you sure data (in transition, on filesystem, at database level) is safe and encrypted? How many levels of security have you applied? Have you thought about possible SQL injections? What about utilization of resources? Can you see saturation? Can you scale out? (Remember about observability and monitoring. It’s continuous, repetitive and long-term task)

With all above you’re ready to become a database ninja.

**P.S.** I was inspired by great book “Database Reliability Engineering” written by Laine Campbell & Charity Majors. Also do not hesitate to leave comments, advices, criticism. I’m still learning and plan to sharp my skills)
