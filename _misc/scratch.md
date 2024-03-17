---

title: "scratch"
description: "thoughts that have not been sorted and arranged much"
image: https://user-images.githubusercontent.com/1816471/133834403-5f652484-769b-46ea-9094-c7aabdd140a5.png

video:
date: 2022-09-09
---

## CDN's
- https://esm.sh/#docs
- https://unpkg.com/
- https://jsdelivr.com, eg https://jsdelivr.com/package/npm/@ffmpeg/ffmpeg
- https://www.skypack.dev/, eg https://cdn.skypack.dev/preact@10.5.5


## data transformation
dataweave by mulesoft (has DSL)
- https://docs.mulesoft.com/dataweave/1.2/dataweave-examples
- https://github.com/mulesoft-labs/data-weave-cli
datasonnet (has DSL)
- https://datasonnet.github.io/datasonnet-mapper/datasonnet/latest/quickstart.html
jolt (defined in JSON)
- https://github.com/bazaarvoice/jolt


## SVG to data URI
https://jsfiddle.net/yyvbqpxL/1/

## T2S beatboxing
https://simulationcorner.net/index.php?page=sam
Input: Bqr.qrff.Bqr.qrff.Bqr.qrff.szs.qrff.szse.Baoo.da.ba.sha.tra....Bqr.qrff.Bqr.qrff....boi...
Input: xrl ll iiII IIII. II. I vriiit mrrrrkkk. Xkreeee. Xkruu.

