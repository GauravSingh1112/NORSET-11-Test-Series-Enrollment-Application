# NORSET 11 Test Series Enrollment Application

class Student:
    def __init__(self, name, email, phone):
        self.name = name
        self.email = email
        self.phone = phone

    def display(self):
        print(f"Name: {self.name}")
        print(f"Email: {self.email}")
        print(f"Phone: {self.phone}")
        print("-" * 30)


class TestSeriesEnrollment:
    def __init__(self):
        self.students = []

    def enroll_student(self):
        print("\n--- Enroll for NORSET 11 Test Series ---")
        name = input("Enter your name: ")
        email = input("Enter your email: ")
        phone = input("Enter your phone number: ")

        student = Student(name, email, phone)
        self.students.append(student)

        print("\nEnrollment Successful!")

    def view_students(self):
        print("\n--- Enrolled Students ---")
        if not self.students:
            print("No students enrolled yet.")
        else:
            for i, student in enumerate(self.students, start=1):
                print(f"\nStudent {i}:")
                student.display()

    def run(self):
        while True:
            print("\n===== NORSET 11 Test Series =====")
            print("1. Enroll Student")
            print("2. View Enrolled Students")
            print("3. Exit")

            choice = input("Enter your choice: ")

            if choice == "1":
                self.enroll_student()
            elif choice == "2":
                self.view_students()
            elif choice == "3":
                print("Exiting application. Goodbye!")
                break
            else:
                print("Invalid choice. Try again.")


# Run the application
if __name__ == "__main__":
    app = TestSeriesEnrollment()
    app.run()
