#MVA pattern#Model View Actor, need of fault tolerance 

mva is mvvm extension where viewmodel becomes an actor with fault tolerance, routing, messenging, logger
What was basic need to reinvent mva?
Making mobile application uncrushable. Biggest problem is understanding what is exception and how it should handled. Idea of making apps un killable was taken from Akka.net in fact from scala/java. The actor systems and fault tolerance.
#What is actor?


https://doc.akka.io/docs/akka/2.5/fault-tolerance.html#supervision-of-top-level-actors

#What is mva actor?

In fact it view model but in fact with few additional things with are not part of mvvm patern. -There are few common states VM(mva Actor) should handle: Navigated, Blank/data loading, load failed, load failed with critical error, load basic data success but some still to come, app closed is possible to recover flow Forms Accors additonaly have: Post/Update validation error, 500 :) server failed, warnings.
Defining an understanding that such cases exists was main issue solver.

#How Communications between Actors is done?

via Routing - is navigation between Actors(VM) and passing data between

via Message- from, to, subject, message

#Summary

MVA is micro actor system where all actors are inside single one app. Fault tolerance, actor thinking can be introduced to any system this is show case of using it mobile app. No big mechanism are required one app so no need to build quaqes for massages. Things as "Supervision and Monitoring" are simply "SomeFlowService and Logger". FlowServices are simly groups of Actors (View models) used for example in wizards that is step by step, screen by screen operations.
