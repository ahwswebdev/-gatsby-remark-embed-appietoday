# gatsby-remark-embed-appietoday
Embed a AppieToday Video in your Markdown

Inspired by [gatsby-remark-embed-youtube](https://github.com/ntwcklng/gatsby-remark-embed-youtube)


## Install 
1. Install plugin to your site:

```bash
npm i https://github.com/ahwswebdev/gatsby-remark-embed-appietoday.git

yarn add gatsby-remark-embed-appietoday
```

2. Add following to your `gatsby-config.js`:
```js
    plugins: [      
      {
        resolve: "gatsby-transformer-remark",
        options: {
          plugins: [
          {
            resolve: "gatsby-remark-embed-appietoday",
            options: {
              width: 800,
              ratio: 1.77, // Optional: Defaults to 16/9 = 1.77
              height: 400, // Optional: Overrides optional.ratio
              related: false //Optional: Will remove related videos from the end of an embedded YouTube video.
            }
          }
          ]
        }
      },
```

Note: if you also rely on `gatsby-remark-responsive-iframe`, you have to define the embed-youtube plugin first:
``` js
plugins: [
  "gatsby-remark-embed-appietoday",
  "gatsby-remark-responsive-iframe"
]
```

3. Restart gastby.

## Usage

```markdown
# Look at this Video:

`appietoday: 2920803`

```


## License

MIT