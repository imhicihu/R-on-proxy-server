# R on proxy server (Windows chapter) #

* This README shows the procedures to run R (and RStudio) inside a proxy server (usually in universities and academics environments).

### How do I get set up? ###

* Summary of setup:
    - Install software
    - Run it
    - Run script
* Software needed:
    - [R](https://cran.r-project.org)
    - [RStudio Desktop](https://www.rstudio.com/products/rstudio/#Desktop) 
    - Update to the latest version of R and RStudio to minimize incompatibilities.
* Software version (tests):
    - RStudio (Mac OSX version): 1.0.136
    - R (Mac OSX version): 3.3.3 GUI 1.69 Mavericks build (7328)
* Procedures:
    - Install [R](https://cran.r-project.org/bin/)
    - Install [RStudio Desktop](https://www.rstudio.com/products/rstudio/#Desktop)
    - Previously, gather information about the configuration of your proxy server: `IP address`, `port`, `username`, `password`

-----------------------
### Mac OSX environment ###

* Deployment:
    - Run RStudio
    - In the Console run this script:
        - `Sys.setenv(http_proxy="http://username:password@19X.16X.X.X:3XXX/")`
    - where `username` must be replaced with your username; `password` with your password; `19X.16X.X.X` *i.e.* with this IP address `192.168.4.1` and `3XXX` *i.e.* with this port: `3128`
    - Inside RStudio, click on the `Tools` menu, then `Install packages`. See below, installing the `archivist` package and all the dependencies involved.
![proxy.png](images/4285276611-proxy.png)
    - Once you download your [packages](https://cran.r-project.org/web/packages/available_packages_by_name.html), they will appear automatically in both software: RStudio and R.
    - See below, the package `archivist` version 2.1.2 recognized.

![archivist-rstudio.png](images/1476422623-archivist-rstudio.png)
![archivist-R.png](images/3011197732-archivist-R.png)



### Copyright ###
![88x31.png](images/3902704043-88x31.png)
This work is licensed under a [Creative Commons Attribution-ShareAlike 2.0 Generic License](http://creativecommons.org/licenses/by-sa/2.0/).

### Legal ###

* All trademarks are the property of their respective owners.