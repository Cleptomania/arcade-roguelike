# Setup

Before we can begin, we need to install Arcade. I'll walk through how to do that using a [virtual environment](https://docs.python.org/3/tutorial/venv.html), but if you have a preferred way to install python packages you can use that. If you're interested in using [PyCharm](https://www.jetbrains.com/pycharm/) which is a Python IDE, you can follow [this tutorial](https://api.arcade.academy/en/latest/install/windows.html#install-arcade-with-pycharm-and-a-virtual-environment) from the Arcade documentaiton to get it setup with a virtual environment with Arcade.

If you want to continue setting it up from the command line you can keep reading this chapter, if you prefer an alternative method of setup, you can skip ahead to the next chapter.

First create a folder for your project, I'll call mine `roguelike`. Then you can run the following command in it to create a virtual environment:

```bash
python -m venv .venv
```

Now that you've created a virtual environment, you can activate it with the following.

On Linux/Mac:

```bash
source .venv/bin/activate
```

On Windows(Powershell):

```powershell
.venv\Scripts\Activate.ps1
```

On Windows(CMD):

```cmd
.venv\Scripts\activate.bat
```

Now that our virtual environment is activated, go ahead and install Arcade with:

```bash
pip install arcade
```

That's all you need! Arcade is our only dependency for this game, so we're all set to go.

In the next chapter we'll begin putting down some boilerplate code to get our Arcade window up and running.