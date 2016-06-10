# Jekyll API Boilerplate [![license](https://img.shields.io/github/license/ixkaito/jekyll-api-boilerplate.svg?maxAge=2592000)](https://github.com/ixkaito/jekyll-api-boilerplate/blob/master/LICENSE)

Jekyll API Boilerplate is a [Jekyll](http://jekyllrb.com/) starter project using a [Jekyll Plugin](http://jekyllrb.com/docs/plugins/) gem "[Jekyll Pages API](https://github.com/18F/jekyll_pages_api)" to generates a JSON file with data for all the Pages, Posts, Documents (i.e. "collections") and StaticFiles with a simple deployment to GitHub Pages.

## Usage

1. Fork this repository

2. Clone the forked repository

3. Inside the directory, execute:

   ```bash
   $ bundle install --path vendor/bundle
   $ bundle exec jekyll serve --baseurl /jekyll-api-boilerplate
   ```

4. You can then see the generated JSON file at [http://localhost:4000/jekyll-api-boilerplate/api/v1/pages.json](http://localhost:4000/jekyll-api-boilerplate/api/v1/pages.json), which will look like this:

   ```json
   {
    "entries": [
      {
        "title": "About",
        "url": "/jekyll-api-boilerplate/about/",
        "tags": [ ],
        "body": "This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at jekyllrb.com You can find the source code for the Jekyll new theme at: jglovier / jekyll-new You can find the source code for Jekyll at jekyll / jekyll"
      },
      {
        "title": "",
        "url": "/jekyll-api-boilerplate/",
        "tags": [ ],
        "body": "Posts Jun 11, 2016 Welcome to Jekyll! subscribe via RSS"
      },
      {
        "title": "Welcome to Jekyll!",
        "url": "/jekyll-api-boilerplate/jekyll/update/2016/06/11/welcome-to-jekyll.html",
        "tags": [ ],
        "body": "You’ll find this post in your _posts directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run jekyll serve, which launches a web server and auto-regenerates your site when a file is updated. To add new posts, simply add a file in the _posts directory that follows the convention YYYY-MM-DD-name-of-post.ext and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works. Jekyll also offers powerful support for code snippets: def print_hi(name) puts \"Hi, #{name}\" end print_hi('Tom') #=> prints 'Hi, Tom' to STDOUT. Check out the Jekyll docs for more info on how to get the most out of Jekyll. File all bugs/feature requests at Jekyll’s GitHub repo. If you have questions, you can ask them on Jekyll Talk."
      }
    ]
   }
   ```

## Deploying to Github Pages

1. Inside the directory, execute:

   ```bash
   $ bundle exec rake deploy
   ```

2. You can then see the generated JSON file at a URL like this: http://username.github.io/jekyll-api-boilerplate/api/v1/pages.json.
