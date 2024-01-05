# Layout of the Website Source Code

The source code for the NWChemEx Community's website lives in this
directory, i.e., `docs/`. This README explains what all the files are and what
goes where.

## Configuration Files

The primary configuration files for the website are:

- `Gemfile` - manages the ruby package dependencies of the website,
- `_config.yml` - manages site-wide settings,
- `_data/authors.yml` - list of people who write website content,
- `_data/navigation.yml` - defines what goes on the top bar of the website


## Website Posts

When there's NWChemEx news to report we issue a "post". These live in the
`_posts/` directory. Community members can be alerted to our posts by
subscribing. These posts should be of community-level interest. Examples
include:

- board meeting summaries,
- upcoming community workshops

## Tutorials

These are meant to be high-level tutorials dedicated to using NWChemEx Community
software. Tutorials for specific plugins are out of scope and should be managed
by the plugin's repository. Examples of tutorial topics are:

- Using NWChemEx for research
- Creating a plugin

## Website Static Pages

The NWChemEx Community website consists of two types of content static and
dynamic. Dynamic content is primarily comprised of posts and tutorials.
Every other page of the website falls under the "static" pages category. This
includes:

- the homepage
- an overview of what the NWChemEx community is
- profiles of the community members
- links to plugins designed for the NWChemEx ecosystem

## Website Assets

"Assets" is the cool name that website developers use to refer to things like
images, scripts, and other files which are to be embedded in the website. If
the asset is meant to be used throughout the website it goes in the `assets/`
directory. Examples of site-wide assets are:

- logos for NWChemEx, the NWChemEx community, sponsors, etc.
- profile pictures for website authors

Images for specific pages should be placed
