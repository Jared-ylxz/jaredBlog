# jaredBlog
This is my blog


mkdir my-blog
<!-- cd my-blog
mkdir back-end front-end-admin front-end-client

cd back-end
go mod init my-blog-backend
go run main.go # 启动服务端 -->

cd my-blog
npm create vite@latest front-end-client # 选择Vue和JavaScript
npm create vite@latest front-end-admin # 选择Vue和JavaScript

cd front-end-client
npm install

src/App.vue 文件只保留 template、style、 script 标签，并删除其他内容
rm src/style.css
src/main.js 删除 import './style.css'

npm install sass -D # -D 是 --save-dev 的简写，表示只在开发环境下安装

mkdir src/styles
touch src/styles/base.scss

npm i -D tailwindcss postcss autoprefixer
npx tailwindcss init
tailwind.config.js 里面的 content 选项改为 content: ["./index.html", "./src/**/*.{vue,js,ts,jsx,tsx}"],

vite.config.js 添加：
import tailwindcss from 'tailwindcss'
import autoprefixer from 'autoprefixer'





npm install pinia

创建一个 stores 目录并添加一个状态管理文件：src/stores/articles.ts