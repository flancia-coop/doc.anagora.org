# Agora.yaml
**Agora.yaml** will be a standard for [[Agora federation]], intersecting with the [[Mycoverse]]. This is a file, served at `.well-known/agora.yaml` or available in an Agora-imported repository root. The latter is closer to the modern (may 2023) approach of Agora organisation. The former is supposed to make a totally new approach possible.

The document is a [[YAML]] document, describing:
- The name of the site
- Its URL schemes, including resources contributed to Agora home pages
- Mappings between local resources and canonical rendered views.
- Exclusions and inclusions (like [[robots.txt]])
- Transclusion policy
- Interwiki maps ~ intermaps
- Integration points (where and how to render each local resource in an Agora context, including executable code)

## Example document

This one is served 
```yaml
type: <garden|stream|stoa|agora>
name: <Agora of Flancia|Bouncepaw's digital garden>
include: <test>
exclude: <test>
repository_url: <url>
website_url: <url>
interwiki_map: []map
- interwiki:
    name: 
        - mycorrhiza
        - myco
    engine: mycorrhiza
    url: https://mycorrhiza.wiki
    mapping_url: <url>
mapping_type: <slug|literal|static>
mapping_template: https://mycorrhiza.wiki/%s
slug: <github|agora>
    
```

Another iteration (simpler):
```yaml
name: Example site
type: garden
mapping:
-
    names:
        - index
        - home
    type: article
    source_url:
        - https://example.org/index.myco
    rendered_url:
        - https://example.org/index.html
        - https://example.org/home.html
```

Sanitize [[html]].

Think about [[WebFinger]]? We could statically generate /webfinger, returning essentially the same mapping as above in webfinger format.

An older example contributed by [[bmann]]: #pull https://github.com/bmann/bmcgarden/blob/master/agora.yaml

#
- a [[feature]].
    - for [[Agora 2023]]
    - See also https://anagora.org/agora-yaml