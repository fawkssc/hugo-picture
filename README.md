# Hugo Picture

Configurable Image processing for Hugo to build responsive images sets.

## `picture.html` Partial Usage

```html

{{- $sourceSet := slice -}}
{{- $sourceSet = $sourceSets | append (dict "Media" "[media-query]" "Processing" (slice (slice "Resize" "#x webp"))) -}}
{{- $sourceSet = $sourceSets | append (dict "Media" "[media-query]" "Processing" (slice (slice "Resize" "#x webp"))) -}}
{{- $sourceSet = $sourceSets | append (dict "Media" "[media-query]" "Processing" (slice (slice "Resize" "#x webp"))) -}}
{{ partial "picture.html" (dict "Resource" $resource "Page" . "SourceSets" $sourceSets -}}
```

### Options

- **Resource** - *(must define `Resource` or `Image`) The image Resource
- **Image** - *(must define `Resource` or `Image`) The name of the image resource to look up
- **Page** - The current context
- **SourceSets** - *(optional)* Array of optional sources for the resource
- **Loading** - *(optional | default: "lazy")* Image loading: "lazy" or "eager" 
- **Attrs** - *(optional)* Hash of attributes to use for the `picture` HTML element
