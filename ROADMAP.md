# Roadmap for MemoryCard

## Project Vision

**Design Philosophy:** Git-like branching & history for emulator saves with full local-first control.

## Phase 0: Core Functionality

* **Goal:** Make MemoryCard fully functional offline with no UI yet
* **Platform scope:** GBA only
* **Save type:** `.sav`
* **Snapshot:** Timestamp, Description, Notes
* Export full library
* Register ROMs/Saves
* Immutable snapshot archive
* Export any snapshot to back into `.sav` file
* Build multiple independent trees for the same game
* DAG (Directed Acyclic Graph) per game
* Setup config file `config.json` for local paths
* File structure
  * `.memorycard/`: Git-like internal data
  * `roms/`: User ROMs
  * `Card/`: MemoryCard data
    * `Card/SaveData/`: Save files, snapshots, etc.
    * `Card/Media/`: Screenshots, thumbnails, etc.
    * `Card/Config.json`: User configuration
    * `Card/src/`: Source code
      * `Card/src/main.py`: Main application

## Phase 1: User Interface

* **Goal:** Basic UI for core functionality
* Show the GBA game cover art
* List registered games
* Show snapshot history per game
* Create new snapshots with description/notes

## Phase 2: Advanced Features

* Auto determine save file type based on ROM
* Support more consoles (NES, SNES, GB, GBC, N64, etc.)
* Convert save files between formats
* Branching and merging save states
* Cloud sync support (Google Drive, Dropbox, etc.)
* Docker containerization
* Drag-and-drop registration
* Flashcard support
* Emudeck compatibility
