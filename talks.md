---
layout: default
title: Talks
---

# Talks
I have given several talks at various conferences and meetups in India and globally in the USA, France and UK. If you want me to speak at your event, please reach out to me at [sharma[dot]atulpriya[at]gmail[dot]com]

Below is a list of my recent talks, grouped by year.

{% assign talks_by_year = site.data.talks | group_by: "year" | sort: "name" | reverse %}
{% for year_group in talks_by_year %}
## {{ year_group.name }}
<div style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: center; margin-top: 20px;">
  {% for talk in year_group.items %}
  <div style="flex: 0 1 calc(50% - 20px); box-sizing: border-box; border: 1px solid #e0e0e0; border-radius: 8px; overflow: hidden; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); text-align: left; background-color: #fff; transition: transform 0.2s ease-in-out; margin-bottom: 20px;">
    <a href="{{ talk.url }}" target="_blank" style="text-decoration: none; color: inherit;">
      <img src="{{ talk.thumbnail }}" alt="{{ talk.title }}" style="width: 100%; height: auto;">
      <div style="padding: 10px;">
        <h4 style="font-size: 16px; margin: 5px 0; color: #333;">{{ talk.title }}</h4>
        <p style="font-size: 12px; color: #555; margin: 5px 0;"> {{ talk.event }}</p>
        <p style="font-size: 12px; color: #555; margin: 5px 0;">{{ talk.date }}</p>
      </div>
    </a>
  </div>
  {% endfor %}
</div>
{% endfor %}
