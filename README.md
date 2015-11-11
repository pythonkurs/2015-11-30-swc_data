# Data/Software Carpentry Workshop 2015-11-30 and 2015-12-01

3.  Once you are done,
    please **send your repository's URL to the [Software Carpentry administrator](mailto:admin@software-carpentry.org)**.
    We build the [list of workshops on the main website](http://software-carpentry.org/workshops/index.html)
    from the data included in your `index.html` page.
    We can only do that if you [customize](CUSTOMIZATION.md) that page correctly
    *and* send us a link to your workshop website.

4.  Please also read
    [the notes on customizing your website](CUSTOMIZATION.md) and the [FAQ](FAQ.md).
    If you're interested in knowing more about why we do things the way we do,
    please check out the [design notes](DESIGN.md).

5.  If you are teaching Git,
    please [create a separate repository](#setting-up-a-separate-repository-for-learners)
    for your learners to practice in.

6.  If you run into problems,
    or have ideas about how to make this process simpler,
    please [get in touch](#getting-and-giving-help).

## Customizing Your Website

1.  Go into your newly-created repository,
    which will be at `https://github.com/your_username/YYYY-MM-DD-site`.
    For example,
    if `your_username` is `gvwilson`,
    the repository's URL will be `https://github.com/gvwilson/2015-07-01-mistaktonic`.

2.  Edit `index.html` to customize the list of instructors,
    workshop venue,
    etc.
    You can do this in the browser by clicking on it in the file view
    and then selecting the pencil icon in the menu bar:

    ![](http://software-carpentry.org/img/workshop-template/edit-index-file-menu-bar.png)

    or you can clone the repository to your desktop,
    edit `index.html` there,
    and push your changes back to the repository.
    Editing hints are embedded in `index.html`,
    and full instructions are in [CUSTOMIZATION.md](CUSTOMIZATION.md).

3.  Edit `_config.yml` in the same way
    so that `workshop_repo` and `workshop_site`
    are the URLs of your repository and your GitHub Pages website respectively.

    Note: the URL for your website is determined automatically
    based on the URL for your repository.
    If your repository is at `https://github.com/gvwilson/2015-07-01-mistaktonic`,
    its GitHub Pages website is at `http://gvwilson.github.io/2015-07-01-miskatonic`.

4.  When you are done editing,
    you can preview your website.
    Again,
    if your repository is `https://github.com/your_username/YYYY-MM-DD-site`,
    its website will be `http://your_username.github.io/YYYY-MM-DD-site`.

Full instructions are available in [CUSTOMIZATION.md](CUSTOMIZATION.md).
This [FAQ](FAQ.md) includes a few extra tips
(additions are always welcome)
and these notes on [the background and design](DESIGN.md) of this template may help as well.

That's it.
The following steps are only necessary if you want to run the website locally on your computer.

## Checking Your Changes

**Note:** to check your changes you need some softwares
that are describe at [Installing Software session](#installing-software).

No matter how you edit `index.html`, you should:

1.  Check your changes by running `tools/check.py` at the command line
    from the root directory of your repository.

2.  Preview your changes by running `tools/preview` and looking at `_site/index.html`.

For some links to work properly,
particularly the link to your workshop's Eventbrite registration page,
you must view `_site/index.html` using an HTTP server.
If you have Jekyll installed,
you can do this by running:

~~~
$ jekyll server -d _site
~~~

and going to http://localhost:4000.
