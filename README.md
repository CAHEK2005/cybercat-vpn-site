# CyberCat VPN Support Chatbot Documentation

## Overview
This chatbot integrates with OpenRouter AI to provide technical support for CyberCat VPN configurations. It uses the `deepseek/deepseek-r1-distill-llama-70b:free` model for responses.

## Features
- Real-time chat interface
- Context-aware conversations
- Error handling and retries
- Modern UI with green color scheme
- Typing indicators and loading states

## Installation
1. Ensure you have Node.js installed
2. Clone the repository
3. Install dependencies: `npm install`
4. Start the development server: `npm run dev`

## Configuration
The CyberCat VPN chatbot is pre-configured with:
- OpenRouter API key
- Model selection
- Default styling

To customize:
1. Edit `src/components/ChatBot.astro`
2. Modify the styles in the `<style>` section
3. Update the API key if needed

## Usage Examples
```javascript
// Sample API call structure
const response = await fetch('https://openrouter.ai/api/v1/chat/completions', {
  method: 'POST',
  headers: {
    'Authorization': `Bearer YOUR_API_KEY`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    model: "deepseek/deepseek-r1-distill-llama-70b:free",
    messages: [{ role: "user", content: "Your question here" }]
  })
});
```

## Troubleshooting
- Check network connections if responses fail
- Verify API key is valid
- Ensure the model is available on OpenRouter
