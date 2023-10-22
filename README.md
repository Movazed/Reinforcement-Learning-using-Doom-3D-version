# Reinforcement-Learning-using-Doom-3D-version
Q-Learning is a reinforcement learning procedure which attempts to learn the value of being in a given state. It tells us the utility of each state in the environment and also decides on the action that an AI agent shall take to maximize final reward by moving to a state with higher utility.



ViZDoom allows developing AI bots that play Doom using only visual information (the screen buffer). It is primarily intended for research in machine visual learning, and deep reinforcement learning, in particular.

ViZDoom is based on ZDoom to provide the game mechanics.

ViZDoom Demo

Features
Multi-platform (Linux, macOS, Windows),
API for Python and C++,
Gymnasium/OpenAI Gym environment wrappers (thanks to Arjun KG Benjamin Noah Beal, Lawrence Francis, and Mark Towers),
Easy-to-create custom scenarios (visual editors, scripting language, and examples available),
Async and sync single-player and multiplayer modes,
Fast (up to 7000 fps in sync mode, single-threaded),
Lightweight (few MBs),
Customizable resolution and rendering parameters,
Access to the depth buffer (3D vision),
Automatic labeling of game objects visible in the frame,
Access to the audio buffer (thanks to Shashank Hegde),
Access to the list of actors/objects and map geometry,
Off-screen rendering,
Episodes recording,
In-game time scaling in async mode.
ViZDoom API is reinforcement learning friendly (suitable also for learning from demonstration, apprenticeship learning or apprenticeship via inverse reinforcement learning, etc.).

Julia (thanks to Jun Tian), Lua, and Java bindings are available in other branches but are no longer maintained.

Cite as
M Wydmuch, M Kempka & W Jaśkowski, ViZDoom Competitions: Playing Doom from Pixels, IEEE Transactions on Games, vol. 11, no. 3, pp. 248-259, 2019 (arXiv:1809.03470)

@article{Wydmuch2019ViZdoom,
  author  = {Marek Wydmuch and Micha{\l} Kempka and Wojciech Ja\'skowski},
  title   = {{ViZDoom} {C}ompetitions: {P}laying {D}oom from {P}ixels},
  journal = {IEEE Transactions on Games},
  year    = {2019},
  volume  = {11},
  number  = {3},
  pages   = {248--259},
  doi     = {10.1109/TG.2018.2877047},
  note    = {The 2022 IEEE Transactions on Games Outstanding Paper Award}
}
or

M. Kempka, M. Wydmuch, G. Runc, J. Toczek & W. Jaśkowski, ViZDoom: A Doom-based AI Research Platform for Visual Reinforcement Learning, IEEE Conference on Computational Intelligence and Games, pp. 341-348, Santorini, Greece, 2016 (arXiv:1605.02097)

@inproceedings{Kempka2016ViZDoom,
  author    = {Micha{\l} Kempka and Marek Wydmuch and Grzegorz Runc and Jakub Toczek and Wojciech Ja\'skowski},
  title     = {{ViZDoom}: A {D}oom-based {AI} Research Platform for Visual Reinforcement Learning},
  booktitle = {IEEE Conference on Computational Intelligence and Games},
  year      = {2016},
  address   = {Santorini, Greece},
  month     = {Sep},
  pages     = {341--348},
  publisher = {IEEE},
  doi       = {10.1109/CIG.2016.7860433},
  note      = {The Best Paper Award}
}
Python quick start
Linux
To install the latest release of ViZDoom, just run:

pip install vizdoom
Both x86-64 and AArch64 (ARM64) architectures are supported. Wheels are available for Python 3.8+ on Linux.

If Python wheel is not available for your platform (Python version <3.8, distros below manylinux_2_28 standard), pip will try to install (build) ViZDoom from the source. ViZDoom requires a C++11 compiler, CMake 3.12+, Boost 1.54+ SDL2, OpenAL (optional), and Python 3.7+ to install from source. See documentation for more details.

macOS
To install the latest release of ViZDoom, just run (it may take a few minutes as it will build ViZDoom from source on M1/M2 chips):

brew install cmake boost sdl2 openal-soft
pip install vizdoom
Both Intel and Apple Silicon CPUs are supported. We recommend using at least macOS High Sierra 10.13+ with Python 3.7+. On Apple Silicon (M1 and M2), make sure you are using Python/Pip for Apple Silicon.

Windows
To install the latest release of ViZDoom, just run:

pip install vizdoom
At the moment, only x86-64 architecture is supported on Windows. Wheels are available for Python 3.8+ on Windows.

Please note that the Windows version is not as well-tested as Linux and macOS versions. It can be used for development and testing but if you want to conduct serious (time and resource-extensive) experiments on Windows, please consider using Docker or WSL with Linux version.

Gymnasium/Gym wrappers
Gymnasium environments are installed along with ViZDoom. See documentation and examples on the use of Gymnasium API.

OpenAI-Gym wrappers are also available, to install them run:

pip install vizdoom[gym]
See documentation and examples on the use of Gym API. OpenAI-Gym wrappers are deprecated and will be removed in future versions in favour of Gymnasium.

Examples
Python (contain learning examples implemented in PyTorch, TensorFlow and Theano)
C++
Python examples are currently the richest, so we recommend to look at them, even if you plan to use other language. The API is almost identical for all languages.

See also the tutorial.

Original Doom graphics
Unfortunately, we cannot distribute ViZDoom with original Doom graphics. If you own original Doom or Doom 2 games, you can replace Freedoom graphics by placing doom.wad or doom2.wad into your working directory or vizdoom package directory.

Alternatively, any base game WAD (including other Doom engine-based games and custom/community games) can be used by pointing to it with the set_doom_game_path/setDoomGamePath method.

Documentation
Detailed descriptions of all ViZDoom types and methods can be found in the documentation.

Full documentation of the ZDoom engine and ACS scripting language can be found on ZDoom Wiki.

Useful articles (for advanced users who want to create custom environments/scenarios):

ZDoom Wiki: ACS (scripting language)
ZDoom Wiki: CVARs (console variables)
ZDoom Wiki: CCMD (console commands)
Awesome Doom tools/projects
SLADE3 - Great Doom map (scenario) editor for Linux, MacOS and Windows.
Doom Builder 2 - Another great Doom map editor for Windows.
OBLIGE - Doom random map generator and PyOblige is a simple Python wrapper for it.
Omgifol - Nice Python library for manipulating Doom maps.
NavDoom - Maze navigation generator for ViZDoom (similar to DeepMind Lab).
MazeExplorer - More sophisticated maze navigation generator for ViZDoom.
Sample Factory - A high-performance reinforcement learning framework for ViZDoom.
EnvPool - A high-performance vectorized environment for ViZDoom.
Obsidian - Doom random map generator, a continuation of OBLIGE.
Contributions
This project is maintained and developed in our free time. All bug fixes, new examples, scenarios, and other contributions are welcome! We are also open to feature ideas and design suggestions.

We have a roadmap for future development work for ViZDoom available here.

License
The code original to ViZDoom is under MIT license. ZDoom uses code from several sources with varying licensing schemes.
