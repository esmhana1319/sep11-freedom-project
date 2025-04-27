# Entry 5
##### 4/26/25

### Previous Buisness with kaboom + progress beyond

Previously, i faced struggles with my game not running due to specific errors with variables. The variable defining my level index was registered as undefined when i would preview. I found the reason for this was similar to the problem i had before and that it was a result of a parentheses being unclosed, causing my code to break. 

Now that the barebones of my game were finally working, i needed to the designs i had created. 

![spritesheet](https://github.com/user-attachments/assets/762e4a1a-e8d6-4916-8b62-85ba35be228a)
![thedoor](https://github.com/user-attachments/assets/97644051-3e07-445d-a1f5-94cdf2482feb)
![coffeeplant](https://github.com/user-attachments/assets/987a6b15-4969-479e-8704-498e963db4f4)

The ones shown here, were the most important to the games function, and the most faulty. The first issue i came across was with when inserting my sprites though was with my spritesheet. 

![sizelimitbreached](https://github.com/user-attachments/assets/ae4b7198-77d8-469b-b5db-ae4f1fec807d)

Kaboom has a texture limit of 2048x2048, and when this limit was breached my game broke. I quickly was able to find out which sprite was making things go awry by looking at the sizes of each of them. My sprite sheet was the only one (thankfully) that was measured in MBs. I quickly solved this by manually resizing it with piskel. 

My second challenge, aside from resizing everything to my liking (which i dont think counts as it was just tinkering with the scale that caused it to work again), was with my games 'key'. When the player collides with the coffee plant, theyll be able to reach the next level and the coffee plant will disapear. This function relies on "onCollide" to work, which decided to stop working once i replaced sprites and rearranged my level code. 

![collideerror](https://github.com/user-attachments/assets/2c6dc5e3-9595-4d28-a261-0cb60cc1319d)

![collideerrrror](https://github.com/user-attachments/assets/ec9546df-27e0-4a12-8883-6ae1d41b3126)

The only difference between this error though and my previous errors was that all of my code seemed to be working fine. My first option in troubleshooting was to ask peers if they experienced a similar problem, which they hadnt. Then i took the initiative to comment out specific parts of my code after making sure all parantheses were closed, functions matched kabooms source, and tags were properly called. The only way my code would work was when the collide functions were gone, which ultimately stripped my game of its purpose. My way to solve this was by ultimately starting over. I went back to my previous log, pasted that code in, and followed my previous steps. Essentially in combining my current code and my old code, i was able to take what worked and filter out what didnt from either save. 

After a couple final touches to the scales of sprites, and some tinkering with their locations, i finally reached my MVP :D







[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
