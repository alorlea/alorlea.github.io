---
layout: page
title: Curriculum Vitae
description: "My professional portfolio"
image:
  feature: 2-point_half.png
  credit: imgkid
  creditlink: http://imgkid.com/blue-tech-background.shtml
share: true
---

## Profile

Telecommunication Engineer major in Distributed Systems with interest in information technology services. Distributed
Computing and large scale systems have become areas I really like to hear about. I am an
ambitious Software Engineer with great interest in new problems and challenges. That is why I show a proactive
personality where I always train myself in new trends and technologies improving my easiness to grasp technologies.

---

## Work Experience

### Software Developer                                                                         [February 2014 - Present]

**[Comeon! Stockholm AB](http://www.comeon.com/)**

**Server side:** Java programming with Servlets, Tomcat and REST services based on drop wizard. Frontend: JavaScript,
Angular JS and JQuery. ***Data layer*** uses mainly MySQL, Neo4j, MongoDB. ***Testing*** includes Junit and Mockito for mocking.
***Version Control*** migrated from SVN to git.

### Research Engineer                                                                         [June 2013 - January 2014]

**[SICS-Swedish Institute of Computer Science	](http://www.sics.se/)**

**Technology:** Java, Maven, Glassfish, cloud technologies used like Amazon EC2 and Open Stack for prototyping and testing.

**_Accomplishments:_**

- Cluster management interface to allow provisioning a cluster through a web wizard from scratch.
-	Implementation of an interface to retrieve deployment progress of a cluster.
-	Bundling of an Amazon Machine Image (AMI) with our predefined software to increase the deployment speed.
-	Bundling of a Virtual Image for Open Stack to offer the same solution as Amazon EC2.
-	Orchestration development for deployment in Bare Metal physical machines.

### Master Thesis in SICS                                                                          [Jamuary 2013 - June 2013]

**[SICS-Swedish Institute of Computer Science	](http://www.sics.se/)**

**Thesis Work: KTHFS Orchestration – Platform as a Service orchestration for Hadoop.**

Design and implementation of a Domain Specific Language for cluster deployment platform to configure Hadoop clusters in Amazon EC2 and Open Stack cloud infrastructures.
**_Supervisor: Dr. Jim Dowling, Examiner: Prof. Seif Haridi_**

<div markdown="0"><a href="http://kth.diva-portal.org/smash/get/diva2:648868/FULLTEXT01.pdf" class="btn">Download the Thesis</a></div>

**_Accomplishments:_**

-	Design orchestration architecture with jclouds, chef and YAML, implemented 2 artifacts based on this design:
	* Implemented a web portal using Java Server Faces with Primefaces that configures a web application with a monitoring application, KTHFS Dashboard.
	* Integrated orchestration architecture in KTHFS Dashboard that allows deployment of a Hadoop cluster with chef and jclouds from a cluster defined in a YAML file.
- Optimize the orchestration architecture, managed to reduce the deployment time by increasing the throughput through asynchronous Future constructs.

### Software Developer                                                                        [July 2010 - February 2011]

**[GSI - Group of Intelligent Systems at ETSIT UPM.]**

**Technology:** Primarily Java programming and software development on this language

---

## Educational Background

### Degree Master of Science, Software Engineering of Distributed Systems (M.Sc.)                [August2011- June2013]
**[KTH – Royal Institute of Technology](http://www.kth.se/)**

**_Master student in parallel with my double degree studies which includes Swedish language courses._**

### Telecommunications Engineering (Equivalent to MSc level accredited by ABET/EAC)           [September 2005- June2013]
**[Technical University of Madrid (UPM)](http://www.etsit.upm.es/index.php/en/)**

**_Double Degree program KTH + UPM, Erasmus exchange program_**

---


{% highlight yaml %}
title:            Site Title
description:      Describe your website here.
disqus_shortname: shortname
# Your site's domain goes here (eg: //mmistakes.github.io, http://mademistakes.com, etc)
# When testing locally leave blank or use http://localhost:4000
url:              //mmistakes.github.io

# Owner/author information
owner:
  name:           Your Name
  avatar:         avatar.jpg
  bio:            "Your bio goes here. It shouldn't be super long but a good two sentences or two should suffice."
  email:          you@email.com
  # Social networking links used in footer. Update and remove as you like.
  twitter:        
  facebook:       
  github:         
  stackexchange:  
  linkedin:       
  instagram:      
  flickr:         
  tumblr:         
  # google plus id, include the '+', eg +mmistakes
  google_plus:    +yourid

# Analytics and webmaster tools stuff goes here
google_analytics:   
google_verify:      
# https://ssl.bing.com/webmaster/configure/verify/ownership Option 2 content= goes here
bing_verify:         

# http://en.wikipedia.org/wiki/List_of_tz_database_time_zones
timezone:    America/New_York
future:      true
pygments:    true
markdown:    kramdown

# Amount of posts to show on home page
paginate: 5
{% endhighlight %}

---

## Running Jekyll

If `jekyll build` and `jekyll serve` throw errors you may have to run Jekyll with `bundled exec` instead.

> In some cases, running executables without bundle exec may work, if the executable happens to be installed in your system and does not pull in any gems that conflict with your bundle.
>
>However, this is unreliable and is the source of considerable pain. Even if it looks like it works, it may not work in the future or on another machine.

{% highlight text %}
bundle exec jekyll build

bundle exec jekyll serve
{% endhighlight %}

---

## Folder Structure

{% highlight bash %}
hpstr-jekyll-theme/
├── _includes
|    ├── browser-upgrade.html       # prompt to upgrade browser on < IE8
|    ├── footer.html                # site footer
|    ├── head.html                  # site head
|    ├── navigation.html            # site navigation
|    └── scripts.html               # jQuery, plugins, GA, etc
├── _layouts
|    ├── page.html                  # page layout
|    ├── page.html                  # post-index layout used on home page
|    └── post.html                  # post layout
├── _posts
├── _sass                           # Sass partials
├── assets
|    ├── css                        # compiled stylesheets
|    ├── js
|    |   ├── _main.js               # plugin options
|    |   ├── scripts.min.js         # concatenated and minifed site scripts
|    |   ├── plugins                # plugin scripts
|    └── └── vendor                 # jQuery and Modernizr scripts
├── images                          # images for posts and pages
├── _config.yml                     # Jekyll options
├── about/                          # about page
├── posts/                          # all posts
├── tags/                           # all posts grouped by tag
└── index.html                      # home page with pagination
{% endhighlight %}

---

## Customization

Most of the variables found here are used in the .html files found in `_includes` if you need to add or remove anything. A good place to start would be to add the `title`, `description`, and `url` for your site. Links are absolute and prefixed with `{{ "{{ site.url " }}}}` in the various `_includes` and `_layouts`, so remember to properly set `url`[^1] to `http://localhost:4000` when developing locally.

### Disqus Comments

Create a [Disqus](http://disqus.com) account and change `disqus_shortname` in `_config.yml` to the Disqus *shortname* you just setup. By default comments appear on all post and pages if you assigned a shortname. To disable commenting on a post or page, add the following to its YAML Front Matter:

{% highlight yaml %}
comments: false
{% endhighlight %}

### Social Share Links

To enable Facebook, Twitter, and Google+ share links on a post or page, add the following to its front matter:

{% highlight yaml %}
share: false
{% endhighlight %}

### Owner/Author Information

Change your name, and avatar photo (200x200 pixels or larger), email, and social networking URLs. If you want to link to an external image on Gravatar or something similar you'll need to edit the path in `head.html` since it assumes it is located in `/images`.

### Google Analytics and Webmaster Tools

Your Google Analytics ID goes here along with meta tags for [Google Webmaster Tools](http://support.google.com/webmasters/bin/answer.py?hl=en&answer=35179) and [Bing Webmaster Tools](https://ssl.bing.com/webmaster/configure/verify/ownershi) site verification.

### Navigation Links

To add additional links in the drop down menu edit `_data/navigation.yml`. Use the following format to set the URL and title for as many links as you'd like. *External links will open in a new window.*

{% highlight yaml %}
- title: Portfolio
  url: /portfolio/

- title: Made Mistakes
  url: http://mademistakes.com  
{% endhighlight %}

---

## Adding New Content with Octopress

While completely optional, I've included Octopress and some starter templates to automate the creation of new posts and pages. To take advantage of it start by installing the [Octopress](https://github.com/octopress/octopress) gem if it isn't already.

{% highlight bash %}
$ gem install octopress --pre
{% endhighlight %}

### New Post

Default command

{% highlight bash %}
$ octopress new post "Post Title"
{% endhighlight %}

Default works great if you want all your posts in one directory, but if you're like me and want to group them into subfolders like `/posts`, `/portfolio`, etc. Then this is the command for you. By specifying the DIR it will create a new post in that folder and populate the `categories:` YAML with the same value.

{% highlight bash %}
$ octopress new post "New Post Title" --dir posts
{% endhighlight %}

### New Page

To create a new page use the following command.

{% highlight bash %}
$ octopress new page new-page/
{% endhighlight %}

---

### Jekyll _includes

For the most part you can leave these as is since the author/owner details are pulled from `_config.yml`. That said you'll probably want to customize the copyright stuff in `footer.html` to your liking.

### Reading Time

On by default. To turn off remove `reading_time` from `_config.yml. Default words per minute is set at 200 and can changed by updating `words_per_minute` in `_config.yml`.

### Feature Images

A good rule of thumb is to keep feature images nice and wide so you don't push the body text too far down. An image cropped around around 1024 x 256 pixels will keep file size down with an acceptable resolution for most devices. If you want to serve these images responsively I'd suggest looking at the [Jekyll Picture Tag](https://github.com/scottjehl/picturefill)[^2] plugin.

The two layouts make the assumption that the feature images live in the *images* folder. To add a feature image to a post or page just include the filename in the front matter like so. 

{% highlight yaml %}
image:
  feature: feature-image-filename.jpg
  thumb: thumbnail-image.jpg #keep it square 200x200 px is good
{% endhighlight %}

If you want to apply attribution to a feature image use the following YAML front matter on posts or pages. Image credits appear directly below the feature image with a link back to the original source.

{% highlight yaml %}
image:
  feature: feature-image-filename.jpg
  credit: Michael Rose #name of the person or site you want to credit
  creditlink: http://mademistakes.com #url to their site or licensing
{% endhighlight %}

#### Post/Page Thumbnails for OG and Twitter Cards

Post and page thumbnails work the same way. These are used by [Open Graph](https://developers.facebook.com/docs/opengraph/) and [Twitter Cards](https://dev.twitter.com/docs/cards) meta tags found in `head.html`. If you don't assign a thumbnail the image you assigned to `site.owner.avatar` in `_config.yml` will be used.

Here's an example of what a tweet to your site could look like if you activate Twitter Cards and include all the metas in your post's YAML.

![Twitter Card summary large image screenshot]({{ site.url }}/images/twitter-card-summary-large-image.jpg)

### Videos

Video embeds are responsive and scale with the width of the main content block with the help of [FitVids](http://fitvidsjs.com/).

Not sure if this only effects Kramdown or if it's an issue with Markdown in general. But adding YouTube video embeds causes errors when building your Jekyll site. To fix add a space between the `<iframe>` tags and remove `allowfullscreen`. Example below:

{% highlight html %}
<iframe width="560" height="315" src="http://www.youtube.com/embed/PWf4WUoMXwg" frameborder="0"> </iframe>
{% endhighlight %}

### Twitter Cards

Twitter cards make it possible to attach images and post summaries to Tweets that link to your content. Summary Card meta tags have been added to `head.html` to support this, you just need to [validate and apply your domain](https://dev.twitter.com/docs/cards) to turn it on.

### Link Post Type

Link blog like a champ by adding `link: http://url-you-want-linked` to a post's YAML front matter. Arrow glyph links to the post's permalink and the the `post-title` links to the source URL. Here's an [example of a link post]({{ site.url }}/sample-link-post/) if you need a visual.

---

## Further Customization

Jekyll 2.x added support for Sass files making it much easier to modify a theme's fonts and colors. By editing values found in `_sass/variables.scss` you can fine tune the site's colors and typography.

For example if you wanted a red background instead of white you'd change `$bodycolor: #fff;` to `$bodycolor: $cc0033;`.

To modify the site's JavaScript files I setup a Grunt build script to lint/concatenate/minify all scripts into `scripts.min.js`. [Install Node.js](http://nodejs.org/), then [install Grunt](http://gruntjs.com/getting-started), and then finally install the dependencies for the theme contained in `package.json`:

{% highlight bash %}
npm install
{% endhighlight %}

From the theme's root, use `grunt` concatenate JavaScript files, and optimize .jpg, .png, and .svg files in the `images/` folder. You can also use `grunt dev` in combination with `jekyll build --watch` to watch for updates JS files that Grunt will then automatically re-build as you write your code which will in turn auto-generate your Jekyll site when developing locally.

---

## Questions?

Having a problem getting something to work or want to know why I setup something in a certain way? Ping me on Twitter [@mmistakes](http://twitter.com/mmistakes) or [file a GitHub Issue](https://github.com/mmistakes/hpstr-jekyll-theme/issues/new). And if you make something cool with this theme feel free to let me know.

---

## License

This theme is free and open source software, distributed under the [MIT License]({{ site.url }}/LICENSE) version 2 or later. So feel free to to modify this theme to suit your needs.

---

[^1]: Used to generate absolute URLs in `feed.xml`, and for canonical URLs in `head.html`. Don't include a trailing `/` in your base url ie: http://mademistakes.com. When developing locally I suggest using http://localhost:4000 or whatever localhost you're using to properly load all theme stylesheets, scripts, and image assets. If you leave this variable blank all links will resolve correctly except those pointing to home.

[^2]: If you're using GitHub Pages to host your site be aware that plugins are disabled. So you'll need to build your site locally and then manually deploy if you want to use this sweet plugin.