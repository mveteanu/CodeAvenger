p5.js SceneManager (Manage multiple scenes in p5.js sketches)
=============================================================

I discovered the [p5.js](http://p5js.org/) library a few month ago when I start teaching programming to a small group of people at my organization. Doing a little bit of research I saw that p5.js is not only used in academic situations ... but a few people are creating games using this fun and easy to use library. 
One of the common tasks in game development is splitting the game is several scenes. Perhaps your game can have:

-	GameIntro
-	Game
-	GameOver
-	HighScores

The challenges in doing this split with p5.js is that you have only one main “game loop”: the draw() function. Since creation of additional good game loops is not quite trivial, the best solution is to take advantage of the single draw() function as main game loop but redirect the action to the appropriate scene.

To ease this kind of task, I created a mini p5.js library called p5.SceneManager. With this library the task of scene management becomes trivial and your code sits nicely organized. Each scene is a like a sketch within the main sketch. You focus on creating the scene like a regular sketch and SceneManager ensure scene switching routing the main setup(), draw(), mousePressed(), etc. events to the  appropriate current scene.

Instead of putting all your code in the main setup() and draw() like this:

```JavaScript
function setup() {

}

function draw() {

}
```

... you put each scene code in the setup() and draw() methods of individual Scene classes:

```JavaScript
function Intro()
{
    this.setup = function() {
    }

    this.draw = function() {
    }

    this.keyPressed = function() {
        this.sceneManager.showScene( Game );
    }
}

function Game()
{
    this.setup = function() {
    }

    this.draw = function() {
    }
}
```

The SceneManager will provide you with methods necessary to switch to the appropriate scene and route the main p5.js events to your defined events.

Source Code
-----------

You can get the source code for free from GitHub at [https://github.com/mveteanu/p5.SceneManager](https://github.com/mveteanu/p5.SceneManager) 
Note: The library is still work in progress. Please feel free to extend it as necessary.

Online demo
-----------

<iframe style="width:100%; height:540px; border:0" frameborder="0" scrolling="no" src="http://www.vmasoft.net/p5/game.html">http://www.vmasoft.net/p5/game.html</iframe>

You can try a few more samples created with p5.SceneManager at [http://www.vmasoft.net/p5/](http://www.vmasoft.net/p5/) 
