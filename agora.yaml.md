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

```

An older example contributed by [[bmann]]: https://github.com/bmann/bmcgarden/blob/master/agora.yaml
```yaml
# unless in the include section, anything file without a .html or .md extension is excluded, 
# as are directories that begin with a period (.)
exclude:
    - _posts/archive/*
    - _ignore/*
    - notes.html
    - links.html
    - journal.html
    - ipfs-404.html
    - index.md
    - blog.html
    - archive.html
    - Gemfile*
    - README.md
    - tags.html
    - _includes/*
    - _layouts/*
    - feed/*

# instead of index.md or index.html in the root of your repo, this is showed as the "home" for your agora
home: _notes/agora.md

# the agora has certain metadata items. This lets front matter used in individual files get mapped to agora norms
frontmatter_mapping:
  git: [[git]]
  link: [[website]]
```

#
- a [[feature]].
    - for [[Agora 2023]]
    - See also https://anagora.org/agora-yaml