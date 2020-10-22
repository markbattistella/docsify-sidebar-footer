<div align="center">

# docsify-sidebarfooter

![Github2npm](https://github.com/markbattistella/docsify-sidebarfooter/workflows/gh2npm/badge.svg?event=registry_package) ![npm (scoped)](https://img.shields.io/npm/v/@markbattistella/docsify-sidebarfooter) ![GitHub](https://img.shields.io/github/license/markbattistella/docsify-sidebarfooter) ![npm bundle size (scoped)](https://img.shields.io/bundlephobia/minzip/@markbattistella/docsify-sidebarfooter)

![Help donate](https://img.shields.io/badge/%20-@markbattistella-blue?logo=paypal&link=https://www.paypal.me/markbattistella/6AUD) ![Buy me a coffee](https://img.shields.io/badge/%20-buymeacoffee-black?logo=buy-me-a-coffee&link=https://www.buymeacoffee.com/markbattistella)

---

:sparkles: ![Demo page](https://img.shields.io/badge/demo-@markbattistella/docsify--sidebarfooter-blue?style=for-the-badge) :sparkles:

</div>

---

This plugin is designed to create a footer area at the base of your sidebar where you can list a copyright year (range), your name or company with a URL, and links to a privacy policy and terms of service.

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
        name:     '',
        url:      '',
        copyYear: '',
        policy:   '',
        terms:    ''
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
```

## Configuration

There are some options available for the `docsify-sidebarfooter`:

| setting   | options |
| :-------- | :------ |
| name      | your name or your company - whoever is the owner
| url       | the url you want the name to link to (optional)
| copyYear  | the first year of copyright. leave blank for current year
| policy    | do you have a Privacy Policy page
| terms     | do you have a Terms of Service page

## Usage

At the bottom of your `_sidebar.md` file add the following code:

```html
<div id="mb-footer"></div>
```

You _can_ add this anywhere, but it's designed for the sidebar.

## Example

![Example output](demo/example.jpg)

## Known issues

At present the sidebar links are relative to the base url, and any sub directories in the address are stripped :disappointed:

It's in the [issue list](https://github.com/markbattistella/docsify-sidebarFooter/issues/1#issue-727165896)!

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
