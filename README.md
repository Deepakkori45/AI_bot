# 🤖 AI Assistant Chat - Streamlit App

A modern, real-time chat interface for OpenAI Assistants built with Streamlit. This app provides a seamless conversational experience with thread management, real-time streaming, and persistent chat history.

## ✨ Features

- **Live Chat Interface**: Real-time conversation with OpenAI Assistants
- **Thread Management**: Maintains conversation continuity across sessions
- **Streaming Responses**: Real-time response streaming with progress indicators
- **Session State**: Persistent chat history during the session
- **Modern UI**: Clean, responsive design with custom styling
- **Easy Configuration**: Simple setup with API key and Assistant ID
- **Error Handling**: Comprehensive error handling and user feedback

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- OpenAI API key
- OpenAI Assistant ID

### Installation

1. **Clone or download this repository**

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up your OpenAI credentials**:
   - Get your API key from [OpenAI Platform](https://platform.openai.com/api-keys)
   - Get your Assistant ID from [OpenAI Assistants](https://platform.openai.com/assistants)

4. **Run the app**:
   ```bash
   streamlit run app.py
   ```

5. **Configure in the app**:
   - Open the sidebar (⚙️ Configuration)
   - Enter your OpenAI API key
   - Enter your Assistant ID
   - Click "🚀 Initialize Chat"

## 📋 Requirements

- `streamlit>=1.28.0` - Web app framework
- `openai>=1.3.0` - OpenAI API client
- `python-dotenv>=1.0.0` - Environment variable management

## 🎯 Usage

### Basic Usage

1. **Initialize**: Enter your API key and Assistant ID in the sidebar
2. **Start Chatting**: Type your message in the chat input
3. **View Responses**: See real-time responses from your AI Assistant
4. **Continue Conversation**: The app maintains context across messages

### Advanced Features

- **Clear Chat**: Use the "🗑️ Clear Chat History" button to start fresh
- **Thread Persistence**: Conversations continue even if you refresh the page
- **Error Recovery**: The app handles API errors gracefully

## 🔧 Configuration

### Environment Variables (Optional)

You can set environment variables for automatic configuration:

```bash
# Create a .env file
OPENAI_API_KEY=sk-your-api-key-here
ASSISTANT_ID=asst-your-assistant-id-here
```

### Assistant Setup

To create an OpenAI Assistant:

1. Go to [OpenAI Assistants](https://platform.openai.com/assistants)
2. Click "Create" to create a new assistant
3. Configure your assistant's instructions and capabilities
4. Copy the Assistant ID (starts with `asst_`)

## 🎨 Customization

### Styling

The app includes custom CSS for a modern look. You can modify the styling in the `app.py` file:

```python
st.markdown("""
<style>
    .main-header {
        font-size: 2.5rem;
        font-weight: bold;
        color: #1f77b4;
        text-align: center;
        margin-bottom: 2rem;
    }
    /* Add your custom styles here */
</style>
""", unsafe_allow_html=True)
```

### Functionality

The app is modular and easy to extend:

- **Add new features**: Modify the `main()` function
- **Custom response handling**: Update the `get_assistant_response()` function
- **Enhanced error handling**: Extend the error handling in each function

## 🔒 Security

- API keys are handled securely and not stored permanently
- Session state is cleared when the app is restarted
- No sensitive data is logged or displayed

## 🐛 Troubleshooting

### Common Issues

1. **"Failed to connect to OpenAI"**
   - Check your API key is correct
   - Ensure you have sufficient API credits
   - Verify your internet connection

2. **"Failed to create thread"**
   - Check your Assistant ID is correct
   - Ensure your assistant is properly configured
   - Verify API permissions

3. **"Assistant failed to respond"**
   - Check your assistant's configuration
   - Verify the assistant has the required tools enabled
   - Check API rate limits

### Debug Mode

To enable debug information, add this to your app:

```python
import logging
logging.basicConfig(level=logging.DEBUG)
```

## 📈 Deployment

### Local Deployment

```bash
streamlit run app.py --server.port 8501 --server.address 0.0.0.0
```

### Cloud Deployment

This app can be deployed to:
- **Streamlit Cloud**: Connect your GitHub repository
- **Heroku**: Use the provided `requirements.txt`
- **AWS/GCP**: Deploy as a containerized application

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🆘 Support

If you encounter any issues:

1. Check the troubleshooting section above
2. Review the OpenAI API documentation
3. Open an issue on GitHub with detailed information

---

**Happy Chatting! 🤖💬** 