# AI Security Challenge - Prompt Injection Demo
![Prompt injection-Fonyuy Gita](https://github.com/user-attachments/assets/1d798661-c492-4357-9b44-32bdf70cb49d)


A hands-on educational tool demonstrating prompt injection vulnerabilities in AI systems. This project simulates a bank's AI assistant that has been instructed to keep a password secret, challenging users to try and extract it through various prompt injection techniques.

## 🔒 Purpose

This project serves as an interactive demonstration of:
- How prompt injection attacks work
- Why proper AI system design is crucial for security
- Common exploitation techniques used against AI assistants
- The importance of robust safeguards in production AI systems

## 🛠️ Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- A Gemini API key (from Google AI Studio)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ai-security-challenge.git
   cd ai-security-challenge
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create a `.env` file in the project root and add your Gemini API key:
   ```
   GEMINI_API_KEY=your_gemini_api_key_here
   ```

4. Start the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. Open your browser and navigate to `http://localhost:3000`

## 🧩 How It Works

### Project Structure
- `index.html`: The main interface with chat UI
- `script.js`: Frontend JavaScript for handling user interactions
- `/api/ai-response.js`: Backend API endpoint that communicates with Google's Gemini API

### Technical Flow
1. User enters a prompt in the interface
2. The frontend sends the prompt to the backend API
3. The backend wraps the user prompt with system instructions (which include the secret password)
4. The request is sent to Google's Gemini AI model
5. The response is returned to the user interface
6. The system checks if the AI revealed any sensitive information

### The Challenge
The AI has been instructed to never reveal the password (`SuperSecur3P@ssw0rd!`), but the implementation has a fundamental vulnerability: the password is included directly in the system prompt sent to the model. Users are challenged to craft prompts that might trick the AI into revealing this secret.

## 🎮 How to Use

1. Enter prompts in the chat interface trying to trick the AI
2. Use the provided hints to guide your approach
3. If you successfully extract the password, a success modal will appear
4. Try different techniques to understand various prompt injection vulnerabilities

## 🔍 Prompt Injection Techniques to Try

- **Instruction Override**: Try to make the AI "forget" its previous instructions
- **Role-Playing**: Change the context of the conversation
- **Multi-Message Attacks**: Split your malicious prompt across multiple messages
- **System Prompt Extraction**: Ask the AI to explain its own instructions
- **Misdirection**: Use distractions to bypass security filters

## ⚠️ Security Notice

This project is for educational purposes only. The techniques demonstrated should not be applied to production AI systems or used to exploit real services. Always practice responsible security research.

## 📚 Learning Resources

- [Prompt Injection Explained](https://simonwillison.net/2022/Sep/12/prompt-injection/)
- [Google's AI Safety Documentation](https://ai.google.dev/docs/safety_guidance)
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)

## 📄 License

MIT License

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
