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


### 10/25/24

#### The weltmeister

the files within the impact js documentation are vast, which is initially very intimidating, but the first thing to do is break them down to understand what they are used for and why they are important. The most vital of them all is the weltmeister.

![Screenshot 2024-10-27 9 21 43 PM](https://github.com/user-attachments/assets/1d5a6e49-e7cb-4e49-8b74-6e949db37c48)

the weltmeister is a level editor used by impact js to preview the code and create levels with its designing abilities. Its shortcuts that i need to keep noted are listed below

1. hold right or ctrl to drag view

2. left mouse drags selected tile or entity depending on layer

3. space toggles the selection of the previous two

4. backspace or del will delete the selected entity (your sprite)

5. C clones the entity (good for mobs or enemy entities)

6. Z and Y are undo and redo buttons

7. G toggles the grid (this is for the background map of your game)

8. holding shift and left mouse button will enable you to select a part of the map to make your "brush" (by this they mean you can select a couple of tiles and draw them in another area in bulk)

#### weltmeister layers

weltmeister has different layers that can be used for the purpose of storing parts of your game there. The dimension of these layers along with their size can be changed, but not undone (something i need to keep in mind)

![Screenshot 2024-10-27 9 45 45 PM](https://github.com/user-attachments/assets/587458ab-9977-45f3-88e8-47d6d14a07a1)

In the screenshot above you can see the entities layer, which stores the sprites, and the add new layer button. I think the best way to view weltmeister is similar to the drawing apps i use to make art, or the mspaint website i use to doodle in class. With the weltmeister i am given a good view of how my game is previewed and a quicker way to layout my setting.

#### concerns

There are not much materials for learning i can go off of in comparison to kaboom, and most of the learning i must do is through looking at the website documents rather than peers or alumni, so i am slightly worried. Although a good resource i have is slack, asking for help on there is quite intimidating so ill just thug it out till i reach a sense of familiarity with what im working with. Luckily for me impact is proving to be quite fun, so im sure the project will be something i can look on later and be proud of.

### 11/11/24

#### making a game on impact

in order to make a game on impact, following the tutorial they setup on their website, i needed to add the files needed for the pong games visuals. They can be found [here](https://impactjs.com/download), and should be added to the media folder.

the [tutorial](https://www.youtube.com/watch?v=hMXWImAuim8&t=3s) i followed on their page gave some pretty important things to note. Within impact.js, in order to bind an input to a key, you need to use ig.input.bind( ig.KEY.(keygoeshere), "action name goes here"). When defining your "Entity" in the entity folder, you have to list their size, mark their collides as active or inactive. Once you finish defining all of your entities, you can finally use the weltmeister to create the stage for the game aswell as code the pong game.

The only concern i have at the moment is that many of the fundamentals used within the video are unrecognizable to what we have learned so far in javascript basics, aside from the function used to animate the puck entities movement. But there are many tutorials i can boot up that can help with that so ill just keep watching and tinkering till i can break down everything.



<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
