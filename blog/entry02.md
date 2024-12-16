# Entry 2
##### 12/15/24 

### What ive been up to: Impact and further brainstorming 

Learning my tool, impact, so far has been interesting. ive found that learning impact with their website is fine, but i really wish there were more sources to go off of, incase my code comes out wrong. The first thing i did after installing impact.js was familiarizing myself with their files and general outputs; ie what each one did and what they were meant for, along with starting to learn how to make entities. 

I found that the best way to learn was by referencing actual games created by impact, in specific their pong game; the most simple, to view a frame i needed to work towards from the beginning. 

Heres a snippet from my learning log regarding the pong game and entiities. 

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

in analyzing how the code worked i was better able to understand what elements i needed to make an enitity, along with what it would look like within impacts "lingo", and although i am not yet fluent in it i feel i better understand slightly 

### Sources 

- My [learning log](../tool/learning-log.md) is linked here 

- [Impact](https://impactjs.com/) my tool, is linked here; specifically i navigated the entity docs on their website 

### Engineering Design Process 

The process of Engineering and Design consist of eight steps 

#### 1. Define the problem [x]
   
#### 2.Research the problem [x]

#### 3.Brainstorm possible solutions [x]

#### 4.Plan the most promising solution [x]

#### 5.Create a prototype []

#### 6.Test and evaluate the prototype [ ] 

#### 7.Improve as needed [ ]

#### 8.Communicate the results [ ]

   Currently, i am just beginning step 5. I have brainstormed and planned the idea i want to create and have done further research to expand on my knowledge on Impact, the tool i am using. Knowing what i know, i can start creating prototypes with impact and move closer to creating my vision for my sep freedom project 

### Skills

A skill i developed was using comments to break down code. I had trouble understanding how to start with impact, so i began looking at my goal code; in this case pong; and breaking down what code does what, along with what it needs to work 

```
developed skill *-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
  using comments  to break down code lvl 9 
-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-
```

Another skill i developed from my previous blog was research and learning on my own, impact didnt have a lot of resources to go off of but i analyzed and tested their code along with looking at their website for more information regarding why each component is important 

```
developed skill *-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
  researching and learning on my own lvl 8
-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-
```



[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
