---
title: "Data Wrangling with R"
author: "Ethan Lew"
date: "March 16 2026"
format: 
    html:
        theme: cosmo
        toc: true
        toc-depth: 3
        toc-location: right-body
        embed-resources: true
execute: 
  freeze: auto
---

# Overview

## Learning Outcomes

By the end of this module, you will be able to:

-   Describe the concept of **Data Wrangling**
-   Describe how **Tibbles are different from data frames**
-   Explain how to convert wide or long data to **tidy data**
-   Explain how to merge relational data sets using **join functions** (next module)
-   Be familiar with major **dplyr functions** for transforming data
-   Create a new **variable** with `mutate()` and `case_when()`
-   Use the **pipe operator** to shape data for analysis and visualization

::: callout-tip
### Multi-Cursor Editing Tip

To use the mouse multi-cursor editing feature:

1.  Select the text you want to edit.
2.  Press **Shift + Alt** and click on other locations where you want the cursor.
3.  You can now edit all selected text simultaneously.
:::

# Introduction to Data Wrangling

## Loading Packages

**Note**: - To add a `code chunk`, you can use the keyboard shortcut `Ctrl + Alt + I` (Windows/Linux) or `Cmd + Option + I` (Mac) in RStudio.

```{r}
# install.packages("tidyverse")
# install.packages("nycflights13")
# install.packages("ggplot2")
library(tidyverse)
library(nycflights13)
library(ggplot2)
```

## Tibbles vs Data Frames

**Data sets in package 'nycflight13'**

-   airlines Airline names.
-   airports Airport metadata
-   flights\* Flights data
-   planes Plane metadata.
-   weather Hourly weather data

```{r}
flights_df <- flights

flights_df

```
------------------------------------------------------------------------
