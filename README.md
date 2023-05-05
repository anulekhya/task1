# task1
Solution for task1 of Sparks Foundation Internship in R(programming language)
data<-read.csv("https://raw.githubusercontent.com/AdiPersonalWorks/Random/master/student_scores%20-%20student_scores.csv")
head(data)
summary(data)
str(data)
any(is.na(data))
x<-data$Hours
y<-data$Scores
plot(x ~ y)
abline(lm(x ~ y))
model<-lm(y ~ x)
Score.prediction<-predict(model,data)
print(Score.prediction)
#prediction of the score of a student who studies 9.25hrs/day
object<-data.frame(x=9.25)
result<-predict(model,object)
print(result)
