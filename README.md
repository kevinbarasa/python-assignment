# python-assignment

--------------------------------------------------python code assignment--------------------------------------------

def calculate_grade(marks):
    if marks >= 90:
        return "A+"
    elif marks >= 80:
        return "A"
    elif marks >= 70:
        return "B"
    elif marks >= 60:
        return "C"
    elif marks >= 50:
        return "D"
    else:
        return "Fail"


def get_valid_marks():
    while True:
        try:
            marks = float(input("Enter the marks obtained by the student: "))
            if 0 <= marks <= 100:
                return marks
            else:
                print("Invalid input! Marks should be between 0 and 100.")
        except ValueError:
            print("Invalid input! Please enter a valid number for marks.")


def main():
    while True:
        print("\n*** Student Grading Program ***")
        marks = get_valid_marks()
        grade = calculate_grade(marks)
        print(f"Grade: {grade}")

        choice = input("Do you want to calculate the grade for another student? (yes/no): ").lower()
        if choice != "yes":
            break

    print("Exiting the program.")


if __name__ == "__main__":
    main()

