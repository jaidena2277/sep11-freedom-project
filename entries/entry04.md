# Entry 4
##### X/X/XX

Recap: In this freedom project I have had multiple weeks to tinker and think about what tool I would like to use for it. I Had multiple options to pick from like Kaboom.js or Melon.js or even Impact.js. The tool I chose was [Kaboom.js](https://kaboomjs.com/) and I believe it was the right choice. My project was about a space platform game that had diffeent levels and you had to jump to go to the next level. So far I have learned how to make the levels and and add cool twists to each level. I only have a few weeks left before the mvp is due. With this in mind I now have to figure out how to make enemy ai for our levels which was quite a difficult task.

Building this ai enemy took a lot out of me. I had alot of trouble understanding the syntax of how to make the ai move on its own and be able to bump into walls and turn around. As I started working on making the ai I realized that it would be smarter to make the body of the ai because I found out that you had to identify your sprite with any class. I identified the sprite as class "enemy", this gave me much more room to code because now I can use this "enemy" class to be called by the many other requirments that needed to be done in order to have an ai. To make the body of course there was more work to be done such as 
```
area(),
anchor("bot"),
body()
```
Even though I had to add these things to make the ai I understood that nothing was more important than adding the "enemy" class to it. I soon finished with the body of the ai and had to import a custom body to it to be able to see the ai. Of course it wasnt moving because I stopped working on the movement to make the body appear because without a body how would I know it works. Most likely console.log but I didnt think of that at the time. 

![image](https://user-images.githubusercontent.com/91745222/234890116-fb50d841-7062-4dde-9504-48a41a8b5f49.png)
This is what the body looks like which has no movement.



Now that the body is done I could move on to how to make the body move. This was probably the most difficult challenge I had. I set the speed to a nice smooth tempo where it wasnt too fast or too slow. I made a function that was going to have the speed in it so all I had to do was call the function every time i needed the speed to be used. I had trouble understanding the syntax and didnt know I needed requirements for the position and area. This is because it needs the current position and area of the sprite to know that it can move. The last part of doing the speed was adding the collisions so that when the ai hit a wall it would turn around and keep bouncing back and fourth repeatedly. This was easier as all I had to do was make it change direction every time the sprite hits the wall.  
```
function patrol(speed = 300, dir = 1) {
	return {
		id: "patrol",
		require: [ "pos", "area" ],
		add() {
			this.on("collide", (obj, col) => {
				if (col.isLeft() || col.isRight()) {
					dir = -dir
				}
			})
		},
		update() {
			this.move(speed * dir, 0)
		},
	}
}
```
I dont know how to add a video of the sprite moving back and fourth so I will show you the code of how I made the sprite bounce back and fourth.

Even after all my effort into making this ai move, it still did not move. I was so confused as to why the ai wasnt moving when Im pretty sure the code worked. I went into a call with one of my partners on [discord](https://discord.com/) to discuss this error that I had made in the code. We talked for a while and I was explaining what I did and asked him why it wasnt working, we couldnt come up with anything and as I was ranting about how sure I was of this working I realized that I didnt call the function. The entire 2 hours of looking at my code and wondering why it doesnt work was all for nothing. SO I added ``` patrol()``` to the code of the sprite so that it could move. It worked! Last objective I wanted to complete was  adding something where when you jump on the ai and it dies. It was actually pretty simple. I already had the sprite defined and most of the other syntax of the code is already defined through kaboom such as ``` .jump and destroy()```. I made it so when the player jumps on the ai the ai explodes and boosts the player off the ground by a tiny margin. This was made using the already defined code of the player and ai aswell as the code defined from kaboom.

In terms of EDP (Education Design Process) I am currently on stage 5 which is creating a prototype. We finished the planning of the MVP and started to create the prototype. The next step is to put all of this in action and test the prototype which would be getting the MVP ready to play. In terms of skills I would say I need to learn or am already learning four skils, collarboration, Communication, Attention to detail , and how to read. With Collaboration and communication I think I need to work more on working with my partners Safe and James and communicate to them more and share the things I learn to them and they should share the things they learn to me so we can grow together.







[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
