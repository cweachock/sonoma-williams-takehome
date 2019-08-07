# Sonoma Williams Technical Challenge #1

##overview 
This challenge was set up with the [vue cli hello world boiler plate](https://cli.vuejs.org/guide/creating-a-project.html#vue-create)
using [npm](https://www.npmjs.com/). The product grid was made with flexbox and the items in the product grid were made with a "product grid component". Using the **v-for** directive we can render a list of items (in this case products and product information) from the **imported JSON** file to the project. So for each item in the data.json we specify the object key, in this case "groups", and use that to build our vue App. We can get the data using **v-bind** to bind the property as a DOM property for the component props in the **productGridItem.vue** component. This component also contains it's own stylings (scss) to affect how the product grid item is displayed. 

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

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
