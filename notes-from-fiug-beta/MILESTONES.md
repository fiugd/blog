
why I open Chrome Dev Tools | why I keep Chrome Dev Tools open
--------------------------------------------------------------
- [ ] troubleshoot/fix fiug code itself (Sources)
- [ ] see console output of previewed file (Console)
- [ ] color picking (Elements)
- [ ] dom troubleshooting (Elements)
- [ ] it fills a screen/pane space which is not filled by something else
- [ ] verify network calls (Network)
- [ ] clear application state (Application)


why I open github.com | why I keep github.com open
--------------------------------------------------
- [ ] impossible to upload a binary through fiug.dev
- [ ] impossible to delete a file and persist to github
- [ ] impossible to delete a folder and persist to github
- [ ] check if gh-pages has built


why I open VS Code | why I keep VS Code open
--------------------------------------------
- [ ] some build systems are not adapted to web: CM addon bundle, CM modes bundle

- [ ] moving around a bunch of files doesn't work
- [ ] awkward integration with file system
- [ ] buggy file management

- [X] (I don't actually keep VS Code open any more)
- [X] service worker flow is not merged to main flow
- [X] no search in project / folder

- [X] doesn't recall scroll position
- [X] doesn't recall code collapse

- [X] can't dev/edit bartok in bartok
- [X] cant CRUD/save a file with service worker
- [X] highlight is weird (themeing and color issues)
- [X] no search in file


-----


basic server functionality in place
  - hosted node services
  - CRUD for services
  - persistance for services
  
UI is basically like VS Code
  - explorer
  - editor / editor tabs
  - terminal

mult-file support

icons and syntax highlighting for different file types

file templates

preview


----------------------------------------
^^^ DONE or mostly in place ^^^


USE CASE: plain old editor with no backend

USE CASE: editor with preview, useful for front-end dev


UI is fully like VS Code (where expected)
  - CRUD for files (nice context menus, etc)
  - switch between services
  - all things connected:
    - files from backend
    - file status indicator
    - file icons
  - tabs work

authorization for bartok (not for hosted services)

deployed to "PROD" (depends on auth being in place)

USE CASE: basic hosting of backend services
  - swagger-type or routes only service
  - PM2 well-connected
  - scale services

USE CASE: intermediate hosting of client/UI services
  - upload binary files: fonts, images, audio, video
  - connect seemlessly to a backend service

USE CASE: advanced hosting of backend services
  - services map (UI)
  - workers on different machine

