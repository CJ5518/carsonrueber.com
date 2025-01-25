---
layout: project
title: 3D Bomb Searcher
---

# 3D Bomb Searcher
![An image from the game](/images/3dBombSearcher/ingame.PNG ){: .projectMainImage}

## Features
The game features riveting minesweeper-like gameplay, but in three dimensions thus making it vastly more difficult.

The game was programmed in C++ and OpenGL, it uses SFML for window management.
The rendering engine is my own, called the CubeEngine, which only renders cubes. The UI is done with [Dear ImGUI](https://github.com/ocornut/imgui).

Graphical rendering performance is honsetly incredible, turns out when all you draw is instanced cubes you can get a pretty good framerate up. The main slowdowns in the game are caused by a very quickly and poorly written raycast algorithm to enable clicking on the cubes.

The game is incredibly difficult, not just because minesweeper is really hard in 3d but also because it is plain old hard to see what you're doing.
