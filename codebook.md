library("data.table", "reshape2","knitr")



subTrain <- fread(file.path(getwd(), "train", "subject_train.txt"))
subTest <- fread(file.path(getwd(), "test" , "subject_test.txt" ))
subAll <- rbind(subTrain, subTest)

yTrain <- fread(file.path(getwd(), "train", "Y_train.txt"))
yTest  <- fread(file.path(getwd(), "test" , "Y_test.txt" ))
yAll <- rbind(yTrain, yTest)

xTrain  <- data.table(read.table(file.path(getwd(), "train", "x_train.txt")))
xTest  <- data.table(read.table(file.path(getwd(), "test", "x_test.txt")))
xAll  <- rbind(xTrain, xTest)

fullSet  <- cbind(subAll,yAll)
fullSet <- cbind(xAll, fullSet)he


