# 1) CLEAR ALL Variables (and also clear the screen)
rm(list=ls())
cat("\014")

# 2) Tell your Code WHERE your Data is (i.e., SET the PATH)
library(rstudioapi)
setwd(dirname(rstudioapi::getActiveDocumentContext()$path))
         
# 3) Read in the data.
WebData = read.csv("webdata.csv")

# 4) Explore the data
str(WebData)
summary(WebData)

###############################################################################################################
# HISTOGRAM
# "Create a histogram showing the distribution of customer ages."
hist(WebData$transactionRevenue,main = paste("Histogram of Transaction Revenue"),xlab = "transactionRevenue") 


###############################################################################################################
# HISTOGRAM FOR Sources
# "How do customers coming from Direct vs. Search compare in terms of total number of transaction revenue?"

# Make Traffic Sources
WebData.Direct   <- subset(WebData, source_num == 0)
WebData.Search <- subset(WebData, source_num == 1)

hist(WebData.Direct$transactionRevenue,main = paste("Histogram of Transaction Revenue for Direct"),xlab = "Transaction Revenue")
hist(WebData.Direct$transactionRevenue,main = paste("Histogram of Transaction Revenue for Search"),xlab = "Transaction Revenue")
hist(WebData.Direct$transactions,main = paste("Histogram of # of Transactions for Direct"),xlab = "# of Transactions")
hist(WebData.Direct$transactions,main = paste("Histogram of # of Transactions for Search"),xlab = "# of Transactions")
