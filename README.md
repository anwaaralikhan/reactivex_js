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


#### How to use operators
* We need to do is import the operators we want to use. 

##### Import
```import { of } from 'rxjs';```

##### Typscript
```public items = of([1, 2, 3])```

##### Html
``` <ul> <li *ngFor="let item of items | async"> </li> </ul> ```


### Start to create a sample observable and subscribe it!
Before creating an observable, let’s recognize the essential concepts in RxJS:

> Observable: represents the idea of an invokable collection of future values or events.

> Observer: is a collection of callbacks that knows how to listen to values delivered by the Observable.

> Subscription: represents the execution of an Observable, is primarily useful for canceling the execution.

> Operators: are pure functions that enable a functional programming style of dealing with collections with operations like map, filter, flatMap, etc.

Let’s create a source observable by the operator of create, and internally produce new events. Then, subscribe the source Observable. (I used the previous version of Rx.js which imports all of the operators to let us get the autocompletion)

```
// create.js
import Rx from "rx";

const source = Rx.Observable.create(observer => {
  observer.onNext("yingray say hi!");
  observer.onNext("frank say hi!");
  observer.onCompleted();
});

const subscription = source.subscribe(
  value => console.log(`Next: ${value}`),
  error => console.log(`Error: ${error}`),
  () => console.log("Completed!")
);
```
