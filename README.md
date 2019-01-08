# reactivex_js

Idea : An API for asynchronous programming with observable streams

`You will write some code which will wait for something to Happen, In Javascript we wait for user events to click, submit forms etc`
`Activities which will happen in the Future!`

Existing solutions & problems :

* How to handle the async event is a big issue. You may come up with Promise function, Async function, etc. 
* Sometimes you need to control a series of tasks with the async event and it’s always hard to deal with. 

Problems : 

* For example, there is no method for stopping the promise when it’s executing. It still has some solutions to work around, but it makes code hard reading and maintaining.

How ReactiveX Solves:
ReactiveX provides a good pattern to control the async event. 
It combines the Observer pattern with the Iterator pattern and functional programming with collections. So that it makes sequences of events like an array and uses the operators like the Lodash. 


#### Rx vs RxJs
> In short, “rxjs” is rewrite of “rx” and is the latest production-ready version of RxJS.
> It have better performance, better modularity, better debuggable call stacks while staying mostly backward compatible.
