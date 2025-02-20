---
title: defaultFrontEndConfig
description: A reference page for defaultFrontEndConfig
sidebar:
  order: 3
slug: 0.1.0-beta.4/config-reference/default-frontend-config
---

`defaultFrontEndConfig` is an object that is used to determine how the default dashboard routes should be rendered in `astroStudioCMS`. This is used to setup your user-facing front-end.

## Usage

```js title="astro.config.mjs" {2-9}
astroStudioCMS({
  defaultFrontEndConfig: {
    injectDefaultFrontEndRoutes: true,
    inject404Route: true,
    htmlDefaultLanguage: 'en',
    htmlDefaultHead: [],
    layoutOverride: './src/layouts/customLayout.astro',
    favicon: '/favicon.svg',
  },
})
```

## `injectDefaultFrontEndRoutes`

Inject Default Routes - Injects the default routes for the StudioCMS front-end

* **Type:** `boolean`
* **Default:** `true`

`injectDefaultFrontEndRoutes` Should the user facing frontend routes be injected into the `astroStudioCMS`. This is used to setup your front-end routes.

## `inject404Route`

Inject 404 Route - Injects a 404 route for handling unknown routes

* **Type:** `boolean`
* **Default:** `true`

`inject404Route` Should the `404` route be injected into the `astroStudioCMS`.  This is used to setup your frontend `404` route.

## `htmlDefaultLanguage`

HTML Default Language - The default language for the HTML tag

* **Type:** `string`
* **Default:** `'en'`

`htmlDefaultLanguage` Used to set the `lang` attribute of your `<html>` of the `astroStudioCMS` webpage.

## `htmlDefaultHead`

* **Type:** `Array`
* **Default:** `optional`

HTML Default Header - The default head configuration for the Frontend

### Usage

```js title="astro.config.mjs" {2-4}
astroStudioCMS({
    htmlDefaultHead: [
        { tag: 'title', content: 'My Awesome Site' },
        {
          tag: 'script',
          attrs: {
            defer: true,
            src: 'https://umami.mydomain.dev/script.js',
            'data-website-id': 'my-umami-website-id',
          }
        }
    ],
})
```

## `layoutOverride`

Layout Override - Allows override of the default layout file

* **Type:** `string`
* **Default:** `optional`

## `favicon`

* **Type:** `string`
* **Default:** `/favicon.svg`

Favicon is relative to the project public folder
