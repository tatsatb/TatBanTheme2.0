# TatBanTheme2.0 

TatBanTheme2.0 is a minimal Hugo theme to build an elegant website and a working blog. The theme is built from scratch using responsive Bootstrap 5 framework.

**[Live demo is on Netlify](https://tatbanthemedemo.netlify.app/).**

Although it has 2.0 in its name, it is still a work-in-progress project. I will be adding more CSS (and hopefully some JS) elements in future releases.

The aim of this theme is not necessarily to provide a _plug and play_ framework, but to encourage people to get started with their own customizations. Pull requests are welcome. 


## Installation 

I am assuming Hugo is already installed in the system  as per the [official instructions](https://gohugo.io/getting-started/installing/) and you have created a Hugo site by running:

```shell
    hugo new site myawesomesite 
    cd myawesomesite
```

You can now install the theme by using either of these three ways:

1. **Clone**: Clone the theme repo into your `themes` folder (if you want to contribute to the theme in future or open pull requests) : 

```shell
git clone https://github.com/tatsatb/TatBanTheme2.0.git themes/TatBanTheme2.0
```

2. **Submodule**: Add As Git Submodule into your `themes` folder (if you currently have no plan of contributing to the theme):

```shell
    git init
    git submodule add https://github.com/tatsatb/TatBanTheme2.0.git themes/TatBanTheme2.0
```

3. For so-called _less-technical_ users: Simply install the theme by downloading the ZIP files by clicking the download option (under green _Code_ button), then extract the files, and then copy the folder to your site's `themes` folder. 




## Quickstart

1. In the root folder of your site (i.e. the `myawesomesite` folder), delete `config.toml` file. 

2. Copy the `config.toml` file from the `themes/TatBanTheme2.0 /examplesite` folder and paste into root `myawesomesite` folder and change the `baseURL` to your website's URL. 

3. Copy everything from `themes/TatBanTheme2.0/exmaplesite/content` folder to `myawesomesite/content` folder. 

4. Inside your terminal, go to `myawesomesite` directory and use the following command. 


```shell
    hugo server -D
```

You should see a working website. 

## Features 

1. **Fully responsive mobile-first theme**. It should look great in any screen. 
2. **Unique design**. The theme was designed from scratch. It is not a fork of any other Hugo/Jekyll/HTML5 theme or anything similar. 
3. **Bootstrap 5**. Elegant CSS framework and icon sets are included. 
4. **Blog-aware theme**. It can generate tags and categories pages by default.
5. **Comments are enabled**. Disqus is configured and enabled by default. 
6. **Separate page templates**. Because your blog posts, list pages, and Homepage should not look the same!
7. **SEO friendly**. Custom description meta-tag for each page.
8. **LaTeX is enabled**. Markdown _is_ great. However, sometimes we do need to write nice-looking equations. Hence, in this theme, LaTeX is integrated (using KaTex library).
9. **Custom HTML is enabled**. Once again, markdown is great. However, sometimes we do need some finer control. So you can directly type in HTML inside any .md files if you are using this theme. 


## Configuring your site

### Basics

The ground rule of customizing any aspect of website for your personal use is to follow the directory structure of theme and create similar directory and files at the site's root directory. 

You do not have to edit files in `themes` folder to edit your site configuration. As per Hugo's [lookup order](https://gohugo.io/templates/lookup-order/), your site's root directory's files will get precedence and Hugo will use your file (instead of theme's file) to render website. If you edit files directly in`themes` folder, your site may become incompatible with future versions of the theme. 


### Social media links

Copy `footer.html` from `themes/TatBanTheme2.0/layouts/partials/` to `myawesomesite/layouts/partials/` folder. Open the copied files in your favorite Text editor/IDE and edit the links to add your Facebook/Twitter/Linkedin/Email ID. 

 
 
### Custom CSS

The themes custom css file is in `themes/TatBanTheme2.0/static/css/`folder with name `banerstyle.css`. You can add your own in `myawesomesite/lstatic/css/` folder and update your sites `header.html` files in `myawesomesite/layouts/partials/` folder


You can add multiple custom stylesheets which will be loaded after the main theme css.
For example, the above line will load the CSS-file placed at `/static/css/custom.css`.



### Homepage settings

The theme uses a different css framework for landing page/homepage. It is located at `themes/TatBanTheme2.0/layouts/partials/index.html`. You can copy and paste in your sites layouts folder and then edit it as you like. If you prefer a simpler/minimal option, you can, of course, make a new homepage: 

Use `singlepage` layout, as found in `themes/TatBanTheme2.0/layouts/_default/` folder and write it in markdown as other pages are written.



### Disable HTML  editing  

As I said, I always feel that sometimes we do need HTML and CSS inside Markdown structure to add more flairs. Hence, in this theme HTML is enabled by default site wide. If you prefer the other way, please delete this part from your `config.toml`: 

```[markup]
    [markup.goldmark]
        [markup.goldmark.renderer]
            unsafe = true
```

You can still selectively add HTML inside your markdown by using `{{< rawhtml >}} _[Put your content here]_ {{< /rawhtml >}}` syntax which employs rawhtml.html shortcode.  


### Typing in LaTeX

To type any equation (or anything for that matter) using LaTeX framework, parameter ````math```` in the front-matter should be set to _true_. 


```shell
---
math: true
---
```

Then, please use double dollar signs to enclose the TeX typesetting. You can also use inline equations by enclosing with single dollar sign.


### Comment system on blog posts

Disqus Comments are enabled by default. Please  update your Disqus username in `disqusShortname` field of your site's `config.toml` file. If you have not signed up to Disqus, you can always [sign up for free](https://disqus.com/profile/signup/).

Just use `single` layout in front matter to make Disqus appear at the bottom of the pages. 


## License 

Copyright © 2022 Tatsat Banerjee

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see <https://www.gnu.org/licenses/>. 

 
