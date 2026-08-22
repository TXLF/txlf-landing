{{- /*
  MARKDOWN output for a single page: the page's own markdown source, with a
  small YAML front matter block so an agent can identify the page without
  parsing prose. Published alongside the HTML at <page>/index.md.
*/ -}}
---
title: {{ .Title | jsonify }}
url: {{ .Permalink | jsonify }}
{{ with .Description }}description: {{ . | jsonify }}
{{ end -}}
{{ if not .Date.IsZero }}date: {{ .Date.Format "2006-01-02" }}
{{ end -}}
{{ with .Params.tags }}tags: {{ . | jsonify }}
{{ end -}}
site: {{ .Site.Title | jsonify }}
---

# {{ .Title }}

{{ .RawContent }}
