# README #

This README shows the procedures to run R (and RStudio) inside a proxy server (usually in universities and academics environments). 

### What is this repository for? ###

* Execute R on a proxy server
* Tested in MacOSX environment

### How do I get set up? ###

* Summary of setup:
    * Install software
    * Run it
    * Run script
* Software needed:
    * [R](https://cran.r-project.org/bin/) (Windows, Mac and Linux)
    * [RStudio Desktop](https://www.rstudio.com/products/rstudio/#Desktop) (Windows, Mac and Linux). 
    * Verify compatibilities between R and RStudio. Update to the latest version to minimize incompatibilites.
* Software version (tests):
    * RStudio (Mac OSX version): 1.0.136
    * R (Mac OSX version): 3.3.3 GUI 1.69 Mavericks build (7328)
    * R (Windows version):
* Procedures:
    * Install [R](https://cran.r-project.org/bin/)
    * Install [RStudio Desktop](https://www.rstudio.com/products/rstudio/#Desktop)
    * Gather information about the configuration of your proxy server: IP address, port, username, password

### Mac OSX environment ###

* Deployment:
    * Run RStudio
    * In the Console run this script:
    * `Sys.setenv(http_proxy="http://username:password@19X.16X.X.X:3XXX/")`
    * where `username` must be replaced with your username; `password` with your password; `19X.16X.X.X` -in my case- with this IP address `192.168.4.1` and `3XXX` -in my case- with this port: `3128`.
    * Inside RStudio, click on the `Tools` menu, then `Install packages`. See below, installing the `archivist` package and all the dependencies involved.
![proxy.jpg](https://bitbucket.org/repo/4pKrXRd/images/623860906-proxy.jpg)
    * Once you download your [packages](https://cran.r-project.org/web/packages/available_packages_by_name.html), they will appear automatically in both software: RStudio and R.
    * See below, the package `archivist` version 2.1.2 recognized by both software.
![archivist-rstudio.jpg](https://bitbucket.org/repo/4pKrXRd/images/3761449446-archivist-rstudio.jpg)
![archivist-R.jpg](https://bitbucket.org/repo/4pKrXRd/images/871921475-archivist-R.jpg)

### Windows environment ###
* Deployment:
    * Run R
    * In the Console run this script:
    * `file.edit('~/.Renviron')`
    * Automatically it will bring a new window. Introduce this statements:
    * `options(internet.info = 0)`
    * `http_proxy = http:// username:password@19X.16X.X.X:3XXX`
    * `http_proxy_user = username:password`
    * `https_proxy = https:// username:password0@19X.16X.X.X:3XXX`
    * `https_proxy_user = username:password`
    * `ftp_proxy = username:password@19X.16X.X.X:3XXX`
    * It should be pointed that `username` must be replaced with your username; `password` with your password; `19X.16X.X.X` -in my case- with this IP address `192.168.4.1` and `3XXX` -in my case- with this port: `3128`.
    * Restart R
    * In the console, introduce this statement
    * `install.packages("XXXXXXX",method="libcurl")`
    * Replace `"XXXXXXX"` with the name of the package you need.
### Contribution guidelines ###

* The less steps, the better
* Plain english

### Releases ###

* Download the checklist on the [Downloads](https://bitbucket.org/imhicihu/r-on-proxy-server/downloads/) section (soon to be released).