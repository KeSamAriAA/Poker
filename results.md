---
layout: default
title: Résultats
permalink: /results.html
---

# Résultats de Poker

{% for year in site.data.results %}
  ## {{ year[0] }}
  {% for month in year[1] %}
    ### {{ month[0] | capitalize }}
    <table>
      <thead>
        <tr>
          <th>Date</th>
          <th>Stakes</th>
          <th>Profit</th>
        </tr>
      </thead>
      <tbody>
        {% for session in month[1].sessions %}
          <tr>
            <td>{{ session.date }}</td>
            <td>{{ session.stakes }}</td>
            <td>{{ session.profit }}</td>
          </tr>
        {% endfor %}
      </tbody>
    </table>
  {% endfor %}
{% endfor %}
