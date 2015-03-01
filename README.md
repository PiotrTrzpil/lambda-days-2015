LambdaDays 2015 report
=========
**Info and insight gathered during a single slice of LambdaDays 2015**

[LambdaDays](http://www.lambdadays.org) just wrapped up, the 2-day functional programming conference in Cracow, with [4 tracks](http://www.lambdadays.org/#programme) and lots of interesting people.
The most popular languages among speakers and probably also audience were Scala, F# and Erlang. There was also some minority consisting of Haskell, JavaScript, Clojure, Ocaml, Idris and Elm here and there.

Here is a report from the front. 

## Day 1

The conference was opened by **keynote** given by Garrett Smith from CloudBees. The talk was streamed to the second hall due to overcrowding (with some difficulties). Garrett talked about functional programming in general, giving some interesting patterns found in it.

Then, I decided to begin with the research track. Professor Kevin Hammon gave there a very enthusiastic talk on **megacore computing**, being a philosophical upgrade over multicore and happening in the near future. Functional programming will make grasping it a reality, bringing unlimited parallelism and abstracting over the processing units executing it, whether CPU or GPU. Although actor model as a solution was unheard of completely, this was overall a pretty insightful talk, centered around concepts of [Paraphrase](http://www.paraphrase-ict.eu) project.

Torben Hoffmann of Erlang Solutions then gave a very engaging talk on **Erlang process model**, showing concepts not unfamiliar to Akka users. Processes, just like actors, are very lightweight and should be created for every task needed. Torben also  talked about processes being restarted independently by supervisor as part of general approach to system resiliency.

Then next talk I attended was a very research-oriented one by Evelina Gabasova. It was a quite interesting talk about
**cancer research** and R pains followed by F# joy. She showed some code examples of doing functional transformations on sets of data downloaded from online cancer research database and looking for correlations in it.

Lars Hupel then gave a talk in Haskell on **functional approach to mocking**. It was quite heavy and I think I will need to watch this one again...

The next presentation given by Andrea Magnorsky was on games and using **functional programming (F#) in the game development**. Although quite interesting, the language was used only in about 10% of the code base, where the performance was not a problem.

The last talk I attended on that day was by Jacek Głodek about practical problems and **misuse of typing and functional programming** when writing typical applications. It ephasized readability and proper expression of domain model or business logic. My quite rich take-away from it was: be wary of tuples, create more case classes, use helper monads like _Option_ only in places where it expresses the intent well.

Now off for the after-party with free beer and pizza.

## Day 2

The day was opened by a **keynote** given Kinga Panasiewicz and gave everyone much positive energy for the start of the day. The topic was centered around the statement that **watching computer screen for a longer time is malicious for the brain** and can be one of the causes of developing brain diseases like schizophrenia. Quite brave of a statement on a programming conference, I think. The latter part of the talk was centered on brain memory (and negative impact of Google Search on it) and Kinga was engaging with the audience in some memory games.

Then, there was a talk on Big Data by Nilanjan Raychaudhuri, showing some general architecture and approach to **building data processing piplines**, a bit centered on Spark.

The next presentation, by André van Delft, was concerned with **algebras describing reactive systems** and in particular one called _Algebra of Communicating Processes_. However, as I was absent on part of it, I cannot say more.

Just before lunch there was a **second keynote**, by Rúnar Bjarnason, telling the tale of joys of functional programming. It was a very interesting talk on the essence of functional thinking, with lots of examples in Scala, although rather introductory. Someone asked: why use Scala and not some pure functional language. May be a matter of taste, but next presentation by Konrad answers the question some more. 

Konrad 'ktoso' Malawski gave a very interesting talk about latency, speed and low level considerations when building **high-performance systems**. With details about many different concepts, it ephasized having interest and knowledge in internal implementations of the code being used. The bottom line was that although functional programming is great and should be used where possible, someone has to think of those mutable impure internals to make it a solid foundation for cleaner design. When using Scala, we can, and should, take a step down through the abstraction layers and use more imperative style in places when performance requires it. The slides, with impressive bibliography, can be found on [SlideShare](http://www.slideshare.net/ktoso/need-for-async-hot-pursuit-for-scalable-internetscale-applications).

Next presentation, by Adam Warski, was perhaps the most practical one. With high speed and precision, he implemented an **Akka application conforming to Reactive Manifesto principles**. Using streams, persistence and clustering, the app contained an actor with journaled storage that was location transparent and immune to some of the nodes going down. It was very insightful to see different modules of Akka smoothly interoperating. The project can be found on [GitHub] (https://github.com/adamw/reactive-akka-pres).

It wouldn't be functional conference without monads. Noel	Markham gave a very fast talk about **abtracting over certain values** when implementing a real-world application concerned with streaming tweets. It showed using monads like _Reader_, _Writer_, _OptionT_ and the _Monad_ monad itself. Then, he used ScalaCheck with some Shapeless contrib library to test the application, easly swapping the Futures for some more test-friendly monads.

I decided to end the day with **even more monads**, by Luc Duponcheel. He showed a simple dsl to rename the concepts of unit, bind, map2, and using applicative functors. 

---------------

Overall, the conference was a very nice experience with great speakers and organization. It was often very hard to choose a track because of many interesting, conflicting topics. Luckily, all of the talks were recorded.
Also, what I missed was polyglot, language oriented topics -- generally, each presentation floated around a single language. I would be great to have a comparison of some functional patterns or features in different languages. 
Anyway, see you next time! 

[This report](https://github.com/PiotrTrzpil/lambda-days-2015) on GitHub
