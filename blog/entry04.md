# Entry 4
##### 3/16/25

### Kaboom: progress from the previous blog

In the last entry, i attempted making my own moving sprite with set animations to demo how my games character would move. I struggled before with getting things to run properly, though, and id keep recieving the same error "onGround is not a function". After comparing my code with the reference on Kabooms website, i was able to deduce that i was missing a couple lines of code that mightve contributed to the error i was facing. Shortly, after a couple process of eliminations and switcharoos here and there, i found that not defining <code> body() </code> of my sprite was causing everything to break. 

![Screenshot 2025-03-02 5 24 34 PM](https://github.com/user-attachments/assets/91a5c286-02a1-4d3c-9845-fe4f2be041d0); 

Now, after successfully solving my previous issue, my next objective was to set the scene for different levels in an rpg format. 

### Kaboom: new progress 

My next line of action, as memtioned in my plan.md, was to learn how to make levels in an rpg format. 

![Screenshot 2025-03-16 8 33 09 PM](https://github.com/user-attachments/assets/f47cdcb6-b680-4d3f-a4b7-c8f4082727f3)

here in these lines of code i define all of my sprites, including the guy i coded before. These will serve to define what will later make the scenery for my levels. 

![Screenshot 2025-03-16 8 33 21 PM](https://github.com/user-attachments/assets/3c847ec1-4927-45a5-ba6b-9c828f552e98)

these lines of code above are what kaboom uses to layout the map for rpg levels, which i found like a text version of the weltmeister from impact (traumatic :0 ). But my current issue also aligns with this specific part in this step, which i will go over later on. 

![Screenshot 2025-03-16 8 33 37 PM](https://github.com/user-attachments/assets/0110e2a6-3f86-42df-8650-32b71c1e85e7)

These lines of code are what kaboom uses to define the layout and connect back to the previously loaded sprites from before. 

### current issue, and stuff to work on for the future 

My current issue with this is that the code i have now wont run due to LevelIdx being undefined, and when i comment out this code and rearrange things it runs just fine. I remembered Astrid dealing with this error previously, but we never found the specific solution as of now. My next objective is to properly define LevelIdx and afterwards implement my own designed sprites into my code. 

### Sources

1. Astrid

2. the [kaboom website](https://kaboomjs.com/)

3. [OpenGameArt](https://opengameart.org/content/zelda-like-tilesets-and-sprites) 

4. [Spriters Resource](https://www.spriters-resource.com/nes/legendofzelda/sheet/8366/)
   
5. open game arts [key sprite](https://opengameart.org/content/key-sprite), which saved me in a hurry while i was looking for one with a transparent background

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

   Currently, i am beginning step 6. I have created a prototype and am now currently testing and evaluating it for errors and bugs

### Skills

A skill i developed was making connections, i recognized that i was dealing with an error one of my peers mentioned before and treated it in a similar manner to which they did

```
developed skill *-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
 making connections lvl 7
-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-
```

Another skill i developed from my previous blogs is looking at different sources to familiarize myself. Kabooms way of creating levels is similar to that of impact where the sprites are defined and later used to build the terrain tile by tile, and i found that it helped a lot with staring at the block of text which didnt make sense initially on my first look 

```
developed skill *-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
looking at and making comparisons with different sources lvl 5
-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-
```





[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
