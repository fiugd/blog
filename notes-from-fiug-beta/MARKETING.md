*A cloud service you don't have to register for.*
*The editor / IDE you didn't have to install.*
*A tool that could change the way you work.*

## Introduction
* fiug does(will do) things that other things do.
* Consequently, one may think fiug IS one of those things.
* Possibly, fiug can be used as one of those things.
* However, it may not be that thing and that is not the sole vision for it.
* Consider the following an exploration of what fiug is and will be.

## TL;DR
* fiug takes inspiration from all of the following in some regard
* fiug will most likely not do any one of these things as well as any one of these do

## Fiug (IS | IS NOT)

### Editor | IDE
- modify and manage files sometimes with other integrations/features
- examples
	- [vscode](https://code.visualstudio.com)
	- [sublime](https://www.sublimetext.com)
	- [Eclipse Theia](https://eclipsesource.com/technology/eclipse-theia)
	- [Light Table](http://lighttable.com)
	- [atom](https://atom.io)
	- [brackets RIP](http://brackets.io)

### IDE | Playground | Code Runner
- online editor and web-based code share/run
- [wiki source code playgrounds](https://en.wikipedia.org/wiki/Comparison_of_online_source_code_playgrounds)
- examples
	- [jsfiddle](https://jsfiddle.net/)
	- [plunker](https://plnkr.co/)
	- [codepen](https://codepen.io/)
	- [stackblitz](https://stackblitz.com/)
	- [runkit](https://runkit.com/)
	- [replit](https://replit.com/)
	- [glitch](https://glitch.com/)
	- [observables](https://observablehq.com/)
	- [iodide.io](https://github.com/iodide-project/iodide)
	- [jupyter notebook hosts](https://www.dataschool.io/cloud-services-for-jupyter-notebook/)
	- [codeframe](https://codeframe.co/)
	- [slingcode](https://slingcode.net/)
	- [codefence](https://codefence.io/)
	- [tio](https://tio.run/#)

### Nocode platform / Multiexperience Development Platforms (MXDP)
- examples
	- [outsystems](https://www.outsystems.com/)
	- [webflow](https://webflow.com/)
	- [airtable](https://airtable.com/)
	- [bubble.io](https://bubble.io/)
	- [kintone](https://www.kintone.com/)

### Mindmap | Knowledge Management Tool
- examples
	- [dendron](https://dendron.so)
	- [roam](https://roamresearch.com/)
	- [athens](https://athensresearch.github.io/athens/)
	- [foam](https://github.com/foambubble/foam)
	- [vs code memo](https://github.com/svsool/vscode-memo)

### Continuous Integration Tool
- code, build, deployment automation
- examples: jenkins, teamCity, bamboo, circleCI, travisCI

### ALM
- application lifecycle management
- examples: many solutions all mostly unknown; difficult to find good examples by name

### APM
- application performance management
- examples: weavescope, splunk, datadog, kubernetes dashboard, ELK/EFK/Kibana

### Editor Extension
- examples
	- [codeswing](https://github.com/codespaces-contrib/codeswing)

### XaaS

> X as a service

- SaaS
	- software as a service
	- examples: Google Apps, Dropbox, Salesforce, Cisco WebEx, Concur, GoToMeeting
- PaaS
	- platform as a service
	- examples: Azure, Heroku, Google App Engine, Stratos, OpenShift
- FaaS
	- functions as a service
	- examples: Amazon Lambda, Google Cloud Functions, Azure Functions, IBM Cloud Functions
- IaaS
	- infrastructure as a service
	- examples: DigitalOcean, Linode, Rackspace, AWS, Azure, Google Compute Engine
- CaaS
	- containers as a service (containers and orchestration)
	- examples: Kubernetes, Docker Swarm, Mesos


### References
- [what is kubernetes](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/)
- [cloud architecture saas faas xaas](https://brainhub.eu/blog/cloud-architecture-saas-faas-xaas/)
- [paas and caas in 15 minutes](https://tanzu.vmware.com/content/intersect/paas-and-caas-in-15-minutes)


2020-08-24 thoughts about who customer is
=========================================
- new to programming
- average dev tired of BS
	- having to install to get started
	- mess of services spread all over the place
- creative type that wants to make music, games, or art
- blogger, note keeper, mind mapper
- presentation giver, conference speaker
- cloud dev ops
- teams or team builders that want it to be easy for any/all of the above


models for marketing similar software
=====================================
- [promlens](https://promlens.com/) - I enjoy both the look-and-feel of marketing AND the product itself


strategy
========

### prior art

Projects like VS Code or Eclipse Theia are already big, well-funded and bound to the use-case which they were designed for.

For example, I looked for easy ways to pull a tree view from many currently existing editors.  The difficulty I faced, I think, was due more to what I mentioned above than my own lack of understanding and capability (I am admittedly biased in this).  These projects are bound to the their paycheck and to the org structure of the teams that create them.

To be clear, Microsoft is not in the business of offering VS Code's components to developers; they are in the business of being the defacto editor that developers use.  Of course, Monaco, but not the rest of VS Code, afaict.


### user adoption

Editors and editor preference are bound to a scarcity model which inspires commitment from their users.  An editor has to be purchased, installed, and/or learned.

My goal is to create a system that has a very low cost to adopt; in fact, one that subverts adoption.  One of the reasons I turn to Chrome Developer tools and/or an index.html on my hard drive is that I prefer no-adopt where possible, even if I have already adopted.

Low barrier-to-entry, low adoption pressure and tight feedback loop are very important to me.  This tool is an extension of that workflow and philosophy, and not an app that is meant to be installed or adopted, per se.