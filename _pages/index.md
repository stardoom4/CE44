---
layout: page
title: Home
id: home
permalink: /
---

<p style="padding: 2em 1em; background: #121212; border-radius: 4px;">
  Take a look at <span style="font-weight: bold">[[Notes]]</span> to get started.
</p>

<p><strong>Shinji Ikari</strong>: Ayanami! Are you all right? Ayanami! …Don’t ever say that! Just don’t say that you have nothing else! Just don’t say that! And don’t say goodbye when you leave for a mission, it’s just too sad. [sobs quietly]<br>
    <strong>Rei Ayanami </strong>: Why are you crying? I’m very sorry I don’t know what I should do or feel at a time like this.<br>
    <strong>Shinji Ikari</strong>: Why don’t you just try smiling?
    [Rei smiles]</p>
<details>
    <summary>Online Presence</summary>
    <a href="https://garud.netlify.app">Website</a><br>
    <a href="https://github.com/stardoom4">Github</a><br>
    <a href="https://letterboxd.com/Celestialentity/">LetterBoxd</a>
</details>

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
