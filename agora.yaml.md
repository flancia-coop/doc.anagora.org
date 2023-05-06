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

```yaml
type: <garden|stream|stoa|agora>
name: <Agora of Flancia|Bouncepaw's digital garden>



```

An older example contributed by [[bmann]]: #pull https://github.com/bmann/bmcgarden/blob/master/agora.yaml

#
- a [[feature]].
    - for [[Agora 2023]]
    - See also https://anagora.org/agora-yaml