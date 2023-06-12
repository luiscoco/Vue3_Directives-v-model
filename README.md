# vue-directives

In Vue.js version 3, directives are special attributes that you can apply to DOM elements or components to add behavior or manipulate the DOM directly. Directives are prefixed with the v- keyword, followed by the directive name. They are used to provide additional functionality to the elements they are attached to.

Here are a few commonly used directives in Vue.js 3 along with some code samples:

## v-model:
The v-model directive is used for two-way data binding between form inputs and Vue.js component data. It automatically updates the data when the input value changes and vice versa.

```html
<input v-model="message" type="text">
<p>{{ message }}</p>
```

```typescript
<script lang="ts" setup>
  import { ref } from 'vue';

  const message = ref('');

  // No need to define a separate method for updating the message,
  // v-model will automatically handle it.
</script>
```

## v-if and v-else:
The v-if directive is used to conditionally render an element or a component based on a truthy value. The v-else directive is used to specify the alternate rendering when the condition is false.

```html
<div v-if="isVisible">
  <p>This element is visible.</p>
</div>
<div v-else>
  <p>This element is hidden.</p>
</div>
```
```typescript
<script lang="ts" setup>
  import { ref } from 'vue';

  const isVisible = ref(true);
</script>
```

## v-for:
The v-for directive allows you to iterate over an array or an object and render a template for each item.

```html
<ul>
  <li v-for="item in items" :key="item.id">
    {{ item.name }}
  </li>
</ul>
```

```typescript
<script lang="ts" setup>
  import { ref } from 'vue';

  interface Item {
    id: number;
    name: string;
  }
  
  const items = ref<Item[]>([
    { id: 1, name: 'Item 1' },
    { id: 2, name: 'Item 2' },
    { id: 3, name: 'Item 3' }
  ]);
</script>
```

## v-bind:
The v-bind directive is used to bind an attribute or a prop of an element to a value or an expression. It allows you to dynamically update the attribute or prop based on the component's data.

```html
<img v-bind:src="imageSrc" alt="Vue.js Logo">
```

```typescript
<script lang="ts" setup>
  import { ref } from 'vue';

  const imageSrc = ref('path/to/image.jpg');
</script>
```

## v-on:
The v-on directive is used to attach event listeners to elements or components. It allows you to execute methods or expressions when a specific event occurs.

```html
<button v-on:click="incrementCounter">Click me</button>
```

```typescript
<script lang="ts" setup>
  import { ref } from 'vue';

  const incrementCounter = () => {
    // Logic to increment the counter
  };
</script>
```

In Vue.js 3 with the Composition API, you can use the <script lang="ts" setup> block to define your component's code in a more concise and streamlined manner. The ref function from the vue package is used to create reactive references to the data. The methods or functions can be defined directly inside the <script lang="ts" setup> block and referenced in the template.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
