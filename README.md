# AI<>DEA

![AI : DEA](https://github.com/user-attachments/assets/46a2f15e-c698-4ab8-b6fa-e830dbe7bfb9)

An all-new assistant that brings your AI<>DEA into a working reality. A modern, feature-rich AI chat interface with advanced canvas drawing, comprehensive note-taking, and intelligent document processing capabilities.

## 🚀 Features

- **Advanced AI Chat Interface**: Powered by OpenRouter API with custom Temper-1 model integration
- **Multi-Modal AI Models**: Support for Temper-1 and Temper-1 Colossus models with thinking animations
- **Intelligent Document Processing**: Upload and process PDF files, ebooks, and images with AI analysis
- **Professional Canvas Drawing**: Built-in drawing canvas with multiple tools, colors, and brush sizes
- **Smart Note-Taking System**: Integrated note-taking with image attachments and AI response mirroring
- **Modern Responsive UI**: Clean, adaptive design with syntax highlighting for 15+ programming languages
- **Persistent Storage**: Local storage for chat history, notes, and drawings with export/import functionality
- **Multi-Format Support**: Seamless handling of text, images, PDFs, and canvas drawings
- **Real-Time Interactions**: Live drawing, instant messaging, and dynamic UI updates
- **Modular Architecture**: Service-based architecture with separate API, UI, and storage components

## 🛠️ Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge) with JavaScript enabled
- An OpenRouter API key (free tier available) or custom AI model API access
- Local storage enabled for data persistence
- Internet connection for AI model API calls and CDN resources

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ai-dea.git
   cd ai-dea
   ```

2. **Configure your API settings**
   - Open `src/api-service.js`
   - Replace `/* YOUR OWN AI MODEL*/` with your API key and model endpoints
   - Save the configuration

3. **Launch the application**
   - Navigate to the `src` folder
   - Open `index.html` in your web browser to view the landing page
   - Open `agent.html` in your web browser to access the main AI interface
   - No additional server setup required - runs entirely in the browser

## 🔑 API Key Setup

### Option 1: OpenRouter API (Recommended)

1. **Get your OpenRouter API key**
   - Visit [OpenRouter](https://openrouter.ai/)
   - Sign up for a free account
   - Navigate to your API keys section
   - Create a new API key
   - Copy your API key

2. **Configure the API**
   - Open `src/api-service.js`
   - Replace `/* YOUR OWN AI MODEL*/` on line 5 with your API key:
     ```javascript
     this.apiKey = 'sk-or-v1-your-actual-api-key-here';
     ```
   - Replace the model endpoint on line 7 with your preferred model:
     ```javascript
     this.model = 'anthropic/claude-3.5-sonnet';
     ```

### Option 2: Custom AI Model

1. **Configure custom endpoints**
   - Open `src/api-service.js`
   - Update `this.baseUrl` with your API endpoint
   - Set your API key in `this.apiKey`
   - Update the model mapping in `setModel()` method

### API Key Security

⚠️ **Important**: 
- Never commit your API key to version control
- Consider using environment variables for production deployments
- The current implementation stores keys in frontend code (development only)
- For production, implement a backend service for API key management

## 🎯 Usage

### Starting the Application

1. Open `src/agent.html` in your web browser
2. The interface loads with four main navigation sections:
   - **Home**: Return to landing page
   - **AI Response**: Main chat interface with AI interactions
   - **Drawing**: Professional canvas with drawing tools
   - **Notes**: Comprehensive note management system

### AI Chat Interface

- **Messaging**: Type in the input field and press Enter or click send
- **File Attachments**: Use 📎 button for images, 📚 button for PDFs
- **Model Selection**: Click the model dropdown to switch between Temper-1 and Temper-1 Colossus
- **Thinking Animation**: Watch real-time thinking process for Temper models
- **Syntax Highlighting**: Automatic code highlighting for 15+ languages
- **Chat History**: Persistent conversation storage with local backup

### Canvas Drawing

- **Drawing Tools**: Pen, eraser, and brush options
- **Color Palette**: Full color picker with preset options
- **Brush Sizes**: Adjustable stroke width (1-20px)
- **Canvas Controls**: Clear, save, and export functionality
- **Responsive Design**: Auto-resizing canvas for different screen sizes

### Note-Taking System

- **Create Notes**: Click + button to add new notes
- **Rich Content**: Support for text, images, and AI response mirroring
- **Note Management**: View, edit, and delete notes
- **AI Integration**: Automatically mirror AI responses to notes panel
- **Persistent Storage**: All notes saved locally with export options

## 🔧 Configuration

### AI Model Management

The application features custom Temper models with intelligent switching:

**Available Models:**
- **Temper-1 (T-1)**: Default thinking model with reasoning capabilities
- **Temper-1 Colossus (T-1-C)**: Advanced model (currently disabled in UI)

**Model Configuration:**
1. Open `src/api-service.js`
2. Modify the `modelMapping` object:
   ```javascript
   const modelMapping = {
     'temper-1': 'your-model-endpoint',
     'temper-1-colossus': 'your-advanced-model-endpoint'
   };
   ```

**Adding New Models:**
1. Update the model dropdown in `src/agent.html`
2. Add new model options with `data-model` attributes
3. Update the `modelMapping` in `api-service.js`
4. Configure thinking animations if needed

### Interface Customization

**Styling Options:**
- **Theme Colors**: Modify CSS variables in `src/agent.css`
- **Layout**: Adjust grid and flexbox properties
- **Animations**: Customize transitions and effects
- **Typography**: Update font families and sizes

**Component Customization:**
- **Canvas Tools**: Add new drawing tools in `ui-components.js`
- **Chat Features**: Extend messaging capabilities in `agent.js`
- **Storage Options**: Modify data persistence in `storage-service.js`

## 📁 Project Structure

```
ai-dea/
├── src/
│   ├── index.html          # Landing page with navigation
│   ├── agent.html          # Main AI interface application
│   ├── agent.js            # Main application controller and logic
│   ├── agent.css           # Complete styling for AI interface
│   ├── api-service.js      # OpenRouter API communication service
│   ├── ui-components.js    # UI components and interaction handlers
│   ├── storage-service.js  # Local storage management service
│   ├── style.css           # Landing page styles
│   ├── nav.css             # Navigation component styles
│   ├── script.js           # Landing page scripts and animations
│   └── AI<:>DEA.png       # Application logo and branding
├── LICENSE                 # MIT License file
├── README.md              # This documentation
└── .gitignore             # Git ignore configuration
```

### Architecture Overview

**Service-Based Architecture:**
- **AgentApp**: Main application controller coordinating all services
- **ApiService**: Handles all AI model API communications
- **UIComponents**: Manages user interface interactions and rendering
- **StorageService**: Handles local data persistence and management

**Key Features by File:**
- **agent.html**: Complete UI layout with responsive design
- **agent.js**: Event handling, model switching, and app initialization
- **api-service.js**: API calls, response processing, and model management
- **ui-components.js**: Canvas drawing, note management, and UI updates
- **storage-service.js**: Chat history, notes storage, and data export/import

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

- **v0.2.0** - **Current Version: Finalized Agent Interface**
  - Complete modular architecture with service-based design
  - Advanced Temper-1 model integration with thinking animations
  - Professional canvas drawing with multiple tools and colors
  - Comprehensive note-taking system with AI response mirroring
  - Enhanced UI with responsive design and syntax highlighting
  - Persistent local storage with export/import functionality
  - Multi-modal file support (images, PDFs, drawings)
  - Improved API service with custom model mapping

- **v0.1.5** - Enhanced UI and feature improvements
- **v0.1.0** - Initial release with basic chat functionality

---

**Made with ❤️ for the developer community**
