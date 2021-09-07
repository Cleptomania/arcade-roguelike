# 01 - Creating a Window

This part assumes that you have gone through [Setup](./setup.md), and are setup and ready to go. Assuming that's the case, we'll get started with creating our game window using Arcade. We'll just create a blank window and set it's background color for this chapter.

This part is mostly straight-forward. First we'll import arcade and setup some constant values.

```Python
import arcade

# Constants
SCREEN_WIDTH = 800
SCREEN_HEIGHT = 600
SCREEN_TITLE = "Roguelike"
```

Next we'll setup a class for our game. This will serve as the main class our game uses. In order to do this, we will subclass the `arcade.Window` class provided from Arcade. We'll name the class `Roguelike`

```Python
class Roguelike(arcade.Window):
    def __init__(self):

        # Call the parent class and set up the window
        super().__init__(SCREEN_WIDTH, SCREEN_HEIGHT, SCREEN_TITLE)

        arcade.set_background_color(arcade.csscolor.CORNFLOWER_BLUE)

    def on_draw(self):
        """Render the screen."""

        arcade.start_render()
        # Code to draw the screen goes here
```

For now we've just got two functions, the `__init__` function which also calls the `__init__` from our parent `arcade.Window` class, and then `on_draw` function. Arcade automatically catches this function, and calls it during it's loop to draw the screen every frame. Additionally, in order for anything in this function to actually output to the screen, we need to call `arcade.start_render()`.

At this point we're not putting anything else in the `on_draw` function, but eventually we'll have some more things in there to draw everything in the game. The background color that we set in the `__init__` function will automatically be used when we call `arcade.start_render()`.

Lastly we just need some startup code to make this actually runnable:

```Python
def main():
    window = Roguelike()
    arcade.run()

if __name__ == "__main__":
    main()
```

If we put everything together, this is our final code for this chapter:

```Python
{!../docs_src/window/final.py!}
```
