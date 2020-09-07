![npm Publish](https://github.com/markbattistella/docsify-sidebarfooter/workflows/npm%20Publish/badge.svg?event=registry_package)

---

# Getting started

## Installation
1. Configure the `docsify-autoFooter`:
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

### via npm
Including it via NPM has one extra step than a normal:

```sh
npm install @markbattistella/docsify-sidebarfooter@1.1.5 --registry="https://npm.pkg.github.com/"
```


1. Insert script into docsify document:
```js
<script src="docsify-sidebarFooter.js"></script>
```


1. If you are using the Privacy Policy and Terms of Service links, then add the two files to the root (next to `index.html`)

	```
	| docs/
	|-- _privacy.md
	|-- _terms.md
	```


1. Add the `<div id="mb-footer"></div>` to the bottom of the `_sidebar.md`. I guess you can add this anywhere, but it's designed for the sidebar.


1. Find a couple of online generators to help fill in the data :smiley:



## Configuration
There are some options available for the `docsify-autoHeaders`:

| setting   | options |
| :-------- | :------ |
| name		| your name or your company - whoever is the owner
| url		| the url you want the name to link to (optional)
| copyYear	| the first year of copyright. leave blank for current year
| policy	| do you have a Privacy Policy page
| terms		| do you have a Terms of Service page


## Usage
Fill in the data within the configuration, and it will all auto populate.


## Example
![Example output](images/example.jpg)

# Contributing
1. Clone the repo:
`git clone https://github.com/markbattistella/docsify-sidebarFooter.git`

1. Create your feature branch:
`git checkout -b my-feature`

1. Commit your changes:
`git commit -am 'Add some feature'`

1. Push to the branch:
`git push origin my-new-feature`

1. Submit a `pull` request
