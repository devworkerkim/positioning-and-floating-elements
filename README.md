# Positioning And Floating Elements | The Odin Project

This is the repo for the Positioning And Floating Elements project in the HTML And CSS course of The Odin Project.  The project was to recreate an [article from the New Scientist](https://www.newscientist.com/article/2286218-ancient-lake-in-marss-gale-crater-may-have-actually-been-a-small-pond/).

## What I Learned

### Gap In Flexbox

I had no clue that the gap property existed for flexbox.  All this time I had been setting the spacing between my items with the margin and padding on the items.  I use a lot of `space-between` for my item spacing, so `gap` has come in real handy.

### Floats

There was a section in the webpage that I figured would be a good opportunity to use the float property.  It was an image that was supposed to be float left with some text to the right of it.  Floating the image to the left was the easy part, but trying to get elements out of the flow line and where I wanted them to go was a pain.  I did find this article [All About Floats](https://css-tricks.com/all-about-floats/) that offered the few standard workarounds for managing flow with floats.  I chose to explicitly define the overflow of the parent element to clear the float for the section I had afterwards.  I originally had the `clear` property in the subsequent section's styling, but I wasn't able to get the whitespace to separate the sections unless I extended beyond what would clear the remaining float space.

### Right Side List Markers

In the sidebar, the example page has this weird listing where the list marker is located on the right side instead of the standard left.  I was able to replicate the look by using the `direction` property to flip the list marker over to the right side as per the article [Display UL bullets and OL numbers on the right side](https://coursesweb.net/html/display-bullets-numbers-right-side_t).  However, going right to left on the direction has left my punctuations on the left hand side.  I tried removing the dot in the ordered list marker like the post [Ordered List without the Period?](https://stackoverflow.com/questions/5945161/html-css-ordered-list-without-the-period) but I was left with what would have been the marker to just follow the text from the item.

### :not()

Just when I thought I had all the selectors I needed, I come to find that there is a way to exclude certain elements.  Using this negation pseudo class, `:not()` will not apply the defined properties to any selector inserted in the parentheses.  I thought I would give this one a try and use it to find all the elements except for the paragraph elements that needed the serif fonts.  It worked like a charm and I didn't have to individually go through setting all the fonts for each element.  This article on [:not from CSS Tricks](https://css-tricks.com/almanac/selectors/n/not/) helped a lot.