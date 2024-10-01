---
layout: page
title: Schedule
permalink: /schedule/
description: Stay updated with the University of South Carolina women's rugby schedule. Find upcoming games, locations, and opponents, and never miss the action.
---
  <div class="posts">
    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th>Date & Time</th>
                    <th>Opponent</th>
                    <th>Location</th>
                </tr>
                <tbody>
                    {% for game in site.games %}
                    <tr>
                      <td>{{ game.date | date: "%B %d, %-I:%M %p" }}</td>
                      <td>{{ game.opponent }}</td>
                      <td>{{ game.location }}</td>
                    </tr>
                    {% endfor %}
                </tbody>
            </thead>
        </table>
    </div>
   </div>