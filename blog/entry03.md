# Entry 3
##### 2/9/25

### Update on winter break goals/ Where ive been in learning my tool + game developing

In my last blog i discussed impact and my progress so far with it, but also the aspiration of learning to make movable sprites that properly work. My main goal for the break after was to successfully make a spirte that could work properly in the game im working to create, which sadly was not going well for me. Long story short, impact and I are NOT compatible, and if you are reading this blog as someone who is NOT mueller and are planning on using impact as your tool, please be prepared to put genuine effort into learning and breaking down its concepts. My main issue with impact i learned over the course of tinkering was that it had too many principles for me to keep track of, and aspects of it were fundamentals that cascaded over fundamentals. As someone who didnt have a lot of time to learn the program with dedication, its almost obvious that the program would be hard for me. Which is why i made the decision to switch tools a while back (really really late to do that; do better than me chat) 

#### Kaboom

  In a desperate attempt to rehabilitate my aspirations for my project i switched back to, my second choice for a tool, kaboom. Youll see that in my sources from below, and the sources from my previous blogs, that there is a stark difference in guides i could find for kaboom compared to impact. 

  The very first thing i did after switching tools wasnt installation (which looking back i shouldve gotten over with first as it was incredibly simple) but communicate with peers who were using the tool. I quickly learned a couple things from Astrid and Chris, two people in period 4 SEP who have made admirable progress with kaboom. 
(not to be a glazer or anything!!(i am totes glazing sorry not sorry) but they are amazing people and were really kind and taught me the main issues id have in advance with kaboom and where to start along with the two ways to install)
  One of the things i picked up from them was that if i were to make a sprite, animating its frames was something id have to remember to prevent errors, and that id need to define the keys needed for its movement properly to also avoid errors. 
  
  The way you establish a sprites animation frames is like this (look at my comments for breakdown) 
```js
	anims: {
		"idle": { //this is the name you define the animation with 
			from: 0, // starting of animation (selects the first frame of the sprites img to ) 
			to: 3, // ending of animation (the frames inbetween from and to values are selected for the ending animation) 
			speed: 5, // pace
			loop: true, // whether or not it should loop 
		},
		"run": {
			from: 4,
			to: 7,
			speed: 10,
			loop: true,
		},
		"jump": 8,
	},
})
```
in order for these animations to play youd need to establish the key functions (again thanking astrid and chris for telling me about this) which would look like this (look at my comments for my breakdown) 
```js
player.onGround(() => { // my inital thought was that this was like a function with an if else statement inside so i was very happy to feel familiar with it omg lets go
	if (!isKeyDown("left") && !isKeyDown("right")) { // if isKeyDown left and right are NOT true that activates the idle animation 
		player.play("idle") // i connected this to calling a function and the parameter we made before with the animations is here
	} else {
		player.play("run") // if the above was not true and left and right were being pressed it would play this animation 
	}
})

onKeyPress("space", () => {
	if (player.isGrounded()) { 
		player.jump(JUMP_FORCE) // jump force variable NEEDS to be defined for this to be recalled pls remember this essie 
		player.play("jump") // [plays jump animation when space is pressed 
	}
})

```

Alot of what i noticed when learning these sprite fundamentals was that althought kabooms language operated uniquely, it was still very similar to the javascript i had been learning outside of the freedom project. This motivated me extremely and i feel as though i regained the motivation to work even hard. 

#### Using what ive learned on my own

In order to demo this, i needed to get my own sprite to work with. Taking inspiration from Chris and Astrids reccomendations, i downloaded a sprite pack to tinker with before designing my own sprites (which is my next aspiration for future logs and blogs).  

![Screenshot 2025-02-09 8 12 18 PM](https://github.com/user-attachments/assets/2d7ad078-a8ce-4c2c-8500-5623c6cfd41b)

Of course, when i went to opengameart.org to browse their sprites, i just had to pick the zelda inspired one as a treat to get me started. Similar to when we demoed bootstrap i had to unzip the file and accessed all the materials i could use for tinkering. My main problem was that the sprite sheet i used would NOT properly slice, so thats something i need to look out for. Also another problem im currently having is that when i attempted applying these fundamentals to the sprite i am using to tinker my game will just not load? Again something im looking forward to fixing by my next blog. 

(before and after i commented the code)
![Screenshot 2025-02-09 8 52 18 PM](https://github.com/user-attachments/assets/13940f36-bc63-44ff-8c86-b105dfcfed74)
![Screenshot 2025-02-09 8 52 52 PM](https://github.com/user-attachments/assets/713f0060-16a4-4b8e-a3aa-3901d7482dd3)
![Screenshot 2025-02-09 8 53 47 PM](https://github.com/user-attachments/assets/5cdd1308-a7a8-46d8-b4c4-60f3aceab8c0)

### Sources

1. Chris and Astrid

2. The [replit youtube video](https://www.youtube.com/watch?v=hgReGsh5xVU) going over how to make a game in kaboom and [ourcade](https://www.youtube.com/watch?v=n-q0pKGhxyw) going over how to work a sprite in kaboom

3. the [kaboom website](https://kaboomjs.com/)

4. [OpenGameArt](https://opengameart.org/content/zelda-like-tilesets-and-sprites) the free source i used for temporary sprite sheets to tinker with

5. [Spriters Resource](https://www.spriters-resource.com/nes/legendofzelda/sheet/8366/) which i downloaded but didnt find appealing (good website though might use later)

### 

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
