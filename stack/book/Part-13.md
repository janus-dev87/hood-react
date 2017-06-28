## Part 13

[![](https://rawgit.com/Bogdan-Lyashenko/Under-the-hood-ReactJS/master/stack/images/13/part-13.svg)](https://rawgit.com/Bogdan-Lyashenko/Under-the-hood-ReactJS/master/stack/images/13/part-13.svg)

<em>13.0 Part 13 (clickable)</em>

### Receive component (next element, to be more precise)

Well, through `ReactReconciler.receiveComponent` React actually calls `receiveComponent` from `ReactDOMComponent` and pass next element there. Reassign it on DOM component instance and call update method. `updateComponent` method actually performs two main actions: update DOM properties and DOM children, based on `prev` and `next` props. Good for us, we already analyzed `_updateDOMProperties` (`src\renderers\dom\shared\ReactDOMComponent.js#946`) method. As you remember, this method mostly process HTML elements properties and attributes, compute styles, handle event listeners etc. What is left, it’s `_updateDOMChildren` (`src\renderers\dom\shared\ReactDOMComponent.js#1076`).

### Alright, we’ve finished *Part 13*. That was a short one.)

Let’s recap what we get here. Look at the scheme one more time, then, let’s remove redundant less important pieces, so it becomes like that:

[![](https://rawgit.com/Bogdan-Lyashenko/Under-the-hood-ReactJS/master/stack/images/13/part-13-A.svg)](https://rawgit.com/Bogdan-Lyashenko/Under-the-hood-ReactJS/master/stack/images/13/part-13-A.svg)

<em>13.1 Part 13 simplified (clickable)</em>

And, probably, let’s fix spaces and alignment as well:

[![](https://rawgit.com/Bogdan-Lyashenko/Under-the-hood-ReactJS/master/stack/images/13/part-13-B.svg)](https://rawgit.com/Bogdan-Lyashenko/Under-the-hood-ReactJS/master/stack/images/13/part-13-B.svg)

<em>13.2 Part 13 simplified&refactored (clickable)</em>

Nice. In fact, that’s all that happens here. So, we can take essential value from the *Part 13*, it will be used for the final `updating` scheme:

[![](https://rawgit.com/Bogdan-Lyashenko/Under-the-hood-ReactJS/master/stack/images/13/part-13-C.svg)](https://rawgit.com/Bogdan-Lyashenko/Under-the-hood-ReactJS/master/stack/images/13/part-13-C.svg)

<em>13.3 Part 13 essential value (clickable)</em>

And then, we have done!


[To the next page: Part 14 >>](./Part-14.md)

[<< To the previous page: Part 12](./Part-13.md)


[Home](../../README.md)
