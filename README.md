def get_response(user_input):
    """Return a predefined reply based on the user's input."""
    text = user_input.lower().strip()

    if text in ("hello", "hi", "hey"):
        return "Hi!"
    elif text in ("how are you", "how are you?"):
        return "I'm fine, thanks!"
    elif text in ("bye", "goodbye", "exit", "quit"):
        return "Goodbye!"
    elif text in ("what is your name", "who are you"):
        return "I'm a simple chatbot!"
    elif text in ("thanks", "thank you"):
        return "You're welcome!"
    else:
        return "Sorry, I don't understand that."


def chat():
    """Run the chatbot loop until the user says bye."""
    print("Chatbot: Hi! Type 'bye' to end the chat.")

    while True:
        user_input = input("You: ")
        reply = get_response(user_input)
        print("Chatbot:", reply)

        if user_input.lower().strip() in ("bye", "goodbye", "exit", "quit"):
            break


if __name__ == "__main__":
    chat()
    
