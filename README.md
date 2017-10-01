### simple jekyll posts generator
As you can guess from the title, this is a node module to generate [jekyll posts](http://jekyllrb.com/)  easily from within your terminal.

#### Installation
type in your terminal :
```
npm install -g jekyll-posts-generator
```
In some computers you need to be an **administrator** to install this module, in that case 
just precede the previous command with ``sudo``.

After installing this package you can access the global command ``jgen`` from within any folder you want.

#### Usage
Navigate to some [jekyll website](http://jekyllrb.com/) folder that have the following structure :
```
.
├── _config.yml
├── _drafts
├── _includes
├── _layouts
├── _posts
|   |── posts are listed here ...
├── _data
├── _site
├── .jekyll-metadata
└── index.html
```

Now you can create a basic article using the ``create command``

```
jgen create-post 'my article title'
```
OR
```
 jgen create-post "my article title"
```

At this time if you go inside ``_posts`` folder, you will see a new file ``[YYYY-MM-DD]-my-article-title.md`` generated for you.
#### Options
You can see the list of options available with any command using
``jgen [COMMAND_NAME] -h`` or ``jgen -h `` to list the options available with the global command ``jgen``,
Here is some examples :
```
#list options available with create command
jgen create-post -h

# specify the current post categories
jgen create-post <postName> -c category1,category2,...

# Specify the layout of the current post
jgen create-post <postName> -l post

# Specify the author of the current post
jgen create-post <postName> -a author

# Specify the subtitle of the current post
jgen create-post <postName> -s subtitle

# Specify the header image of the current post
jgen create-post <postName> -himg header-image-path

# You can specify multiple options at the same time :
jgen create-post <postName> -l post -c category1,category2

# Create new category 
jgen create-category <categoryName> 
```




#### TODO
* Add other essential options.
* Add test cases.
* ...
