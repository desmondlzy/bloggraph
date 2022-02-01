---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
type: publications
summary: "A wonderful paper."
thumbnail: 
paper: "url-to-your-paper.pdf"
venue: 
  name: SIGGRAPH 2022
  url: to-publisher-website
  note: conditionally accepted
authors:
  - name: Foo, Bar
    affiliations: [1, 2]
    url: https://desmondlzy.me

affiliations:
  - name: University of Foo
    url: https://foo.edu
  - name: Institute of Bar
    url: https://bar.org
---
{{< numbering h2=false h3=false >}}
{{< publication/information >}}

## Your content here.

In this work, we present a...