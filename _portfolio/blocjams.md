---
layout: post
title: Bloc Jams
thumbnail-path: "img/bloc_jams_bg.jpg"
short-description: Bloc Jams is a digital music player that provides unlimited, ad free streaming.

---

{:.center}
![]({{ site.baseurl }}/img/bloc_jams_bg.jpg)

## Explanation

Bloc Jams is a digital music player that lets people choose the music they want to listen to from a variety of albums that are provided. The free, unlimited, ad free streaming separates Bloc Jams from other digital music players. Bloc Jams is also available on all mobile platforms.

## Problem

I wanted to create a page that displayed all of the albums that Bloc Jams has to offer. This page would allow users to view and select the album that they wanted to listen to by simply clicking on it.

## Solution

I created three files for the collection page. The first two were the basic HTML and CSS files that set the foundation for the page and included links to essential files. I wanted to include a nav bar at the top of the page that included the Bloc Jams logo and contained the name of the current page that the user would be on (in this case the name of the page would be "collection").

{% highlight HTML %}
        <nav class="navbar"> <!-- nav bar -->
            <a href="index.html" class="logo">
                <img src="assets/images/bloc_jams_logo.png" alt="bloc jams logo">
            </a>
            <div class="links-container">
                <a href="collection.html" class="navbar-link">collection</a>
            </div>
        </nav>
{% endhighlight %}

The third file that I created was the Javascript file, in which I used jQuery to formulate some of the code. I created a template that would be used to display the information of all albums in an orderly fashion. I then used ```$(window).load``` method to load the album covers as thumbnails.

{% highlight Javascript %}
$(window).load(function() {
    var $collectionContainer = $('.album-covers');
    $collectionContainer.empty();

    for(var i = 0; i <12; i++) {
        var $newThumbnail = buildCollectionItemTemplate();
        $collectionContainer.append($newThumbnail);
    }
});
{% endhighlight %}


## Results

The code created a page that displayed all of the albums within Bloc Jams (12 in total) in 3 rows, each containing 4 items. Each item contained the name of the album, the album artist, and the number of songs in each album. The top of the page displayed a nav bar that consisted of the Bloc Jams logo, which was a link to the main page, and a link to the page that contained the collection of albums that Bloc Jams has to offer (the current page that the user would be on).

## Conclusion

I created a user friendly page that allowed users to view the collection of albums that Bloc Jams has to offer. Along with this, I created a nav bar that allows users to easily navigate though the site.
