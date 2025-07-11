# List GitHub Repos
|![Home Page](screen1.png "Home Page")|![Repo Page](screen2.png "Repo Page")|
|:---:|:---:|

![GitHub repo size](https://img.shields.io/github/repo-size/seyon123/list-github-repos?style=for-the-badge) ![GitHub last commit](https://img.shields.io/github/last-commit/seyon123/list-github-repos?label=Last%20Commit&style=for-the-badge) ![GitHub](https://img.shields.io/github/license/seyon123/list-github-repos?style=for-the-badge)
 ## Overview
 This repo lists all of your GitHub repos onto a webpage. The styling and functionality can easily be customized to meet your needs.

 ## Prerequisites

 jQuery is required for this repo to work properly. You can see it being called in [index.html](index.html).

 ## How To Use
1. Fork this repository.
1. Rename it to `[your username].github.io`.
   - *[Optional]* Rename to something else (like `myrepos`) if you wish for it to appear as a `subfolder`.
1. In your own repo's `Settings=>Pages` choose the main branch and Save.
1. *[Optional]* If you added a subfolder in step 2, then edit your own repo's About section, uncheck `Use your GitHub Pages website` and write  `[your username].github.io/myrepos/` **manually**.

That's it!

### More advanced usage
There are mainly 2 files from this repository that you need, [js/script.js](js/script.js) and [css/styles.css](css/styles.css). The JavaScript file gets necessary information about the user's repositories from GitHub's API and the CSS file contains styling for elements. You can see both being called in [index.html](index.html).

#### If you want a form instead of auto list
In the HTML page **remove the comment out** besides the div with ID of `title` to return the form.

#### If you want to show the repositories of a different user than yourself
In the HTML page **manually** fill `var user = '...';`.

#### Extras
In the html page you can move the div named `repo-box` to where you want the repositiories to show:
```html
<div id="repo-box"></div>
```

Finally, if you wish to modify or create your own syling, the following classes and ids are used to styling. You may make or add changes to these as you desire in [css/styles.css](css/styles.css):
```html
#repo-box    -> <div> contains all the repositories being printed out
.error-box   -> <div> error message div when user name is not correct
.error-msg   -> <h1> message of the error
.repo-item   -> <div> contains the information for repository
.title       -> <h1> title of the repository
.description -> <p> description of the repository
.bottom      -> <div> contains the icons and values for language, stars and forks of repo
.img         -> <span> contains images of language, stars, and forks
.language    -> <div> contains image and values for language
.star        -> <div> contains image and values for number of stars
.fork        -> <div> contains image and values for number of forks
```
*Note: UIkit was also used for some styling and icons. You may have to use your own icons if you dont want to use UIkit.*
