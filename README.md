 TripPlanner_Langgraphs

An intelligent AI-powered travel planning application built with LangGraph, FastAPI, and Streamlit. This application helps users create comprehensive travel plans with real-time data, expense calculations, and detailed itineraries.

 Features

- AI-Powered Travel Planning: Generate detailed travel itineraries using advanced language models
- Real-time Data Integration: Access current weather, place information, and currency conversion
- Comprehensive Cost Analysis: Detailed expense breakdowns and budget planning
- Dual Itinerary Options: Both popular tourist destinations and off-beat locations
- Interactive Web Interface: User-friendly Streamlit frontend with chat-like interaction
- RESTful API: FastAPI backend for scalable and efficient processing
- Multi-Tool Integration: Weather, place search, calculator, and currency conversion tools

## 🛠️ Technology Stack

- Backend: FastAPI, LangGraph, LangChain
- Frontend: Streamlit
- AI Models: Groq, OpenAI (configurable)
- Tools: Weather API, Place Search, Currency Conversion, Calculator
- Architecture: Agentic Workflows with State Management

## 📋 Prerequisites

- Python 3.8+
- API keys for:
  - Groq (or OpenAI)
  - Google Places API
  - Weather API
  - Currency conversion API

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd TripPlanner_Langgraphs
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   GROQ_API_KEY=your_groq_api_key
   OPENAI_API_KEY=your_openai_api_key
   GOOGLE_PLACES_API_KEY=your_google_places_api_key
   WEATHER_API_KEY=your_weather_api_key
   CURRENCY_API_KEY=your_currency_api_key
   ```

## 🎯 Usage

### Running the Application

1. **Start the FastAPI backend**
   ```bash
   uvicorn main:app --reload --host 0.0.0.0 --port 8000
   ```

2. **Start the Streamlit frontend**
   ```bash
   streamlit run streamlit.py
   ```

3. **Access the application**
   - Frontend: http://localhost:8501
   - API Documentation: http://localhost:8000/docs

### Using the API

Send a POST request to `/query` endpoint:

```bash
curl -X POST "http://localhost:8000/query" \
     -H "Content-Type: application/json" \
     -d '{"question": "Plan a trip to Goa for 5 days"}'
```

### Example Queries

- "Plan a trip to Goa for 5 days"
- "Create a budget-friendly itinerary for Paris in 3 days"
- "Plan a weekend getaway to the mountains with adventure activities"
- "Organize a family trip to Disney World with cost breakdown"

## 🏗️ Project Structure

```
TripPlanner_Langgraphs/
├── main.py                 # FastAPI application entry point
├── streamlit.py           # Streamlit frontend interface
├── agentic_workflows.py   # LangGraph workflow builder
├── prompt.py              # System prompts and configurations
├── requirements.txt       # Python dependencies
├── setup.py              # Package setup configuration
└── tools/                # Custom tools and utilities
    ├── weather_tool.py           # Weather information tool
    ├── place_search_tool.py      # Place search and details tool
    ├── expense_calculator_tool.py # Cost calculation tool
    ├── currency_converter.py     # Currency conversion tool
    └── arithmetic_tool.py        # Mathematical operations tool
```

## 🔧 Available Tools

### Weather Information Tool
- Provides current weather conditions
- Forecast data for travel planning
- Temperature, humidity, and precipitation information

### Place Search Tool
- Find attractions, restaurants, and hotels
- Get detailed information about locations
- Real-time place data from Google Places API

### Expense Calculator Tool
- Calculate total trip costs
- Break down expenses by category
- Budget planning and analysis

### Currency Converter Tool
- Real-time currency conversion
- Multi-currency support
- Exchange rate calculations

### Arithmetic Tool
- Mathematical operations for cost calculations
- Percentage calculations
- Budget adjustments

## 🤖 AI Workflow

The application uses LangGraph to create an intelligent workflow:

1. **User Input**: Travel query is received
2. **Agent Processing**: AI agent analyzes the request
3. **Tool Selection**: Appropriate tools are selected based on the query
4. **Data Gathering**: Real-time data is collected from various APIs
5. **Response Generation**: Comprehensive travel plan is created
6. **Output**: Formatted response with detailed itinerary and costs

## 📊 Response Format

The AI generates comprehensive travel plans including:

- Day-by-day itinerary with detailed schedules
- Hotel recommendations with approximate costs
- Attraction details and visiting information
- Restaurant suggestions with price ranges
- Activity recommendations for entertainment
- Transportation options and costs
- Detailed cost breakdown by category
- Daily budget estimates
- Weather information for the destination

## 🔒 Security Considerations

- API keys are stored in environment variables
- CORS is configured for cross-origin requests
- Input validation using Pydantic models
- Error handling for API failures

## 🚀 Deployment

### Local Development
```bash
# Backend
uvicorn main:app --reload --host 0.0.0.0 --port 8000

# Frontend
streamlit run streamlit.py
```

### Production Deployment
- Use a production WSGI server like Gunicorn
- Set up proper environment variables
- Configure reverse proxy (nginx)
- Enable HTTPS
- Set up monitoring and logging

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Check the API documentation at `/docs`
- Review the error logs for debugging

## 🔄 Updates and Maintenance

- Regularly update API keys and dependencies
- Monitor API rate limits
- Keep LangChain and LangGraph versions updated
- Test with different travel scenarios

---

Note: This application generates AI-powered travel plans. Always verify information, especially prices, operating hours, and travel requirements before making bookings or travel arrangements. 