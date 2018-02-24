## Jekyll Test

A place to experiment with Jekyll and github Pages.

You can use the [editor on GitHub](https://github.com/grahamwhaley/jekyll_test/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/grahamwhaley/jekyll_test/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

# Blog
Can we get the blog to appear??

## One
{% for post in site.posts %}
{{ post.date | date_to_string }} » {{ post.title }}
{% endfor %}

## Two
{% for post in site.posts %}
<li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}

## Three
{% for post in site.posts %}
{{ post.url }}>{{ post.title }}
{% endfor %}

Did it work??

# embed blogs?

And let's try to embed our blog....

{% for post in paginator.posts %}
  <div class="postWrapper">
    <h2><a href="{{ post.url | remove_first:'/'}}">{{ post.title }}</a></h2>  
    <div class="postDate">{{ post.date | date:"%B %d, %Y" }}</div>
    <div class="postContent">{{ post.content }}</div>
  </div>
{% endfor %}

