# Website

This website is built using [Docusaurus 2](https://docusaurus.io/), a modern static website generator.

## Development

### Generating the MDX files

From `packages/tools`, run `node website/processDocs.js --env dev`

### Getting the translations

```shell
CROWDIN_PERSONAL_TOKEN=..... yarn crowdinDownload
```

### Building the doc

From `packages/doc-builder`, run:

```shell
WEBSITE_BASE_URL=http://localhost:8077 yarn buildDev
```

Or to build a particular locale:

```shell
WEBSITE_BASE_URL=http://localhost:8077 yarn buildDev --locale fr
```

`processDocs.js` will also build everything by default, but it takes a long time, so using the above commands is convenient for dev.

## Translation

Translation is done using https://crowdin.com/

## Building for production

This is done in `release-website.sh` from the repository https://github.com/joplin/website/
