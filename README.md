# vue-modality-v3
A really nice Vue.js modal component. (**Compatible with Vue.js 3**)

#### [Demo](https://ovictorpereira.github.io/vue-modality-v3/ "Demo")

## Installation
NPM
```bash
$ npm install vue-modality-v3
``` 
Register the component globally...
```js
import { createApp } from 'vue'
import App from './App.vue'

import VueModalityV3 from 'vue-modality-v3'

createApp(App)
.component('VueModality', VueModalityV3)
.mount('#app')

```

... or register it locally
```js
import VueModalityV3 from 'vue-modality-v3'
export default {
  components: {
    VueModality: VueModalityV3
  }
};
```

## Usage
```html
<vue-modality ref="myRef" title="My Title" centered>
  body content
</vue-modality>
```
```js
// OPTIONS API
// Inside a method
// give your modal a ref and open it by calling :
this.$refs.myRef.open()

// or close it by calling:
this.$refs.myRef.hide()
```

```js
// COMPOSITION API
setup () {
	const myRef = ref(null)
	const openMyModal = () => { myRef.value.open() }
	return {
		myRef,
		openMyModal
	}
}
```



## Available props

| Prop                             | Type             | Default                | Description              |
|--------------------------|---------------|--------------------|----------------------|
| width         |               String |    400px                   |                                             |
| centered   | Boolean           | false                    | Vertically  centered   |
| overlay    | Boolean           | false     |  |
| text-center         |               Boolean |    false                   |                                             |
| title     |         String           |     Modal                |                             |
| title-class   | String           |                        |                                           |
| hide-header     | Boolean           |      false                  |                 |
| hide-footer     | Boolean           |         false               |                 |
| ok-title     | String           |            Ok            |                  |
| ok-disabled     | Boolean           |         false               |                 |
| ok-class     | String           |                        |                 |
| ok-loading     | Boolean           |        false          |      Shows the loading icon           |
| hide-ok     | Boolean           |      false                  |       Hides the ok button          |
| cancel-title     | String           |          Cancel              |                |
| cancel-disabled     | Boolean           |         false               |                 |
| cancel-class     | String           |                        |                 |
| hide-cancel     | Boolean           |      false                  |       Hides the cancel button          |
| no-close-on-backdrop     | Boolean           |      false                  |               |
| no-close-on-esc     | Boolean           |      false                  |               |
| error     | Boolean           |      false                  |      Shows error icon         |
| success     | Boolean           |      false                  |      Shows success icon         |

## Events
| Event    |  Description |
|----------|--------------|
| open     |  When you open the modal       |
| hide     |   When you hide the modal       |
| ok        |    When the Ok button is pressed      |
| cancel        |    When the Cancel button is pressed      |