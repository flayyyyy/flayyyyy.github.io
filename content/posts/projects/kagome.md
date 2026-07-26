---
title: "Superconductivity in Kagome Metal AV3Sb5"
displayTitle: "Superconductivity in Kagome Metal AV<sub>3</sub>Sb<sub>5</sub>"
description: "Exploring a novel topological superconductor"
publishDate: "20 May 2023"
tags: ["projects"]
updatedDate: 27 July 2026
---

## Problem

1. Add a link on your homepage to either your GitHub profile and/or email address as per [IndieLogin's](https://indielogin.com/setup) instructions. You _could_ do this via `src/components/SocialList.astro`, just be sure to include `isWebmention` to the relevant link if doing so.
2. Create an account @ [Webmention.io](https://webmention.io/) by entering your website's address.
3. Add the link feed and api key to a `.env` file with the key `WEBMENTION_URL` and `WEBMENTION_API_KEY` respectively, you could rename `.env.example` found in this template. You can also add the optional `WEBMENTION_PINGBACK` link here too.
4. Go to [brid.gy](https://brid.gy/) and sign-in to each social account[s] you wish to link.
5. Publish and build your website, remember to add the api key, and it should now be ready to receive webmentions!

## What is the BdG framework

Put simply, it's a way to show users who like, comment, repost and more, on various pages on your website via social media.

This theme displays the number of likes, mentions and replies each blog post receives. There are a couple of more webmentions that I haven't included, like reposts, which are currently filtered out, but shouldn't be too difficult to include.

## Exploring the unknown: Kagome

Your going to have to create a couple of accounts to get things up-and-running. But, the first thing you need to ensure is that your social links are correct.

### Linking it to the experiments

Firstly, you need to add a link on your site to prove ownership. If you have a look at [IndieLogin's](https://indielogin.com/setup) instructions, it gives you 2 options, either an email address and/or GitHub account. I've created the component `src/components/SocialList.astro` where you can add your details into the `socialLinks` array, just include the `isWebmention` property to the relevant link which will add the `rel="me authn"` attribute. Whichever way you do it, make sure you have a link in your markup as per IndieLogin's [instructions](https://indielogin.com/setup)

```html
<a href="https://github.com/your-username" rel="me">GitHub</a>
```

### Further work: arXiV

Next, head over to [Webmention.io](https://webmention.io/) and create an account by signing in with your domain name, e.g. `https://astro-cactus.chriswilliams.dev/`. Please note that .app TLDs don't function correctly. Once in, it will give you a couple of links for your domain to accept webmentions. Make a note of these and create a `.env` file (this template include an example `.env.example` which you could rename). Add the link feed and api key with the key/values of `WEBMENTION_URL` and `WEBMENTION_API_KEY` respectively, and the optional `WEBMENTION_PINGBACK` url if required. Please try not to publish this to a repository!

:::note
You don't have to include the pingback link. Maybe coincidentally, but after adding it I started to receive a higher frequency of spam in my mailbox, informing me that my website could be better. TBH they're not wrong. I've now removed it, but it's up to you.
:::

## Acknowledgements

Many thanks to [Kieran McGuire](https://github.com/chrismwilliams/astro-theme-cactus/issues/107#issue-1863931105) for sharing this with me, and the helpful posts. I'd never heard of webmentions before, and now with this update hopefully others will be able to make use of them. Additionally, articles and examples from [kld](https://kld.dev/adding-webmentions/) and [ryanmulligan.dev](https://ryanmulligan.dev/blog/) really helped in getting this set up and integrated, both a great resource if you're looking for more information!
