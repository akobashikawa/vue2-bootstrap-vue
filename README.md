# vue2-bootstrap-vue

- [Starting with Bootstrap-Vue step by step](https://www.ma-no.org/en/programming/javascript/starting-with-bootstrap-vue-step-by-step)

- npm install -g @vue/cli
- vue create vue2-bootstrap-vue
  - Manually select features
    - Babel
    - Router
    - Linter / Formatter
  - Version: 2.x
  - Use history mode for router: No
  - Pick a linter / formatter config: ESLint + Prettier
  - Lint on save
  - Dedicated config files
  - Save as a preset: No
- cd vue2-bootstrap-vue
- npm run serve
  - http://localhost:8080/
- npm install bootstrap@4.3.1 bootstrap-vue

- main.js
```js
import Vue from "vue";
import App from "./App.vue";
import router from "./router";

Vue.config.productionTip = false;

/*--------------------REGISTER BOOTSTRAP---------------------------------*/
import { BootstrapVue, IconsPlugin } from "bootstrap-vue";
// Import Bootstrap an BootstrapVue CSS files (order is important)
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";
// Make BootstrapVue available throughout your project
Vue.use(BootstrapVue);
// Optionally install the BootstrapVue icon components plugin
Vue.use(IconsPlugin);
/*-----------------------------------------------------------------------*/

new Vue({
  router,
  render: (h) => h(App),
}).$mount("#app");
```