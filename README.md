# vue-checkbox-radio
> A Vue component to easily styling checkbox and radio inputs


[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Latest Version on NPM](https://img.shields.io/npm/v/vue-checkbox-radio.svg?style=flat-square)](https://npmjs.com/package/vue-checkbox-radio)

## Usage

**Checkbox**

```html
<checkbox name="robot" value="1">I'm a robot</checkbox>
```

**Radio**

```html
<radio name="robot" value="1">I'm a robot</radio>
<radio name="robot" value="0">I'm not a robot</radio>
```

## Install

yarn

```bash
yarn add vue-checkbox-radio
```

npm


```bash
npm install vue-checkbox-radio --save
```

## Setup

Register the plugin.

```js
import CheckboxRadio from 'vue-checkbox-radio';

Vue.use(CheckboxRadio);
```

Or register components manually.

```js
import {Checkbox, Radio} from 'vue-checkbox-radio';

Vue.component('checkbox', Checkbox);
Vue.component('radio', Radio);
```

## Params

Parameter | Type | Default
--------- | ---- | ------
id | `string` | [checkbox/radio]-id-[element uid]
name | `string` | `null`
value | `string` | `null`
className | `string` | `null`
checked | `boolean` | `false`
required | `boolean` | `false`

## Events

Both components emit `change` event.

## Full example

```html
<checkbox
    id="input-terms"
    name="terms"
    value="1"
    className="terms"
    :change="someMethod"
    checked
    required>
    I agree to the <a href="#">terms of service</a>
</checkbox>
```

## Styling

Components are wrapped by `checkbox-component` and `radio-component` classes and it uses label:before to draw the input. Checkout [Checkbox.vue](src/components/Checkbox.vue) or [Radio.vue](src/components/Radio.vue) source for more info.

## License

MIT © [Mario Juárez](https://github.com/mariomka)
