{{- /*
  MARKDOWN output for the home page: the home page's markdown source followed
  by every edition of the festival, so an agent that fetches a single file gets
  the whole site.
*/ -}}
---
title: {{ .Site.Title | jsonify }}
url: {{ .Permalink | jsonify }}
description: {{ .Site.Params.organization.description | jsonify }}
site: {{ .Site.Title | jsonify }}
---

# {{ .Site.Title }}

{{ .RawContent }}

## Past and upcoming events

{{ range (where .Site.RegularPages "Type" "in" .Site.Params.mainSections).ByDate.Reverse -}}
- [{{ .Title }}]({{ .Permalink }}) — {{ .Date.Format "January 2, 2006" }}
{{ end }}
## Site pages

{{ range .Site.RegularPages.ByTitle -}}
{{ if not (in $.Site.Params.mainSections .Type) -}}
- [{{ .Title }}]({{ .Permalink }})
{{ end -}}
{{ end }}
