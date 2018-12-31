# Toast theme for Hugo

[Hugo-Toast](https://aymericgerardin.github.io/hugo-toast/) is adapted from the [Hugo-initio](https://miguelsimoni.github.io/hugo-initio-site/) theme.

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

[Example Site](https://aymericgerardin.github.io/hugo-toast/exampleSite)

[config.toml](https://github.com/aymericgerardin/hugo-toast/exampleSite/config.toml)


### Home page layout

#### Sub header section

```toml
showSubheader = true
```
When activating showSubheader you need a subheader.md markdown in your content folder with title and content. It will display this content on the home page just after the header

#### Service catalog

```toml
showServices = true
```
When activating showServices you need a section in your content folder, in this section you need pages for each service with this information:
* title: the title of the service
* image: image path in static folder for this service
* the content to be displayed after the image
Currently the layout is setup assuming 3 services pages, so Bootstrap column set to 4 

@TODO compute dynamicaly the Bootstrap column number based on the services pages number

#### Where Section

```toml
showWhere = true
```
When activating showWhere you will need:
* a where.md file in your content folder with 
..* title: the title of the section in the home page
..* content: the content displayed on the right column of the section
* a googlemap.md file in the content folder of your website, this file should contain the googlemap embedded code for you location.
..* You need to change the width and height of this code to 400, 400

```html
<!-- google embended iframe -->
	<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d6216.966082917585!2d-104.86987163358975!3d39.5521443406065!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x876c85750d25588d%3A0x7f20747ef1bbb6ca!2sToastmasters+International!5e0!3m2!1sen!2sfr!4v1546194840317" width="400" height="400" frameborder="0" style="border:0" allowfullscreen></iframe>
<!-- google embended iframe -->   
```

### Footer layout
The footer layout assume 3 sections activated (3 columns for Bootstrap configuration)
@TODO compute dynamicaly the Bootstrap column number based on sections activated

#### MailChimp subscribe to newsletter form

```toml
footerEnableMailChimpWidget = true
```
When activating footerEnableMailChimpWidget you will need:
* a mailchimp.md file in your content folder with 
..* the embedded mailchimp code generated on the mailchimp website
..*	remove the fff background color markup
..* remove any blank line in the file

```html
<!-- Begin Mailchimp Signup Form -->
<link href="//cdn-images.mailchimp.com/embedcode/slim-10_7.css" rel="stylesheet" type="text/css">
<style type="text/css">
	#mc_embed_signup{clear:left; font:14px Helvetica,Arial,sans-serif;  width:300px;}
	/* Add your own Mailchimp form style overrides in your site stylesheet or in this style block.
	   We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. */
</style>
<div id="mc_embed_signup">
<form action="" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
    <div id="mc_embed_signup_scroll">
	<input type="email" value="" name="EMAIL" class="email" id="mce-EMAIL" placeholder="adresse email" required>
    <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
    <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="" tabindex="-1" value=""></div>
    <div class="clear"><input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button"></div>
    </div>
</form>
</div>
<!--End mc_embed_signup-->  
```

#### Follow me section

```toml
footerEnableFollowme = true
```
When activating footerEnableFollowme please fill the "Social Networks" configuration section below

#### Contact section

```toml
footerEnableContact = true
```
You need the address and email field setup 
@TODO add google map option in this section


### Social Networks

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

See the whole configuration in the [config.toml](https://github.com/aymericgerardin/hugo-toast/exampleSite/config.toml) file.

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
$ hugo server
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

Thanks to [Steve Francia](https://github.com/spf13) for creating Hugo and the awesome community around the project. And also thanks to [Sergey Pozhilov](http://www.gettemplate.com/) for creating this awesome theme and also Miguel Simoni [Hugo-initio](https://miguelsimoni.github.io/hugo-initio-site/)
