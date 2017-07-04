[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/arsnebula/nebula-loader)
[![Polymer Version](https://img.shields.io/badge/polymer-v2-blue.svg)](https://www.polymer-project.org)
[![Sauce Labs Build Status](https://img.shields.io/badge/saucelabs-passing-red.svg)](https://saucelabs.com/beta/builds/f06d310d3c614422913dd58585f6d5f2)
[![Gitter Chat](https://badges.gitter.im/org.png)](https://gitter.im/arsnebula/webcomponents)
[![Become a Patreon](https://img.shields.io/badge/patreon-support_us-orange.svg)](https://www.patreon.com/arsnebula)

# \<nebula-loader\>

Display a loading progress overlay.

* A full-screen overlay with backdrop and centered dialog
* Supports optional title, spinning icon, progress bar and text fields
* Supports [WAI-ARIA](https://www.w3.org/TR/wai-aria-practices-1.1/) for **a11y**

## Installation

```sh
$ bower install arsnebula/nebula-loader
```

## Getting Started

Import the package.

```html
<link rel="import" href="/bower_components/nebula-loader/nebula-loader.html"> 
```

Add the element.

```html
<nebula-loader
  title="Loader"
  icon="icons:refresh"
  progress=40
  text="40%">
</nebula-loader>
```

The element is also designed to be easy to create programatically. The `show` method will ensure the element is appended and removed from the `document.body` automatically. The method returns a promise that is resolved when the element is closed.

```js
// create the element
const loader = document.createElement('nebula-loader')

// show the element - automatically appended to document.body
loader.show({
  title: 'Loading',
  icon: 'icons:refresh',
  progress: 40,
  text: '40%' 
}).then(() => {
  console.log('Loader has been closed')
})

// update the progress as applicable (if showing progress bar)
loader.progress = 50
loader.text = '50%'

// cancel when finished background work
loader.close()
```

*For more information, see the API documentation.*

## Contributing

We welcome and appreciate feedback from the community. Here are a few ways that you can show your appreciation for this package:

* Give us a **Star on GitHub** from either [webcomponents.org](https://www.webcomponents.org/element/arsnebula/nebula-element-mixin) or directly on [GitHub](https://github.com/arsnebula/nebula-element-mixin).

* Submit a feature request, or a defect report on the [Issues List](https://www.webcomponents.org/element/arsnebula/nebula-element-mixin/issues).

* Become a [Patreon](https://www.patreon.com/arsnebula). It takes a lot of time and effort to develop, document, test and support the elements in our [Nebula Essentials](https://www.webcomponents.org/collection/arsnebula/nebula-essentials) collection. Your financial contribution will help ensure that our entire collection continues to grow and improve.

If you are a developer, and are interested in making a code contribution, consider opening an issue first to describe the change, and discuss with the core repository maintainers. Once you are ready, prepare a pull request:

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Change Log

See [CHANGELOG](/CHANGELOG.md)

## License

See [LICENSE](/LICENSE.md)