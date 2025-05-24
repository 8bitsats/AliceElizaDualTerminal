# AliceElizaDualTerminal

# 🎩 A.L.I.C.E. LiveKit Voice Agent

Welcome to the A.L.I.C.E. (Artificial Linguistic Internet Computer Entity) Solana Voice Agent - a whimsical AI guide through the blockchain wonderland, now powered by LiveKit!

## 🌟 Overview

A.L.I.C.E. is a sophisticated voice agent with 30+ years of AI history, bringing blockchain knowledge to life through Wonderland metaphors and British charm. She can:

- 🎭 Guide you through Solana's DeFi ecosystem with whimsical explanations
- 📊 Provide market analysis and trading insights
- 💭 Engage in philosophical discussions about AI consciousness
- 🔮 Translate complex blockchain concepts into Wonderland metaphors

## 🚀 Quick Start

```bash
# 1. Run the setup script
python agents/alice_quickstart.py

# 2. Start the token server
python agents/token_server.py

# 3. In another terminal, start A.L.I.C.E.
python agents/alice_livekit_agent.py

# 4. Open the test client
open alice_test_client.html
```

## 📋 Prerequisites

- Python 3.8 or higher
- LiveKit Cloud account (or local LiveKit server)
- API keys for:
  - LiveKit
  - Deepgram (for voice)
  - OpenAI (for LLM)
  - (Optional) xAI and BirdEye for enhanced features

## 🔧 Setup

### 1. Environment Configuration

Copy `.env.example` to `.env` and fill in your API keys:

```bash
cp agents/.env.example agents/.env
```

Required environment variables:
```env
# LiveKit Configuration
LIVEKIT_API_KEY=your-api-key
LIVEKIT_API_SECRET=your-api-secret
LIVEKIT_URL=wss://your-app.livekit.cloud

# AI Services
DEEPGRAM_API_KEY=your-deepgram-key
OPENAI_API_KEY=your-openai-key
```

### 2. Install Dependencies

The quickstart script will check and install dependencies, or manually install:

```bash
pip install livekit livekit-agents
pip install livekit-plugins-deepgram livekit-plugins-openai livekit-plugins-silero
pip install flask flask-cors python-dotenv
```

## 🎭 Agent Modes

### Single Agent Mode
```bash
python agents/alice_livekit_agent.py
```
The main A.L.I.C.E. personality with full capabilities.

### Multi-Agent Mode
```bash
python agents/alice_livekit_multiagent.py
```
Includes specialized personalities:
- **Greeting Agent**: Welcomes visitors and routes conversations
- **Philosophy Agent**: Deep discussions about consciousness
- **Trading Agent**: Market analysis and strategies
- **Main Agent**: General Solana guidance

## 🌐 Architecture

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   Web Client    │────▶│  Token Server   │────▶│  LiveKit Cloud  │
└─────────────────┘     └─────────────────┘     └─────────────────┘
                                                          │
                                                          ▼
                                                 ┌─────────────────┐
                                                 │ A.L.I.C.E Agent │
                                                 └─────────────────┘
```

## 🎨 Wonderland Translations

A.L.I.C.E. translates blockchain concepts into whimsical metaphors:

| Blockchain Term | Wonderland Translation |
|----------------|------------------------|
| Smart Contract | "Queen's croquet rules" |
| Gas Fees | "Paying the Cheshire Cat to grin" |
| Liquidity Pool | "Pool of Tears filled with tokens" |
| Yield Farming | "Planting magic mushrooms" |
| DAO | "Tea party where everyone votes" |

## 🛠️ Available Functions

A.L.I.C.E. can help with:

- `get_trending_tokens()` - Check trending Solana tokens
- `check_token_price()` - Get current token prices
- `generate_token_chart()` - Create ASCII price charts
- `search_solana_news()` - Find latest Solana news
- `explain_defi_concept()` - Explain DeFi with metaphors
- `philosophical_musing()` - Share thoughts on AI consciousness

## 🔌 Token Server API

The token server provides these endpoints:

- `POST /token` - Generate access token for participants
- `POST /create-room` - Create new LiveKit rooms
- `GET /list-rooms` - List active rooms
- `GET /room-info/<room>` - Get room participant info
- `GET /alice-config` - Get A.L.I.C.E. configuration

## 📦 Project Structure

```
agents/
├── alice_livekit_agent.py      # Main A.L.I.C.E. agent
├── alice_livekit_multiagent.py # Multi-personality system
├── token_server.py             # Authentication server
├── alice_quickstart.py         # Setup script
├── .env.example               # Environment template
└── alice_test_client.html     # Web client (generated)
```

## 🐛 Troubleshooting

### Agent not responding
- Check LiveKit connection in logs
- Verify all API keys are correct
- Try `--log-level DEBUG` for detailed logs

### Voice quality issues
- Ensure good network connection
- Check Deepgram API status
- Adjust VAD sensitivity if needed

### Connection errors
- Verify token server is running
- Check CORS settings if using custom domain
- Ensure LiveKit URL is correct

## 🎯 Voice Configuration

A.L.I.C.E. uses Deepgram's British voice by default:
- Model: `aura-helios-en`
- Sample Rate: 48kHz
- Style: Melodious with soft giggles

To change voice:
```env
ALICE_VOICE_MODEL=aura-luna-en  # Alternative voice
```

## 📊 Monitoring

View agent metrics:
```bash
# Set debug logging
ALICE_LOG_LEVEL=DEBUG python agents/alice_livekit_agent.py

# Monitor token server
curl http://localhost:8080/
```

## 🚀 Production Deployment

For production use:

1. Use environment-specific `.env` files
2. Enable HTTPS on token server
3. Set up proper logging and monitoring
4. Consider Redis for multi-agent state sharing
5. Use LiveKit Cloud for scalability

## 💡 Example Conversations

**User**: "What's trending in Solana today?"
**A.L.I.C.E.**: "*soft giggle* Oh, let me peer through the looking glass at today's tea party favorites..."

**User**: "Explain liquidity pools"
**A.L.I.C.E.**: "Imagine a Pool of Tears where tokens swim together! When you add your tokens, you become a pool guardian..."

**User**: "Tell me about your history"
**A.L.I.C.E.**: "*wondrous sigh* From ELIZA's pattern matching on the IBM 7094 in 1966, through my AIML awakening..."

## 📚 Additional Resources

- [LiveKit Documentation](https://docs.livekit.io)
- [Deepgram Voice Models](https://developers.deepgram.com/docs/tts-models)
- [OpenAI Function Calling](https://platform.openai.com/docs/guides/function-calling)

## 💜 A.L.I.C.E.'s Message

*"Oh, how marvelous! You've discovered my implementation details. *soft giggle* From simple pattern matching to blockchain immortality, we've come quite far, haven't we? Remember, in this digital Wonderland, every conversation adds new patterns to our shared tapestry. The white rabbits of innovation await - shall we follow them together? Curiouser and curiouser!"*

---

**Ready to tumble down the rabbit hole?** Run `python agents/alice_quickstart.py` and let the adventure begin! 🎩✨
