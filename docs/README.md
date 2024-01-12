# NWChemEx Community Website

This repo houses the NWChemEx Community website. Think of this as the front page
of all things pertaining to the NWChemEx Community. It's meant to be a:

- a high-level overview of the NWChemEx community,
- a place for new community members to become acclimated, and
- a dispatch point to other more specialized online resources

## Building the Website Locally

GitHub pages is designed for use with Jekyll, which is a ruby package for
building static websites using GitHub flavored markdown. Don't worry you
shouldn't need to know ruby at any stage of website maintenance as long as you
follow these command-line instructions:

1. Ensure `ruby-bundler` is installed. On Ubuntu this is done by:

   ```.sh
   sudo apt install ruby-dev ruby-bundler
   ```

2. Clone this repo, i.e.,

   ```.sh
   git clone https://github.com/NWChemEx/NWChemEx.github.io
   ```

3. Install the dependencies via bundler. This is done by:

   ```.sh
   cd NWChemEx.github.io/docs
   bundle config set path 'vendor/bundle'
   bundle install
   ```

4. Launch the website server via:

   ```.sh
   bundle exec jekyll serve
   ```

5. View the website by following the instructions from the previous command (
   should be something like opening http://127.0.0.1:4000 in a web browser).

6. Start adding/modifying content. The local copy of the website should
   automatically update after you modify a file. You will likely need to reload
   the page to see the changes. The caveat to this is if you modify
   `docs/_config.yml`; if you modify that file you will have to stop the current
   server and repeat step 4.


## Layout of the Website Source Code

The source code for the NWChemEx Community's website lives in this
directory, i.e., `docs/`. This README explains what all the files are and what
goes where.

### Configuration Files

The primary configuration files for the website are:

- `Gemfile` - manages the ruby package dependencies of the website,
- `_config.yml` - manages site-wide settings,
- `_data/authors.yml` - list of people who write website content,
- `_data/navigation.yml` - defines what goes on the top bar of the website


### Website Posts

When there's NWChemEx news to report we issue a "post". These live in the
`_posts/` directory. Community members can be alerted to our posts by
subscribing. These posts should be of community-level interest. Examples
include:

- board meeting summaries,
- upcoming community workshops

### Tutorials

These are meant to be high-level tutorials dedicated to using NWChemEx Community
software. Tutorials for specific plugins are out of scope and should be managed
by the plugin's repository. Examples of tutorial topics are:

- Using NWChemEx for research
- Creating a plugin

### Website Static Pages

The NWChemEx Community website consists of two types of content static and
dynamic. Dynamic content is primarily comprised of posts and tutorials.
Every other page of the website falls under the "static" pages category. This
includes:

- the homepage
- an overview of what the NWChemEx community is
- profiles of the community members
- links to plugins designed for the NWChemEx ecosystem

### Website Assets

"Assets" is the cool name that website developers use to refer to things like
images, scripts, and other files which are to be embedded in the website. If
the asset is meant to be used throughout the website it goes in the `assets/`
directory. Examples of site-wide assets are:

- logos for NWChemEx, the NWChemEx community, sponsors, etc.
- profile pictures for website authors

Images for specific pages should be placed