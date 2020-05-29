# v-title

Auxiliary text display（like `el-tooltip`）.

https://yujinpan.github.io/v-title/

## Usage

### Install

```
npm install --save v-title
```

### Require element-ui

If your project does not use element-ui,
you need to introduce a separate element-ui package, like this:

```js
import 'v-title/lib/element-ui';
```

### Global registration

```js
import Vue from 'vue';
import VTitle from 'v-title';

Vue.use(VTitle);
```

### In-component registration

```js
import VTitle from 'v-title';

export default {
  components: {
    VTitle
  }
};
```

### Complete example

- delay(modifier): show delay
- light(modifier): use light effect, default use dark
- overflow(modifier): use overflow mode
- multiple(modifier): use multiple line mode(**need set element's `line-height > offsetHeight`**)
- title-placement(attribute): tooltip placement

```xml
<template>
  <p v-title="title"></p>
  <p v-title.delay="title"></p>
  <p v-title.light="title"></p>
  <p v-title.overflow="title"></p>
  <p v-title.overflow.multiple="title"></p>
  <p v-title="title" title-placement="bottom">
    top(-start, -end), right(-start, -end), bottom(-start, -end),
    left(-start, -end)，default: top
  </p>
</template>

<script>
import VTitle from 'v-title';

export default {
  directives: {
    VTitle
  },
  data() {
    return {
      title: 'test',
    };
  }
};
</script>
```
