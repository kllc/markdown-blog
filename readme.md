# GitHub Pages Url

https://kllc.github.io/markdown-blog/

# How to use

- Create an article in markdown and push it to github.
- Write the path (src) and other attribute information of the article in index.js.

```javascript
// index.js
export default () => {
  const index = [
    {
      src: "md/sample/sample1.md", // [Mandatory] Article path
      anchor: false, // [Default value is false] True for external links from the top page
      date: "22.1.1", // Article creation date
      title: "Sample", // Article Title
      text: "text text text", // Article Summary Description
      img: "https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png", // Image to set in the article
      topics: ["vuetify", "markdown"], // Article Topics
      author: {
        name: "k", // Author's name
        avatar: "https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png", // Author's Avatar
        message:
          "vuetify sample. https://store.vuetifyjs.com/products/parallax-theme-free", // Introduction of the author, message from the author
      },
    },
    {
      src:"md/sample/sample2.md" // It works even if only 'src' is entered.
    },
    :
  ];
  return index;
};
```

# Localhost testing with Docker

Type the following command at a command prompt

`docker run -d -p 8080:80 -v "%cd%:/usr/local/apache2/htdocs/" --name docker-httpd --rm httpd:alpine`

http://localhost:8080
