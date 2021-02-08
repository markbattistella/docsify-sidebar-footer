<div align="center">

# docsify-sidebarfooter

![Github2npm](https://github.com/markbattistella/docsify-sidebarfooter/workflows/gh2npm/badge.svg?event=registry_package) ![npm (scoped)](https://img.shields.io/npm/v/@markbattistella/docsify-sidebarfooter) ![GitHub](https://img.shields.io/github/license/markbattistella/docsify-sidebarfooter) ![npm bundle size (scoped)](https://img.shields.io/bundlephobia/minzip/@markbattistella/docsify-sidebarfooter)

---

[![](https://img.shields.io/badge/%20-@markbattistella-blue?logo=paypal&style=for-the-badge)](https://www.paypal.me/markbattistella/6AUD)
[![](https://img.shields.io/badge/%20-buymeacoffee-black?logo=buy-me-a-coffee&style=for-the-badge)](https://www.buymeacoffee.com/markbattistella)

[![](https://img.shields.io/badge/demo-@markbattistella/docsify--sidebarfooter-1E5749?style=for-the-badge)](https://markbattistella.github.io/docsify-sidebarfooter/)

</div>

---

This plugin is designed to create a footer area at the base of your sidebar (or page) where you can list a copyright year (range), your name or company with a URL, and links to a privacy policy, terms of service, and a cookies policy.

---

## Installation

### Update `index.html` file

Assuming you have a working [docsify](https://docsify.js.org/) framework set up, it is easy to use the plugin.

1. Add the following script tag to your `index.html` via either CDN or downloading it and using it locally:

    ```html
    <!-- unpkg.com -->
    <script src="https://unpkg.com/@markbattistella/docsify-sidebarfooter@latest"></script>

    <!-- jsDelivr -->
    <script src="https://cdn.jsdelivr.net/npm/@markbattistella/docsify-sidebarfooter@latest"></script>

    <!-- locally -->
    <script src="docsify-sidebarfooter.min.js"></script>
    ```

1. In docsify setup configure the plugin:

    ```js
    <script>
    window.$docsify = {
      autoFooter: {
        name:       String,          // company display name (required)
        copyYear:   Int,             // start copyright year (required)
        url:        String,          // company url (optional)
        policy:     Bool | String,   // show Privacy Policy (optional)
        terms:      Bool | String,   // show Terms of Service (optional)
        cookies:    Bool | String,   // show Cookies Policy (optional)
        onBody:     Bool             // if true it is on the main doc
      }
    };
    </script>
    ```

### npm install

Or if you're using `npm` to manage your dependencies:

```sh
npm i @markbattistella/docsify-sidebarfooter
```

### Additional files

If you are using the Privacy Policy, Terms of Service, or Cookie links, then add the files to the root (next to `index.html`). However, if you inputted strings make sure they are in the location of that path with the correct filename.

```md
| docs/                      | docs/
|-- index.html               |-- site/
|-- _privacy.md              |---- privacy.md
|-- _terms.md                |---- terms.md
|-- _cookies.md              |---- cookies.md
```

## Configuration

There are some options available for the `docsify-sidebarfooter`:

| setting    | required | type           | options                            |
|------------|:--------:|----------------|------------------------------------|
| `name`     | Y        | String         | your name or company               |
| `copyYear` | Y        | String         | first year of copyright            |
| `url`      | N        | String         | url you want the `name` to link to |
| `policy`   | N        | Bool or String | path to `policy`                   |
| `terms`    | N        | Bool or String | path to `terms`                    |
| `cookies`  | N        | Bool or String | path to `cookies`                  |
| `onBody`   | N        | Bool           | display in the body not sidebar    |

## Usage

At the bottom of your `_sidebar.md` file add the following code:

```html
<footer id="mb-footer"></footer>
```

## Contributing

1. Clone the repo:

    `git clone https://github.com/markbattistella/docsify-sidebarFooter.git`

2. Create your feature branch:

    `git checkout -b my-feature`

3. Commit your changes:

    `git commit -am 'Add some feature'`

4. `Push` to the branch:

    `git push origin my-new-feature`

5. Submit the `pull` request
