# PackHacks 2021 Create Your First Website

This readme file contains any resouces mentioned in the related videos as well as solutions to common problems.

## Episode 0: Prerequisities

Websites are a great project for anyone who wants to have place that is uniquely theirs.
They're especially useful for students looking for jobs or internships because you can talk about yourself, your hobbies, and your projects in more detail than a resume.

We'll need a few tools to help us create and run our website.

0. **A Web Browser:** I'll assume that you already have one installed.
   Pretty much any modern browser (i.e. Chrome, Edge, Firefox, etc.) will be fine.
   It's possible that you'll have issues with older versions of Internet Explorer.
1. **A GitHub Account:** If you don't already have one, sign into [GitHub](https://github.com/) and create an account.
   If you have an account through your school or work, I'd recommend using a personal account so you don't risk losing access to your code and legally own your code.
2. **Git:** Git is a commandline tool that helps synchronize our code between our local computer and a remote repository like GitHub.
   You can download it [here](https://git-scm.com/downloads).
3. **A Code Editor:** Although any text editor will technically work, I'd recommend one that has some tools to help us write HTML.
    - [Visual Studio Code](https://code.visualstudio.com/) is an open-source code editor created by Microsoft.
      It's the editor I use throughout these videos.
      I also have an extension installed called [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) that will nicely format my code when I save it.
    - [Atom](https://atom.io/) is a free and open-source text editor developed by GitHub.
      You can install a package like [atom-beaufity](https://atom.io/packages/atom-beautify) to help format your code.

## Episode 1: First Webpage

We'll create our first HTML page.

### Common Problems

> The `Hello, World!` text is really small.

Make sure you put `Hello, World` inside an `<h1>` section and closed the section with a closing `</h1>` tag.

## Episode 2: Publishing To GitHub

Now that we have our first HTML page, we'll publish it to GitHub.

### Common Problems

> I don't see a link in the GitHub Pages section of the settings.

If you created your branch as `gh-pages` like in the video, everything should go smoothly.
If you used another name like `master` or `main`, you'll need to manually select this branch as the one you want to use in the GitHub Pages section of the settings

> I see a 404 error on GitHub.

Make sure you named your page `index.html` and it's not in any subfolders in your project.
When building your site, GitHub is expecting a file with this exact name at the root of your project.

### GitHub PATs & Having Git Remember Your Password

-   If you use your password, you might get an annoying from GitHub warning you that you should use Personal Access Token (PAT) instead of a password when using the commandline.
    You can learn how to create one [here](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).

-   It can be a little annoying to have to enter your username and password every time you want to push to GitHub.
    You can have your credientials be stored by following the instructions [here](https://stackoverflow.com/questions/46645843/where-to-store-the-personal-access-token-from-github), but note your credientials will be stored on your computer in plain text.
    -   If you're using a PAT instead of a password, enter your PAT where you would put a password.

## Episode 3: Adding Content

We'll start adding some personal content and styling to our `index.html` page.

### Bootstrap

We use Bootstrap to help us with the styling of our site.
Follow the CSS and JS instructions under the Quick Start guide [here](https://getbootstrap.com/docs/4.0/getting-started/introduction/).

If you want to try things I didn't show in the video, you can look at the [documentation](https://getbootstrap.com/docs/4.0).

### Common Problems

> My site doesn't look like the video.
> The Bootstrap stuff doesn't have any affect.

Make sure you correctly imported Bootstrap into your file, especially the CSS portion, in your head section.
Your file should look something like this:

```html
<!DOCTYPE html>
<head>
    <!-- Any other stuff in your head section -->
    <link
        rel="stylesheet"
        href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css"
        integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm"
        crossorigin="anonymous"
    />
</head>
<body class="d-flex flex-column" style="min-height: 100vh">
    <!-- Stuff on your body section -->

    <!-- Include JS Bootstrap stuff -->
</body>
```

> When I tried to make my picture circular, it looks like an oval instead.

This can happen if you try to use photos that are very rectangular.
Try cropping the photo you want to use into a square and try again.

## Episode 4: Adding More Pages

Now that we have a nice looking home page in `index.html`, we can use it as a template to create other pages on our site.

### Common Problems

> When I try to go to `MyName.github.io/ProjectName/contact.html` on GitHub I get a 404 error.

Try going to `MyName.github.io/ProjectName/contact` instead.
GitHub doesn't seem to recognize `.html` unless it's directly linked from `index.html` (which we'll do in episode 5)

## Episode 5: Adding a Navbar

Now that we have multiple pages, we'll make a navbar to link them together.

### Common Problems

> My navbar button (the one that appears when the page is narrow) isn't working.

The navbar uses some of the JS parts of Bootstrap, so make sure to include them.
Your page should look something like this:

```html
<!DOCTYPE html>
<head>
    <!-- Include CSS Boostrap stuff -->
</head>
<body>
    <!-- The rest of your body -->

    <script
        src="https://code.jquery.com/jquery-3.2.1.slim.min.js"
        integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN"
        crossorigin="anonymous"
    ></script>
    <script
        src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js"
        integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q"
        crossorigin="anonymous"
    ></script>
    <script
        src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js"
        integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl"
        crossorigin="anonymous"
    ></script>
</body>
```

## Episode 6: Further Learning

We now know how to create a nice-looking, professional site.
Although we just covered the basics, here are a few tools you can learn more about.

-   **Buying Your Own Domain:** You can purchase a domain cheaply from somewhere like [Google Domains](https://domains.google/) for as little as $12/year.
    To read about how to set up Google Domains with GitHub pages, see [here](https://dev.to/trentyang/how-to-setup-google-domain-for-github-pages-1p58).
-   **Jekyll:** [Jekyll](https://jekyllrb.com/) is a static site generator and what I use for my website.
    It allows you to avoid writing redundant code by putting sections in their own file and including them where needed, as well as making page templates that can extend each other.
    It integrates really well with GitHub pages.
-   **React:** [React](https://reactjs.org/) is a JavaScript library originally developed at Facebook.
    It allow you to create elements on the page as a combination of HTML and JavaScript called "components".
    These components can be reused to avoid reduncancy.
