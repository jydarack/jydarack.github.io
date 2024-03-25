---
layout: page
title: Reading stats
permalink: /stats/
---
{% assign startyear = site.startyear %}
{% assign latestyear = site.time | date: "%Y" %}
{% capture latestupdate %} {{site.time | date: "%Y" }}-{{site.time | date: "%j" | plus: 7 | prepend: '000' | slice: -3, 3 | to_a }} {% endcapture%}

{% assign post_dates = "" | split: ',' %}
{% for post in site.posts %}
{% assign post_date = post.date | date: "%Y-%j" | to_a %}
{% assign post_dates = post_dates | push: post_date %}
{% endfor %}

<div class="waffle-reading">
{% for cur_year in (startyear..latestyear) reversed %}
    {% assign num_days = 365 %}
    {% assign leap_years = "2016, 2020, 2024, 2028, 2032" | split: ", " %}
    {% if leap_years contains cur_year %}
        {% assign num_days = 366 %}
    {% endif %}
    {% assign old_month = 0 %}
    {% assign cur_month = 1 %}

<h2>{{cur_year}}</h2>
    <div class="year-waffle">
        <div class="month-waffle">

    {% for cur_day in (1..num_days) %}
        {% capture cur_date %} {{cur_year}}-{{cur_day | prepend: '000' | slice: -3, 3}} {% endcapture%}
        {% assign cur_date = cur_date | date: "%Y-%j" | to_a %}
        {% assign cur_month = cur_date | date: "%m" | plus: 0 %}

        {% if cur_month != old_month %}
            {% if cur_month != 1 %}
                </div>
                <div class="month-waffle">
            {% endif %}
            {% capture day_offset %} {{cur_year}}-{{cur_month}}-01 {% endcapture %}
            {% assign day_offset = day_offset | date: "%Y-%m-01" | date: "%u" | plus: -1 %}
            {% for ofs in (1..day_offset) %}
                <div class="daily placeholder">&nbsp;</div>
            {% endfor %}  
            
            {% assign old_month = cur_month %}
        {% endif %}

        {% if post_dates contains cur_date %}
            <div class="daily published">&nbsp;</div>
        {% else %}
            <div class="daily">&nbsp;</div>
        {% endif %}

        {% if cur_date == latest_update %}
            {% break %}
        {% endif %}
        
    {% endfor %}
        </div>
    </div>
{% endfor %}
</div>