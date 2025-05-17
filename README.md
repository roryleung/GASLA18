# IVACS 2024 conference website

This is the code for the conference website for the [2024 Conference on Inter-Varietal Applied Corpus Studies]() (IVACS 2024) -- based on the code for [EMNLP 2023](https://github.com/acl-org/emnlp-2023)

It's currently using the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/).

# Table of contents

* [Forking for a New Conference](#forking-for-a-new-conference)
   * [Important Files](#important-files)
   * [Domain Setup](#domain-setup)
* [License](#license)


# Forking for a New Conference

For a new conferences, you may either set up a repository from scratch by forking the original [Minimal Mistakes repository](https://mmistakes.github.io/minimal-mistakes/) or you may fork this repository directly. The latter may be easiest since all of the changes that are required for more complex things like the web-based schedule to work are already there. However, the disadvantage of forking this repository is that the version of the Minimal Mistakes theme will be out of date and you might miss out on bugfixes and new features. 

**IMPORTANT**: Note also that if you fork this repository, you will get all of the existing conference's pages and blog posts and schedule and other content. Therefore, it is up to you to modify/temporarily remove that content before you make your website public so that your new domain is not indexed by search engines with old content. It might be best to rename the `gh-pages` branch so that the website for the new conference does not get built with content from the old conference. You can rename the branch back to `gh-pages` once you have made sufficient changes locally to remove/modify the old conference content.

**Extra note based on my experience for IVACS'24**: I downloaded the [EMNLP 2023](https://github.com/acl-org/emnlp-2023) repository, unzipped, pruned some of the unnecessary files which were specific to EMNLP (images, blogposts, subpages, etc), and edited the files mentioned below. Then created a new GitHub repository, pushed this local repository using git, and updated the GitHub repository settings under 'Pages' (source and build) in order to publish under my <username>.github.io/<repository_name> . In addition I edited the Gemfile and _config as instructed on the [Mimimal Mistakes page](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/#remote-theme-method) (I specified the version of MM forked for NAACL'21 -> EMNLP'23 which was 4.16.4). After a short delay to build, the page went live :)


## Important Files

If you fork this repository, the following files are the ones to pay attention to in order to create content for the website:

- `_pages/xxx.md` : The markdown files contain the main contents of the different web pages of the website. Please note that
  once you fork, you would need to move the already existing .md files out into a different folder so that old pages do not
  get rendered into the new website.

- `downloads/` : Contains files that can be downloaded from the website.

- `_sass/minimal-mistakes/*.scss` : SASS files that control the look and the feel of the website. The file `_program.scss` is not part of the them and controls the look and feel of the web schedule page.

- `_data/navigation.xml` : YAML file that contains the links in the masthead at the top of the website and also links in the various sidebars. 

- `_data/authors.yml` : YAML file that contains the information about the various blog post authors, e.g., Program Chairs, Diversity Chairs, General Chair. This file _must_ be updated with the right names and links.

- `_config.yml` : YAML file that contains meta-information about the website that should be set properly for a new conference. Details are given in the comments in the file. You must edit this file properly before making the website public.

- `_posts/*.md` : If you are going to have a blog, this where the blog posts live and are named `YYYY-MM-DD-title.md`. Same as the
  files under `_pages`, you should move out already existing files from this folder to prevent them from getting rendered.

- `CNAME` : You should delete this file since this contains the old external domain from the older conference. This file will be
  automatically re-generated when you add the new external domain for the new conference. If you do not remove this file, you will
  get a page build warning from GitHub.


## Domain Setup

In my case the underlying GitHub Pages URL is https://cainesap.github.io/ivacs2024/

I bought a domain (https://www.ivacs2024.com/) and configured the repository settings, and those for the domain as described here: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site


## License

The MIT License (MIT)

Copyright (c) 2018 Association for Computational Linguistics.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
