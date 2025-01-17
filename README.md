# React-anchorify-text [![Build Status](https://travis-ci.org/mobilusoss/react-anchorify-text.svg?branch=develop)](https://travis-ci.org/mobilusoss/react-anchorify-text) [![npm version](https://badge.fury.io/js/react-anchorify-text.svg)](http://badge.fury.io/js/react-anchorify-text) [![codebeat badge](https://codebeat.co/badges/26eb9d7d-bc90-4351-8a22-ea198e350aff)](https://codebeat.co/projects/github-com-mobilusoss-react-anchorify-text-master)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fmobilusoss%2Freact-anchorify-text.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fmobilusoss%2Freact-anchorify-text?ref=badge_shield)

Create anchor tag with urls in text.

## Demo

[View Demo](http://mobilusoss.github.io/react-anchorify-text/example/)

## Installation

```bash
npm install --save react-anchorify-text
```

## API

### `AnchorifyText`

#### Props

```javascript
AnchorifyText.propTypes = {
  text: React.PropTypes.string.isRequired,
  linkify: React.PropTypes.object,
  flags: React.PropTypes.string,
  nonUrlPartsRenderer: PropTypes.func,
};
```

  * `text`: String to parse url

  * `linkify`: An instance of [linkify-it](https://github.com/markdown-it/linkify-it). default: `new LinkifyIt().tlds(require('tlds'))`

  * `target`: href target for anchor tag, default to "_blank".

  *  `nonUrlPartsRenderer`: callback for non-url parts of the `text`.

  * ~~`regex`: Regular expression as string to detect url .~~

  * ~~`flags`: Regular expression's frag, default to "ig".~~

  `regex` and `flags` props are removed from v2.0.0. Use [linkify-it](https://github.com/markdown-it/linkify-it) instance instead.

#### Children

If no children are passed to `AnchorifyText`, found urls will be rendered as `<a>` tag.
If one child are passed to `AnchorifyText`, found urls are rendered as child tag with `url` as prop.


## Usage example

```javascript

const textWithUrl = "Hello Google(http://google.com) and GitHub => https://github.com/ and Apple(www.apple.com)";

<AnchorifyText text={textWithUrl}></AnchorifyText>

<AnchorifyText text={textWithUrl}>
  <MyCustomAnchor></MyCustomAnchor>
</AnchorifyText>
```

See  [example](https://github.com/mobilusoss/react-anchorify-text/tree/develop/example)

```bash
yarn
yarn run start:example
```

## Tests

```bash
yarn run test
```

## Update dependencies

Use [npm-check-updates](https://www.npmjs.com/package/npm-check-updates)


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fmobilusoss%2Freact-anchorify-text.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fmobilusoss%2Freact-anchorify-text?ref=badge_large)