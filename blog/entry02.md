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

###


[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
