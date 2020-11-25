# 🤩 [Tailwindcss 2.x.x](https://tailwindcss.com/) Webpack Setup

## ✋ Please go through the README completely

List of dev dependencies

| Package                 | Version |
| ----------------------- | ------- |
| @babel/core             | ^7.12.9 |
| @babel/preset-env       | ^7.12.7 |
| autoprefixer            | ^10.0.2 |
| babel-loader            | ^8.2.1  |
| css-loader              | ^5.0.1  |
| fibers                  | ^5.0.0  |
| file-loader             | ^6.2.0  |
| html-loader             | ^1.3.2  |
| html-webpack-plugin     | ^4.5.0  |
| mini-css-extract-plugin | ^1.3.1  |
| postcss                 | ^8.1.10 |
| postcss-import          | ^13.0.0 |
| postcss-loader          | ^4.1.0  |
| sass                    | ^1.29.0 |
| sass-loader             | ^10.1.0 |
| style-loader            | ^2.0.0  |
| tailwindcss             | ^2.0.1  |
| webpack                 | ^5.6.0  |
| webpack-cli             | ^4.2.0  |
| webpack-dev-server      | ^3.11.0 |

👉 `purge` option is enabled Manually in `tailwind.config.js` instead of depending on the `NODE_ENV`

---

To run dev server

```
npm run dev
```

dev server runs on [http://localhost:9000/](http://localhost:9000/)

---

To get the production build

```
npm run build
```

---

you can add new pages(multiple html files) by importing them into the `src/js/index.js`

### 💡 don't forget to add the entry in the webpack.config.js under plugins setion

```
  plugins: [
    new HtmlWebpackPlugin({
      template: "src/index.html",
    }),
    new HtmlWebpackPlugin({
      filename: "page.html",
      template: "src/page.html",
    }),
    ... create new pages and add entry here and import them into the src/js/index.js
  ],
```

⚠️ don't forget to add the `filename` otherwise it is taken as the default entry creating a `index.html`(also overrides the actual index.html) instead of the actual filename(page.html)

# 👉 Please Support and Subscribe to My [Youtube](https://www.youtube.com/channel/UCpOHt5d6GG-mvo-_pU06rhQ?sub_confirmation=1) Channel

## Made with ❤️ - by [FrontEndFunn](https://www.youtube.com/channel/UCpOHt5d6GG-mvo-_pU06rhQ?sub_confirmation=1)
