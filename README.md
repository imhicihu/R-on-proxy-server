# README #

This README would normally document whatever steps are necessary to get your application up and running.

### What is this repository for? ###

* Run R under a proxy server
* Version 1.0.1

### How do I get set up? ###

* Summary of setup:
    * Install software
    * Run it
    * Run script
* Software needed:
    * [R](https://cran.r-project.org/bin/) (Windows, Mac and Linux)
    * [RStudio Desktop](https://www.rstudio.com/products/rstudio/#Desktop) (Windows, Mac and Linux). 
    * Verify compatibilities between R and RStudio.
* Procedures:
    * Install [R](https://cran.r-project.org/bin/)
    * Install [RStudio Desktop](https://www.rstudio.com/products/rstudio/#Desktop)
    * Gather information about the configuration of your proxy server: IP address, port, username, password
* Deployment instructions:
    * Run RStudio
    * In the Console run this script:
    * `Sys.setenv(http_proxy="http://username:password@19X.16X.X.X:3XXX/")`
    * Replace 
    * Download [packages](https://cran.r-project.org/web/packages/available_packages_by_name.html) needed.
    * Or download the checklist on the [Downloads](https://bitbucket.org/imhicihu/r-on-proxy-server/downloads/) section.

### Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines