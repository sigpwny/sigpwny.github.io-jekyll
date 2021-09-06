---
layout: page
title: Events
---

{% assign events = site.events | sort: "date" %}
{% for event in events reversed %}
- #### [{{ event.title }}]({{ site.baseurl }}{{ event.url }})
{% endfor %}

<h2 class="my-5 header"> Schedule </h2>
<hr/>
<br>
<p style="text-align:center"><iframe src="https://calendar.google.com/calendar/embed?height=600&wkst=1&bgcolor=%23ffffff&ctz=America%2FChicago&src=c2lncHdueUBnbWFpbC5jb20&color=%237CB342" style="border:solid 1px #777" width="800" height="600" frameborder="0" scrolling="no"></iframe></p>
