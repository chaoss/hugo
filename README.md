# Experimental CHAOSS Static Website


This project started as an experiment to take a markdown export of the content on the CHAOSS wordpress and see they could be used to build a statically-generated website.

This idea was presented to the CHAOSS community call and there seems to be a lot of benefits to moving to a static site:
- less expensive to host
- less confusion with multiple plugins
- version-controlled changes with a git-based workflow
- Content can be written in markdown
  - User-friendly Content management UIs are also available (such as DecapCMS) if desired
- Ability to separate the theming/styling/structure of the site from the content
  - Separating the content also allows it to potentially be translated to other languages for accessibility


## Building Locally

This site uses [Hugo](https://gohugo.io/) as its templating engine to generate the site. Hugo has [basic usage](https://gohugo.io/getting-started/usage/) and [installation](https://gohugo.io/installation/) documents on their website.


Once hugo is installed, you can run `hugo serve` in this project's directory to start a local web server and preview the content.

**Note about Offline Builds**
Note about the build process: Some pages of the website, such as the CHAOSS charter, are fetched from other github repositories at build time using the GitHub API. If you do not have internet access when you first build the site, the builds will fail.

Once these pages are downloaded, hugo will cache them so that subsequent builds can be done offline (so long as you dont add a new page that needs to be fetched from online).