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

