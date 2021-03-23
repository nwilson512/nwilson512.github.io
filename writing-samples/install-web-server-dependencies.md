---
title: 'Install web server dependencies'
type: task
---

[← Back to landing](/writing-samples/create-a-statamic-web-server-on-google-cloud-platform)

Once you've created your GCP VM and enabled access by adding your key to the metadata, you can configure your VM as a web server. Just as with development, start configuration by installing dependencies.

**Perform the following steps to install dependencies on your GCP VM:**

1. Update the **apt** package manager:

  ```
  sudo apt update
  ```

2. Install Git:

  ```
  sudo apt install git
  ```

3. [Install php 7.3](https://computingforgeeks.com/how-to-install-php-7-3-on-debian-9-debian-8/)

[← Back to landing](/writing-samples/create-a-statamic-web-server-on-google-cloud-platform)
