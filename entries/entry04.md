# Entry 4
##### X/X/XX

Recap: In this freedom project I have had multiple weeks to tinker and think about what tool I would like to use for it. I Had multiple options to pick from like Kaboom.js or Melon.js or even Impact.js. The tool I chose was Kaboom.js and I believe it was the right choice. My project was about a space platform game that had diffeent levels and you had to jump to go to the next level. So far I have learned how to make the levels and and add cool twists to each level. I only have a few weeks left before the mvp is due. With this in mind I now have to figure out how to make enemy ai for our levels which was quite a difficult task.

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

Even after all my effort into making this ai move, it still did not move. I was so confused as to why the ai wasnt moving when Im pretty sure the code worked. I went into a call with one of my partners to discuss this error that I had made in the code. We talked for a while and I was explaining what I did and asked him why it wasnt working 



[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
