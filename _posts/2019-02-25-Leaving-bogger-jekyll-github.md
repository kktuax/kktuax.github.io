---
layout: post
title: "Leaving Blogger in favor of Jekyll and GitHub"
tags: [jekyll, github, blogger, blog]
---

For almost 6 years, this blog had been hosted at [Blogger](https://www.blogger.com/), and it was a pretty decent experience: you can get up and running with your blog pretty fast. They supported using your own domain which was exactly what I was looking for. However, I was not so comfortable hosting my site on Google: since they [decided to kill Google Reader](https://googleblog.blogspot.com/2013/03/a-second-spring-of-cleaning.html), I was a bit skeptical that they will shut down the service at any point. Anyway, I had to do something with the blog: it was still using HTTP and, since HTTPS if finally gaining traction (thank you [Let's encrypt](https://letsencrypt.org/)!), I was planning to configure SSL sooner than later.

## Jekyll and Github to the rescue

I've been for a while interested in static page generators: it makes a lot of sense for web pages that are not so often updated (such as, unfortunatelly, my blog). In the end, it's the ultimate caching: you generate the contents in advance, and then you just serve the static content. There are other engines, but [Jekyll](https://jekyllrb.com) has become really popular nowadays. GitHub [supports them for GitHub Pages](https://help.github.com/en/articles/about-github-pages-and-jekyll) and they even have an [Blogger import plugin](https://import.jekyllrb.com/docs/blogger/)! Seemed like the perfect match.

## From zero to blog in a few steps

After a small research on GitHub, I found a template of my liking: [Type-on-Strap](https://github.com/sylhare/Type-on-Strap). I [forked the repo](https://github.com/kktuax/kktuax.github.io), renamed it to 
`myusername.github.io` and in a few clicks I had a working site published on Github! The next step was to setup my domain, which was also quite easy. I added in [my domain's DNS configuration](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages) four A entries pointing to:
 * 185.199.108.153
 * 185.199.109.153
 * 185.199.110.153
 * 185.199.111.153

Then, from GitHub's repo settings, I just had to [add the domain](https://help.github.com/en/articles/adding-or-removing-a-custom-domain-for-your-github-pages-site) and select to force HTTPS. Et voilà! My domain was working and they automatically created a certificate for me.

## Conclusion

Now becomes the really hard part: putting your own content, but so far I'm happy with the change. And if eventually GitHub decides to shut down this free service, I can just generate locally the content with Jekyll and host it on a dumb server somewhere else.
