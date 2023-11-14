# colorpicker

A very beautiful color picker, supports input and output of multiple color formats, and supports gradient color selection.

Note: This document is for Vue3ColorPicker v2. If you are looking for an older versions, refer to the v1 branches.The v2 version is a destructive update, and some functions in v1 are no longer supported. Please use it with caution

[Live Demo](https://github.com/haixin-fang/vue3-color-picker/)

[中文文档](https://github.com/haixin-fang/vue3-color-picker/blob/main/README.ZH-cn.md)

![vue3-color-picker](src/assets/example.jpg)

## Installation

```
yarn add vue3-color-picker
```

OR

```
npm install vue3-color-picker
```

## How to use

### The first step is global registration

```
import Vue3ColorPicker from "vue3-color-picker";
import "vue3-color-picker/style.css";

createApp(App)
  .use(router)
  .use(Vue3ColorPicker)
  .mount("#app");
```

OR

```vue3
import { ColorPicker } from "vue3-color-picker";
import "vue3-color-picker/style.css";

export default defineComponent({
components: { ColorPicker },
});
```

### Usage

```vue3
<template>
  <div>
     <color-picker v-model:pureColor="pureColor" v-model:gradientColor="gradientColor"/>
  </div>
</template>
<script lang="ts">
  import { ref } from "vue";
  import { ColorInputWithoutInstance } from "tinycolor2";

  export default defineComponent({
     setup() {
       const pureColor = ref<ColorInputWithoutInstance>("red");
       const gradientColor = ref("linear-gradient(0deg, rgba(0, 0, 0, 1) 0%, rgba(0, 0, 0, 1) 100%)");

       return { pureColor, gradientColor }
     }
  });
</script>

```

[Live Demo](https://aesoper101.github.io/vue3-color-picker/)
