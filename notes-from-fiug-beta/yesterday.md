#### 2021-07-15 | TBD
	- ocaml language
	- delete operation

#### 2021-06-28 | 2021-07-15
	- doc loading speed (still not completely solved)
	- preview wildcards, help, hidden controls
	- service worker service operations
	- svg favicon
	- palette menu click items
	- minor fix for editor indent
	- test patterns ++
	- ink language running in browser + syntax highlight

#### 2021-06-15 | 2021-06-28
	- preview command
	- ls command
	- all components responding correctly on file delete: mainly editor+tabs
	- over-arching changes to application state tracking
	- file operation handling in service worker + tests
	- testing patterns++ (copied from vermiculate project, adpated to node abstraction)

#### [fiug.dev 2021-06-14 video](https://www.youtube.com/watch?v=zDPFYCLt_rE)

#### 2021-04-20 | 2021-06-14
	- fix issue with tree icons
	- editor tabs close all
	- git commit ++
	- editor code collapse caret hiding / code folding
	- terminal commands: node + cat
	- APL lang support ++
	- improved loading logo
	- markdown preview scroll recall
	- editor minimap + editor doc state + context menus

#### [bartok|fiug 2021-04-18 video](https://www.youtube.com/watch?v=ODoJo1G39Kw)

#### [bartok|fiug 2021-04-14 video](https://www.youtube.com/watch?v=jxTI9ICtAj8)

#### 2021-03-06 | 2021-04-20 - 0.4.2 Git Commit, Changes, Terminal ++
	- tighter tree integration
		- file changes
	- tons of issues relating to fileName vs fileName+/filePath/blah..
	- fix issues with express abstraction vs request method
	- fix move/rename issues
	- fix tab issues
	- new terminal
	- terminal features
		- git
		- history
		- up and down arrows to nav history
		- watch system events
	- commiting to github
	- iframe can listen to and trigger system events
	- hotkey for move line up
	- hotkey for toggle comments

#### 2021-01-29 | 2021-03-06 - 0.4.1 Github, Tree Module, Repo/Name dancing
	- add github read integraion (Jan 30 - Feb 1st week end)
	- move "welcome" into it's own repo "fiug-welcome" (Jan 31)
	- new tree module ( Feb 14 - March 6++ )
	- create a beta environment for fiug (Feb 22)

#### 2020-11-15 | 2021-01-29 - Angular+, Service Worker, misc exploring
	- Editor Recall
		- create: Nov 15 - https://github.com/crosshj/experiments/commit/3bdf280b3da21bde316dc56df7fc852fe5f94ffb
		- disable: Nov 15 - https://github.com/crosshj/experiments/commit/007377b93d178e7ae023377c23b508eeacb35518 
	- misc exploration (Nov 15 - Jan 27)
		- old experiments: quadcopter, rangersAdvent, encrytWebWorker
		- UI frameworks exploration: vue, angular, ember, svelte
		- asciidoc, systemjs
		- move bartok out of experiments and call it fiug (Jan 27)
	- service worker refactor ( Jan 29 )

#### 2020-10-15 | 2020-11-15 - Stylus, Search, languages, experiments
	- Stylus support (Oct 15)
	- Search Project (Oct 18 - Nov 15)
	- open parent when child is selected
	- untracked files (files that are not in tree)
	- edit fiug/bartok in fiug/bartok (service id:0)
	- languages
		- wat (web assembly)
		- ocaml (fail)
		- pascal
		- julia
		- typescript
		- ascii to svg (markdown)
	- experiments
		- texture packer
		- 2-way messaging (template - which template?? )
		- zip a project
		- editor linting
		- file drop (to upload)
		- webcam
		- hex edit
		
#### [2020-10-20 - bartok | fiug 2020-10-21 video](https://www.youtube.com/watch?v=UVkLaif92Xg)

#### 2020-10-05 | 2020-10-15 -
	- intial effort of tracking language/template progress (Oct 6)
	- Command Palette (Oct 9)
	- JSX example refactor (Oct 12)
		- begin improved support for including files
	- gml parsing with Ohm (Oct 12)
	- experiments golden-layout, image pasting (Oct 13)

#### 2020-09-29 | 2020-10-05 - languages, CRUD, & tightening overall use
	- more languages, syntax, templates
	- tighten provider file CRUD
	- remove console warnings and update some dependencies
	- reuse tabs if not changed
	- mime types in service request handler
	- better opening and closing services from settings view

#### 2020-09-19 | 2020-09-27 - languages & misc
	- add a ton of language templates, icons, syntax
	- experiment webtorrent
	- experiment zip
	- experiment git integration

#### 2020-09-02 | 2020-09-06 - service map
	- connect triggers to listeners in service map
	- add a bunch of triggers in app
	- mess with service map layout
	- add zoom
	- add ability to move nodes
	- add sidebar for details about a node

#### 2020-08-29 | 2020-08-30 - refactor, fix settings,template issues
	- move around a bunch of files; further test provider integration
	- fix settings and template issues
	- settings issue still exists on page reload

#### 2020-08-25 | 2020-08-26 - fix tab,preview bugs
	- fix a lot of tab closing issues
	- fix f5 not working when terminal has focus
	- fix terminal/preview switching issues

#### 2020-08-15 | 2020-08-16 - settings view, provider abstraction
	- create settings view
	- create provider API in service worker
	- minor modifications to bartok basic server

#### 2020-08-11 | 2020-08-12 - no files/services open views
	- no files open view
	- no service selected view


> 2020-08-12 this file created
> purpose: highlight what changed in hindsight on a roughly day-to-day basis


#### 2020-07-20 [bartokv0.4.0 PREVIEW](https://www.youtube.com/watch?v=_wWBVz9gvSk)
	- service worker
	- editor improvements
	- wasm
	- open local folder
	- css 3d

#### 2020-06-07 [bartok v0.3.2](https://www.youtube.com/watch?v=lPs6YQCHlc4)
	- status bar++
	- graph template
	- file system

#### 2020-04-27 [bartokv0.3.1](https://www.youtube.com/watch?v=1pV9gX1ida0)
	- preview
	- templates

#### 2020-04-13 [bartokv0.3](https://www.youtube.com/watch?v=LAKMr2ARd34)
	- editor can use local storage
	- file types: icons and syntax highlighting
	- folder operations
	- file changes and status
	- new status bar
	- improved service map

#### 2020-03-30 [bartok v0.2](https://www.youtube.com/watch?v=NJc68mc8Wag)
	- multi-file system
	- editor tabs
	- terminal commands++
	- service map

#### 2020-03-24 [bartok v0.1](https://www.youtube.com/watch?v=nFXOxs-oDMA)
	- single-file system
	- looks a little more like VS Code
	- basic tree, editor, terminal
	- back end: persist, update, pm2(early)

#### 2020-03-20 [bartok v0](https://www.youtube.com/watch?v=yKxyX_6NMZQ)
	- basic front end - bootstrapp-like
	- basic back end