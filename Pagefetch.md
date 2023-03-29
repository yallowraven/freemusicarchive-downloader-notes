## Skeleton of a CLI
As this script is the first pass of the pipeline, it is going to be the entrypoint to the entire CLI tool for now.

## Just fetching
Using `argparse`, getting the target URL from the args, and retrieving the HTML with `requests` is a trivial task, and as Free Music Archive does not check for the browser the client is requesting with, it serves the page just fine.

## URL validation
With the current progress, any page can be retrieved. However, we need to introduce a check so we only ever accept URLs of Free Music Archive music listing pages. 

## Page validation
Now, we also have to establish that the Free Music Archive page is a song listing. For this, we can inspect the contents and look for occurences of the regex `<div class="play-item[^\n]*` (obtained from the research last time).