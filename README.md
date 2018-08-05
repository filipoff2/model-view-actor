# model-view-actor (mva)
mva is mvvm extention where viewmodel becomes an actor with fault tolerance.
# What was basic need to reinvernt mva?
Making mobile application uncrashable. Biggest problem is undenrstanding what is excpetion and how it should handled.
Idea of making apps unkillable was taken from Akka.net in fact from scala/java. The actor systems and fault tolerance.
# What is actor?
https://doc.akka.io/docs/akka/2.5/fault-tolerance.html#supervision-of-top-level-actors
# What is mva actor?
In fact it view model but in fact with few addional things with are not part of mvvm patern.
-There are few common states VM(mva Actor) should handle:
Navigated, Blank/data loading, load failed, load failed with critical error, load basic data success but some still to come.
Forms: Post/Update validation error, 500 :) server failed, warnings , app closed is possible to recover flow.
Defining an understanding that such cases exists was main issue solver.
# How Comunications between Actors is done?
- via Routing - is navigation between Actors(VM) and passing data beteen them 
- via messages  

