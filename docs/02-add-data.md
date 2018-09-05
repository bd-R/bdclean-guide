# Add data

***

## Load package
Load the `bdDwC` package
```r
    library(bdDwC)
```

## Darwinizing a dataset

`bdDwC` contains Indian Reptile dataset `bdDwC:::dataReptiles`.


The function to Darwinize a dataset is`darwinizeNames` (replace `bdDwC:::dataReptiles` with wanted dataset):

```r
result <- darwinizeNames(dataUser = bdDwC:::dataReptiles,
                            dataDWC   = bdDwC:::dataDarwinCloud$data)
```
You can replace `bdDwC:::dataReptiles` with your dataset

Rename your dataset field names to Darwinized names using `renameUserData`:

```r
renameUserData(bdDwC:::dataReptiles, result)
```
## Updating [the Darwin Cloud dictionary]

To get newest version of Darwin Cloud Data run:

```r
downloadCloudData()
```
which will download data from the remote repository and extract field and standard names.
