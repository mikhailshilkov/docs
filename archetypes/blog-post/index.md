---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
meta_image: meta.png
authors:
    - joe-duffy
tags:
    - some-tag
---

Summarize the post. What you put here will appear on the index page. In most cases, you'll also want to add a Read More link after this paragraph (though technically, that's optional). To do that, just add a comment like the one below.

<!--more-->

And then everything _after_ that comment will appear on the post itself.

Posts are written in [Markdown](https://daringfireball.net/projects/markdown/) and rendered with [BlackFriday](https://github.com/russross/blackfriday).

## Headings Are Generally Title-Cased

Just something to keep in mind.

## Code Blocks

[Syntax highlighing](https://gohugo.io/content-management/syntax-highlighting/) is handled by Hugo with code fences, along with an optional language specifier. Here, we're specifying `typscript`, but there are [other languages available](https://gohugo.io/content-management/syntax-highlighting/#list-of-chroma-highlighting-languages) as well.

```typescript
let bucket = new aws.s3.Bucket("stuff");
...
```

If you don't want any syntax highlighting, just leave out the language bit:

```
Like this, for example.
```

## Images

To add images to your post, place them alongside this file (or within the folder containing it), then reference them relatively:

![Placeholder Image](meta.png)

### The Meta Image

The image you specify as a `meta_image` in your post's frontmatter will be used for rendering [OpenGraph](http://ogp.me/) previews &mdash; Twitter cards, Slack previews previews and the like. For best results, we recommend the following specs, based on the [Twitter dev docs](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards):

Aspect Ratio  | Size          | Format  | Background
------------- | ------------- | ------- | ------------------------
2:1           | 1600×800      | PNG     | Opaque (No Transparency)

Previewing your post as you develop can be a little tricky. The [Twitter Card Validator](https://cards-dev.twitter.com/validator) is a helpful tool, but it requires a publicly accessible URL, so one thing you can do is

## Other Media

If you'd like to embed a YouTube video, Hugo has a [shortcode](https://gohugo.io/content-management/shortcodes/) for that also:

{{< youtube "kDB-YRKFfYE" >}}

And one for Tweets, too:

{{< tweet 1147203941609984002 >}}
