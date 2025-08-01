## 🌍AI Travel Agent – Multi-Tool Travel Planner with LangChain, Gradio & LLMs

Welcome to AI Travel Agent, your intelligent and interactive travel planning assistant built with LangChain, OpenAI, Gradio, and external APIs like RapidAPI and Tavily. This system can plan trips, recommend destinations, suggest what to pack, search real-time travel info, and even book hotels via API — all in natural language.

✈️ Features
🏙️ Destination Recommendations

🏨 Hotel Booking via RapidAPI

🔍 Real-time travel info (weather, attractions, food, etc.) using Tavily

🧠 Fallback strategy using different LLMs (GPT-4 and GPT-4.1-nano)

📊 LangSmith Integration for Observability

💬 Gradio-powered Chat Interface

📁 Project Structure
bash
Copy
Edit
.
├── app.py                    # Main application file (for Gradio + Hugging Face)
├── requirements.txt          # All dependencies for deployment
├── .env                      # Environment variables (Not to be shared publicly)
├── README.md                 # You're reading it!
🚀 Setup Instructions
1. Clone the Repo
bash
Copy
Edit
git clone https://github.com/YOUR_USERNAME/ai-travel-agent
cd ai-travel-agent
2. Create a .env File
Create a .env file in the root directory and add:

env
Copy
Edit
OPENAI_API_KEY=your-openai-api-key
TAVILY_API_KEY=your-tavily-api-key
RAPIDAPI_KEY=your-rapidapi-key
LANGSMITH_API_KEY=your-langsmith-key
3. Install Requirements
bash
Copy
Edit
pip install -r requirements.txt
🧠 How It Works
🧰 Tools Used
Tool Name	Description
DestinationRecommender	Suggests popular cities in a given country
HotelBooking	Books hotels using RapidAPI's Booking API
TavilySearch	Gets real-time local info (weather, attractions, etc.)

🧪 LLM Strategy
Model	Purpose
GPT-4.1-nano	Fast responses for short queries
GPT-4	Powerful model for long/complex tasks
LangSmith	For tracing and debugging

💡 Example Query
“Plan a trip to Japan in December. Suggest places, what to pack and key info. Give me a detail of dishes according to the famous places in Japan. Book a hotel for me in Tokyo. I would like to spend my New Year.”

🖼️ Gradio UI
Launch the local app:

bash
Copy
Edit
python app.py
You’ll get a Gradio web interface like this:


📦 Hugging Face Deployment
1. Upload Files
app.py → Rename from app_hf.py if needed

requirements.txt → Rename from requirements_hf.txt

README.md

You can upload via:

Hugging Face CLI: git add . && git commit && git push

Or manually under the “Files and versions” tab of your Hugging Face Space.

2. Set Secrets
Add your keys in Settings > Repository Secrets:

Name	Value
OPENAI_API_KEY	your OpenAI key
TAVILY_API_KEY	your Tavily key
RAPIDAPI_KEY	your RapidAPI key
LANGSMITH_API_KEY	your LangSmith key

📊 LangSmith Dashboard
Once you run the app, visit:
👉 https://smith.langchain.com
You'll find traces under the “MyTravelAgent” project.

🛡️ .gitignore
Important: Add .env to your .gitignore file to protect your API keys.

gitignore
Copy
Edit
.env
__pycache__/
*.pyc
*.ipynb_checkpoints
🧠 Future Improvements
Add flight booking integration

Expand country and city database

Use LangGraph instead of basic LangChain agents

Enable multi-lingual support

👩‍💻 Author
Dania Amin Khan


📄 License
MIT License — Free to use with attribution.
