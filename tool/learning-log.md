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

11/24/24 (apologies for no screenshots, my computer has been acting up and wont allow me to drop pngs into the editor)

### weltmeister cont

i figured out how to properly preview the weltmeister on the ide without using replit, which is this command below that is put into the terminal

```console
php -S localhost:8000
```

after using this command, which works similarly to http-server by making a directory available on localhost:8000; ie good for opening static websites or in this case the weltmeister

### Entity

in order to make "sprites" or characters within your game, impact uses ig.entity to define the parameters and properties it will have. This can range from collison to the general size of the entity

directly sourced from documentation**

```js
// Create your own entity, subclassed from ig.Enitity
EntityPlayer = ig.Entity.extend({

    // Set some of the properties
    collides: ig.Entity.COLLIDES.ACTIVE,
    type: ig.Entity.TYPE.A,
    checkAgainst: ig.Entity.TYPE.B,

    size: {x: 16, y: 16},
    health: 50,

    // Load an animation sheet
    animSheet: new ig.AnimationSheet( 'media/player.png', 16, 16 ),

    init: function( x, y, settings ) {
        // Add animations for the animation sheet
        this.addAnim( 'idle', 0.1, [0,1,2] );
        this.addAnim( 'jump', 0.1, [3,4,5] );

        // Call the parent constructor
        this.parent( x, y, settings );
    }

    update: function() {
        // This method is called for every frame on each entity.
        // React to input, or compute the entity's AI here.

        if( ig.input.pressed('jump') ) {
            this.vel.y = -100;
            this.currentAnim = this.anims.jump.rewind();
        }

        // Call the parent update() method to move the entity
        // according to its physics
        this.parent();
    }
});
```
 the code above from their document page is the framework for defining an entity within your game, which monitors its size, collision, and calls a conditional for movement. in the pong game from the last learning log, the entitys were defined with this same framework for the pong and paddle. in order for the physics of the game to function, they must be defined first through ig.entity

 ### next objectives

 use ig.entity to define an entity for practice, and try making the entity move in weltmeister

### 12/8/24

### Entity cont

in the <code>entities</code> folder of impact, you can insert the files for your entities; js files; that will establish their animation values, PNG, scale, speed, etc.

a simple entity that gets moved around by colliding with other entities will look somewhat like this <code>puck.js folder</code>

```js
ig.module(
	'game.entities.puck'
)
.requires(
	'impact.entity'
)
.defines(function(){

EntityPuck = ig.Entity.extend({

	size: {x:48, y:48},
	collides: ig.Entity.COLLIDES.ACTIVE,

	animSheet: new ig.AnimationSheet( 'media/puck.png', 48, 48 ),

	bounciness: 1,

	init: function( x, y, settings ) {
		this.parent( x, y, settings );

		this.addAnim( 'idle', 0.1, [0,1,2,3,4,4,4,4,3,2,1] );

		this.vel.x = -200;
		this.vel.y = 100;
	}
});

});
```
this code below defines the size of the puck along with establishes its collides as active; this means any other entity it comes into contact with will make a collision. For the puck, this is vital code to make the pong game work properly
```js
size: {x:48, y:48},
	collides: ig.Entity.COLLIDES.ACTIVE,
```

this code below defines what frame the puck will change to based on its pngs animation; while its idle animation is 0.1, when it collides with another entity it will use the frames <code>[0,1,2,3,4,4,4,4,3,2,1]</code>
```js
this.addAnim( 'idle', 0.1, [0,1,2,3,4,4,4,4,3,2,1] );
```

### 3/2

#### kaboom sprite animations
```js
loadSprite("guy", "/images/gfx/character.png", {
                sliceX: 17,
                sliceY: 8,
```
the code above is what i used to load my sprite first things first, slicex and slice y cuts the source img you use for the sprite so later on when you animate it, the frames are defined by what number they are after they are sliced

```js
anims: {
                    "idle": 18,

                    "run": {
                        from: 18,
                        to: 19,
                        speed: 10,
                        loop: true,
                    },
                    "jump": 24,
                },
```

this code defines the animations of the sprite, from: and to: are used to define what frames will play when the action is executed; speed and loop maintain the framerate of your animation

after i added all the necessary code to iterate what these animations did and when they occured, my code would not run at all. Very confusing at first but what i realized was that i forgot a very important part that rendered everything useless. Body() was something i needed to add in this piece of code

```js
            const player = add([
                sprite("guy"),
                pos(center()),
                anchor("center"),
                area(),
                body(),
                scale(10, 10),
            ])
```

this basically makes sure the sprite follows the laws of gravity. and brings it back down when it jumps. In forgetting to add this, none of my code would work because gravity is literally a fundamental of the movements i was making my sprite do. 
<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
