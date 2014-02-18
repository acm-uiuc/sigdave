---
layout: default
title: Sig Dave
---

# Blog Posts #
  <ul class="posts">
    {% for post in site.posts %}
      <li>
        <span>{{ post.date | date_to_string }}</span> &raquo;
        {% if site.baseurl == '/' %}
            <a href="{{ post.url }}">{{ post.title }}</a>
        {% else %}
            <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
        {% endif %}
      </li>
    {% endfor %}
  </ul>

# DJ Roomba #
<p><img src="{{ site.baseurl }}images/design.svg" alt="DJ Roomba Design" /></p>
## Pictures ##
<ul>
  <li><a href="{{ site.baseurl }}images/doomba.jpg">doomba</a></li>
  <li><a href="{{ site.baseurl }}images/sonotube.jpg">sonotube mounted</a></li>
</ul>

## TODO ##
- Write a wiimote joystick config for working with dj roomba
- Connect and test Port Expander
- Take pictures during meetings for easier documentation
### Storm Launcher ###
- convert camera feed to image stream
- ffmpeg to capture video feed
- analysis red dot trail to get distance estimates
- add swtich to laser dot
 - Check voltage of wire
