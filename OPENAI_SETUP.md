# OpenAI Integration Setup

## Overview
The Gen AI bots in this app are now powered by OpenAI's GPT API. To enable AI responses, you need to configure your OpenAI API key.

## Setup Instructions

### 1. Get OpenAI API Key
1. Go to [OpenAI Platform](https://platform.openai.com/)
2. Sign up or log in to your account
3. Navigate to API Keys section
4. Create a new API key
5. Copy the API key (it starts with `sk-`)

### 2. Configure API Key
1. Open `lib/config/api_config.dart`
2. Replace `YOUR_OPENAI_API_KEY_HERE` with your actual API key:
   ```dart
   static const String openaiApiKey = 'sk-your-actual-api-key-here';
   ```

### 3. Security Note
⚠️ **Important**: Never commit your actual API key to version control. Consider using environment variables or secure storage for production apps.

## Features
- **Smart Conversations**: Each bot uses GPT-3.5-turbo for intelligent responses
- **Context Awareness**: Maintains conversation history for better responses
- **Bot Personalities**: Each bot introduces itself with its specific name
- **Error Handling**: Graceful fallbacks when API is unavailable
- **Loading States**: Visual feedback while AI is thinking

## Usage
1. Navigate to Gen AI page
2. Tap on any bot
3. Tap "Chat with Bot"
4. Start chatting with your AI-powered bot!

## Troubleshooting
- If you see "OpenAI API key not configured" message, check step 2 above
- If responses are slow, this is normal for API calls
- If you get errors, check your API key and internet connection

## API Costs
- OpenAI charges per token used
- GPT-3.5-turbo is cost-effective for most use cases
- Monitor your usage on the OpenAI dashboard
