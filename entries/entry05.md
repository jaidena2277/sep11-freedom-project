# Entry 5
##### X/X/XX

Recap: In this freedom project I have had multiple weeks to tinker and think about what tool I would like to use for it. I Had multiple options to pick from like Kaboom.js or Melon.js or even Impact.js. The tool I chose was [Kaboom.js](https://kaboomjs.com/) and I believe it was the right choice. My project was about a space platform game that had diffeent levels and you had to jump to go to the next level. So far I have learned how to make the levels, add difficulty to them, and make an ai that acts as the enemy. The goal for the weeks I had to work on this was to build an MVP(Most Viable Product) for my freedom project. All my partners and I have to do is add everything we have learned and compile it into a single game.

Challenge: To start this off the first challenge I had was not so much the levels but the problem the level caused. All i had to do was make three levels for the MVP, one would be easy the next is medium and the last is hard. The problem I had was the size of the blocks and enemy ai. The way I initially designed the levels was for there to be blocks you need to jump on top of in order to avoid touching the ai or spikes. 
``` js
   "         *   ",
		"  *         ",
		"                    ",
		"       $$    *   ",
		"     ===           ",
		"                    ",
		"   ^^  > = @  ",
		"============  ",
``` 
In this image I made a level where you spawn at the start and then you are forced to jump on the top of the four blocks at the start because there is spikes underneath te four blocks and if you somehow manage to get past the spikes there is an ai that is inescapable because I made the height low on purpose so you cant jump over it. The main problem for this level was the ai. I made the ai way to big and it was bigger than a block so if you got the timing wrong and tried to jump on the block while the ai was near it, the ai's hitbox would be too big and you would accidentally hit it. To fix this problem I cut down the ai to be the right height. It took a few tries because I wanted it to be the perfect height where it wasnt to big and not too small. 

```js
                "                *    *       $",
                "    *                        $",
                "                           $",
                "                       =    $",
                "                  =    =   $",
                "           $$     =    =    $",
                "       ====       ===    = $" ,
                "         *              =    $",
                "                      =       ",
                "       ^^     =      =  >       =",
                "===========================     =",
                "=  *          =                 =  ",
                "=             =  *              =",
                "=             =          =      =  ",
                "=             =          =      = ",
                "= @   >    =  =          =      =",
                "============    ================",
                "            $$$          *             ",
                "    *       ====                   ",
```
This was the next level I made and the new problem was the spikes AND the blocks. The spikes were now bigger than the blocks and I had to cut them into smaller portions to fix the annoyance of trying to jump on a block but dying due to the bigger size of the spike. The rest of the level was fine until you went down to floor 2. On floor two I added a gap to make the level have pzzaz. This part did not work due to the size of the blocks being too big. The character was unable to fit through the gap couldnt move on to the next level.

```js
" *               $              = = =            *    =",
        "             $  =    =           *  =                =",
        "         $   =       =             =                =",
        "         =         = =   =   =    =                 = ",
        "      =^^ ^^ ^^     f=   >        =    ^^^          =",
        "===============================================     =",
        "=                                                   =",
        "=                                                   =  ",
        "=                                                   =  ",
        "=    ^     >   >    >    >     >    >    >   >    > =    ",
        "=    ================================================     ",
        "=                                                   =",
        "=                                                   =",
        "=  $$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$=    ",
        "=  $$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$f=     ",
        "=====================================================      ",
        "",
        "",
        "",
        "",
        "",
        "",
        "",
        " @",
```
The last level was the best level I made. The first floor was a basic design with only spikes and blocks and a cool little trick I added but I will get into that later. The second floor however made the level live up to the difficulty of hard because I added 9 bots that all bump into each other making them unpredictable and giving the user a harder time with completing the floor. In addition the user could not just simply play the game enough to figure out a pattern in the bumps and try to time its jumps to kill them because the ai bumped each other periodically meaning they would bump each other at random. Once you are on the last floor its a piece of cake. I wanted to reward the user with a whole bunch of coins on their way to the portal to claim victory... Or so it seemed. As I mentoned before I added a little trick. When they reach the portal at the bottom they LOSE!!!. This is because I added a fake portal to the game. I took inspiration from my partner safes idea for adding a portal to the game to change levels. It was super easy to make, I just copied the code of our spike we had and changed the image of it into a portal and reclassed it.
```js
"f": () => [
			sprite("fake"),
			area(),
			body({ isStatic: true }),
			anchor("bot"),
			offscreen({ hide: true }),
			"danger",
```
Its funny because after someone dies to the one at the very start of the level they think to themselves " how funny but now I have to get past it and get to the real portal". Jokes on them, Beating the game was SUPER easy once they get to the third level. All they have to do is jump off the map on the left side and right before the limit where you die is the real portal.

Onto the next smaller challenge. This challenge was hard to hard to fix at first but really easy to fix once you see what the problem is. Kind of like when you blunder in a game of chess and realize your mistake. One of my partners had a problem with restarting the game and every time they tried to press a key to restart the game it would show an error pop up. This was really annoying because after he tried to look for 2 hours he told me to help him and I didnt understand how to fix it. But using the rubber ducky method without knowing it, Safe was telling me how every time he pressed a key it was supposed to restart. When he said that my brain started focusing and visualising what that actually meant and then it hit me. What if we changed the ```Function keypressed()``` to ```Function mousePressed``` because if you think about it. We are using keys to move so it would make sense for it to malfunction so if we just switch the function to mouse presssed it would be all good.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
