---
layout: default
meta-description: "Stanford Systems Seminar--Held Thursdays at 11 AM PST."
---

The **Stanford Systems Seminar** is an opportunity for Stanford students doing systems research to present their work to a larger audience and to invite guest speakers.
Seminars are held virtually on Thursdays at 11 AM PST.
The seminar is organized by [Deepti Raghavan](https://deeptir.me) and [Peter Kraft](http://petereliaskraft.net).
To receive regular updates on upcoming talks, as well as Zoom links to join them, please reach out to one of us so we can add you
to our mailing list (Stanford affiliates only).  Please also reach out to us if you are interested in presenting next quarter.

<!-- Read our blog post on our [why we're running this seminar]({{ site.baseurl }}/about). -->

{% for category in site.data.talks %}
# {{ category.type }}
<div class="talk-list">
  {% for talk in category.members %}
  <div class="talk list-group-item">
  <div class="talk-date">{{ talk.date }}</div>
  <div class="talk-presenter"><a href="{{ talk.website }}">{{ talk.speaker }}</a></div>
  {% if talk.title %}
  <div><span>{{ talk.title }}</span></div>
  {% endif %}
  {% if talk.abstract %}
    <details>
    <summary>Abstract</summary>
    {{ talk.abstract }}
    </details>
  {% endif %}
  {% if talk.biography %}
    <details>
    <summary>Bio</summary>
    {{ talk.biography }}
    </details>
  {% endif %}
  {% if talk.recording %}
    <a href="{{ talk.recording }}">Recording</a>
  {% endif %}
  {% if talk.livestream %}
    <a href="{{ talk.livestream }}">Livestream Link</a>
  {% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}
