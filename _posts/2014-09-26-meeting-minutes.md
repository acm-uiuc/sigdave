---
layout: post
title:  "Reboot Fall 2014"
---

Hey, so we're going to start up meeting minutes again since SIGDave is back in full swing.

# Last Meeting (9/19/14)

Last week we went over designs and plans for the Food Button. There were 2 basic
designs for the Food Button that we explored:

- Note PLEEEEEASE let me know if you can think of better names for the designs :p 

## Design 1: Food Button Microwave

<img src="{{ site.baseurl }}images/food_button_microwave.jpg" />


## Design 2: Flexistand

<img src="{{ site.baseurl }}images/flexistand_btn.jpg" />

# This Meeting (9/26/14)

We decided to go with the Flexistand design. Here is a rough outline of the specification:

- [ ] Build small enclosure (about 3" x 6") to house components
- [X] Big red button (about 3" x 3") acts as switch
- [ ] Beagle Bone Black acts as controller (3.5" by 2.1")
- [ ] Lamp to serve as camera mount/lighting
- [X] Web Cam
- [ ] Connection to internet (to post to twitter or mailing list)
- [ ] Web Cam extension cable

### Optional Features

- Face Plate for ports
- LED rope + transparent edges (Light up when taking picture)


## Posting on Twitter

So as promised, here is a quick demo of how easy it is to post onto twitter....
I've gone ahead and setup the twitter account [TheFoodButton](https://twitter.com/TheFoodButton).
After setting up API KEYs and OAUTH access, this was all that was required using Twython

{% highlight python %}
from twython import Twython

twitter = Twython(APP_KEY, APP_SECRET,
                  OAUTH_TOKEN, OAUTH_SECRET)
                  
with open('anakin-its-working-o.gif', 'rb') as f:
    twitter.update_status_with_media(media=f, status="It's Working!")
{% endhighlight %}

I considered using the [requests](http://docs.python-requests.org/en/latest/) library, but since
the Twitter API is a moving target I opted for a twitter specific wrapper.

Email should also be pretty easy, so no worries there.

Either way it looks like we have a decent crowd this year. We'll start actively developing starting next week.

- Marcell V.C
