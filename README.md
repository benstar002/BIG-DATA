Group Members:
1. HURUMA Innocent           ID:25514
2. Kajibwami Baraka Joel     ID:26091
3. Nibishaka Thoti Pacifique ID:26543
4. Nzayisenga Bernard        ID:25286





#Question 1. 
def input_student_info():

    name = input("Enter student's name: ")
    age = int(input("Enter student's age: "))
    
    num_courses = int(input("Enter number of courses (2 or 3): "))
    while num_courses not in [2, 3]:
        print("You can only enter 2 or 3 courses.")
        num_courses = int(input("Enter number of courses (2 or 3): "))
    
    grades = []
    for i in range(num_courses):
        grade = float(input(f"Enter grade for course {i + 1}: "))
        grades.append(grade)

    return name, age, grades

def calculate_average(grades):
    
    if len(grades) == 0:
        return 0
    return sum(grades) / len(grades)

def display_student_info(name, age, grades, average):
   
    print("\n--- Student Information ---")
    print(f"Name: {name}")
    print(f"Age: {age}")
    print("Grades:", ", ".join([str(g) for g in grades]))
    print(f"Average Grade: {average:.2f}")

def main():
   
    name, age, grades = input_student_info()
    average = calculate_average(grades)
    display_student_info(name, age, grades, average)
main()


# Question 2
def check_palindrome():
   
    user_input = input("Enter a string: ")

   
    clean_input = user_input.replace(" ", "").lower()

    
    if clean_input == clean_input[::-1]:
        print("Yes, it is a palindrome")
    else:
        print("No, it is not a palindrome")
check_palindrome()

# Question 3
def process_texts():
    
    text1 = input("Enter the first text: ")
    text2 = input("Enter the second text: ")

 
    combined_text = text1 + text2

    characters = [char for char in combined_text]


    print("Thank you for using my application")

 
    return characters


chars = process_texts()
print("Characters in combined text:", chars)
