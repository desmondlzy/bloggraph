---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
type: publications
summary: "A wonderful paper."
thumbnail: 
paper: "url-to-your-paper.pdf"
venue: 
  name: My Favorite Journal 2022
  url: to-publisher-website
  note: conditionally accepted
authors:
  - name: Wishes, Best
    affiliations: [1]
    notes: [1]
    url: https://desmondlzy.me
  - name: New Year, Happy
    affiliations: [1, 2]
    notes: [2]
    url: https://desmondlzy.me
notes:
  - sole first author
  - sole last author

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