# MathHub News

MathHub has a [news feed](http://mathhub.info/News/) and we need to keep the news flowing on this.

Technically, posts are stored as Markdown files in the [MathHub News Repository](http://github.com/MathHubInfo/News/), from which we export a [JSON file](https://mathhub.info/news.json), which is in turn shown by the [MathHub FrontEnd](https://mathhub.info). 

Here is how to make a post:

1. clone the [MathHub News Repository](http://github.com/MathHubInfo/News/) and create a new file `YYYY-MM-DD-<short title>.md` in the `_posts` directory or [directly use the web editor](https://github.com/MathHubInfo/News/new/master/_posts).
2. Start writing away describing what is new; the contents of the file follow thte following template
   ```
   ---
   date: YYY-MM-DD
   title: A descriptive title
   ---
   the text in Markdown
   ```
   commit this to the `master` branch and push (if you have cloned the News repos) or make a merge request.  
