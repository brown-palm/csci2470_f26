---
layout: page
title: Staff
description: A listing of all the course staff members.
nav_exclude: false
---

## Instructor

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

## Graduate TA

{% assign graduate_tas = site.staffers | where: 'role', 'Graduate TA' %}
{% for staffer in graduate_tas %}
{{ staffer }}
{% endfor %}

## Head TA

{% assign htas = site.staffers | where: 'role', 'Head TA' %}
{% for staffer in htas %}
{{ staffer }}
{% endfor %}


{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}


## Teaching Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}