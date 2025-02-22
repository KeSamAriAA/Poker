---
layout: default
title: Résultats
---

# Résultats de Poker

{% for year in site.data.results %}
  ## {{ year[0] }}
  {% for month in year[1] %}
    ### {{ month[0] | capitalize }}
    <table>
      <tr>
        <th>Date</th>
        <th>Stakes</th>
        <th>Profit</th>
      </tr>
      {% for session in month[1].sessions %}
        <tr>
          <td>{{ session.date }}</td>
          <td>{{ session.stakes }}</td>
          <td>{{ session.profit }}</td>
        </tr>
      {% endfor %}
    </table>
  {% endfor %}
{% endfor %}
