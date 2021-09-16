---
title: Releases
layout: default
permalink: /releases/
---


<div style="width:100%;display:flex;flex-direction:row;justify-content: space-around; max-width: 60em; margin: 2em;">
		<div style="margin: 0 auto;line-height: 2em;width: 10em;">
				<div style="
		background: #d1d1a2; height: 5em; width: 100%; color: black; font-size: 1.2em; font-weight: bold; padding: 0.25em; margin-bottom: 0.5em;
">input freeform</div>
				<div style="line-height: 1.3em;">say anything.  dont't worry about if it gets done.  just make a note.</div>
		</div>
		<div style="margin: 0 auto;line-height: 2em;width: 10em;">
				<div style="
		background: #559bd4; height: 5em; width: 100%; color: black; font-size: 1.2em; font-weight: bold; padding: 0.25em; margin-bottom: 0.5em;
">judge priority</div>
				<div style="line-height: 1.3em;">does the observed contribute to overall progress and does it have to be done in order to keep the project moving</div>
		</div>
		<div style="margin: 0 auto;line-height: 2em;width: 10em;">
				<div style="
		background: #ce9178; height: 5em; width: 100%; color: black; font-size: 1.2em; font-weight: bold; padding: 0.25em; margin-bottom: 0.5em;
">work drive</div>
				<div style="line-height: 1.3em;">is there something about doing this that is interesting and worth tackling? can you do some small part of it to inspire movement forward?</div>
		</div>
		<div style="margin: 0 auto;line-height: 2em;width: 10em;">
				<div style="
		background: #95d1f1; height: 5em; width: 100%; color: black; font-size: 1.2em; font-weight: bold; padding: 0.25em; margin-bottom: 0.5em;
">complete summary</div>
				<div style="line-height: 1.3em;">can we learn from the progress made and what it took to get done? does this open the project to new possibilites?</div>
		</div>
</div>

<ul>
{% for release in site.releases %}
  <li><span>{{ release.date | date_to_string }}</span> &nbsp; <a href="{{ release.url }}">{{ release.title }}</a> - {{ release.category }} - {{ release.description }}</li>
{% endfor %}
</ul>
