{{- $dateFormat := .Site.Params.dateFormat -}}
{{- if not $dateFormat -}}{{- $dateFormat = "2006-01-02" -}}{{- end -}}
+++
title = "{{ replace .Name `-` ` ` | title }}"
date = "{{ now.Format $dateFormat }}"
tags = []
categories = []
imgs = []
toc = true
comments = false
justify = false  # text-align: justify;
license = ""  # CC License
draft = true
+++

