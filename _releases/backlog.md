---

title: "backlog"
description: "features and fixes to think about when release planning"
image: https://user-images.githubusercontent.com/1816471/133831476-abf1dfa0-d67f-421c-95d0-c821be5864ff.png
video:

started:
released:
date: 2099-01-01

category: planned

---

<!-- ![image](https://bit.ly/fiugLanscape1) -->
<!-- ![image](https://bit.ly/fiugLanscape2) -->
<!-- ![image](http://bit.ly/fiugLandscape3) -->
<!-- ![image](http://bit.ly/fiugLandscape4) -->


# customer facing concerns still at large
- panes and pane related
- starting a github repo with fiug
	- from scratch
	- from folder on local hard drive
- uploading files into a repo
- removing a repo
- viewing / cleaning up storage
- issues with .keep files and ##PLACEHOLDER## files
- tree dragging/droping
- terminal
	- arrow keys
	- tab completion
	- links (to something within app)
- search performance

- themes
- extensions/plugins/store, see [store incubate](https://github.com/crosshj/fiug-incubator/blob/main/1ncubate/store/store.js)
- open from fiug badge on github
- [X] editor horizontal scroll

<!-- more -->

# exiled from v0.4.6
- word wrap in editor
- editor search bar docks at top versus floating over
- use prose mirror for markdown rendering
	- https://prosemirror.net/examples/markdown/
	- come with the advantage of being able to implement WYSIWG later
- node REPL (and other REPL's as well)
- minimap for large files (fails on service-worker dist, for example)
- minimap should reproduce ascii art reliably
	- because if it doesn't then how can we trust regular code to be repoduced reliably?
- markdown frontmatter
- on first open, project should show Readme.md open if exists
- markdown support, image templates, and maybe other templates loaded by default when fiug loads
- when editor search returns no results -> "undefined of 1"
- when rollup error occurs ( ie, /!/script  case), indicate this somehow to caller
- after files are commited, should remove "changed" status
- codemirror mini-map doesn't appear until doc is focused
- codemirror native scrollbars
	- need to be styled to be invisible
	- horizontal scrollbar needs to be visible
	- issues with native appearing when zoomed out
	- see issues surrounding [this](https://github.com/crosshj/fiug-beta/commit/cd6037706efef2818456e7460060e9919248c3b0)
- close all doesn't work properly
	- does actually close tabs
	- when next file is opened, all files are back
- should be able to delete a cloned repository
- should be able to update service worker without opening chrome dev tools
- ^^^ see "nice to have 2021-10-04", items starting with "a way to"
- should be able to run code from terminal in context of main app (not in worker or iframe)
- should be able to list triggers and listeners currently attached to app (see previous item, maybe)
- run a github action from terminal
	- see [github REST docs: actions](https://docs.github.com/en/rest/reference/actions)
	- esp. see [create-a-workflow-dispatch-event](https://docs.github.com/en/rest/reference/actions#create-a-workflow-dispatch-event)
	- this approach could be super-powerful for many different things
- a way to paste an image in editor like can be done on github
- a way to jump to current repo on github from fiug

# nice to have 2021-10-04
- history that remembers across sessions
- export root to zip
- import root from zip
- upload file
- upload folder
- paste image
- paste file
- terminal tab completion
- terminal left and right arrows (and insert/delete)
- node scripts accept input (interactive)
- a way to delete cloned repos
- a way to delete app state (for refresh)
- a way to update app
- notification that a new version is available
- ...


# exiled from v0.4.5
- [ ] sometimes file is read as '##PLACEHOLDER##' and replacement is not fetched from github
	- this seems to occur where file is read directly from store
	- this means that user must visit file first before it is read
	- an example of this occuring
		1. clone crosshj/fiug-beta
		2. preview terminal/.example.html
		3. observe failure when loading terminal/.example.js
	- this was noted without as much detail in v0.4.4
- [ ] should be able to delete a repo as well as pull it

# exiled from v0.4.4

- [ ] bug: .keep files not removed when file is created in empty dir

- [ ] git config alias
	- git config --global alias.br branch
	- git config --global alias.ci commit
	- git config --global alias.st status
- [ ] refactor
	- [X] major modules in their own folders: editor, tree, sw
	- [ ] wire up UI to use modules from folders vs in "modules" folder
	- [ ] remove "shared" folder (or drastically reduce size)
- [ ] git pull: get changes from remote for a repo that already exists
	- [ ] when repo is "pulled" should not blow away .git folder
	- [ ] when repo is "pulled" should not blow away current changes
- fiug command? gh/octokit command?
	- [ ] list all repos that are cloned
	- [ ] list all repos from an owner
	- [ ] list all branches for a repo
	- [ ] do everything [github CLI](https://cli.github.com/) does (lol)
- [ ] worker transpiling
- [ ] consider using webcomponent or shadow dom vs iframe
	- [case in point](https://medium.com/bbc-design-engineering/goodbye-iframes-6c84a651e137)
	- or don't make this decision / do this work right now
- [ ] editor horizontal scroll
- [ ] merge editor changes with git changed(?)
- [ ] feed exclusively on update event
	- editor tabs: order, open, changed, new, pinned
	- tree: service name, selected, changed, new, open, scroll?
	- editor: selected, history, scroll, etc
	- terminal: current dir (if not in session), service name
- [ ] write a custom CM mode that works by wrapping another syntax highlighter:
	- http://www.java2s.com/example/javascript/codemirror/codemirror-custom-mode-apply-styles-on-keywords.html
	- (or dynamically loads any given mode?)
- [ ] settings: should show status of pulling/cloning
	- might not do this, instead show loading dots in terminal
- [ ] search: chokes sometimes (use GH search api?)
- [ ] tabs: still weird issues / dancing
- [ ] tree: parent folder not indicating changed child
- [ ] delay occurs before editor loads sometimes
	- issue seems to occur because of file store get
	- issue may not exist now that browser storage is less used
- [ ] copy is hooked up in tree
- [ ] tree(?) fires multiple events
	- when dragging from one folder to another
- [ ] offline command downloads all files from repo
- [ ] DO NOT: download all files in service manifest on first load
	- balance this against offline usage
	- especially do not download files needed for templates
- [ ] DO: load editor modes as needed, cache and cleanup
- [ ] DO: clean up editor state as needed
	- when undo file change reverts to unchanged state, this file is touched but no longer changed
	- when a touched file is closed, it is no longer touched
- [ ] clear(?) editor state for files when changed outside editor
- [ ] file "##PLACEHOLDER##", it's possible there are other issues with this
- [ ] service worker should clean up previous cache stores (but not app state)
- [ ] DO: clean up orphaned files
	- files that are not opened and not in tree should be removed from store
- [ ] DO NOT: keep state in many different places
	- which files are open: tracked in SW and tabs
	- which files are changed: tracked in SW and tabs
	- editor changes and file changes in different stores

### REMOVE DEAD CODE
- [ ] terminal module
	- cleanup following rewrite/shift in mindset
	- includes removing old preview code
- [ ] editor
	- load doc should be handled strictly by plugin
	- state should come from outside module
- [ ] editor tabs
	- shift to rely strongly on SW state
- [ ] tree / explorer
	- anything left from previous iteration?


# exiled from v0.5.0 release planning

- [ ] on editor scroll, show minimap viewport indicator overlay, disappear when scroll is done

- [ ] focus on / zoom to a folder (in explorer)
- [ ] search has performance issues
- [ ] uploading images + binary files

- [ ] terminal should get cwd and service name from query params
- [ ] terminal left/right arrows for editing buffer
- [ ] terminal tab completion

- [ ] editor tabs order of next tab closing should make sense
- [ ] explorer: add expand/collapse
- [ ] explorer: overscroll seems to not be working
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

- [ ] service worker should provide endpoint for directory contents list


# exiled from v0.6.0 release planning
- [ ] themes fixed
- [ ] cleaner loading view
- [ ] golden layout or similar for pane splitting
- [ ] rename project/service
- [ ] auto-detect tabs vs spaces
- [ ] linter - https://codemirror.net/demo/lint.html
- [ ] show 80 char limit line
- [ ] scrolled shadow at top to indicate file is scrolled down
- [ ] mouse clicks on terminal to select menu items (?)
- [ ] deploy pipeline
	- https://jenkins.io/projects/blueocean/



# themes

[a cool theme gallery](https://themes.vscode.one/)

At some point, I'd like to tackle themes.  Here are some thoughts on that.

An example of switching user preference for color scheme:
from [web.dev color scheme](https://web.dev/color-scheme/)

``` javascript
const meta = document.querySelector('meta[name="color-scheme"]');
let colorScheme = 'light';
meta.content = colorScheme
if (!window.frameElement) {  
	window.setInterval(() => {    
		colorScheme = colorScheme === 'light' ? 'dark' : 'light';
		document.documentElement.style.colorScheme = colorScheme; 
		meta.content = colorScheme;
		const root = window.frames[0].document.documentElement;
		root.style.colorScheme = colorScheme;
		root.querySelector('meta[name="color-scheme"]').content = colorScheme;
	}, 3000);
}
```


# css
- audit css - https://css-tricks.com/tools-for-auditing-css/
- dynamic css
	- css is returned as a service by SW
	- settings affect what css is returned
	- this benefits themes probably most of all

# fonts
- allow customizing fonts
- https://input.djr.com/preview/
- https://www.elegantthemes.com/blog/wordpress/best-programming-fonts
- https://tonsky.me/blog/font-size/
- option to use fonts with ligatures eg. https://github.com/tonsky/FiraCode


# tabs
- tabs can be reordered
- tabs can be pinned
- tabs grouped (like chrome tab groups)
- opened tabs saved on a per project basis


# similar to what I've already built
- https://blog.stackblitz.com/posts/introducing-webcontainers/

# found from codesandbox.io
- first of all, why does bartok not use codesandbox?
	- https://github.com/codesandbox/codesandbox-client/tree/master/standalone-packages/react-sandpack
	- https://github.com/codesandbox/codesandbox-client/tree/master/standalone-packages/sandpack
- https://browsix.org/ - Run C, C++, Go and Node.js programs as processes
- https://github.com/jvilk/BrowserFS -  in-browser filesystem, NodeJS filesystem API, various backends

# picture editor
- got to it before me: [https://docs.replit.com/tutorials/kaboom](https://docs.replit.com/tutorials/kaboom)

# debugging
- sort of on the fence about this since Chrome Dev Tools debugging works well enough
- also the concept of running a js file (for example) is still in its infancy

<div style="
	margin-top: 3em;
	background: url(/images/process.png);
	width: 100%;
	height: 225px;
	background-size: 600px;
	background-position-y: -90px;
	background-repeat: no-repeat;
"></div>

# freeform input of ideas here
- quickly take notes, edit/create images, explore visual ideas, explore logical idea
- make slides easily
- make charts/graphs easily
- annotate images easily
- mock up systems easily

- application resources cleanup
- preview/templates allow a different form of interaction with files vs text editing
- hide and show UI elements quickly and easily, ie editor, terminal, tree
- bundle templates with syntax highlighting
- static analysis, code mapping, service map, etc
- themes and usage of theme by templates/preview, dynamic css
- development meta
	- regular vlog release
	- blog
	- clearer release planning
- terminal
	- [ ] arrow keys
	- [ ] tab to auto-complete
	- [ ] customizable prompt
	- [ ] recall history across sessions
	- [ ] view recent commits
- editor
	- horizontal scroll bar
	- re-order tabs
- status bar
	- line up relevant info to associated pane
	- version
- application bundle
- internal application links
	- from terminal to some file + line number
	- from file to another file, esp. markdown
	- from one place in current file to another place in same file
- tree
	- focus to folder
	- file status colors


# 2021-02-26 todo
- [X] straighten the way that files are stored in service worker (full path for id)
- [X] templates that work across services
- [X] fix preview/lock

- [X] version endpoint in SW - version and commit hash
- [ ] github actions
	- example https://github.com/marketplace/actions/gh-pages-deploy
	- example https://dev.to/pierresaid/deploy-node-projects-to-github-pages-with-github-actions-4jco

- [ ] load file without service being open
- [X] better "first view" for people that are new
- [X] better loading view
- [X] favicon
	- https://austingil.com/svg-favicons/

- [X] switching between services is awkward

- dumbdown, tree languages - https://github.com/treenotation/jtree


# 2020-10-11 todo
- [ ] split editor (mutliple editor panes)
- [ ] editor: diff view
- [X] preview performance issues
- [ ] javascript/modular templates (vs html-only)
- [X] terminal watch file
- [ ] preview hot reloading
- [ ] dynamic/virtual files (to feed into preview)
- [ ] settings integration with service worker
- [X] delay loading all services
- [ ] improved/cleaner service map
- [ ] system services connected to each other
- [ ] service details in service map
- [ ] command palette commands
- [ ] arrange images on single image (use spritemap techniques/code)
- [ ] clean up and connect listeners/triggers
- [ ] automatic add vendor deps to service manifest (cached offline)
- [ ] package storage (like package.json/node_modules)
- [ ] share project (zip/torrent)
- [ ] one template/multiple file extensions supported
- [X] connect context menu commands
- [ ] connect action bar things

- [X] minimap
- [ ] go to line number
- [X] all terminal commands working well (like unix)
- [X] working directory in terminal prompt
- [X] delay loading service on initial load (loading all code-BAD)
- [X] editor: hover highlights expand/collapse indicators
- [X] git support integrated
- [X] messaging between template and editor
- [X] file search connected
- [X] import css in jsx files
- [X] untracked files (Untitled-1)
- [X] paste image / file
- [X] tabs versus spaces switching

# 2020-09-17 TODO
- less tabs, close all tabs
- [X] create/delete file/folder works with provider
- [X] issue with preview, binary file shows in preview instead
- CRUD, connecting service nodes working in service map (decide what it means to connect from code POV)
- [X] switch between tabs and spaces

# 2020-09-17 TODO
- [ ] *.todo, *.slides, *.graph - all services should come with "native" support for these
	- graphs - https://en.wikipedia.org/wiki/Category:Infographics
- [ ] *.settings - treat settings as templated files with a common UI?
- [X] connect git
	- https://github.com/isomorphic-git/isomorphic-git
	- real/beefy FS abstraction layer

# 2020-08-22 TODO
- [X] save a file with Bartok Basic Server provider
- [x] project switch
- [X] list of curent providers in settings

- tons of issues
	- [X] tab closing closes tabs that shouldn't close
	- [X] preview doesn't show if project doesn't have templates (global templates)
	- [X] project loads index.js even if it doesn't exist
	- [X] tabs are not recalled for projects other than welcome project
	- [X] switching between preview and terminal is broken in some cases
	- [X] settings view has tab switching problems
	- [X] preview fails after fresh boot

- preview full screen
	- [X] should hide most UI elements; only show fullscreen controls
	- [ ] fullscreen state is wonky


# 2020-08-01_1829 TODO
- [X] trying to get service worker fully fleshed out
- [X] make terminal not rely on callback pattern
	- [X] instead, it should fire an event and only pop that event off pending queue when answer is heard
	- [X] should have a timeout with this
- [X] seperate template listening and DOM updating from terminal code

# 2020-07-19_1731 TODO
recall all things
- [X] editor tabs (remember open, selected, and scroll position)
- [X] editor (load last loaded file)
- [X] preview (load last loaded preview)
- [X] panes (window width same as previous, recall positions)

connect all context menu items
- [X] huge list...

create|update|delete for service API in serviceHandler
- need this before service worker fork can be merged

reset page for ui
- [ ] kill service worker cache (or maybe don't use this)
- [ ] kill/reload serviceHandler
- [X] kill tree cache (sessionStorage)
- [X] kill all the recalled things (above)
- [X] kill service worker (which will be reloaded with boot())
- [X] kill moduleCache (localStorage) (maybe should be sessionStorage)
- [X] reloadServices true versus false

- [ ] BUG: loading page shows loading bar multiple times


# 2020-07-14_1902 TODO
- [ ] editor collaborative
- [X] mini map
- [ ] download ZIP
- [ ] react template loading spinner
- [ ] search in folder
- [ ] share service
- [ ] shared libs should load in offline mode
- [ ] smoother development flow on file change
- [ ] storage usage indicators: memory & file system
- [ ] todo app: export to bartok file system
- [ ] todo app: groups
- [ ] todo app: item edit
- [ ] upload a folder
- [ ] upload binary files
- [X] ability to close last file
- [X] bypass "let's go" button on repeat usage
- [X] command palette
- [X] default view for no service selected
- [X] edit bartok in bartok
- [X] editor code folding
	- https://codemirror.net/doc/manual.html#addon_foldcode
- [X] fix: closing (and opening?) a folder should not save that folder as selected
- [X] folders open when contained file is selected
- [X] full screen for preview
- [X] preview binary files: image, font, audio, video
- [X] preview uses service worker
- [X] recall open files
- [X] recall pane sizes
- [X] recall pinned preview
- [X] recall scroll position per file
- [X] recall selected file
- [X] search in file
- [X] switch indent between tabs and spaces
- [X] todo priority
- [X] todos import
- [X] export todo's: JSON
- [X] export todo's: markdown
- [X] fix issue with explorer pane resizing
- [X] read bartok ui (now called "fugue") in bartok
- [X] recall open tree folders
- [X] rename file-examples to be more descriptive
- [X] status bar line and column number update
- [X] todo scrolling


# 2020-07-01 TODO
- [ ] bitcoin/blockchain in browser (and why?)
- [ ] inline font: https://www.webucator.com/blog/2016/11/inline-web-font-avoid-fout/
- [ ] open a folder from local hard drive
	- https://www.html5rocks.com/en/tutorials/file/filesystem/#toc-dir-reading
	- https://www.html5rocks.com/en/tutorials/file/filesystem-sync/
- [ ] webtorrent
	- in a worker: https://github.com/webtorrent/webtorrent/issues/1248
	- see browser-server and aether-torrent from ^^^
- [ ] web loading time
- [ ] share
- [ ] export zip
- [ ] import zip
- [ ] web build system / service layer
- [ ] services graph / service selection
- [ ] template creation flow & overall template design
	- allow preview to interact with other bartok web components
- [ ] settings
	- define a backend
	- define a workflow
- [ ] log in (auth with an identity provider)
- [ ] collaboration
	- https://github.com/lesmana/webrtc-without-signaling-server
	- https://github.com/cjb/serverless-webrtc
	- https://peerjs.com/
- [ ] open a page that is just the file in editor or preview mode; options editor + preview (or other mashup)
- [ ] web persistence layer
	- [X] localforage in serviceworker
	- browserFS?
- [x] indent using tabs
- [X] code folding
- [X] finish tree context menu
- [X] images/binary files
- [X] open preview in new window / share
- [X] codemirror elegance & bug where editor shows blank
- [X] non editor tabs
- [X] read bartok web in bartok web
- [X] write bartok web in bartok web
- [X] require an npm package (and use it)

# DEPLOY | VERSION CONTROL
- https://app.diagrams.net/#G18h5403wK012mFwEuMETVVnQiyZmXPJOy
<!-- ![image](https://user-images.githubusercontent.com/1816471/116312252-31e6f380-a77a-11eb-946d-2eedc07ab5b5.png) -->


# exiled from scratch.md
### AN ATTEMPT AT FOCUS
#### What is an MVP for Bartok?
- CRUD services: editor, preview, templates?
- visualize services & connections: service map
- monitor services: service map
- deploy services: ???
- manage services: scale, scale policy, etc: ???
#### What are the nice-to-have sink holes?
- complete parity with items shown in MARKETING.md
- going too far with any given item listed in MVP statement
- open-endedness of the platform
- cool things to make release videos look nicer (preview)?
#### Potential Sinkhole Hard Examples:
- meta
	- how do UI services work? how much of Bartok UI is built with them?
	- can I build bartok with bartok editor?
- editor
	- could spend too much time (too much?) building an editor and putting all the cool things in it
	- perhaps editor should have it's own MVP/sink-hole evaluation
	- parity: does it do all the beloved editor things?
	- completeness: does it do everything right?
	- innovation: does it do cool things that other editors do not do?
- visuals
	- less concern about time waste here because visuals have appeal
	- would like to fully grasp how far is too far
	- there needs to be a basic set of items in service map
	- how they look is not as much important as how they connect
- monitor
	- similar case as with visuals
	- this depends on visuals being in place
	- need to be able to read logs
	- need to be able to view resource usage
- deploy
	- similar case as with visuals
	- is this a distinct item from manage (below)?
	- need to figure out how to do this
	- this depends on screens that have not been built
- manage
	- what does it mean to manage?
		- scale
		- scale policy
	- similar case as with visuals
	- need to figure out how to do this
	- this depends on screens that have not been built
#### What are currently the biggest "win" items?
- ... (not sure the following reflects the answer to this question)
- service save in chunks (because some files are huge)
- [ ] service templates
- [ ] logs streaming from server
- [ ] metrics streaming from server
- [ ] service map showing real stats
- [ ] UI ran from within bartok ecosystem (soft exploration into first-class services)
- [ ] server ran from within bartok ecosystem (more serious foray into first-class services)
- [X] files need id's for uniqueness <<< HUGE!!!
- [X] service map showing real services
- [X] file templates (UI services)
- [X] file preview (htm, svg, react)
- [X] direct file system based service (to enable next two wins)
### FILE CHANGES
 - [X] only keep changed tabs open, reuse previous/unchanged tabs
 - [X] tabs stay open across reload
 - [X] scroll/cursor position remembered
 - [X] allow closing last tab
### PACKAGE.JSON / CONFIG
 - [ ] package.json should be ideal and not strict?
	 - (comments, unquoted, single quotes, trailing commas, etc)
 - [ ] package.json should be service.json? .bartok.yml ?
 - [X] service should get its name from package.json
### TEMPLATES
 - [ ] templates for services? routeHandler, uiTemplate, plainNode, etc
 - [ ] eject templated app? (export)
### preview
 - [X] better release notes recording videos - page of code SUCKS!
 - [X] sidepane shows preview for React Component, HTML, markdown, etc
 - [X] use iframe: https://stackoverflow.com/questions/5050380/set-innerhtml-of-an-iframe
 - [X] links are clickable in editor (NOPE - in preview instead)
 - document renders/previews differently for certain doc types
	 - [X] [.md] - show rendered html and allow to switch
	 - [X] [.svg]
	 - [X] [.jsx] - do react!
	 - [X] [.ipynb] - jupyter notebook
		 - https://github.com/jsvine/notebookjs
		 - https://github.com/finnp/ipynb
	 - [.tp.json] (made up) - sprite editor and mapped preview (texture packer)
### unsorted
- [ ] bundling in browser
	- http://webpack.github.io/playground/
 	- https://github.com/systemjs/systemjs
- [ ] inline controls for codemirror - https://github.com/enjalot/Inlet
- [IP] show binary files as HEX
- [X] show preview in side (instead)
- [ ] node in the browser (and for that matter, the other language runtimes or emulators)
	https://blog.cloudboost.io/how-to-run-node-js-apps-in-the-browser-3f077f34f8a5
- [X] diff - http://cemerick.github.io/jsdifflib/demo.html
- [x] import/require/ read files from within preview
	- eg. `<img src="crosshj/fiug-beta/.NOTES/images/process.png" />`
	- eg. `import { foo } from 'someServicePath/file.mjs'`
- [ ] import and export services
- [ ] backup and restore
- [ ] recycle bin / trash can
- [ ] backup sqllite file ?
- [x] panes remember position
- [ ] pane splitting (as with a framework that allows open-ended pane manipulation)
- [X] code diff
- [X] page resize doesn't respect min width for explorer
- [ ] explorer can be hidden more beautifully, will auto-show and dismiss
- [X] terminal/preview can be hidden
- [X] terminal can take up full screen
- [ ] link files - files which store links and show them in preview
- [X] mini-map / preview within files
- [ ] https://12factor.net/ - obey???
- [X] remember scroll and cursor positions per file
- [X] command pallete
- [X] find in file dialogs
	- error dialogs / message popups
	- notifications
- [ ] keep up with VS CODE: icons, fold/match lines, folder arrows
- [X] code folding & fold all, etc
- keyboard shortcuts:
 - [ ] ctrl-g: go to line
 - [x] ctrl-p: command pallet
 - [ ] https://codemirror.net/demo/sublime.html
 - [ ] https://codemirror.net/doc/manual.html#option_extraKeys
- [ ] draggable tabs (to reorder)
- [ ] draggable files and folders (maybe)
- [ ] popup to indicate certain keyboard shortcuts are pressed
- [ ] connect codemirror to a language server ( LSP )
	- see crosshj/fiug-beta/.welcome/1ncubate/editor/editor.language.server.js
	- code completion, etc
- [ ] language parser/lexer does double duty as syntax highlighter
	- https://foo123.github.io/examples/codemirror-grammar
	- ohm - https://github.com/harc/ohm
	- pegjs/peggy - https://pegjs.org, https://github.com/peggyjs/peggy
	- jison - https://github.com/zaach/jison
	- chevotrain - https://chevrotain.io/docs
	- nearley - https://github.com/kach/nearley
- [ ] stream contents of big files to codemirror (possible?)
- language support:
	- Rust, Julia, Swift, APL, ML, lisp, C#, OCaml, F#, other??
	- https://codemirror.net/mode/index.html
- [ ] color picker in file edit mode
- [ ] make it easy to edit svg's in CSS
- [x] ascii representation of service nodes
	- http://asciiflow.com/ - draw ascii nodes
	- https://github.com/ivanceras/svgbob - convert to svg
- [ ] https://www.dwitter.net/ - 2d graphics in 150 characters
- [ ] spritesheet tool? https://www.leshylabs.com/apps/sstool/
