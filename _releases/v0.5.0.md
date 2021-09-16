![image](https://bit.ly/fiugLandscape1)

# bartok v0.5.0
started: TBD
release: TBD

- [ ] on editor scroll
	- show page overlay for a moment
	- then disappear
- [ ] preview
	- if current doc matches matcher
	- show it after preview command exec'ed

- [ ] import rewrites in SW with something like this: [lexer](https://github.com/guybedford/es-module-lexer)
OR
- [ ] use [import maps](https://github.com/WICG/import-maps)

- [ ] focus on / zoom to a folder (in explorer)
- [ ] search has performance issues
- [ ] uploading images + binary files
- [ ] click to select file from command palette opener

- [ ] terminal should get cwd and service name from query params
- [ ] terminal left/right arrows for editing buffer

- [ ] editor tabs order of next tab closing should make sense
- [ ] explorer: add expand|collapse
- [ ] explorer: overscroll seems to not be working
- [ ] explorer: scroll bar hide/show causes status circle to dance (on Mac)
- [ ] explorer > right-click > Open In Preview
	- should work with new terminal preview command

- [ ] context menu for terminal
- [ ] terminal passes hotkey events to parent
	- control-s: save
	- control-p: open file
	- control-shift-p: command window

- [ ] reveal in sidebar is broken
- [ ] editor tabs: keep open, pin, reveal in sidebar

- [ ] clean up for editor document state
- [ ] make sure editor undo history works properly

- [ ] terminal tab completion

- [ ] service worker should provide endpoint for directory contents list
- [ ] path resolution needs to be a module or endpoint; this needs to be a solved issue


- [ ] git clone + git pull + status + push (in terminal)
- [ ] git pull should bring in new changes (okay to reject if changes exist on local)
- [ ] on repo "clone", don't pull all files
	- instead get from github as needed (except for templates)

Summary
=======

Current State
=============

##### meta
- [ ] themes fixed
- [ ] cleaner loading view
- [X] import files
- [X] export files
- [ ] !!! bartok version at bottom left should be connected to real something

##### paneView
- [ ] golden layout or similar for pane splitting

##### explorer
- [ ] rename project/service

##### editor
- [ ] auto-detect tabs vs spaces
- [ ] linter - https://codemirror.net/demo/lint.html
- [ ] show 80 char limit line
- [ ] scrolled shadow at top to indicate file is scrolled down

##### terminal
- [ ] mouse clicks on terminal to select menu items (?)
- [ ] loading spinner & done checkmark
	- https://stackoverflow.com/questions/2685435/cooler-ascii-spinners
	- http://jsfiddle.net/sindresorhus/2eLtsbey/embedded/result/
	- https://github.com/sindresorhus/cli-spinners/blob/HEAD/spinners.json

##### server
- [ ] deploy pipeline
	- https://jenkins.io/projects/blueocean/

##### statusBar

##### serviceMap
- https://www.weave.works/oss/scope/

![image](https://bit.ly/fiugLanscape2)

![image](http://bit.ly/fiugLandscape3)

![image](http://bit.ly/fiugLandscape4)

<style>
	#container p:first-child img {
		filter: hue-rotate(377deg) contrast(1.25) saturate(4);
	}
	#container p:nth-child(18) img {
		filter: hue-rotate(53deg) contrast(1.25) saturate(5);
	}
	#container p:nth-child(19) img {
		filter: hue-rotate(0deg) contrast(1.25) saturate(7);
	}
	#container p:nth-child(20) img {
		filter: hue-rotate(132deg) contrast(1.25) saturate(4);
	}
</style>
