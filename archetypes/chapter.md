---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
weight: 10 # The smaller the higher position in the navigation and vice versa
tags: []
chapter: true
pre: "<b>X. </b>"
---

### Chapter X

# {{ replace .Name "-" " " | title }}



<!-- Content goes here -->




{{% button href="https://github.com/SpacehuhnTech/wiki/issues/new?title=Changes for {{ replace .Path "\\" "/" }}&body=I'd like to suggest changes for `{{ replace .Path "\\" "/" }}`%0A%0A:link: [Wiki](https://spacehuhn.wiki/{{ replace .Dir "\\" "/" }}{{ replace .TranslationBaseName "_index" "" }})%0A:link: [Source](https://github.com/SpacehuhnTech/wiki/blob/main/content/en/{{ replace .Path "\\" "/" }})%0A%0A<!-- Describe your desired changes -->" icon="fas fa-comment" %}}&nbsp;Suggest changes{{% /button %}}

{{% button href="https://github.com/SpacehuhnTech/wiki/blob/main/content/en/{{ replace .Path "\\" "/" }}" icon="fab fa-github" %}}&nbsp;Source{{% /button %}}