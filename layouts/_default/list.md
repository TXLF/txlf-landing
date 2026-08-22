{{- /*
  MARKDOWN output for a section or list page: the section's own markdown source
  followed by a link list of its pages.
*/ -}}
---
title: {{ .Title | jsonify }}
url: {{ .Permalink | jsonify }}
{{ with .Description }}description: {{ . | jsonify }}
{{ end -}}
site: {{ .Site.Title | jsonify }}
---

# {{ .Title }}

{{ with .RawContent }}{{ . }}

{{ end -}}
{{ with .Pages.ByDate.Reverse }}
## Pages

{{ range . }}- [{{ .Title }}]({{ .Permalink }})
{{ end }}{{ end -}}
