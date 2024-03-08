# Overview

This is Kevin Kosewick and Emma Hardin-Parker's MADA project repository.

# Structure

* All data goes into the subfolders inside the `data` folder.
* All code goes into the `code` folder or subfolders.
* All results (figures, tables, computed values) go into `results` folder or subfolders.
* All products (manuscripts, supplement, presentation slides, web apps, etc.) go into `products` subfolders.
* The `renv` folder is automatically generated by the `renv` package, and is
used to keep track of packages.
* See the various `README.md` files in those folders for some more information.

# Content 
* The `renv` folder is automatically generated by the `renv` package and you
should never edit it manually. This folder is used to store information about
the packages you are using in your project.
* There are multiple special files in the repo.
  * `README.md`: this file contains instructions or details about the folder it
  is located in. You are reading the project-level `README.md` file right now.
  * `renv.lock`: a special file in JSON format used to keep a log of which
  packages and versions your project uses.
  * `.gitignore`: this file gives instructions to the version control system,
  Git, and tells it which files we do not need to record versions of. Usually
  these are various files containing local settings.
  * `.Rprofile`: whenever you restart the R session, R will source (run all
  code in) this script. Right now this is used by `renv` to make sure we have
  the correct packages and versions installed.

You can read about keeping track of projects with `renv`
[here](https://rstudio.github.io/renv/articles/renv.html).
Basically, whenever you install new packages or update old packages, you need
to run `renv::snapshot()` to update the `renv.lock` file, which is a list of
packages and versions that the package uses. When you open the R project on a
new computer, you can run `renv::restore()` to reinstall all the packages that
you recorded in the `renv.lock` file.


