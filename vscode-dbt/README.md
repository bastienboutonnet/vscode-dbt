# vscode-dbt

Provides snippets for dbt and Jinja functions in SQL, YAML, and Markdown.

Cool Tip: For a richer integration between dbt and vscode you should install [vscode-dbt-power-user](https://marketplace.visualstudio.com/items?itemName=innoverio.vscode-dbt-power-user) it does a **LOT** of cool stuff such as: code navigation between your models, completion aware of your dbt project, and much more. **dbt power user has a dependency on this extension so you'll also find my snippets in there! Give it a go!**

## Features

### Generic Jinja

`for` loops, conditionals, blocks, variable settings etc. See [source](./snippets/snippets_sql.json) for a full list

### dbt-SQL

`ref`, `source`, `log`, `config`, `snapshots`, `log` etc. See [source](./snippets/snippets_sql.json) for a full list.

### Model Overview

This snippet helps coders provide a high-level overview of every model in a standard way.

### YAML

`ref`, `source`, `var` etc. See [source](./snippets/snippets_yaml.json) for a full list.

### Markdown

`docs` definitions. See [source](./snippets/snippets_markdown.json) for a full list.

## Set-up

To enable support for these snippets when viewing a SQL, YAML, or Markdown file in Visual Studio Code, enter `Ctrl + K, M` (or `Ctrl + Shift + P` and search for "Change Language Mode").
Then select Jinja SQL, Jinja YAML, or Jinja Markdown respectively.

Alternatively, add the following to your Visual Studio Code settings in your dbt project:

```json
"files.associations": {
    "**/<dbt-project-dir>/**/*.yaml": "jinja-yaml",
    "**/<dbt-project-dir>/**/*.yml": "jinja-yaml",
    "**/<dbt-project-dir>/**/*.sql": "jinja-sql",
    "**/<dbt-project-dir>/**/docs/**/*.md": "jinja-md"
}
```

If snippet suggestions still do not work after selecting the appropriate language, try adding the following configuration to you Visual Studio Code project settings:

```json
"editor.quickSuggestions": {
    "strings": true
}
```

## Known Issues

Using the Jinja YAML language for YAML files changes the default comment style from YAML (`#`) to Jinja style (`{# #}`), which can cause YAML syntax errors.
Likewise, using the Jinja Markdown language on Markdown files changes the default comment style from Markdown (`<-- -->`) to Jinja style.

## Credits

### dbt jinja concepts

adapted from https://github.com/fishtown-analytics/atom-dbt/blob/master/snippets/dbt-sql.cson

### Jinja Concepts

adapted from https://github.com/danielchatfield/atom-jinja2/blob/master/snippets/atom-jinja2.cson
and https://github.com/fishtown-analytics/atom-dbt/blob/master/snippets/dbt-jinja.cson

## Release Notes
