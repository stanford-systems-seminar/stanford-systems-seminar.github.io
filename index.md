---
layout: default
meta-description: "Stanford Systems Seminar--Held Tuesdays at 4 PM PST."
---

The **Stanford Systems Seminar**, sponsored by [Platform Lab](https://platformlab.stanford.edu/), is an opportunity for Stanford faculty and students working in systems to present their research and invite guest speakers.
Seminars are held in-person/hybrid on Tuesdays in the Gates Fujitsu Room (Gates 403) at 4 PM PST, with an online option on Zoom.  Food is provided.
The seminar is organized by [Priya Mishra](https://priya2698.github.io/) and [Anjiang Wei](https://cs.stanford.edu/~anjiang/).
To receive regular updates on upcoming talks, as well as Zoom links to join them virtually, please [subscribe via mailman](https://mailman.stanford.edu/mailman/listinfo/platformlab). Please also reach out to us if you are interested in presenting.

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

Credit to the [Stanford MLSys Seminar Series](https://mlsys.stanford.edu/) for the site theme!
