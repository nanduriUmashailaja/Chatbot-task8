# Chatbot-task8
Create a rule-based chatbot.
# Rule-based Chatbot in Python
def chatbot_response(user_input):
    user_input = user_input.lower() 
    #Rules
    if "hello" in user_input or "hi" in user_input:
        return "Hello! How can I help you today?"
    elif "how are you" in user_input:
        return "I'm just a bot, but I'm doing great! How about you?"
    elif "your name" in user_input:
        return "I'm RuleBot, your chatbot assistant."
    elif "bye" in user_input or "goodbye" in user_input:
        return "Goodbye! Have a nice day!"
    elif "time" in user_input:
        from datetime import datetime
        return f"The current time is {datetime.now().strftime('%H:%M:%S')}."
    elif "date" in user_input:
        from datetime import datetime
        return f"Today's date is {datetime.now().strftime('%Y-%m-%d')}."
    else:
        return "I'm not sure how to respond to that. Can you rephrase?"

# Main loop
print("🤖 RuleBot: Hi! I'm your chatbot. Type 'bye' to exit.")
while True:
    user_input = input("You: ")
    if user_input.lower() in ["bye", "goodbye"]:
        print("🤖 RuleBot:", chatbot_response(user_input))
        break
    response = chatbot_response(user_input)
    print("🤖 RuleBot:", response)
