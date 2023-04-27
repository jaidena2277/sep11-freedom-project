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

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
