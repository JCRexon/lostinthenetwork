+++
title = "Setting Up This Blog"
date = 2024-05-06T14:50:07+01:00
draft = false
+++

Hi there 👋

I want to briefly share with you how I got this blog up and running. Nowadays, it is much easier to stand up a static blog site and publish content. I will provide a short commentary and links where appropriate.

I started off by considering what tool I wanted to use for the code that underpins the site. After researching options, I was left with a decision between Pelican and Hugo. I settled on Hugo, as Hugo is built on Golang, and the quick start was more accessible to me at the time. Check out the quick start documentation here:

<https://gohugo.io/getting-started/quick-start/>

Once I got the test site up and running, my attention turned to themes. Themes in Hugo are ways to change the appearance of your site by leveraging the contributions of the Hugo ecosystem. In my case I settled on the ‘PaperMod’ theme from Aditya Telange. I love the minimalist design combined with deep functionality. You can find the theme here:

<https://themes.gohugo.io/themes/hugo-papermod/>

My site was functional and pretty. However, my blog was isolated to my localhost which is not a recipe for mainstream success. I had previously hosted a site before, but it was through a hosting provider (I didn’t rate them highly) and I wanted to do it differently this time. The advances of cloud computing have lowered the barrier to entry for many things on the Web. In this case, I leveraged AWS Amplify to host my static site.

I had never used AWS Amplify before, so I didn’t even know where to start. In fact, I started off by spinning up a new Lightsail instance before reconsidering – my thought was, ‘Why do I need the full overhead of a VM?’ I doubled back to the Hugo documentation and found the following page:

<https://gohugo.io/hosting-and-deployment/hosting-on-aws-amplify/>

I followed the prescriptive steps, et voilà! You may need to do some tweaking to get yours up and running, but I barely did anything beyond the steps outlined in the above link. You may want to create a domain specifically for your site, in that case you can follow the built-in steps on AWS Amplify.

That’s it! I now have a site up and running that, I confess, I still I need to tweak. This is a marathon, not a spring, over time I will address the oddities you may encounter when using this blog.
