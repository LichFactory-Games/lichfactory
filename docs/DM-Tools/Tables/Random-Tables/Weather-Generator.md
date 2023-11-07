---
share: true
date: 2022-04-16
title: "Weather Generator"
tags:
  - worldbuilding
date created: Friday, November 3rd 2023, 2:35:58 pm
date modified: Saturday, November 4th 2023, 5:50:43 pm
---

> [!dice]+ Weather 
> 
> Temperature: `dice: [[Weather Generator#^temperature]]|Temperature`
> 
> Wind: `dice:[[Weather Generator#^wind]]|Wind`
> 
> Precipitation: `dice:[[Weather Generator#^precipitation]]|Precipitation`
^generator

| dice: 1d20 | Temperature                             |
| ---------- | ----------------------------------- |
| 1-14       | Normal for the season               |
| 15-17      | `dice: 1d4*10` F colder than normal |
| 18-20      | `dice: 1d4*10` F hotter than normal |
^temperature

| dice:1d20 | Wind        |
| --------- | ----------- |
| 1-12      | No Wind     |
| 13-17     | Light Wind  |
| 18-20     | Strong Wind |
^wind

| dice:1d20 | Precipitation       |
| --------- | ------------------- |
| 1-12      | No Rain             |
| 13-17     | Light precipitation |
| 18-20     | Heavy precipitation |
^precipitation
