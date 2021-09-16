---

title:  Planning
description: an example of a planning post
date:   2021-08-21
category: planned

---

This is a WIP to serve as an example of what a planning post should look like. 

## backlog
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


<!-- more -->

