## Nuxt 3 + Tailwind CSS v4 조합으로 새 프로젝트를 만들기

> npx nuxi@latest init my-nuxt-tailwind-app

✔ Which package manager would you like to use?  
npm

✔ Initialize git repository?  
Yes

✔ Would you like to install any of the official modules?  
@nuxt/ui – The Intuitive UI Library powered by Reka UI and Tailwind CSS  

> cd my-nuxt-tailwind-app  
> npm install  
> npm install -D tailwindcss @tailwindcss/vite autoprefixer  
  
nuxt.config.ts
```
// https://nuxt.com/docs/api/configuration/nuxt-config
import tailwindcss from '@tailwindcss/vite'

export default defineNuxtConfig({
  compatibilityDate: '2025-05-15',
  devtools: { enabled: true },
  modules: ['@nuxt/ui'],
  css: ['~/assets/css/main.css'],
  vite: {
    plugins: [tailwindcss()]
  },
  postcss: {
    plugins: {
      '@tailwindcss/postcss': {},
      autoprefixer: {}
    }
  }
})
```

