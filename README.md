LambdaDays 2015 report
=========
**Info and insight gathered during a single slice of LambdaDays 2015**


## Day 1

LambdaDays, the functional programming conference in Cracow, with 3 tracks and lots of interesting people.
It was in fact a more functional first day + reactive second day.

The conference was opened by keynote given by Garrett Smith from CloudBees. With some technical difficulties, the talk was streamed to the second hall due to overcrowding. Garrett talked about functional programming in general, giving some interesting patterns found in it. Overall, it was quite motivating start.

Then, I decided to begin with the research track. Professor Kevin Hammon gave there a very enthusiastic talk on megacore computing, being a philosophical upgrade over multicore and happening in the near future. Functional programming will make grasping it a reality, bringing unlimited parallelism and abscracting over the processing units executing it, whether CPU or GPU. Although actor model was skipped and unheard of completely, this was overall a pretty insightful talk, promoting the [Paraphrase](http://www.paraphrase-ict.eu) project.



Konrad 'ktoso' Malawski gave a very interesting talk about latency, speed and low level considerations when building high-performance systems. With details about many different concepts, it ephasized having interest and knowledge in internal implementations of the code being used. The bottom line was that although functional programming is great and should be used where possible, someone has to think of those mutable impure internals to make it a solid foundation for cleaner design. When using Scala, we can, and should, take a step down through the abstraction layers and use more imperative style in places when performance requires it. The slides, with impressive bibliography, can be found on [SlideShare](http://www.slideshare.net/ktoso/need-for-async-hot-pursuit-for-scalable-internetscale-applications).

Next presentation, by Adam Warski, was perhaps the most practical one. With high speed and precision, he implemented an Akka application conforming to Reactive Manifesto principles. Using streams, persistence and clustering, the app contained an actor with journaled storage that was location transparent and immune to some of the nodes going down. It was very insightful to see different modules of Akka smoothly interoperating. The project can be found on [GitHub] (https://github.com/adamw/reactive-akka-pres).

It wouldn't be functional conference without monads. Noel	Markham gave a very fast talk about abtracting over certain values when implementing a real-world application concerned with streaming tweets. It showed using monads like Reader, Writer, OptionT and the Monad monad itself. Then, he used ScalaCheck with some Shapeless contrib library to test the application, easly swapping the Futures for some more test-friendly monads.

I decided to end the day with even more monads, by Luc Duponcheel. He showed a simple dsl to rename the concepts of unit, bind, map2, and using applicative functors. 
