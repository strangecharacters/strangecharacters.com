---
title: "Hugo Netlify Tailwind"
date: 2022-01-05T18:26:51Z
draft: true
---

How to set up a site using Hugo and TailwindCSS and host it for free on Netlify.

create a github repo with a readme
get the repo via its url and put it in local directroy
git clone URL  in my hugo dir and a folder will be created 
hugo/reponame

install hugo 
create a new hugo site in the current directory . The "." represents the currrent directory
`hugo new site . --force`
We have to use the --force falg because hugo expects an empty dir, we have cloned a README file into the dir.

if we hugo serve we will see a blank page because there's no theme being used 

add a theme as submodule / hugo mod

```
cd quickstart
git init
git submodule add -b stable https://github.com/jpanther/congo.git themes/congo

```



Still a blank theme?
Add the theme setting in config.toml
theme = "congo"

hugo serve should show 'My New Hugo Site"

commit and push to github
```
git add .
git commit -m "installed hugo and theme"
```

Creating a new repo on github gives us a default branch name of 'main'

`git push origin main`


copy sample content from exampleSite in the theme folder and paste it into the root of the site.

This theme uses a folder for config files so I renamed the default config.toml to original-config.toml 
The pasted confog files now give our site its settings.

I got an error here

ERROR 2022/02/06 17:54:41 Failed to get JSON resource "https://api.twitter.com/1/statuses/oembed.json?id=&omit_script=true": Failed to retrieve remote file: Not Found, body: "{\"errors\":[{\"message\":\"Sorry, that page does not exist\",\"code\":34}]}"
If you feel that this should not be logged as an ERROR, you can ignore it by adding this to your site config:
ignoreErrors = ["error-remote-getjson"]

Taking its suggestion I added the line
ignoreErrors = ["error-remote-getjson"]
to config/_default/config.toml

Putting it at the end of the config/_default/config.toml didn't work

PUtting it at the top of the file and stopping and restarting the server
`hugo serve`
seemed to work.


hugo serve
create a new page in the content folder 
`hugo new about.md`
test it
localhost:1313/about/


Our theme has config/menus.en.toml with some sample links 
Add or edit an entry with this format
```
[[main]]
  name = "About"
  pageRef = "about"
  #url = "https://github.com/jpanther/congo"
  weight = 40
  ```

  The pageRef parameter allows you to easily reference Hugo content pages and taxonomies. It is the quickest way to configure the menu as you can simply refer to any Hugo content item and it will automatically build the correct link.

  To link to external URLs, the url parameter can be used.

create a new post
`hugo new foldername/postname.md`

The fromt matter for these articles will come from the archetypes it can find in

```
/archetypes
themes/congo/archtypes
```

The default archetype will be used for all content unless there's something more specific.
if there's `/archetype/docs.md`
it will be used to create 
`hugo new docs/sample.md`

`hugo new articles/something-interesting.md`


table of contents
markup.toml added table of content settings



add an email signup form

email form shortcode

syntax highlighting

multilanguage 

commit and push to github




Tables of Content
An email signup form from Convertkit
Comments submitted to Netlify and saved in github, added to static pages on build

Tailwind Theme, customisations
