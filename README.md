### Basics

#### Markdown

Files ending in `.md` are in [markdown syntax](http://daringfireball.net/projects/markdown/syntax). They are parsed using the [kramdown](http://kramdown.gettalong.org/) parser, which means that a few extra features are enabled -- most importantly references:

    The earth is round[^earth2014] and marxism is correct.[^capitalism1800]
    
    ### References
    [^earth2014]: First reference.
    [^capitalism1800]: Second reference.

#### Links

Links to pages in the site are typed like this: `/updates/2014/07/18/dare-to-win-4-out-now/`. In other words, they're relative URLs. To get a relative URL just remove the `https://thirdworldists.github.io/` from the full URL of the page.

#### Directories

The folder `_posts` gets translated into the directory `updates` when the site is rendered, so to link to a post type `/updates/...` rather than `/_posts/`. The `_publications` and `_wiki` folders lose the `_` prefix when the site is rendered.

#### Creating a new post

See the "example post" file in the `_posts` directory.

#### Updating

Once you edit a file, your changes should be reflected in the live version of the site within a few minutes. If they aren't showing up, check the build status image above. If it says there's a failure: congratulations, you've broken it.

---

### Under-the-hood

Knowledge of markdown should be sufficient for editing 95% of the site content so you shouldn't need to worry about this unless you want to make major changes. 

#### Jekyll

This site is generated using [Jekyll](http://jekyllrb.com/).

#### Front Matter

Most of the markdown files will begin with a block of text starting and ending with `---`. This is YAML [Front Matter](http://jekyllrb.com/docs/frontmatter/) syntax.

#### Liquid

`{{ some_text }}` or `{% some_text %}` appears throughout. This is the [Liquid template system](http://jekyllrb.com/docs/templates/).

#### HTML

This website is written with [bootstrap](http://getbootstrap.com/).
