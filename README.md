# Rails associations exercise
Create the tables, models and associations required to get the following methods working:

## Setup methods
student_one = {name:'Jason'}
student_two = {name:'Yomi'}
teacher = {name:'Ian'}

@student_one = Student.create(student_one)
@student_two = Student.create(student_two)
@teacher = Teacher.create(teacher)

@teacher.students << @student_one
@teacher.students << @student_two

## Testing methods
@teacher.students # should return and Jason and Yomi (inside an ActiveRecord::Associations::CollectionProxy)
@student_one.teachers #should return Ian (inside an ActiveRecord::Associations::CollectionProxy)
