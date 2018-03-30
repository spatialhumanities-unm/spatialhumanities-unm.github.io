---
layout: default
title: Spatial Humanities Working Group Schedule
css: spatial-humanities
---

<div class="row col-sm-12">
	<h1>Spring 2018 Events</h1>
	<p>We usually meet on Fridays from 3:30 to 5, but feel free to arrive late or leave early as your schedule permits. While we encourage everyone to participate in the conversation, you are more than welcome to simply hang out and listen!</p>
	<p>Many of our events discuss a pre-circulated paper, but don't be afraid to turn up even if you haven't had a chance to read it. When available, links to download the paper should be clearly visible beneath the abstract.</p>
</div>

<div class="row col-sm-12">
	<h1 class="orange">Next Meeting</h1>
</div>

{% for event in site.data.events.2018-spring %}

{% if event.next == true %}

<div class="row row-talk next-meeting">

<div class="col-xs-12 text-xs-left col-sm-3 text-lg-right">
	<div class="month">{{event.month}}</div>
	<div class="day">{{event.day}}</div>
	<div class="weekday">{{event.weekday}}</div>

	<div class="time">{{event.time}}</div>
	<div class="place">{{event.place}}</div>

	{% if event.image-name != nil %}
		<a href="images/{{event.image-name}}" data-lightbox="{{event.person}}" data-title="{{event.person}} poster">
			<img src="images/{{event.image-name}}" width="100%" class="talk-poster">
		</a>
	{% endif %}

</div>

<div class="talk-desc col-sm-8">
<div class="month">&nbsp;</div>

  <h2 class="person">{{event.person}}</h2>
	<div class="time">{{event.department}}</div>
	<div class="place">{{event.affiliation}}</div>

	<h3 class="title">{{event.title}}</h3>
	<h4 class="subtitle">{{event.subtitle}}</h4>

	<p class="abstract">{{event.abstract | markdownify }}</p>

	{% if event.paper-links != nil %}
		{% for paper in event.paper-links %}
			<div class="download"><a href="{{paper[1]}}">{{paper[0]}}</a></div>
		{% endfor %}
	{% endif %}

</div>

</div> <!-- end row -->

{% endif %}
{% endfor %}



<div class="row">
	<h1>Future Events</h1>
</div>

{% for event in site.data.events.2018-spring %}

{% if event.upcoming == true and event.next == false  %}
<div class="row row-talk">

<div class="col-xs-12 text-xs-left col-sm-3 col-lg-3 text-lg-right">
	<div class="month">{{event.month}}</div>
	<div class="day">{{event.day}}</div>
	<div class="weekday">{{event.weekday}}</div>

	<div class="time">{{event.time}}</div>
	<div class="place">{{event.place}}</div>

</div>

<div class="talk-desc col-xs-9">
<div class="month">&nbsp;</div>

	<h2 class="person">{{event.person}}</h2>
	<div class="time">{{event.department}}</div>
	<div class="place">{{event.affiliation}}</div>
</div>

</div> <!-- end row -->

{% endif %}
{% endfor %}


<div class="row">
	<h1>Previous Events</h1>
</div>

{% for event in site.data.events.2018-spring %}

{% if event.upcoming == false and event.next == false  %}
<div class="row row-talk next-meeting">

<div class="col-xs-12 text-xs-left col-sm-3 text-lg-right">
	<div class="month">{{event.month}}</div>
	<div class="day">{{event.day}}</div>
	<div class="weekday">{{event.weekday}}</div>

	<div class="time">{{event.time}}</div>
	<div class="place">{{event.place}}</div>

	{% if event.image-name != nil %}
		<a href="images/{{event.image-name}}" data-lightbox="{{event.person}}" data-title="{{event.person}} poster">
			<img src="images/{{event.image-name}}" width="100%" class="talk-poster">
		</a>
	{% endif %}

</div>

<div class="talk-desc col-sm-8">
<div class="month">&nbsp;</div>

  <h2 class="person">{{event.person}}</h2>
	<div class="time">{{event.department}}</div>
	<div class="place">{{event.affiliation}}</div>

	<h3 class="title">{{event.title}}</h3>
	<h4 class="subtitle">{{event.subtitle}}</h4>

	<p class="abstract">{{event.abstract | markdownify }}</p>

</div>

</div> <!-- end row -->


{% endif %}
{% endfor %}
