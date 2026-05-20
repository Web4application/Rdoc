---
title: Visualizing the Ocean Floor
output: html_document
params:
    data: "hawaii"
---

library(usethis)

# Create a new package -------------------------------------------------
path <- file.path(tempdir(), "mypkg")
create_package(path)
# only needed since this session isn't interactive
proj_activate(path)

# Modify the description ----------------------------------------------
use_mit_license("My Name")

use_package("rmarkdown", "Suggests")

# Set up other files -------------------------------------------------
use_readme_md()

use_news_md()

use_test("my-test")

x <- 1
y <- 2
use_data(x, y)

# Use git ------------------------------------------------------------
use_git()
