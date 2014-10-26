getting-cleaning-data-project
=============================

Introduction
=============================

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis.This repository contains my work for this course.

About the raw data
=============================

The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

About the script
=============================

Summary:I created a script called run_analysis.R which will merge the test and training sets together. 

1. Download the data source and put into a folder on your local drive. You'll have a UCI HAR Dataset folder.
2.After merging testing and training, labels are added and only columns that have to do with mean and standard deviation are kept.
3.The script will create a tidy data set containing the means of all the columns per test subject and per activity. 

About the Code Book
=============================

The CodeBook.md file shows information about raw and tidy data set and elaboration made to transform them.
