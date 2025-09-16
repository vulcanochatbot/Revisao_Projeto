# CITATION_GUIDE.md

## Campos mínimos (CFF 1.0.1):

- `cff-version: 1.0.1`

- `title` claro

- `authors` como lista (`- given-names` / `family-names` ou `- name`)

- `license`: "MIT"

- `version`: "0.1.0"

- `date-released`: "AAAA-MM-DD"

- `repository-code`: **entre aspas**, "https://github.com/<owner>/<repo>"

### Recomendados:

- `message` (frase curta de citação)

- `keywords` (lista)

## Template válido:

```yaml
cff-version: 1.0.1
message: "Se usar este projeto, por favor cite assim:"
title: "<TÍTULO>"
authors:
  - given-names: "<Nome>"
    family-names: "<Sobrenome>"
repository-code: "https://github.com/<owner>/<repo>"
license: "MIT"
version: "0.1.0"
date-released: "2025-09-16"
