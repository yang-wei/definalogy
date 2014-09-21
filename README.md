#Definalogy

Albert Einstein
> If you can't explain it *simply*, you dont't understand it well enough.

A collection of non-wiki style in defining vocabulary related to computer programming languages. These definition are from sources like [stackoverflow](stackoverflow.com) where brilliat people contributing. This list aims to help people to
 * understand concepts first before they head to documentation or Wikipedia
 * explain thing in ~~wiki~~ analogy/metaphor styles to customers, students, family members etc

Short, simple, cool enough.
##Table of Contents
 - [Closure](#closure)
 - [Encapsulation](#encapsulation)
 - [Framework](#framework)
 - [Object](#object)
 - [Recursion](#recursion)
 - [Rest](#rest)
 - [Variable](#variable)


<a name="closure"/>
###Closure
Both explaination are in Javascript
####First Explaination
There was a princess...
```
function princess() {
```
She lived in a wonderful world full of adventures. She met her Prince Charming, rode around her world on a unicorn, battled dragons, encountered talking animals, and many other fantastical things.
```
    var adventures = [];

    function princeCharming() { /* ... */ }

    var unicorn = { /* ... */ },
        dragons = [ /* ... */ ],
        squirrel = "Hello!";
```
But she would always have to return back to her dull world of chores and grown-ups.

```
    return {
```
And she would often tell them of her latest amazing adventure as a princess.
```
        story: function() {
            return adventures[adventures.length - 1];
        }
    };
}
```
But all they would see is a little girl...
```
var littleGirl = princess();
```
...telling stories about magic and fantasy.
```
littleGirl.story();
```
And even though the grown-ups knew of real princesses, they would never believe in the unicorns or dragons because they could never see them. The grown-ups said that they only existed inside the little girl's imagination.

But we know the real truth; that the little girl with the princess inside...

...is really a princess with a little girl inside.

_by [Jacob Swartwood][closure_ref1]_

####Explaination 2
The kitchen is a closure that has a local variable, called trashBags. There is a function inside the kitchen called getTrashBag that gets one trash bag and returns it.

We can code this in JavaScript like this:
```
function makeKitchen () {
  var trashBags = ['A', 'B', 'C']; // only 3 at first

  return {
    getTrashBag: function() {
      return trashBags.pop();
    }
  };
}

var kitchen = makeKitchen();

kitchen.getTrashBag(); // returns trash bag C
kitchen.getTrashBag(); // returns trash bag B
kitchen.getTrashBag(); // returns trash bag A
```
_by [dlaliberte][closure_ref2]_

**[⬆ back to top](#table-of-contents)**
###Encapsulation
#####The Beauty of Encapsulation
Now, in my opinion, to really understand encapsulation, one must first understand abstraction.

Think, for example, in the level of abstraction in the concept of a car. A car is complex in its internal implementation. They have several subsystem, like a transmission system, a break system, a fuel system, etc.

However, we have simplified its abstraction, and we interact with all cars in the world through the public interface of their abstraction. We know that all cars have a steering wheel through which we control direction, they have a pedal that when you press it you accelerate the car and control speed, and another one that when you press it you make it stop, and you have a gear stick that let you control if you go forward or backwards. These features constitute the public interface of the car abstraction. In the morning you can drive a sedan and then get out of it and drive an SUV in the afternoon as if it was the same thing.

However, few of us know the details of how all these features are implemented under the hood. Think of the time when cars did not have a hydraulics directional system. One day, the car manufactures invented it, and they decide it to put it in cars from there on. Still, this did not change the way in which users where interacting with them. At most, users experienced an improvement in the use of the directional system. A change like this was possible because the internal implementation of a car is encapsulated. Changes can be safely done without affecting its public interface.

Now, think that car manufactures decided to put the fuel cap below the car, and not in one of its sides. You go and buy one of these new cars, and when you run out of gas you go to the gas station, and you do not find the fuel cap. Suddenly you realize is below the car, but you cannot reach it with the gas pump hose. Now, we have broken the public interface contract, and therefore, the entire world breaks, it falls apart because things are not working the way it was expected. A change like this would cost millions. We would need to change all gas pumps in the world. When we break encapsulation we have to pay a price.

So, as you can see, the goal of encapsulation is to minimize interdependence and facilitate change. You maximize encapsulation by minimizing the exposure of implementation details. The state of a class should only be accessed through its public interface.

_by [Edwin Dalorzo][encapsulation_ref]_
**[⬆ back to top](#table-of-contents)**

###Framework
If I say you to cut a paper of dimension 5m by 5m then surely you would do that. But then I ask you to cut 1000 paper of the same dimension. Then you won't do the measuring for 1000 times, obviously you would make a frame of 5m by 5m and then with the help of it you would be able to cut 1000 papers in less time. So, what you did is you made a framewok which would do that type of task. So, instead of performing same type of task again and again for same type of applications, what you do is you create a framework having all those facilities together in one nice packet and hence providing the abstraction for your application and more importantly many applications.

_by [Neha Choudhary][framework_ref]_


###Object
I like the original metaphor used by Alan Kay, who coined "object-oriented programming": Objects are like cells in a body. They are each programmed with their own behaviors and communicate by passing messages to one another, which they again respond to with their own internally defined behavior. No one cell knows what's inside another — they just know how to handle their own tasks and communicate with each other.

_by [Chuck][object_ref]_


###Recursion
>A _**child**_ couldn't sleep, so her mother told her a story about _**a little frog**_,<br>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;who couldn't sleep, so the frog's mother told her a story about _**a little bear**_,<br>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;who couldn't sleep, so the bear's mother told her a story about _**a little weasel**_...<br>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;who fell asleep.<br>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;...and the _**little bear**_ fell asleep<br>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;...and the _**little frog**_ fell asleep;<br>
>...and the _**child**_ fell asleep.

_by [A CS Professor][recursion_ref]_


###REST
This blog post is a bit long, so I decided to point this to the original blog post. To understand RESTFUL service in interesting way, please read [How I Explained REST to My Wife][rest_ref]

_by Ryan Tomayko_
**[⬆ back to top](#table-of-contents)**

###Variable

![Eloquent Javascript][eloquentjavascript]
You should imagine variables as tentacles, rather than boxes. They do not contain values; they grasp them—two variables can refer to the same value. A program can only access the values that it still has a hold on. When you need to remember something, you grow a tentacle to hold on to it or you reattach one of your existing tentacles to it.

_by [Marijin Haverbeke][variable_ref]
**[⬆ back to top](#table-of-contents)**

[wikipedia]:http://en.wikipedia.org/wiki/JavaScript
[closure_ref1]:http://stackoverflow.com/questions/111102/how-do-javascript-closures-work/6472397#6472397
[closure_ref2]:http://stackoverflow.com/a/7285658/2844763
[encapsulation_ref]:http://stackoverflow.com/a/11970468/2844763
[framework_ref]:http://stackoverflow.com/a/12733126/2844763
[object_ref]:http://stackoverflow.com/a/995204/2844763
[recursion_ref]:http://everything2.com/user/wharfinger/writeups/recursion
[rest_ref]:http://www.looah.com/source/view/2284
[eloquentjavascript]:http://eloquentjavascript.net/2nd_edition/preview/img/octopus.jpg
[variable_ref]:http://eloquentjavascript.net/2nd_edition/preview/02_program_structure.html
