# Fishtank Vue Icons

`@fishtank/icons-vue` is an NPM module which allows all icons from the Fishtank Design System to be
imported directly as VueJS modules without the need for any sort of Webpack loaders or other
complicated build pipeline.

## Installation

```sh
npm install @fishtank/icons-vue
```

## Basic Usage Instructions

Each of the icons in the system can be imported via a CamelCase name matching its official definition and
added to your Vue component:

```javascript
import Vue from 'vue'
import { Calendar24 as CalendarIcon } from '@fishtank/icons-vue'

export default Vue.extend({
  //...
  components: {
    CalendarIcon
  }
  //...
})
```

Then in your view template:

```html
<div>
  <CalendarIcon/>
</div>
```

## Development

This package is autogenerated by walking the icon files in the `@fishtank/icons` npm module's
`dist/` directory.  The primary javascript build relies on RollupJS and a custom plugin to
generate the javascript based on the aforementioned `dist/` directory.  There is also a
utility build process which produces a compatible typescript definition file.