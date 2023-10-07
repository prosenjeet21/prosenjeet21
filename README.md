# Define a dictionary of true/false questions and their correct answers
true_false_questions = {
    "DNA is composed of two strands, one of which is complementary to the other. (True/False)": True,
    "Prokaryotic cells have a nucleus. (True/False)": False,
    "RNA is single-stranded. (True/False)": True,
    "Mitochondria are found in plant cells. (True/False)": True,
    "All cells have a cell membrane. (True/False)": True
}

# Function to ask true/false questions and check answers
def ask_true_false_question(question, correct_answer):
    user_answer = input(f"{question} ").strip().lower()
    if user_answer == "true" and correct_answer is True:
        return True
    elif user_answer == "false" and correct_answer is False:
        return True
    else:
        return False

# Function to quiz the user
def quiz_user(true_false_questions):
    score = 0
    for question, correct_answer in true_false_questions.items():
        if ask_true_false_question(question, correct_answer):
            print("Correct!")
            score += 1
        else:
            print("Incorrect.")
    
    print(f"You got {score}/{len(true_false_questions)} questions correct.")

# Start the quiz
print("Welcome to the True/False Quiz!")
quiz_user(true_false_questions)
