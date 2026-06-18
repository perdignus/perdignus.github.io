---
layout: post
title: "A brave new world"
date: 2026-06-18
categories: blog
---

# A beginning

> How to get to a blank page in the first place.

So you have some free time, a couple of ideas for a hobby, a bit of money to spend. You think to yourself "Man, I should start a blog, or at least a website. How hard can it be?"

Turns out, not very hard, except if you overcomplicate it.
This page is a short journey about how I have gotten around to creating this blog, and maybe to inspire some other poor sod to do the same.

## My beginning

Alright, you met the criterea above, and are actually starting to acquire and turn on a website. But where to start?
In my case, that is with a DNS. You could, of course, just not use a custom DNS/hostname. But then you are stuck with often times a non personal somewhat ugly hostname.
Thus the hunt for a DNS.

For those that do not know, there is a whole market of DNS names. That name at the top of your browser is worth someting to someone, thus it will be traded. Popular domains will cost more than some obscure sentence combined with a sketchy top-level-domain (the part after the `.` in the url).
For example, `blog.com` probably costs a lot. Both to purchase at first, and then to renew each year.  
But `myoriginalideatostartablog.it.xyz` might only cost 50 cent a year.

So you think, alright lets get brainstorming for a fun domain name! It should be somewhat relevant to what you want to do, but also obscure enough that nobody else has already claimed it, and is not so obvious as to be worth more on the market.
My first start in this is often to go for latin or other languages, and translate a bunch of words or concepts and see what comes out the other end.
The second step is to grab a dictionary, digitally nowadays, so that you can lookup synonyms for the previous results.
Repeat and iterate untill satisfied... Which differs from person to person, and I just stopped when I had three fine options and had already spent half an hour on it.

Well, jobs done then! The difficult part is over, as naming things is one of the _hard_ problems in tech. So now it should just be a matter of registering it and foila!

That turned out to be the somewhat easier part. For I would spent the hour or so comparing various DNS registars for their offerings of the same domain, often with wildly differing prices!  
What went for just €5,- in one provider, could go to 25,- or up to 50,- in some cases... (per year!)
And then there is the matter of rendered services, such as privacy and ease of use.

Oh well, in the end I found out about the ICANN. Which is the Internet Corporation for Assigned Names and Numbers, basically a non profit watchdog to keep dns in check. They accredit registars, so that you know they are a stable option to select. And so I did. As I am based in Europe, I currently value that my internet is somewhat kept within the EU.
To that end, I selected for a provider that is also in the EU. This was definetely not the cheapest option available. In the end, I also just had to chose, as it had been a long day, and I wanted a website darn it!

## Domain expension: vacillation

Fancy that, a domain name to call your own. But no where to use it on yet.
Now it was time to ask myself, what kind of site do I want to blog on?

Something like wordpress? Build a website from scratch or Skratch? Maybe something in between?
I wanted to reduce the hassle, but still have a decent website to call my own. So I settled for a static web site, meaning no real backend. What you see is what you get.
Ideally something where I can just type in some markdown file, and it magically transforms into html.

Now, I was originally intending to host the whole thing on Azure in some free tier. But then I saw advice that Github pages is free as well, but also has a build in static site generator. That seemed like a great idea, thus that is what you are probably looking at.

## Getting it up

A domain name, something to generate the site, and somewhere to put it. Case closed?
Not yet it isn't.

For you see, I have no experience hosting a website or managing DNS. It turns out, you can not just point github to a dns, and say: go go static website. And then expect it to work.  
It required finicking with CNAMEs, A and AAAA records, and a lot of debugging and thrawling through documentation to get it working.

You first need to (or should) verify with github that the domain is actually yours. That is done through editing your DNS records to include some magic text that github provides.
Then afterwards you need to map the default github static webpage domain to your DNS and vice versa.  
It got complicated further by me using a .dev extension. That requires the site to use HTTPS, and thus require a certificate. I did not however realise that this is already included in github services by default.

Luckilly, there are very helpful (but just as many confusing) posts on the internet. And when in doubt, it is possible to point an agent at the problem and have it hallucinate the correct solution for you.

The end result? This page, which will definetely see some different styling, layout and all such over the coming period of time.
Maybe that will become its own page, but as a starting point this is good enough.