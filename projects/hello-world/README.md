# Hello World

This project shows you how to start an all TypeScript based Vue.Js 3 using Vite.

* Create a new [vite project](https://github.com/vitejs/vite#getting-started)
* Add the [following tsconfig.json](https://v3.vuejs.org/guide/typescript-support.html#recommended-configuration) at your root directory 
* Install TypeScript `npm install typescript`
* Create `shims-vue.d.ts` at `src` folder with the following content ([source](https://stackoverflow.com/questions/63724523/how-to-add-typescript-to-vue-3-and-vite-project))

``` TypeScript
declare module "*.vue" {
  import { defineComponent } from "vue";
  const Component: ReturnType<typeof defineComponent>;
  export default Component;
}
```
* Rename the generated `main.js` to `main.ts`.
* Change `<script type="module" src="/src/main.js"></script>` at `index.html` to `<script type="module" src="/src/main.ts"></script>`.
* Run `npm run dev` for development or `npm run build` to build your project.


