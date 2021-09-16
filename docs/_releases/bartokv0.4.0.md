![Release Image](https://bit.ly/fiugLotusPic)

# bartok v0.4.0
started: 2020-06-07
release: 2021-01-29

- service worker
	- faster loading
	- offline
	- paradigm shift in file handling & UI services
- editor improvements
- playing around / preparing
	- wasm
	- open folder
	- css 3d versus svg 3d
<div style="height: 100%"></div>

### some thoughts

- I make a ton of lists and notes - MASSIVE STRUCTURE
- I don't always have time to bring order to this or implement
- I get anxiety about not being able to complete this stuff
- I want to move faster, be less worried, have less friction
<div style="height: 100%"></div>


![image](https://user-images.githubusercontent.com/1816471/119406848-5e2a5d00-bcb1-11eb-8b6e-7e7c987a26a5.png)


  - this chart is sort of a slippery grok, but the intent/effect is golden and the math seems legit
  - there may be a few things lost when considering creating a feature vs automating a task
    - "was it even possible to do the thing before" versus "time you shave off"
    - and maybe more, but my brain goes on to other things before I can dive deeper
<div style="height: 100%"></div>

<img
 style="max-height:unset; width: 100%; margin: auto;"
src="https://user-images.githubusercontent.com/1816471/119406959-8b770b00-bcb1-11eb-8dbf-e5f69f4f19b7.png" alt="" />

<div style="height: 100%"></div>


## Current State

### meta
  - [X] service worker and IndexDB (localforage)
  - [X] edit bartok in bartok
  - [X] upload binary files
  - [X] upload whole folder
  - [X] pop out preview
  - [X] languages for preview
  - [X] search icon (magnifer) should be connected to somehting

### panes
  - [X] pane position/size remembered (on page reload)
  - [X] close/hide panes and remember this (on page reload)

### explorer
  - [X] recall open folders and selected file (on page reload)
  - [X] recall scroll position on page reload (or scroll selected into view)

### editor
  - [X] syntax highlight for clojure
  - [X] improved loading
  - [X] recall last used file
  - [X] recall previous tabs
  - [X] context menu for tabs (close all / other)
  - [X] per file, remember scroll position (on file reload & page reload)

### status bar
  - [X] connected to line & col #
  - [X] recall previous file type (on page reload)

### templates
  - [X] templates run through service worker
  - [X] match based on tag in file contents

### preview
  - [X] default file should load in preview on page load
  - [X] recall last shown preview on page reload

### service map
  - [X] show registered triggers in map

### terminal
  - no updates

### server
  - no updates