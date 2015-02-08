# plotting the four graphs
##Worklog
##read and subsetting data
directory <- "C:/Users/map05/Documents/Silconvalley"
electricity <- read.table("household_power_consumption.txt", header = T,  sep=";", comment.char="%", stringsAsFactors=FALSE, na.strings="?")
dataplott<- subset(electricity, electricity$Date=="1/2/2007"|electricity$Date=="2/2/2007") 
## plotting graph 1
directory <- "C:/Users/map05/Documents/Silconvalley"
electricity <- read.table("household_power_consumption.txt", header = T,  sep=";", comment.char="%", stringsAsFactors=FALSE, na.strings="?")

hist(subset(Nudataplott)$Global_active_power,xlab = "Global Active Power(kilowatts)",  col = "red", main = "Global Active Power")
"code for plot 2
plot(Nudataplott$datetimer, Nudataplott$Global_active_power, type="l", xlab ="datetime", pch=22,ylab= "Global Active Power (kilowatts)")
##code for plot 3
plot(Nudataplott$datetimer, Nudataplott$Sub_metering_1, type="n", xlab="datetime", ylab="Energy Sub metering")

sub_metering1 <- data.frame(sub_metering, datetimer)

str(sub_metering)

sub_meter1 <- sub_metering$submeter1
Sub_meter2 <- sub_metering$submeter2
Sub_meter3 <- sub_metering$submeter3
date_time <- sub_metering$datetimmed

str(sub_metering)

submeter1 <- Nudataplott$Sub_metering_1
submeter2 <-  Nudataplott$Sub_metering_2
submeter3 <- Nudataplott$Sub_metering_3
datetimmed <- Nudataplott$datetimer

sub_range <- range(0, submeter1, submeter2, submeter3)

plot(sub_metering$datetimmed, sub_metering$submeter1, type="l", col="black", ylim=sub_range, xlab ="datetime",  ylab= "Energy Sub metering")
lines(sub_metering$datetimmed,sub_metering$submeter2, type ="l", col="red")
lines(sub_metering$datetimmed,sub_metering$submeter3, type= "l", col="blue")
legend("topright", pch =1, col= c("black", "red", "blue"), legend =c("sub_metering_1", "sub_metering_2", "sub_metering_3")) 

##code for plot 4
par(mfrow =c(2,2))

plot(Nudataplott$datetimer,Nudataplott$Global_active_power,type="l",  ylab ="Global Active Power(kilowatts)", xlab="datetime")
plot(Nudataplott$datetimer,Nudataplott$Voltage, type="l", xlab = "datetime",ylab="Voltage")

str(sub_metering)

submeter1 <- Nudataplott$Sub_metering_1
submeter2 <-  Nudataplott$Sub_metering_2
submeter3 <- Nudataplott$Sub_metering_3
datetimmed <- Nudataplott$datetimer

sub_range <- range(0, submeter1, submeter2, submeter3)

plot(sub_metering$datetimmed, sub_metering$submeter1, type="l", col="black", ylim=sub_range, xlab ="datetime",  ylab= "Energy Sub metering")
lines(sub_metering$datetimmed,sub_metering$submeter2, type ="l", col="red")
lines(sub_metering$datetimmed,sub_metering$submeter3, type= "l", col="blue")
legend("topright", pch =1, col= c("black", "red", "blue"), legend =c("sub_metering_1", "sub_metering_2", "sub_metering_3")) 

plot(Nudataplott$datetimer,Nudataplott$Global_reactive_power,type="l", xlab="datetime", ylab = "Global Reactive Power")


