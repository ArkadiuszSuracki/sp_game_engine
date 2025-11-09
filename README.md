# st_game_engine

A small C++/CMake playground for building a simple game-style app on top of **raylib**.

Current features:

- window settings loaded from `config.ini`
- embedded Roboto font loaded from memory (`resources/fonts/roboto_font.h`)
- simple MVC-ish project layout (`core/`, `controllers/`, `views/`, `resources/`)
- main menu (Play Game, Options, Exit) controlled with arrow keys
- options screen with fullscreen toggle and “back”
- game screen with a basic 3D scene and FPS-like camera (WASD + mouse)
- in-game debug overlay toggled with `~` for quick on-screen logs
- ESC does **not** close the app (we handle it ourselves)

Tested on Ubuntu 24 with KDevelop.

## Project structure

```text
st_game_engine/
├── CMakeLists.txt
├── config.ini
├── main.cpp
├── resources/
│   └── fonts/
│       └── roboto_font.h
└── src/
    ├── core/
    │   ├── App.h / App.cpp
    │   ├── Config.h / Config.cpp
    │   ├── ResourceManager.h / ResourceManager.cpp
    │   └── DebugOverlay.h / DebugOverlay.cpp
    ├── controllers/
    │   ├── BaseController.h
    │   ├── MenuController.h / .cpp
    │   ├── OptionsController.h / .cpp
    │   └── GameController.h / .cpp
    └── views/
        ├── MenuView.h / .cpp
        ├── OptionsView.h / .cpp
        └── GameView.h / .cpp
