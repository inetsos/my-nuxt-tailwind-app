## Nuxt 3 + Tailwind CSS v4 - 자주 사용하는 UI 컴포넌트, Vercel 배포

https://inetsos.tistory.com/479

https://my-nuxt-tailwind-app.vercel.app/ vercel 배포

### 1. 프로젝트 만들기

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
  
### 2. Tailwind CSS 설정
  
- nuxt.config.ts    
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
  
### 3. CSS 파일 생성

assets/css/main.css 파일을 만들고 아래처럼 작성하세요:  
@import "tailwindcss";  
  
### 4. Components
  
- App.vue 
- layouts\default.vue  
- pages\index.vue  
- components\Alert.vue  
- components\BaseButton.vue  
- components\Card.vue  
- components\Footer.vue  
- components\InputField.vue  
- components\Modal.vue  
- components\Navbar.vue  


![Tailwind UI 컴포넌트](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fsm5hH%2FbtsO4sHxaYr%2FAAAAAAAAAAAAAAAAAAAAANEA2QNHx-SmRkZTTuHzzpLFQlJyabW8-r8UEcun6jY5%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1753973999%26allow_ip%3D%26allow_referer%3D%26signature%3D7hmlcXgPYjrnhOlI%252BwDlSNNWqoA%253D)

![Tailwind UI 컴포넌트 - 모달](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2Fb1RN0e%2FbtsO4eW0Uus%2FAAAAAAAAAAAAAAAAAAAAAGcpwuavbxzmPISqy82QHNoimCHcObUcr9FzFqn7RA22%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1753973999%26allow_ip%3D%26allow_referer%3D%26signature%3D02ahDDtnump06H4Sufa7EC9Uv6c%253D)

  
### 5. nuxt 프로젝트를 Vercel에 배포
  
1. 프로젝트를 GitHub에 Push합니다.  
2. https://vercel.com 에 접속하여 로그인합니다 (GitHub 계정으로 로그인 추천).  
3. "Add New..." -> Project 를 클릭하고, GitHub 저장소를 선택합니다.  


https://my-nuxt-tailwind-app.vercel.app/