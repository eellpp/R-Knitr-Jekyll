# R-Knitr-Jekyll
Scripts to post to Jekyll Blog with Rmd files

This script is by blogger [chepec](https://chepec.se/2014/07/16/knitr-jekyll.html)

## Workflow

#### One Time

1) Copy the build_jekyll.sh to root of the blog site and provide execute permission
Update the SITE variable in the build_jekyll.sh script

```
SITE="path/to/your/site/without/trailing/slash"
```

2) Copy the _knitr directory to root of the blog
Open _knitr/render_post.R and update variable

```
site.path <- "path/to/your/site/with/trailing/slash/"
```

#### Posting

1. Create the .Rmd file in _knitr directory. 
2. From the blog root director run
```
# to convert all _knitr/*.Rmd files to _posts/*.md (does not overwrite existing md)
build_jekyll.sh -c

#  to build a specific script
build_jekyll.sh -f _knitr/<filename>.Rmd 
```

This will create the .md file in the _posts directory
build the site

```
build_jekyll.sh -b
```

Reference:

The [blog post](https://chepec.se/2014/07/16/knitr-jekyll.html) explains clearly the workings of the script. I changed some parts to fit to my needs and there are more todos like Automatic post URL generation in format YYYY-mm-dd-post-title etc. Added this here to keep track of the changes.
