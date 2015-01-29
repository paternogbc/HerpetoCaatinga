# HerpetoCaatinga
This database contains herpetofauna species list for most of the Protected Areas in Caatinga, Northeast Brazil.

### Protected areas covered:
1- Estação Ecológica Raso da Catarina  
2- Estação Ecológica Aiuaba  
3- Estação Ecológica Seridó  
4- Parque Nacional Serra da Capivara  
5- Parque Nacional Serra das Confusões   
6- Parque Nacional Ubajara  
7- Parque Nacional Chapada Diamantina  
8- Parque Nacional Catimbau  

### How to use this dataset?

* Load data in Excell:  

Copy [Raw data]( https://raw.githubusercontent.com/paternogbc/HerpetoCaatinga/master/Herpeto_dataset.csv) to clipboard. Paste in Excell and choose to separate colum with comma (.csv). 

* Or load data in R:  

1. First install these packages:
```{r}
install.packages("RCurl")
install.packages("foreign")
```

2. Load data from Github to R

```{r}
library(RCurl);library(foreign)
url.data <- paste("https://raw.githubusercontent.com/paternogbc/HerpetoCaatinga/master/Herpeto_dataset.csv",sep="")
myData <- getURL(url.data,ssl.verifypeer = FALSE)
mat <- read.csv(textConnection(myData))
``` 


