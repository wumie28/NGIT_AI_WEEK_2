class Student :

    def __init__(self, name:str, student_id:str):
                self.student_id = student_id
                self.score_list = []
                self.student_id = student_id
                self.name = name
                
          
                
                
                
    def  add_score(self, *score):
            try:
               for i in score:

                 if   0 <= i <= 100 :
                      self.score_list.append(i) 
                      print (f"score {i}  added for {self.name}")
                 else:
                        print ("score must be between 0 and 100")
                 return "All valid score have been added" 
            except ValueError:
                print ("Error : Invalid Score ")





    def calculate_average(self):
          average = sum(self.score) / len (self.score)    
          return average 

    def get_grade(self):
         average_score = self.calculate_average()
         if  average_score >=70 :
              return "Grade A"
         elif average_score >= 60:
              return "Grade B"
         elif average_score>=40:
              return "Grade C"
         elif average_score >=30:
              return "Grade D"
         else: 
              return "Grade F"



    def print_report(self) :
        print(f"Report for {"self.name"} of student id of {self.student}")
        print(f"scores: {self.score_list}")
        print(f"Average:{self.calculate_average()}")
        print(f"Grade:{self.get_grade()}")


james =  Student("James" , "wds_0015")  
john =   Student("John" ,  "wds_0005") 
jack =   Student("Jack", "wds_0009") 

james.add_score(60)
james.add_score(70)


john.add_score (70)
john.add_score (50)


jack.add_score (65)
jack.add_score(72)







                











