AG News Dataset (subset)
========================

This dataset contains short news article texts drawn from the AG News corpus.

Files
-----
train.csv         - 120,000 labelled news texts (header row + 120,000 samples)
test_no_labels.csv -  7,600 news texts without labels (header row + 7,600 samples)

Classes
-------
1 - World
2 - Sports
3 - Business
4 - Sci/Tech

Format
------
train.csv columns:        Class Index, Title, Description
test_no_labels.csv columns: Title, Description

Loading the data (pseudocode)
------------------------------
rows = []
for each line in CSV file (skip header):
    fields = split line by comma (respecting quoted fields)
    rows.append(fields)

# For train.csv each row is: (class_index, title, description)
# For test_no_labels.csv each row is: (title, description)
