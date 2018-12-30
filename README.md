# Toast theme for Hugo

[Hugo-Toast](https://aymericgerardin.github.io/hugo-toast-site/) is adapted from the [Hugo-initio](https://miguelsimoni.github.io/hugo-initio-site/) theme.

### Original Template Info

**Licensing:** MIT (for more options, go to the [original template site](https://miguelsimoni.github.io/hugo-initio-site/))  
**Designer:** Miguel Simoni  

## Installation

```
$ cd /<your-hugo-site-directory>
$ git submodule add https://github.com/aymericgerardin/hugo-toast.git themes/hugo-toast
```

More info: [hugo setup guide](https://gohugo.io/overview/installing/)

## Configuration

[Example Site](https://github.com/aymericgerardin/hugo-toast/tree/master/exampleSite)

[config.toml](https://github.com/aymericgerardin/hugo-toast/tree/master/exampleSite/config.toml)

### Sections


```toml
showSubheader = true
showServices = true
showRecentWorks = false
showDownload = false
showClients = false

footerEnableContact = true
footerEnableFollowme = true
footerEnableMailChimpWidget = true
```
### Social Networks Icons

You can add as many social networks as you want in the params.social array following this template:

```toml
[[params.social]]
  title = "facebook"
  url = "https://www.facebook.com/nickname"
  icon = "fa-facebook-square"
  footer = true
  sharethis = true
  network = "facebook"
```

See the whole configuration in the [config.toml](https://github.com/aymericgerardin/hugo-toast/tree/master/exampleSite/config.toml) file.

### Comments

Powered by [Disqus](https://disqus.com)

```toml
[params.disqus]
    site = "your-disqus-short-name"
```

Disable the comments system by leaving the `params.disqus.site` empty.

### Google Analytics

```toml
[params.google.analytics]
    trackerID = "GA-000000000-0"
```

Disable the Google Analytics by leaving `params.google.analytics.trackerID` empty.

### Almost there...

In order to see your site in action, you can run Hugo's built-in local server.

```
$ hugo server -D
```

Now enter [`http://localhost:1313/`](http://localhost:1313/) in the address bar of your browser.

## Deployment

- [Hosting on GitHub](https://gohugo.io/hosting-and-deployment/hosting-on-github/)
- [More hosting and deployment options](https://gohugo.io/hosting-and-deployment/)

## Contributing

- Found a bug?
- Got an idea for a new feature?

Let me know it using the [issue tracker](https://github.com/aymericgerardin/hugo-toast/issues).
Or make it directly: [pull request](https://github.com/aymericgerardin/hugo-toast/pulls).

## License

This port is released under the MIT License. 

## Thanks

Thanks to [Steve Francia](https://github.com/spf13) for creating Hugo and the awesome community around the project. And also thanks to [Sergey Pozhilov](http://www.gettemplate.com/) for creating this awesome theme.
