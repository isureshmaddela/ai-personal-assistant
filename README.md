# ai-personal-assistant
Your personal mentors, anytime. Anywhere.

MentorAgents is an AI-powered platform where users interact with agents modeled after legendary real-world experts—like Elon Musk for startups, Naval Ravikant for wealth, or Lex Fridman for AI. Ask questions, get tailored guidance, and learn from the best minds — anytime, anywhere.

🚀 Features
Legendary Mentor AI Agents: Chat with AI versions of famous entrepreneurs, investors, and thought leaders
Intelligent Memory System: Both short-term and long-term memory capabilities using MongoDB
RAG-Powered Knowledge: Vector database containing comprehensive mentor profiles, life experiences, and wisdom
Gamified Learning Experience: Interactive React-based frontend with engaging user experience
Real-time Conversations: Fast and responsive chat interface powered by FastAPI
Personalized Insights: Get tailored advice based on your specific questions and context
🛠 Tech Stack
Backend
FastAPI - High-performance Python web framework
LangGraph - Advanced AI agent orchestration with memory management
LangChain - LLM integration and RAG implementation
MongoDB - Document database for persistent memory and state management
Vector Database - Semantic search for mentor knowledge retrieval
Groq - Fast LLM inference
Sentence Transformers - Text embeddings for RAG
Frontend - Todo
React - Modern frontend framework
Interactive UI - Gamified chat experience
🏗 Architecture
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   React Web     │    │   FastAPI        │    │   MongoDB       │
│   Frontend      │◄──►│   Backend        │◄──►│   Database      │
│                 │    │                  │    │                 │
└─────────────────┘    └──────────────────┘    └─────────────────┘
                                │
                                ▼
                       ┌──────────────────┐
                       │   LangGraph      │
                       │   AI Agents      │
                       │                  │
                       └──────────────────┘
                                │
                                ▼
                       ┌──────────────────┐
                       │   Vector DB      │
                       │   (RAG System)   │
                       │                  │
                       └──────────────────┘
Key Components
AI Agent Layer: LangGraph manages intelligent conversations with mentor personalities
Memory Management:
Short-term memory for conversation context
Long-term memory for user preferences and history
Knowledge Retrieval: RAG system pulls relevant mentor insights from vector database
API Layer: FastAPI provides high-performance backend services
Data Persistence: MongoDB stores conversation history and agent states
🚀 Quick Start
Prerequisites
Python 3.11+
Node.js 16+
MongoDB instance
Groq API key
Backend Setup
Clone the repository

https://github.com/shubhamprajapati7748/mentoragents.git
cd mentoragents/backend
Install dependencies

# Using uv (recommended)
uv install

# Or using pip
pip install -e .
Environment Configuration

cp .env.example .env
# Edit .env with your API keys and configuration
To Create long term memory

python src/mentoragents/tools/create_long_term_memory.py
Run the backend

uvicorn mentoragents.main:app --reload --host 127.0.0.1 --port 8080
The API will be available at http://127.0.0.1:8080.

The API docs will be available at http://127.0.0.1:8080/docs.

🤖 Available Mentors
Naval Ravikant - Entrepreneur, Angel Investor, Philosophy
Elon Musk - Innovation, Technology, Space Exploration
Warren Buffett - Investing, Business Strategy, Long-term Thinking
And many more... (Expanding mentor library)
💬 How It Works
Choose Your Mentor: Select from available mentor personalities
Ask Your Question: Type your question or describe your challenge
Get Personalized Advice: The AI agent retrieves relevant knowledge and provides mentor-style guidance
Continue the Conversation: Build on previous discussions with persistent memory
🧠 Memory System
Short-term Memory: Maintains conversation context within sessions
Long-term Memory: Remembers user preferences, past topics, and learning progress
Knowledge Base: Continuously updated mentor profiles and experiences
🔧 Configuration
Key configuration options in backend/src/mentoragents/core/config.py:

RAG Settings: Embedding model, chunk size, retrieval parameters
Memory Settings: Message limits, summary triggers
Database Settings: MongoDB collections and connection settings
API Settings: CORS, server configuration
🤝 Contributing
We welcome contributions! Please see our Contributing Guidelines for details.

Fork the repository
Create a feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request
📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙏 Acknowledgments
LangChain and LangGraph communities for AI agent frameworks
The mentors whose wisdom inspired this project
Open source contributors making AI accessible
📧 Contact & Support
Suresh Maddela