# Testing of deploying a Hugo Template to Netflify

### Disclaimer

I am testing out this features before actually building one for myself to avoid confusion with editing and deploying.

This is due to the blogdown package has recently changed hence a lot of previous tutorials are different than what it is at the time of writing.

I am not fluent with Programming Languages outside of R, so I try my best to study the deployment features first before going deeper into manifacturing my own page.

### Steps Taken

1.  Create Repository in Gitlab
2.  Open R Studio
3.  Install "Blogdown" package.
4.  blogdown::install_hugo(force = TRUE)
5.  Create project and select Web Page with Blogdown
6.  Select a template, in this case, i like what i saw at https://www.dsquintana.blog/free-website-in-r-easy/ , hence i used the suggested template “gcushen/hugo-academic”
7.  Run "blogdown::serve_site()" to see a preview of what the web looks like
8.  Run "blogdown::stop_server()" after I have finished observing the preview
9.  Run "blogdown::build_site()" to prepare the web page for deployment. What it does is create a public file.
10.  Add a .gitignore file in your folder. Add public/ to prevent uploading public file to git. This is due to netlify will build it automatically and serve it to our users and we don't need to do that.
11.  Now once my folder is good to go, I pushed everything into my Git Repository build at step 1.
12.  Next I register an account at Netlify for free.
13.  I link my Git Repository to my Netlify account and build.
14.  Sometimes it can fail during deployment, but to my surprise it didnt. But if it does, go to your config.yaml or config.toml and register your website link to it. Sometimes it might be your hugo version.