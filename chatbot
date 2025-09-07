# Codealpha_repsitoryname
import java.util.*;

public class ChatBot {
    private static final Map<String, String> responses = new HashMap<>();

    static {
        // Frequently Asked Questions (FAQs)
        responses.put("hello", "Hi there! How can I help you today?");
        responses.put("hi", "Hello! What can I do for you?");
        responses.put("how are you", "I'm just a bot, but I'm doing great! Thanks for asking.");
        responses.put("your name", "I'm ChatBot, your virtual assistant!");
        responses.put("bye", "Goodbye! Have a great day!");
        responses.put("what is ai", "Artificial Intelligence (AI) is the simulation of human intelligence in machines.");
        responses.put("what is java", "Java is a high-level, object-oriented programming language used worldwide.");
        responses.put("thanks", "You're welcome! Happy to help 😊");
    }

    private static String preprocess(String input) {
        // Lowercase and remove punctuation
        return input.toLowerCase().replaceAll("[^a-zA-Z0-9 ]", "").trim();
    }

    private static String getResponse(String input) {
        input = preprocess(input);

        // Direct matching
        if (responses.containsKey(input)) {
            return responses.get(input);
        }

        // Keyword-based responses
        if (input.contains("weather")) {
            return "I can't check live weather yet, but you can try Google Weather 🌤️.";
        } else if (input.contains("time")) {
            return "The current time is " + new Date();
        } else if (input.contains("help")) {
            return "Sure! I can answer questions about AI, Java, or just chat casually.";
        }

        return "I'm not sure about that. Can you rephrase?";
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("🤖 ChatBot: Hello! Ask me anything (type 'bye' to exit).");

        while (true) {
            System.out.print("You: ");
            String userInput = scanner.nextLine();

            if (preprocess(userInput).equals("bye")) {
                System.out.println("🤖 ChatBot: " + responses.get("bye"));
                break;
            }

            String botResponse = getResponse(userInput);
            System.out.println("🤖 ChatBot: " + botResponse);
        }

        scanner.close();
    }
}

