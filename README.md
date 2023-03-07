# reactivity-fundamentals-vuejs3

# Declaring Reactive State
We can create a reactive object or array with the reactive() function:

`import { reactive } from 'vue'`
`const state = reactive({ count: 0 })`

Reactive objects are JavaScript Proxies and behave just like normal objects. The difference is that Vue is able to track the property access and mutations of a reactive object.


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

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
