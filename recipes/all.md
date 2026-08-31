---
layout: default
title: all recipes
---
{{ $path := .Get "path" }}
{{ $files := readDir $path}}

{{ range $files }}
  {{ if strings.HasSuffix .Name ".md" }}
    {{ .Name }}
  {{ end }}
{{ end }}
