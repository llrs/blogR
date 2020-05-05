+++
title = "{{ replace .Name "-" " " | title }}"
subtitle = ""

# Add a summary to display on homepage (optional).
summary = ""

date = {{ .Date }}
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = []
description = ""

# Is this a featured post? (true/false)
featured = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []
categories = []

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
# projects = ["internal-project"]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
  
[editor_options]
  chunk_output_type = "console"

+++

```{r setup, include = FALSE}
knitr::opts_chunk$set(collapse = TRUE, 
                      linenos=table) # To add line numbers
```


### References

```{r bibsetup, echo=FALSE, message=FALSE, warning=FALSE}
## Load knitcitations with a clean bibliography
library('knitcitations')
cleanbib()
cite_options(hyperlink = 'to.doc', citation_format = 'text', style = 'html')
pi <- sessioninfo::package_info()
packages <- c(pi$package[pi$attached], 'knitcitations')
l <- sapply(packages, function(x){citation(x)[1]}, simplify = FALSE)
bib <- c(l, 'blogdown' = citation('blogdown')[2])
```

```{r results = 'asis', echo = FALSE, cache = FALSE}
bibliography(style = 'html')
```

### Reproducibility

<details>
```{r reproducibility, echo = FALSE}
## Reproducibility info
options(width = 120)
sessioninfo::session_info()
```
</details>
