<div align="center">

# docsify-sidebarfooter

![Github2npm](https://github.com/markbattistella/docsify-sidebarfooter/workflows/gh2npm/badge.svg?event=registry_package) ![npm (scoped)](https://img.shields.io/npm/v/@markbattistella/docsify-sidebarfooter) ![GitHub](https://img.shields.io/github/license/markbattistella/docsify-sidebarfooter) ![npm bundle size (scoped)](https://img.shields.io/bundlephobia/minzip/@markbattistella/docsify-sidebarfooter)

![Help donate](https://img.shields.io/badge/%20-@markbattistella-blue?logo=paypal&link=https://www.paypal.me/markbattistella/6AUD) ![Buy me a coffee](https://img.shields.io/badge/%20-buymeacoffee-black?logo=buy-me-a-coffee&link=https://www.buymeacoffee.com/markbattistella)

</div>

---

This plugin is designed to create a footer area at the base of your sidebar where you can list a copyright year (range), your name or company with a URL, and links to a privacy policy, terms of service, and a cookies policy.

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
      footerOptions: {
        name:     '',     // company display name (required)
        url:      '',     // company url (optional)
        copyYear: '',     // start copyright year (required)
        policy:   true,   // show Privacy Policy (optional)
        terms:    true,   // show Terms of Service (optional)
        cookies:  true    // show Cookies Policy (optional)
      }
    };
    </script>
    ```

### npm install

Or if you're using `npm` to manage your dependencies:

```sh
npm install @markbattistella/docsify-sidebarfooter
```

### Additional files

If you are using the Privacy Policy and Terms of Service links, then add the two files to the root (next to `index.html`)

```md
| docs/
|-- index.html
|-- _privacy.md
|-- _terms.md
|-- _cookies.md
```

## Configuration

There are some options available for the `docsify-sidebarfooter`:

| setting   | required | type   | options                                |
| :-------- | :------: | :----- | :------------------------------------- |
| name      | Y        | String | your name or your company              |
| url       | N        | String | the url you want the `name` to link to |
| copyYear  | Y        | String | the first year of copyright            |
| policy    | N        | Bool   | do you have a Privacy Policy page      |
| terms     | N        | Bool   | do you have a Terms of Service page    |
| cookies   | N        | Bool   | do you have a Cookies Policy page      |

## Usage

At the bottom of your `_sidebar.md` file add the following code:

```html
<div id="mb-footer"></div>
```

You _can_ add this anywhere, but it's designed for the sidebar.

## Known issues

None :smile:

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
