---
layout: post
title:  "View CSV Data from the Command Line"
date:   2016-09-06 17:49:57 +0200
categories: jekyll update
---
This is a convenient way to view csv data in the command line. I copied this command from Chris Jean's blog, so make sure you check out his original post for more information.

Using a combination of `cat`, `column` and `less`, CSV data can be rendered into a nice table and quickly navigated. Here is an example:

```{engine='bash'}
cat file.csv | sed -e 's/,,/, ,/g' | column -s, -t | less -#5 -N -S
```

SOURCE: [Chris Jean's blog][cjblog]

[cjblog]: https://chrisjean.com/view-csv-data-from-the-command-line/
