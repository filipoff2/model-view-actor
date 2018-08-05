# model-view-actor (mva)
mva is mvvm extention where viewmodel becomes an actor with fault tolerance, routing, messenging, logger 
# What was basic need to reinvent mva?
Making mobile application uncrashable. Biggest problem is undenrstanding what is excpetion and how it should handled.
Idea of making apps unkillable was taken from Akka.net in fact from scala/java. The actor systems and fault tolerance.
# What is actor?
https://doc.akka.io/docs/akka/2.5/fault-tolerance.html#supervision-of-top-level-actors
# What is mva actor?
In fact it view model but in fact with few addional things with are not part of mvvm patern.
-There are few common states VM(mva Actor) should handle:
Navigated, Blank/data loading, load failed, load failed with critical error, load basic data success but some still to come,
app closed is possible to recover flow
Forms Accors additonaly have: Post/Update validation error, 500 :) server failed, warnings ,.
Defining an understanding that such cases exists was main issue solver.
# How Comunications between Actors is done?
- via Routing - is navigation between Actors(VM) and passing data beteen  
- via Messager - from, to, subject, message  

# Summary
MVA is micro actor system where all actors are inside single app. 
Fault tolerance, actor thinkig can be intoduced to any system this is show case of using it mobile app. 
