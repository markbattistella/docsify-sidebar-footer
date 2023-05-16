<div align="center">

# docsify.js sidebar footer

</div>

This plugin enhances your website's sidebar or page by creating a footer area where you can display important information. It automatically updates the copyright year or range, allows you to include your name or company with a URL, and provides links to a privacy policy, terms of service, and cookies policy pages. By utilising this plugin, you can easily showcase relevant legal information, personalise your website, and promote transparency and compliance.

## Installation

!> **Note: There are breaking changes in the configuration from `v4.x` to `v5.x`. Please take the time to read all the documentation before upgrading**

### Update `index.html` file

Assuming you have a working [docsify](https://docsify.js.org/) framework set up, it is easy to use the plugin.

1. Add one of the following script tags to your `index.html` via either CDN or downloading it and using it locally:

    ```html
    <!-- unpkg.com -->
    <script src="https://unpkg.com/@markbattistella/docsify-sidebarfooter@latest"></script>

    <!-- jsDelivr -->
    <script src="https://cdn.jsdelivr.net/npm/@markbattistella/docsify-sidebarfooter@latest"></script>

    <!-- locally -->
    <script src="docsify-sidebar.min.js"></script>
    ```

1. In docsify setup configure the plugin:

    ```js
    <script>
    window.$docsify = {
      autoFooter: {

        // the name you wish to display as the copyright holder
        name:        String,

        // the URL (personal or company) which clicking the `name` goes to
        url:         String,

        // the start year of copyright
        copyYear:    String,

        // show the privacy policy link
        policy:      Bool | String,

        // show the terms of service link
        terms:       Bool | String,

        // show the cookies policy link
        cookies:     Bool | String,

        // use your own css styles or the built in ones
        customStyle: Bool | String
      }
    };
    </script>
    ```

### Additional files

#### Default

If you set the `policy`, `terms`, or `cookies` options to `true` the URL links for those pages will look for the markdown files directly next to the `index.html` file:

```js
// ... other config
policy: true,
terms: true,
cookies: true,
// ... other config
```

```md
- index.html      --> https://your-awesome-site.com/#/
- _policy.md      --> https://your-awesome-site.com/#/_policy
- _terms.md       --> https://your-awesome-site.com/#/_terms
- _cookies.md     --> https://your-awesome-site.com/#/_cookies
```

#### Sub-folder

However, if you enter a string it will append that to the base URL of your website:

```js
// ... other config
policy: 'site/policy',
terms: 'site/terms',
cookies: 'site/cookies',
// ... other config
```

```md
- index.html      --> https://your-awesome-site.com/#/
- site/
  \__ policy.md   --> https://your-awesome-site.com/#/site/policy
  \__ terms.md    --> https://your-awesome-site.com/#/site/terms
  \__ cookies.md  --> https://your-awesome-site.com/#/site/cookies
```

#### External links

If you host your policy, terms, or cookies messages on an external website (or need to link to a parent company policy) you can add them in as the full URL:

```js
// ... other config
policy: "https://my-other-website.com/policy",
terms: "https://my-other-website.com/terms",
cookies: "https://my-other-website.com/cookies",
// ... other config
```

These will open those pages in a new tab directly.

## Configuration

There are some options available for the `docsify-sidebarfooter`:

| Setting       | Type           | Options                            |
|---------------|----------------|------------------------------------|
| `name`        | String         | your name or company               |
| `url`         | String         | url you want the `name` to link to |
| `copyYear`    | String         | first year of copyright            |
| `policy`      | Bool or String | - `false` hides it from the site<br/>- `true` defaults to `_policy.md`<br/>- a custom string will direct to that |
| `terms`       | Bool or String | - `false` hides it from the site<br/>- `true` defaults to `_terms.md`<br/>- a custom string will direct to that |
| `cookies`     | Bool or String | - `false` hides it from the site<br/>- `true` defaults to `_cookies.md`<br/>- a custom string will direct to that |
| `customStyle` | Bool or String | - `false` uses in-built css (sidebar styled)<br/>- `true` applies no styles, you can create your own<br/>- `sidebar` uses the in-built css designed for the sidebar<br/>- `body` uses the in-built css designed for the body |

## Usage

### Sidebar

At the bottom of your `_sidebar.md` file add the following code:

```html
<footer id="mb-footer"></footer>
```

### Body

Under the `<div id="app"></div>` in your `index.html` file, add the following code:

```html
<footer id="mb-footer"></footer>
```

## Styling

The links container is sectioned into different classes for you to customise as much (or little) as you wish.

```html
<footer id="mb-footer">
  <div class="footer-container">
    <div class="footer-text">
      <span class="footer-text-copyright">
        Copyright © YYYY-YYYY
      </span>
      <span class="footer-text-author">
        <a target="_blank" href="">Your website name</a>
      </span>
    </div>
    <div class="footer-link">
      <span class="footer-links-policy">
        <a href="">Policy</a>
      </span>
      <span class="footer-links-terms">
        <a href="">Terms</a>
      </span>
      <span class="footer-links-cookies">
        <a href="">Cookies</a>
      </span>
    </div>
  </div>
</footer>
```

## Contributing

1. Clone the repo:<br>`git clone https://github.com/markbattistella/docsify-sidebarFooter.git`
2. Create your feature branch:<br>`git checkout -b my-feature`
3. Commit your changes:<br>`git commit -am 'Add some feature'`
4. `Push` to the branch:<br>`git push origin my-new-feature`
5. Submit the `pull` request
