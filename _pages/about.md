---
layout: about
title: about
permalink: /
subtitle: <a href="https://study.iitm.ac.in/ds/">DS, IIT Madras</a>

profile:
  align: right
  image: prof_pic.jpeg
  address:

news: false  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
---

Hi there! I’m Hamees, currently pursuing my BS at IIT Madras in Data Science and Applications. I work across speech, language, and applied scientific research, and I enjoy building things that actually make it into the real world. I’m also active in open source and spend a lot of time experimenting with models, tools, and ideas that push my understanding forward.

Outside tech, you’ll usually find me on a basketball court or reading manga. I also enjoy teaching and sharing what I learn along the way.


<div class="news">
            <h2>news</h2>
            {% if site.news  -%}
            <div class="table-responsive">
              <table class="table table-sm table-borderless">
              {%- assign news = site.news | reverse -%}
              {% for item in news limit: site.news_limit %}
                <tr>
                  <th scope="row">{{ item.date | date: "%b %-d, %Y" }}</th>
                  <td>
                    {% if item.inline -%}
                      {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
                    {%- else -%}
                      <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
                    {%- endif %}
                  </td>
                </tr>
              {%- endfor %}
              </table>
            </div>
          {%- else -%}
            <p>No news so far...</p>
          {%- endif %}
          </div>

