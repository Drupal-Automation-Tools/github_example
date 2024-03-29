# GitHub Workflow Example 

## Table of Contents

#### <a href="#overview">Overview: How to use this repo</a>
#### <a href="#prerequisites">Prerequisites/Assumptions</a>
#### <a href="#install">Install</a>
#### <a href="#directory-structure">Overview of what's in this repository (typical Acquia Cloud directory structure)</a>
#### <a href="#forking">Forking the project to your own repository</a>
#### <a href="#acquia-cloud-dev">Testing your work in an Acquia Cloud development environment</a>
#### <a href="#local-dev">Testing your work in your local development environment</a>
#### <a href="#branching">Modifying the Poem project (branching and merging)</a>
#### <a href="#pull-request">Submitting your changes as a GitHub "pull request"</a>
#### <a href="#rebasing">Preparing a tidy pull request (rebasing)</a>
#### <a href="#code-review">Code reviewing the pull request on GitHub</a>
#### <a href="#merging">Merging in changes from the pull request on GitHub</a>
#### <a href="#remotes">Working with multiple remotes</a>


### <a id="overview" name="overview">Overview</a>

This repository includes a simple Drupal installation profile. The README you are reading includes exercises based on this repo and the Drupal site it includes, demonstrating Git/GitHub/Acquia Cloud workflows. These lessons touch on basics of working with Git and practical, hands-on examples of working with distributed/decentralized version control.

To follow these lessons you will need to install the included Drupal Example profile and think of something to contribute to it.

Contributing is easy. The front page of the example site is a form generated by the Poem module. (Poem module lives in sites/all/modules/poem.) As of version 7.x-1.0, the form includes a few radio buttons that let you generate your own "Roses are Red, Violets are Blue" poem. To follow these lessons, you need to think of something to add or modify in Poem module. For example: You can add another input option to make the poem more customizable; you can add some theming to make the output prettier; you can make the form generate a different poem. (The idea here is just to give you something to follow through the entire fork -> test -> pull request -> code review -> merge workflow.)


### <a id="prerequisites" name="prerequisites">Prerequisites</a>

These lessons assume:
* You know how to install Drupal locally
* You have basic working knowledge of Drupal development (e.g. [Form API](http://api.drupal.org/api/drupal/developer%21topics%21forms_api_reference.html/7))
* You have Git installed
* This lesson also assumes your normal workflow includes at least three hosted Git repositories (e.g. an official repo on GitHub, your working copy or "fork" of the repo on GitHub, and another copy of the repo on Acquia Cloud)


### <a id="install" name="install">Install</a>

1. Copy, or "clone", this repository:

        git clone git://github.com/bryanhirsch/github_example

1. Create a local sites directory that will be ignored by Git (note: if you're confused about where different files live in this repo, this is explained in the next section: <a href="#directory-structure">Overview of what's in this repository (typical Acquia Cloud directory structure)</a>)

        cd path/to/github_example
        cd sites
        # Note: .gitignore (in the top-level directory of this repo) instructs Git to ignore sites/example.localhost.
        cp -r default example.localhost
        cd example.localhost
        cp default.settings.php settings.php

1. Set up your Virtual Host. Instructions here vary a little depending on your set-up. Here's what you would do in MAMP:

        # Open /Applications/MAMP/conf/apache/extra/httpd-vhosts.conf
        # Add this:
        <VirtualHost *>
          DocumentRoot "/Volumes/Shared/home/bryanhirsch/www/github_example/docroot"
          ServerName example.localhost
        </VirtualHost>

        # Open /etc/hosts and add this:
        127.0.0.1 example.localhost

1. Open your browser and go to http://example.localhost. You should see a familiar Drupal installation screen, select the profile called, "Example", and proceed with Drupal installation.

Once the site is installed, the home page should have a simple poem-making form. This form is generated by the Poem module in sites/all/poems.


### <a id="forking" name="forking">Forking the project to your own repository</a>


### <a id="directory-structure" name="directory-structure">Overview of what's in this repository (typical Acquia Cloud directory structure)</a>

Directory structure
-------------------

    docroot/                          <-- Drupal
    docroot/sites/                    <-- symlink to ../sites/
    docroot/profiles/github_example/  <-- simlink to ../../github_example
    sites/
    github_example/


### <a id="acquia-cloud-dev" name="acquia-cloud-dev">Testing your work in an Acquia Cloud development environment</a>
### <a id="local-dev" name="local-dev">Testing your work in your local development environment</a>
### <a id="branching" name="branching">Modifying the Poem project</a>
### <a id="pull-request" name="pull-request">Submitting your changes as a GitHub "pull request"</a>
### <a id="rebasing" name="rebasing">Preparing a tidy pull request (rebasing)</a>
### <a id="code-review" name="code-review">Code reviewing the pull request on GitHub</a>
### <a id="merging" name="merging">Merging in changes from the pull request on GitHub</a>
### <a id="remotes" name="remotes">Working with multiple remotes</a>