## would like to do a 3D version of this as an example for fiug
[Legend Of Zelda Fan Art](https://dribbble.com/shots/14564003-Hylian-Crest-Legend-of-Zelda-fan-art)
[Making of ...](https://www.linkedin.com/posts/tatiana-bischak-20575448_illustration-legendofzelda-nintendo-ugcPost-6847153376778559488-W75S)


What if the running instance of fiug were considered a remote?  To change running instance, push to that remote:
[git push to different remote](https://stackoverflow.com/questions/5181845/git-push-existing-repo-to-a-new-and-different-remote-repo-server)

https://gist.github.com/xavierfoucrier/c156027fcc6ae23bcee1204199f177da


database
--------
https://www.liquibase.com/ - brings CI/CD/versioning to databases
https://www.prisma.io/ - ORM (like mongoose)
https://stackfame.com/knexjs-complete-tutorial - query builder
https://phiresky.github.io/blog/2021/hosting-sqlite-databases-on-github-pages/

discord gitter etc
------------------

[youtuber + discord + zapier](https://gist.github.com/methdev/2e82914189c072231855002ccd21f18c)
https://andyczerwonka.com/discord-for-software-development-teams-34eb025d6440
https://gitter.im/crosshj/Lobby


computer history
----------------
how I started with computers [Commodore VIC-20](https://youtu.be/yg04GyhS3ss?t=739)


ui ux mockup tools
------------------
- https://alternativeto.net/software/invision/
- https://alternativeto.net/software/uxpin/
- https://alternativeto.net/software/zeplin/
- https://alternativeto.net/software/balsamiq-mockups/
- https://www.proofhub.com/articles/invisionapp-alternatives


regex, regular expression, regexp
---------------------------------
- [build regex from text](https://regex-generator.olafneumann.org/)


fonts
-----
- [create and edit truetype fonts](https://www.online-tech-tips.com/computer-tips/how-to-create-your-own-fonts-and-edit-truetype-fonts/)


Cognitive Behavior Therapy
--------------------------
[Two Easily Remembered Questions That Silence Negative Thoughts | Anthony Metivier](https://www.youtube.com/watch?v=kvtYjdriSpM)

Are my thoughts useful?
How do they behave?

applied to software development:
Is this feature useful?
How does it behave?


random
------
- waiting is not a problem; waiting with desire to move forward is a problem
- measure code change as risk, but shouldn't this also map to AST branch change (loose question)


personal information store
--------------------------
- I have information all over the place: bookmarks(favorites), likes, notes, email, recordings, gists
- I'd like to have a way to search and organize all of that
- as an extension, I consider a web search and the resulting threads a matter of personal information
	- make it easy to search and follow threads and come back later to it
	- see MARKETING.md/Mindmap | Knowledge Management Tool

image processing
----------------
- image clustering
	- keep a bunch of pictures as one file
	- disassembling: superpixels in javascript - https://github.com/kyamagu/js-segment-annotator/blob/master/js/image/segmentation/slico.js
	- assembling/packing: https://github.com/mapbox/potpack
	- image segmentation - https://www.youtube.com/watch?v=ZF-3aORwEc0
	- kinda what I had in mind here - https://www.pureref.com/
		- image references
		- image searching

- images with extra data
	- extra: 3d data, notes, etc
	- https://medium.com/better-programming/hide-data-within-an-image-507f571aab89
	- https://github.com/exif-js/exif-js
	- probably should wait until hex viewer is in place before going really far with this


2020-09-30 shaders webgl
------------------------
- http://webglplayground.net/ - I like the way source is handled here; divided into meaningful sections
- shadertoy
- fragment and vertex shaders - would like to support previews of these

2020-09-19 settings
-------------------
- settings view could be the first example of preview iframe that interacts with rest of the app
- settings should be a json file with .settings extension
- this should not be hidden at first, but may be later
- preview should be html that is loaded in iframe
- iframe should message the external app
- message should be heard by service worker handler and affect app settings
- these settings are used to update settings file (and consequentially, the html file)


2020-09-17 LOOSE
----------------
- demo driven development, versus ticket or changelog driven
- delivery versus debt (false dichotomy?)


2020-08-16 Note and Musing
==========================
- THIS SUCKS:  I am manually updating files and refreshing all the time

#### distractions | focus | procrastination
- lot's of things suck and need improved
- many things are cool and not big impact but fun to work on
- anxiety about first item and pain relieving effect of second item

### browsersysnc integration
- http://localhost:3222/browser-sync/browser-sync-client.js
- https://www.browsersync.io/docs/options/#option-socket
- https://www.google.com/search?q=browsersync+without+websocket+polling
- https://github.com/BrowserSync/browser-sync/issues/684#resolving_polling_url
- https://github.com/BrowserSync/browser-sync/issues/599#option-to-stop-polling


TIME AS MONEY
=============

- rephrase all tasks in terms of money and/or time
	- started work on Bartok on March 15, 2020
	- hourly pay rate ~=
	- average amount of time per day on bartok ~=

- how much would I pay to use bartok (trick question)?
- how much would you have to pay me to use bartok (trick question)?


Service Worker
==============

- chrome://serviceworker-internals/
- https://developers.google.com/web/fundamentals/primers/service-workers/high-performance-loading
- https://developers.google.com/web/fundamentals/instant-and-offline/offline-cookbook
- cache - https://hasura.io/blog/strategies-for-service-worker-caching-d66f3c828433/
- https://blog.codecentric.de/en/2019/09/service-workers-tricks-traps/
- events - https://w3c.github.io/ServiceWorker/#execution-context-events

- lifecycle picture - https://www.digitalocean.com/community/tutorials/demystifying-the-service-worker-lifecycle
- lifecycle picture - https://hasura.io/blog/strategies-for-service-worker-caching-d66f3c828433/

- https://www.oreilly.com/library/view/building-progressive-web/9781491961643/ch04.html#note_sw_controlling_after_load

- stream from service worker - https://developers.google.com/web/updates/2016/06/sw-readablestreams

- websocket from service worker?

## serverless framework and aws lambdas
- https://github.com/Dynobase/serverless-dynamodb-api-boilerplate
- associated article => https://dynobase.dev/dynamodb-serverless-framework/
- https://www.serverless.com/
- https://docs.aws.amazon.com/cdk/latest/guide/home.html
- https://d1.awsstatic.com/whitepapers/architecture/AWS-Serverless-Applications-Lens.pdf



UNSORTED
========

- https://thiscouldbebetter.github.io/ - lots of cool stuff here; I like this approach of trying everything
- https://gist.cafe/ - run code snippets on your server, embed in web
- how to implement a programming language
	- [http://lisperator.net/pltut/](http://lisperator.net/pltut/)
	- [http://angg.twu.net/miniforth-article.html](http://angg.twu.net/miniforth-article.html) - bootstraping a forth in 40 lines of Lua

- https://www.x3dom.org/
- http://create3000.de/x_ite/getting-started/#xhtml-dom-integration
- https://docs.stackery.io/docs/quickstart/quickstart-nodejs/

- may be useful with all the stringifying - https://github.com/jsbin/jsbin/blob/master/public/js/vendor/stringify.js

- https://react-live.netlify.app/

- https://observablehq.com/
- https://bl.ocks.org/
	- https://bl.ocks.org/mbostock/11357811 - Wilson's algorithm (maze generation)
- http://www.biofabric.org/gallery/pages/SuperQuickBioFabric.html

- https://stackoverflow.com/questions/51549390/how-to-disable-third-party-cookie-for-img-tags

- https://wall.alphacoders.com/search.php?search=fractal

- http://unikernel.org/projects/ - would be cool if services were compiled to unikernels


- inspiration
	- https://github.com/hundredrabbits/Orca
	- https://jspaint.app/
	- https://www.windows93.net/
	- https://windows96.net/
- not inspiration, but very similar use case
	- https://azure.microsoft.com/en-us/resources/videos/building-web-sites-with-visual-studio-online-monaco/
- mvc/architectural/BS stuff:
	- https://mvc.givan.se/ -
	- New Jersey vs MIT - https://news.ycombinator.com/item?id=12065570
	- https://en.wikipedia.org/wiki/Worse_is_better

- https://picolabs.atlassian.net/wiki/spaces/docs/pages/1189992/Persistent+Compute+Objects

- https://www.html5rocks.com/en/tutorials/file/filesystem-sync/

- SVG Editor - https://github.com/SVG-Edit/svgedit
- SVG Optimize - http://petercollingridge.appspot.com/svg-editor
- SVG URL Encoder (for CSS) - https://yoksel.github.io/url-encoder/
- SVG minifier - https://www.svgminify.com/
- SVG loading spinners - https://loading.io/spinner/
- Font To SVG Path: https://danmarshall.github.io/google-font-to-svg-path/
- SVG Path Editor: https://yqnn.github.io/svg-path-editor/

- ascii text
- http://patorjk.com/software/taag/#p=testall&f=Graffiti&t=notes

- ascii from pic
- https://www.ascii-art-generator.org/


memory usage and performance
============================
- https://auth0.com/blog/four-types-of-leaks-in-your-javascript-code-and-how-to-get-rid-of-them/
- https://github.com/paulirish/memory-stats.js/blob/master/memory-stats.js
- https://web.dev/monitor-total-page-memory-usage/


fugue: (the UI portion of the bartok ecosystem)
===============================================
components:
- dom: init dom, change/update dom
	- https://micro-frontends.org/ - custom components, etc
- listeners: process event, call some update function that dom has passed
- triggers/actions: user interacting with dom causes system event to be fired
- state?

web assembly
============
- https://www.toptal.com/virtual-reality/assemblyscript-and-webassembly-tutorial
- wasm in-browser
	- https://play.rust-lang.org/
	- https://wasdk.github.io/WasmFiddle/
	- https://webassembly.studio/
- many languages using wasm - https://stackoverflow.com/a/47483989
- many languages wasm - https://github.com/appcypher/awesome-wasm-langs
- https://hacks.mozilla.org/2018/10/webassemblys-post-mvp-future/
- implicit http caching, streaming - https://v8.dev/blog/wasm-code-caching
- https://webassembly.sh/
- https://wapm.io/
- https://wapm.io/package/JeremyLikness/wasi-ubasic
- create a map of wasm tech
	- wasmtime / wasi
	- wasmer - https://github.com/wasmerio/wasmer
	- emscripten
	- https://wiki.nikitavoloboev.xyz/web/webassembly
	- wabt vs binaryen
	- https://github.com/appcypher/awesome-wasm-runtimes - seems very server bound
- https://engineering.q42.nl/webassembly/ (assemblyscript plus webgl)
- https://madewithwebassembly.com/ (showcase)

web workers
===========
- this is a pattern I would like to be able to take for granted
- https://github.com/crosshj/experiments/commit/3a782bfe4e6b2184b5c5fbac204068f24f33aece
- https://github.com/crosshj/experiments/blob/gh-pages/svg/engine-src/expressionEngine.js#L211
- https://github.com/crosshj/experiments/blob/gh-pages/rangers.advent/rangers.advent.js#L507
- https://github.com/crosshj/experiments/blob/gh-pages/encryt-web-worker/index.html#L63

- paint worklet: https://developers.google.com/web/updates/2018/01/paintapi
- https://bitsofco.de/web-workers-vs-service-workers-vs-worklets/


webgpu
======

- https://06wj.github.io/WebGPU-Playground/#/Samples/HelloCanvas


visual studio code insiders
===========================

- https://vscode-web-test-playground.azurewebsites.net/?enter=true

animation
=========

- bodymovin / lottie-web - https://codepen.io/collection/nVYWZR/

fantasy consoles
================

- https://script-8.github.io/
- https://www.lexaloffle.com/pico-8.php
- https://discord.gg/sFeDxWK (fantasy consoles)
- https://github.com/paladin-t/fantasy

pixel art
=========

- https://www.aseprite.org/

javascript module formats
=========================

- https://weblogs.asp.net/dixin/understanding-all-javascript-module-formats-and-tools

mod tracker
===========

- https://www.youtube.com/watch?v=j5K3D_40VhQ&list=PLZbQ5WGwsCLGOWSS9wC2iPUI-sGcF2Hpy

graphs on the fly
-----------------
- https://flowchart.fun/ - I love the way they do it
- a ton more at this HN discussion - https://news.ycombinator.com/item?id=26303784


# toObject for a class with getters
- [example](https://www.typescriptlang.org/play?#code/MYGwhgzhAEBCkFNoG8BQBIAZpYYAmCA-AFzQQAuATgJYB2A5gNoC6GoA9rUgLzQAUAB0rsBEEmSp0mzAJTRuAPmgApAMoB5AHIA6AWEoQEfNVu0UaDapgCefcgAtqEADTQhIiDJmoM5dic15fjlFaAcnbWwIXAJCbUoEPABXYCM+diTyYjBaa1d3AWJzKRClNHR0DPJGAuYgu0cYSGgc6xka4QFWCoTyJMpaaCqMAF9XZBHvEZ9QSBgAWXZgAGtoBAAPcgRaPBh4QxQMKJieaEYAcjwwLfPXc8ocvHYAW1voc9p2cgBRdadyc7degIcjQK5bPgycroXr9QZcADu0AAItcjDJtH4AJIaVSSBiQswCEDUch8ABEABVye0AAzdaboYGgh47F6Q6GwgbQebXezxR7s7zoRmfH5-CiQw49EFw96Ydjsc6jVDTVDATgUaCYYQAL22QURPKWy0hAG4fAB6S0a2gQdggBDaEDseh8dQAIwAVghgORtMz1AjaAAFToISjkazIhDRGgCPwGPiLFa6YR+KMCBBeGaah1Ol1ugJmfH0Ky2HXsfW0Vy0JIgECuABMOaAA)

# langauge features I am curious about
- specs (clojure) https://clojure.org/guides/spec
- transducers (clojure) https://www.youtube.com/watch?v=4KqUvG8HPYo




### boxes and wires
- https://reactflow.dev/
- https://crosshj.com/experiments/svg/


# keyboard shortcuts | hotkeys
- http://aka.ms/vscodekeybindings

# data transformation | tools
- https://jsonata.org/
- jsonpath (and others?) - https://news.ycombinator.com/item?id=19949240
- https://github.com/antonmedv/fx
- https://github.com/stedolan/jq

# use of img vs css background to display picture on page
[stack overflow post about this](https://stackoverflow.com/questions/492809/when-to-use-img-vs-css-background-image)
> this seems like a situational smell to me, there's no consensus
> I find it frustrating

# wet codebase
[video](https://www.deconstructconf.com/2019/dan-abramov-the-wet-codebase)
- I watch all of these with a resentment that tempers my ability to consume them
- there is a base premise: I know what I am talking about and this is THE way to do this or to think in general
- nuance is lost and all of the solutions come with their own associated problems

## All the Little Things | Sandi Metz | RailsConf 2014
[video](https://www.youtube.com/watch?v=8bZh5LMaSmE)
- wrapping final solution in OO is premature

## Minimal API Surface Area | Sebastian Markbage | JSConf EU 2014
[video](https://www.youtube.com/watch?v=4anAwXYqLG8)
- why do people use javascript?
	- agree with ubiquity, but there is more
	- overhead to using other languages
	- all languages get it wrong about what matters to their users, even JS
	- JS is extensible enough, usable enough, etc.  edges others out
	- see https://github.com/crosshj/experiments/tree/gh-pages/simple_c/homeworkJS

## On the Spectrum of Abstraction | Cheng Lou | react-europe 2016
[video](https://www.youtube.com/watch?v=mVVNJKv9esE)
- side note: are all abstraction issues boiled down to files vs folders issues?
	- should I create one file that has everything in it and ask reader to scroll down?
	- should I have a folder that contains tons of files that are short?
- I like the graphs that are used in these slides
- cost of using declarative DSL versus procedure/imperative
- power vs utility
- utility of constraints


# milestones
[first commit](https://github.com/crosshj/experiments/commit/6292251303faf84243b30c20c8770f6f73372459)
