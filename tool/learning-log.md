-# Tool Learning Log

## Tool: **IMPACT.JS**

## Project: **interactive game**

---

### 10/18/24:

#### IMPACT INTRO

in order to get started on impact, i went to their webpage and downloaded the documents i needed to install it. The zip file when unzipped contains the github repo made by the developers that gives all the materials needed to learn impact, along with the license to use it. in order to do this i followed a quick intro tutorial by Aditya Mittal which i will link [here](https://youtu.be/Z6k0WPd2DOk?si=DhTFMP0TMnOGxTuL)

Aditya and the developers of impact describe it as a framework rather than a library. In other words i should think of it as the skeleton of my game that allows it to run. 

#### IMPACT TERMINOLOGY PT ONE

```js
ig.Entity 
```
every object within my game must be within the class <code> ig.entity </code>, this means that whatever "stuff" i add to the game should be a sub class of this 

```js
ig.system.run()
```
this is called by an interval of 60 times per second which is set by impact in order to smoothly run the game by calling two methods called by <code> .run() </code> which are <code> .update() </code> and <code> .draw() </code>. 
  
Now, knowing what impact is, its classes, and a couple of its methods my next objective is to try making a simple pong game using a tutorial i found on their website.  


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
