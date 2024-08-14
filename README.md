# Healthcare-Bot-system-using-python
# Healthcare Bot System

# Knowledge Base
knowledge_base = {
    "What is the treatment for fever?": "The treatment for fever typically involves rest, hydration, and over-the-counter medications such as acetaminophen or ibuprofen.",
    "What are the symptoms of diabetes?": "The symptoms of diabetes include increased thirst and urination, fatigue, and blurred vision.",
    "How can I prevent heart disease?": "Preventing heart disease involves maintaining a healthy diet, exercising regularly, and managing stress.",
    "What is the cure for cancer?": "There is no single cure for cancer, but treatment options include surgery, chemotherapy, and radiation therapy.",
    "What are the symptoms of flu?": "The symptoms of flu include fever, cough, sore throat, and body aches."
}

# Response Generator
def generate_response(user_input):
    for question, answer in knowledge_base.items():
        if user_input.lower() in question.lower():
            return answer
    return "I'm not sure about that. Can you please rephrase your question?"

# Chatbot Interface
def chatbot():
    print("Welcome to the Healthcare Bot!")
    while True:
        user_input = input("Enter your question or symptom: ")
        response = generate_response(user_input)
        print("Bot: " + response)

# Run Chatbot
chatbot()
