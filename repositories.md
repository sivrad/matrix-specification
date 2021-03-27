# Matrix Repositories

## About

### Name Format

The format of a repository name is `matrix-<NAME>`.

## Repository List

| Name                                                | Type        | Description                                                                                                                                                                                          |
| --------------------------------------------------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`matrix-collection-template`](collection-template) | NPM Package | This is a template for creating a new collection. This could be automated but for the time being, creation of collections do not occur enough to justify building a tool to create a new repository. |
| [`matrix-schema`](schema)                           | JSON files  | This contains the JSON schemas for `./collection.json` and `./types/*.json`.                                                                                                                         |
| [`matrix-collection-cd`](collection-cd)             | NPM Package | Package that generates the Typescript classes before a collection is published.                                                                                                                      |

[collection-template]: https://github.com/sivrad/matrix-collection-template
[schema]: https://github.com/sivrad/matrix-schema
[collection-cd]: https://github.com/sivrad/matrix-collection-cd
