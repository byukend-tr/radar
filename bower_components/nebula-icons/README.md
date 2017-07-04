[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-green.svg)](https://www.webcomponents.org/element/arsnebula/nebula-icons)
[![Polymer Version](https://img.shields.io/badge/polymer-v2-blue.svg)](https://www.polymer-project.org)
[![Sauce Labs Build Status](https://img.shields.io/badge/saucelabs-passing-red.svg)](https://saucelabs.com/beta/builds/aa51c233627249d78e2d5e6d46ecf8cb)
[![Gitter Chat](https://badges.gitter.im/org.png)](https://gitter.im/arsnebula/webcomponents)
[![Become a Patreon](https://img.shields.io/badge/patreon-support_us-orange.svg)](https://www.patreon.com/arsnebula)

# \<nebula-icons\>

Share SVG icons resources between custom elements.

- Compatible with [Polymer Custom Iconset Generator](https://poly-icon.appspot.com)
- Define custom iconsets and share them between custom elements
- SVG tags are rendered into Light DOM for easy styling

## Installation

```sh
$ bower install -S arsnebula/nebula-icons
```

## Usage

Import the element.

```html
<link rel="import" href="/bower_components/nebula-icons/nebula-icons.html">
```

Define your iconsets once, anywhere in your application. Each iconset is defined by a unique name.

```html
<nebula-iconset name="custom" size="24">
  <svg>
    <defs>
      <g id="add"><path d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"></path></g>
    </defs>
  </svg>
</nebula-iconset>
```

Render icons anywhere in your application. Icons are accessed with a compount key formatted as `[iconset]:[id]`.

```html
<nebula-icon icon="custom:add"></nebula-icon>
```

Style the icon using CSS variables or standard CSS properties.

```css
<style>
  nebula-icon {
    --nebula-icon-size: 48px;
    color: darkred;
  }
</style>
```

*For more information see the API Reference documentation.*

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