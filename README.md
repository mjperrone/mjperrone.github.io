# [mjperrone.github.io](https://mjperrone.github.io/)


## setup

```bash
yarn init -2
mkdir empty
hexo init empty
#  edit package.json and .gitignore manually
cp -r empty/* .
git clone https://github.com/hexojs/hexo-theme-landscape.git themes/landscape
```

## ongoing
add page

```bash
yarn run hexo new post
```

build and serve

```bash
yarn build
yarn server
```

## themes

```bash
git submodule add https://github.com/hexojs/hexo-theme-landscape.git themes/landscape
git submodule add https://github.com/liuxiaotian/hexo-theme-lous themes/lous
```