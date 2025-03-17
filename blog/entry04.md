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





[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
