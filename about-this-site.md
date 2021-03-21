---
title: 'About this site'
fieldset: default
hook: "Learn how this site is built, what technologies it is built on, and how you can build one just like it."
template: about_how
type: concept
---

## How this site is built

This site is built on a the following noteworthy technologies and frameworks:

* Google Cloud Platform
* Statamic
* GitHub
* Tailwind CSS
* Sass CSS
* Laravel Valet

My development workflow follows this path:

![Development environment](/assets/img/development.png)

* **GitHub** functions as source control
* **Laravel Valet** powers the server in my development environment
* **Google Cloud Platform** hosts the production server

## Google Cloud Platform details

Google Cloud Platform (GCP) is large cloud services platform that competes with the likes of Amazon Web Services and Microsoft Azure. Cloud platforms are very large and complex topics, so I'll limit the discussion to the architecture of this site as it relates to GCP.

At the time of writing, traffic and performance requirements are very small and limited a to development scope.

This web server runs on a single `g1-small` Compute Engine instance with 10GB of magnetic drive space. The instance is running on a standard Debian deployment, and I manage the website from there.

I provide limited instructions on [deploying and configuring a Google Cloud project](/samples/writing/create-a-statamic-web-server-on-google-cloud-platform) for this site in the sample works section.

## Laravel Valet details

Since Statamic, my CMS was built on top of the Laravel PHP framework, I elected to use Laravel Valet as the server in my development environment. I'm using a standard configuration. I also host my API on valet is well.

I provide instructions for [installing and configuring Valet](/samples/writing/install-and-configure-laravel-valet) for use with this site as part of my sample works section.

## GitHub details

For version control, GitHub was an obvious choice. I have used Git extensively in both writing and development work. Note that in my implementation, I'm storing the full site on my local repository and in GitHub.

I provide instructions for [Cloning this site from GitHub](/samples/writing/clone-this-site-into-your-local-development-environment) to work with this site as part of my sample works section.

## Statamic details

I chose to use Statamic for a couple of reasons: It supports my authoring strategies, and I used it in private work at other companies. As a documentation site, Statamic supports content modularity through the cascade, text variables through global variables, and reasonably extensible authoring through an extensible markup.

I provide instructions for [Installing Statamic](/samples/writing/install-and-configure-statamic) within this site as part of my sample works section.

## Tailwind CSS and Sass

I'm using the Tailwind framework and Sass streamline visual site development. I have very little time to focus on visual development, so I want to keep my commitments in this area to a minimum.

I provide instructions for [installing and configuring](/samples/writing/install-tailwind-css) the Tailwind framework and Sass for this site as part of my sample works section.

## Design and style guide

In developing the site's style elements, I created the following guidance:

### Text

* All fonts should be sans-serif, either Helvetica or arial.

* Titles should large, bold, and use sentence case for natural readability.

* In paragraphs, set font size to 14 point to even further improve readability. Avoid any text below 11 point.

### Graphics and layout

* Use generous white space to cleanly divide separate elements.

* Use iconography to grant visual touch points and lend unwritten structure to long areas of text. Experiment with black/white icons as well as greyscale.

* Avoid any logos or overt branding elements. Attempting to brand oneself with a logo never goes well.

### Colors

* Make moderate use of greyscale, and use the primary colors inline with text to attract and magnify choice elements and areas.

* Primary colors should be sharp, bright and vibrant for content you want to call out. Make restrained use of subtle blending and gradients to indicate quality and leverage new hardware's increased color space to indicate modernity.

* Provide relief from high contrast blacks, whites, and colors with areas of warmth in text areas.

{{ partial:colorbar }}
