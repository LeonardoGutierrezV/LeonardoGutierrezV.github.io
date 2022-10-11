---
layout: single
title: PowerPlatform Haks
excerpt: "Esta es una recopilación aleatoria de codigos utiles para PowerPlatform"
date: 2022-10-11
classes: wide
header:
  # teaser: /assets/images/uipath-plugin-install/logo.png
  teaser_home_page: true
  # icon: /assets/images/rpa_icon.png
categories:
  - Powerplatform
  - Powerautomate
  - Powerapps
tags:
  - Powerplatform
  - Powerautomate
  - Powerapps
---

### Fecha Powerautomate a Fecha numeríca Excel.

```json
div(sub(ticks(utcNow()),ticks('1899-12-31T00:00:00.0000000Z')),864000000000)
```
