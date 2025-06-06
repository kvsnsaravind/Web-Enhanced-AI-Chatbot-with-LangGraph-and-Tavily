# Web-Enhanced-AI-Chatbot-with-LangGraph-and-Tavily
A memory-aware AI chatbot with real-time web search using Tavily and LLaMA 3 via Groq.


# 🧠 Web-Enhanced Memory Chatbot with LangGraph + Tavily + LLaMA 3

> A stateful, intelligent chatbot powered by LangGraph, with persistent memory and real-time web search via Tavily.

---

## 🚀 Features

- 🗣️ **Conversational Chatbot**: Responds intelligently to user input using Groq-hosted LLaMA 3.
- 🧠 **Memory Support**: Maintains conversation state using LangGraph’s stateful workflow engine.
- 🌐 **Web Search Tool**: Uses Tavily to answer real-world, up-to-date questions with internet results.
- 🔁 **Dynamic Routing**: If LLM decides a tool is needed, it automatically routes the query to Tavily and then continues the chat.

---

## 🧱 Tech Stack

| Component       | Description                            |
|------------------|----------------------------------------|
| **LangGraph**     | For building and managing stateful workflows |
| **LangChain**     | Prompt chaining, tool binding          |
| **Groq**          | Runs LLaMA 3 with ultra-low latency   |
| **LLaMA 3**       | Language model used for reasoning     |
| **Tavily**        | Web search tool for real-time info    |
| **Python**        | Programming language for implementation |

---

## 🔧 Setup Instructions

### 1. Install Dependencies

```
pip install langchain langgraph langchain_community python-dotenv
````

> If you're using Groq, also set your API key in your environment.

### 2. Set API Keys

In your Python script or `.env` file:

```
GROQ_API_KEY=your-groq-api-key
TAVILY_API_KEY=your-tavily-api-key
```

---

## 🧠 How It Works

1. 🧾 **User Message**: A message enters the system (`state["messages"]`).
2. 🧠 **Chatbot Node**: LLaMA 3 responds. If it needs a tool, LangGraph routes to the `ToolNode`.
3. 🌍 **Tavily Tool**: Executes real-time web search and returns results.
4. 🔁 **Back to Chatbot**: LangGraph routes back to LLM to process the tool output.
5. 📬 **Memory**: Conversation history is retained using `add_messages`.

---

## 🧩 Example Usage

Run the script and interact:

```
User: What's the capital of France?
Assistant: The capital of France is Paris.

User: What is the latest news about OpenAI?
Assistant: (Uses Tavily to fetch recent articles...)
```

## 📜 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

* [LangChain](https://github.com/langchain-ai/langchain)
* [LangGraph](https://github.com/langchain-ai/langgraph)
* [Tavily](https://www.tavily.com/)
* [Groq](https://groq.com/)
* [Meta LLaMA 3](https://ai.meta.com/llama/)

