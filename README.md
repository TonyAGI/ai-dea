# AI<>DEA

An all-new assistant that brings your AI<>DEA into a working reality. A modern, feature-rich AI chat interface with canvas drawing, note-taking, and document processing capabilities.

## 🚀 Features

- **AI Chat Interface**: Powered by OpenRouter API with support for multiple AI models
- **Document Processing**: Upload and process PDF files, ebooks, and images
- **Canvas Drawing**: Built-in drawing canvas for visual collaboration
- **Note Taking**: Integrated note-taking system with image attachments
- **Modern UI**: Clean, responsive design with syntax highlighting for code
- **Chat History**: Persistent chat history with local storage
- **Multi-format Support**: Handle text, images, and documents seamlessly

## 🛠️ Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- An OpenRouter API key (free tier available)

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ai-dea.git
   cd ai-dea
   ```

2. **Open the project**
   - Navigate to the `src` folder
   - Open `index.html` in your web browser to view the landing page
   - Open `agent.html` in your web browser to access the main AI interface

## 🔑 API Key Setup

### Getting Your OpenRouter API Key

1. Visit [OpenRouter](https://openrouter.ai/)
2. Sign up for a free account
3. Navigate to your API keys section
4. Create a new API key
5. Copy your API key

### Configuring the API Key

1. Open `src/agent.html` in a text editor
2. Find the API key configuration (around line 1000):
   ```javascript
   "Authorization": "/* YOUR API KEY HERE */",
   ```
3. Replace `/* YOUR API KEY HERE */` with your actual API key:
   ```javascript
   "Authorization": "Bearer sk-or-v1-your-actual-api-key-here",
   ```
4. Save the file

### API Key Security

⚠️ **Important**: Never commit your API key to version control. Consider using environment variables or a separate configuration file for production deployments.

## 🎯 Usage

### Starting the Application

1. Open `src/agent.html` in your web browser
2. The interface will load with three main sections:
   - **AI Response**: View AI-generated responses with syntax highlighting
   - **Canvas**: Draw and sketch ideas
   - **Notes**: Create and manage notes with image attachments

### Chat Interface

- Type your message in the input field
- Press Enter or click the send button
- Attach images using the 📎 button
- Upload documents using the 📚 button
- View chat history in the left panel

### Canvas Drawing

- Switch to the Canvas tab
- Use your mouse to draw
- Perfect for brainstorming and visual collaboration

### Note Taking

- Switch to the Notes tab
- Click the + button to create new notes
- Attach images to your notes
- View and manage all your notes

## 🔧 Configuration

### Changing AI Models

The application uses DeepSeek R1 by default. To change the model, modify the `model` parameter in the API request:

```javascript
"model": "deepseek/deepseek-r1-0528:free",
```

Available models on OpenRouter include:
- `deepseek/deepseek-r1-0528:free` (default)
- `anthropic/claude-3.5-sonnet`
- `openai/gpt-4o`
- `meta-llama/llama-3.1-8b-instruct`

### Customizing the Interface

You can customize the appearance by modifying the CSS in `src/agent.html`:
- Colors and themes
- Font sizes and styles
- Layout and spacing
- Animation effects

## 📁 Project Structure

```
ai-dea/
├── src/
│   ├── index.html          # Landing page
│   ├── agent.html          # Main AI interface
│   ├── style.css           # Landing page styles
│   └── script.js           # Landing page scripts
├── README.md               # This file
└── .gitignore             # Git ignore file
```

## 🛡️ Security Considerations

- API keys are stored in the frontend code (not recommended for production)
- Consider implementing a backend service for API key management
- Use HTTPS in production environments
- Regularly rotate your API keys

## 🤝 Contributing

We welcome contributions! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Setup

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [OpenRouter](https://openrouter.ai/) for providing AI model access
- [PDF.js](https://mozilla.github.io/pdf.js/) for PDF processing
- [Highlight.js](https://highlightjs.org/) for syntax highlighting
- [GSAP](https://greensock.com/gsap/) for animations

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/ai-dea/issues) page
2. Create a new issue with detailed information
3. Include your browser version and any error messages

## 🔄 Version History

- **v0.1.5** - Current version with improved UI and features
- **v0.1.0** - Initial release

---

**Made with ❤️ for the developer community**
