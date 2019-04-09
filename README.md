![stability-wip](https://img.shields.io/badge/status%3A%20-archived-orange.svg)

# Rationale #

* This README shows the procedures to run R (and RStudio) inside a proxy server (usually in universities and academics environments).
* This guide is a living document that will grow and adapt over time.

### What is this repository for? ###

* Execute R on a proxy server
* Tested in MacOSX & Windows environments (up to now)

### How do I get set up? ###

* Summary of setup:
    - Install software
    - Run it
    - Run script
* Software needed:
    - [R](https://cran.r-project.org) (Windows, Mac and Linux)
    - [RStudio Desktop](https://www.rstudio.com/products/rstudio/#Desktop) (Windows, Mac and Linux). 
    - Update to the latest version of R and RStudio to minimize incompatibilities.
* Software version (tests):
    - RStudio (Mac OSX version): 1.0.136
    - R (Mac OSX version): 3.3.3 GUI 1.69 Mavericks build (7328)
    - R (Windows version): 3.3.3 64 bits
* Procedures:
    - Install [R](https://cran.r-project.org/bin/)
    - Install [RStudio Desktop](https://www.rstudio.com/products/rstudio/#Desktop)
    - Previously, gather information about the configuration of your proxy server: IP address, port, username, password

-----------------------
### Mac OSX environment ###

* Deployment:
    - Run RStudio
    - In the Console run this script:
        - `Sys.setenv(http_proxy="http://username:password@19X.16X.X.X:3XXX/")`
    - where `username` must be replaced with your username; `password` with your password; `19X.16X.X.X` *i.e.* with this IP address `192.168.4.1` and `3XXX` *i.e.* with this port: `3128`
    - Inside RStudio, click on the `Tools` menu, then `Install packages`. See below, installing the `archivist` package and all the dependencies involved.
![proxy.png](https://bitbucket.org/repo/4pKrXRd/images/4285276611-proxy.png)
    - Once you download your [packages](https://cran.r-project.org/web/packages/available_packages_by_name.html), they will appear automatically in both software: RStudio and R.
    - See below, the package `archivist` version 2.1.2 recognized.

![archivist-rstudio.png](https://bitbucket.org/repo/4pKrXRd/images/1476422623-archivist-rstudio.png)
![archivist-R.png](https://bitbucket.org/repo/4pKrXRd/images/3011197732-archivist-R.png)

-----------------------
### Windows environment ###
* Deployment:
    - Run R
    - In the Console run this script:
        - `file.edit('~/.Renviron')`
    - Automatically it will bring a new window. Introduce this statements:
        - `options(internet.info = 0)`
        - `http_proxy = http:// username:password@19X.16X.X.X:3XXX`
        - `http_proxy_user = username:password`
        - `https_proxy = https:// username:password0@19X.16X.X.X:3XXX`
        - `https_proxy_user = username:password`
        - `ftp_proxy = username:password@19X.16X.X.X:3XXX`
    * It should be pointed that `username` must be replaced with your username; `password` with your password; `19X.16X.X.X` *i.e.* with this IP address `192.168.4.1` and `3XXX` *i.e.* with this port: `3128`
    * Restart R
    * In the console, introduce this statement
        - `install.packages("XXXXXXX",method="libcurl")`
    * Replace `"XXXXXXX"` with the [name of the package](https://cran.r-project.org/web/packages/available_packages_by_name.html) you need.

![archivist.png](https://bitbucket.org/repo/4pKrXRd/images/377615290-archivist.png)

-----------------------
### Contribution guidelines ###

* The less steps, the better
* Plain english

### Releases ###

* Download the checklist on the [Downloads](https://bitbucket.org/imhicihu/r-on-proxy-server/downloads/) section (soon to be released).

### Changelog ###

* Please check the [Commits](https://bitbucket.org/imhicihu/r-on-proxy-server/commits/) section for the current status

### Copyright ###
![88x31.png](https://bitbucket.org/repo/4pKrXRd/images/3902704043-88x31.png)
This work is licensed under a [Creative Commons Attribution-ShareAlike 2.0 Generic License](http://creativecommons.org/licenses/by-sa/2.0/).

### Legal ###

* All trademarks are the property of their respective owners.