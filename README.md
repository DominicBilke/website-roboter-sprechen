# 🤖 Talking Robot Assistant

A modern, interactive AI-powered robot assistant website with voice recognition, multi-language support, and a futuristic robotic design.

## 🌟 Features

### 🎤 Voice Interaction
- **Speech Recognition**: Built-in voice-to-text functionality
- **AI Responses**: Powered by OpenAI GPT-3.5 for intelligent conversations
- **Text-to-Speech**: Automatic voice synthesis of responses
- **Multi-language Support**: English and German voice recognition

### 🌍 Language Support
- **Automatic Detection**: Language automatically set based on domain
  - `roboter-sprechen.de` → German
  - `talk-robot.info` → English
  - `robotic-assistant.com` → English
- **Manual Switching**: Users can manually toggle between languages
- **Localized Content**: All UI elements, legal information, and responses in both languages

### 🎨 Modern Design
- **Futuristic Theme**: Robotic-inspired design with glowing effects
- **Responsive Layout**: Optimized for desktop, tablet, and mobile devices
- **Glass Morphism**: Modern translucent UI elements with backdrop blur
- **Animated Elements**: Smooth transitions, hover effects, and micro-interactions
- **Dynamic Robot Images**: Rotating robot pictures that change every 5 seconds

### 🔒 Privacy & Legal
- **Privacy Policy**: Comprehensive data protection information
- **Imprint**: Company and legal information
- **Modal Popups**: Clean, accessible legal information display
- **External Links**: Direct links to official legal pages

## 🚀 Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **AI Integration**: OpenAI GPT-3.5 API
- **Voice Recognition**: Web Speech API
- **Speech Synthesis**: Web Speech Synthesis API
- **Design**: Custom CSS with modern features (Grid, Flexbox, Animations)
- **Fonts**: Google Fonts (Orbitron, Roboto)

## 📁 Project Structure

```
talking-robot-assistant/
├── index.html          # Main website file
├── images/             # Robot images and assets
│   ├── pic01.jpg      # Robot image 1
│   ├── pic02.jpg      # Robot image 2
│   ├── ...            # Additional robot images
│   └── robotic_header.png  # Header image
├── README.md           # This file
└── .gitignore          # Git ignore file (if using version control)
```

## 🛠️ Installation & Setup

### Prerequisites
- Modern web browser with Web Speech API support
- OpenAI API key for AI responses

### Quick Start
1. **Clone or download** the project files
2. **Add your OpenAI API key** in the `askQuestionVoice` function
3. **Upload to your web server** or open locally in a browser
4. **Configure domains** for automatic language detection

### OpenAI API Setup
1. Get your API key from [OpenAI Platform](https://platform.openai.com/)
2. Replace the placeholder in the JavaScript code:
```javascript
'Authorization': 'Bearer YOUR_API_KEY_HERE'
```

## 🌐 Domain Configuration

The website automatically detects the language based on the hostname:

| Domain | Language | Description |
|--------|----------|-------------|
| `roboter-sprechen.de` | German | German version of the site |
| `talk-robot.info` | English | English version of the site |
| `robotic-assistant.com` | English | English version of the site |
| Other domains | English | Defaults to English |

## 🎯 Key Features Explained

### Voice Recognition System
```javascript
// Speech recognition setup
if ('webkitSpeechRecognition' in window) {
    recognition = new webkitSpeechRecognition();
    recognition.lang = currentLanguage === 'en' ? 'en-US' : 'de-DE';
}
```

### Robot Image Rotation
```javascript
// Change robot image every 5 seconds
setInterval(changeRobotImage, 5000);
```

### Language Detection
```javascript
function detectLanguageFromUrl() {
    const hostname = window.location.hostname;
    if (hostname === 'roboter-sprechen.de') return 'de';
    if (hostname === 'talk-robot.info' || hostname === 'robotic-assistant.com') return 'en';
    return 'en'; // Default
}
```

## 🎨 Customization

### Colors
Modify the CSS custom properties in `:root`:
```css
:root {
    --primary: #00d4ff;      /* Main accent color */
    --secondary: #ff6b9d;    /* Secondary accent */
    --accent: #7c3aed;       /* Additional accent */
    --bg-dark: #0a0a0f;      /* Background color */
}
```

### Robot Images
Add or replace images in the `images/` folder and update the array:
```javascript
const robotImages = [
    'images/your-image1.jpg',
    'images/your-image2.jpg',
    // ... add more images
];
```

### Legal Information
Update company details in the `legalContent` object:
```javascript
const legalContent = {
    imprint: {
        title: 'Imprint',
        content: `Your company information here...`
    }
    // ... other legal content
};
```

## 📱 Browser Compatibility

- **Chrome**: Full support (recommended)
- **Firefox**: Full support
- **Safari**: Full support
- **Edge**: Full support
- **Mobile Browsers**: Responsive design with touch optimization

## 🔧 Troubleshooting

### Voice Recognition Not Working
- Ensure HTTPS is enabled (required for Web Speech API)
- Check browser permissions for microphone access
- Verify Web Speech API support in your browser

### AI Responses Not Working
- Verify OpenAI API key is correct
- Check API quota and billing status
- Ensure proper CORS configuration

### Design Issues
- Clear browser cache
- Verify CSS is loading properly
- Check for JavaScript errors in console

## 📄 License

This project is proprietary software developed by Bilke Web- und Softwareentwicklung.

## 👨‍💻 Developer Information

**Company**: Bilke Web- und Softwareentwicklung  
**Address**: Hanauer Landstrasse 291 B, 60314 Frankfurt am Main  
**Phone**: +49 174 849 3008  
**Email**: info@dominic-bilke.de  
**Website**: [www.dominic-bilke.de](https://www.dominic-bilke.de)

## 🤝 Contributing

This is a proprietary project. For questions or support, please contact the development team directly.

## 📞 Support

For technical support or questions about this project:
- **Email**: info@dominic-bilke.de
- **Phone**: +49 174 849 3008
- **Website**: [www.dominic-bilke.de](https://www.dominic-bilke.de)

---

**Last Updated**: December 2024  
**Version**: 2.0  
**Status**: Production Ready 