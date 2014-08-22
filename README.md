Egesoft Blog
====

Company blog.

#Posts

Posts are under `_posts` directory in Markdown format. You can find the documentation of Markdown at [Daring Fireball](http://daringfireball.net/projects/markdown) if you need it.

##Publish a Post

- Create an empty file under `_posts` with naming: `YYYY-MM-DD-post-title.md`.
- Add config header:
```yaml
---
layout: post
title: "Post Title"
category: "Post Category"
tags: [tag1, tag2, tag3]
author: author-shortname
---
```
- Add content below the header.

That's it commit the changes and push them to the `gh-pages` branch.

#Config

All of the configurations can be found on `_config.yml`.

##Author Info

In order to display your information on your posts there should be a configuration on `_config.yml`.

Notice the `authors` key on the yaml file. Add your information below it with your unique desired short name. You will be adding this shortname to the post headers as well.

Example config:

```yaml
 authors:
   selami:
     name: Selami Şahin
     emailHash: 1bdf09922951ed72da5e0a6b3b12bf40
     bio: 'Valuable Turkish musician.'
     web: 'http://selamisahin.com.tr'
```

`emailHash` value is the md5 encoding of the email address. This is used for Gravatar images. Simply calculate it on [md5.cz](http://md5.cz) with your Gravatar email address.

#Credits

- [Jekyll](http://jekyllrb.com/)
- [Lanyon Theme](http://lanyon.getpoole.com/)

#Author
- İsmail Demirbilek ([@dbtek](https://twitter.com/dbtek))