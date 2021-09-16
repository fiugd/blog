---

title: "backlog"
description: "features and fixes to think about when release planning"
image: https://bit.ly/fiugGearsWorld
video:

started:
released:
date: 2099-01-01

category: planned

---


# customer facing concerns still at large
- getting started
- panes and pane related
- starting a github repo with fiug
	- from scratch
	- from folder on local hard drive
- uploading files into a repo
- removing a repo
- viewing / cleaning up storage
- search performance
- performance (be specific about this)
- tree dragging/droping
- issues with .keep files and ##PLACEHOLDER## files
- editor horizontal scroll
- terminal
	- arrow keys
	- tab completion
	- links (to something within app)
- themes
- extensions/plugins/store
- open from fiug badge on github


<!-- more -->

# exiled from v0.4.4

- [ ] tree changed files indicator icons are still jumping on Mac on hover/exit
- [ ] other git commands: list, open, close, pull
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
http://www.java2s.com/example/javascript/codemirror/codemirror-custom-mode-apply-styles-on-keywords.html
(or dynamically loads any given mode?)
- [ ] settings: should show status of pulling/cloning
- [ ] search: chokes sometimes (use GH search api?)
- [ ] tabs: still weird issues / dancing
- [ ] tree: parent folder not indicating changed child
- [ ] delay occurs before editor loads sometimes
	- issue seems to occur because of file store get
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





# themes

[a cool theme gallery](https://themes.vscode.one/)

At some point, I'd like to tackle themes.  Here are some thoughts on that.

An example of switching user preference for color scheme:
from [web.dev color scheme](https://web.dev/color-scheme/)

``` javascript
<script>
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
</script>
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

# random
- waiting is not a problem; waiting with desire to move forward is a problem
- measure code change as risk, but shouldn't this also map to AST branch change (loose question)

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

# input freeform
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
	- arrow keys
	- tab to auto-complete
	- customizable prompt
	- recall history across sessions
	- view recent commits
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

