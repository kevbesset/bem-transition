# BEM Transition

A VueJs component for transition with BEM compliance created during the [#1PAM challenge](https://github.com/kevbesset/one-package-a-month).
Most of all, it adds "-" after the transition name in order to have BEM compliant classes.

## Usage

```vue
<template>
  <div class="my-component">
    <bem-transition name="fade">
      <div v-if="show">Fade me</div>
    </bem-transition>
  </div>
</template>
```

and then your css will look like this with BEM compatibility :

```css
.fade--enter-active,
.fade--leave-active {
  transition: opacity 300ms;
}

.fade--enter-from,
.fade--leave-to {
  opacity: 0;
}

.fade--enter-to,
.fade--leave-from {
  opacity: 1;
}
```