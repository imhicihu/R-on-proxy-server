# README #

This README shows the procedures to run R (and RStudio) inside a proxy server (usually in universities and academics environments). 

### What is this repository for? ###

* Execute R on a proxy server
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
    * where `username` must be replaced with your username; `password` with your password; `19X.16X.X.X` -in my case- with this IP address `192.168.4.1` and `3XXX` -in my case- with this port: `3128`.
    * Inside RStudio, click on the `Tools` menu, then `Install packages`. See below, installing the `archivist` package and all the dependencies involved.
![proxy.jpg](https://bitbucket.org/repo/4pKrXRd/images/947355778-proxy.jpg)
    * Download your [packages](https://cran.r-project.org/web/packages/available_packages_by_name.html) as needed.
    * Or download the checklist on the [Downloads](https://bitbucket.org/imhicihu/r-on-proxy-server/downloads/) section (soon to be released).

### Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines