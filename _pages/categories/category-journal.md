---
title: "Journal"
layout: archive
permalink: categories/journal
author_profile: true
sidebar_main: true
---
{% assign posts = site.categories.Journal %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}