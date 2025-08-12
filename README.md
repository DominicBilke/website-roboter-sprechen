# 🤖 Talking Robot Assistant

A modern, interactive AI-powered robot assistant website with voice recognition, multi-language support, and a futuristic robotic design.

## 🌟 Features

### 🎤 Voice Interaction
- **Speech Recognition**: Built-in voice-to-text functionality using Web Speech API
- **AI Responses**: Powered by OpenAI GPT-3.5 for intelligent conversations
- **Text-to-Speech**: Automatic voice synthesis of responses
- **Multi-language Support**: English and German voice recognition with proper language detection

### 🌍 Complete Language Support
- **Automatic Detection**: Language automatically set based on domain
  - `roboter-sprechen.de` → German
  - `talk-robot.info` → English
  - `robotic-assistant.com` → English
- **Manual Switching**: Users can manually toggle between languages
- **Complete Localization**: All UI elements, descriptions, features, and legal information in both languages
- **Professional Translations**: Natural, fluent language appropriate for each market

### 🎨 Modern Robotic Design
- **Futuristic Theme**: Robotic-inspired design with glowing effects and animations
- **Glass Morphism**: Modern translucent UI elements with backdrop blur effects
- **Responsive Layout**: Optimized for desktop, tablet, and mobile devices
- **Animated Elements**: Smooth transitions, hover effects, and micro-interactions
- **Dynamic Robot Images**: Rotating robot pictures that change every 5 seconds with smooth transitions
- **Custom Robotic Microphone**: Futuristic microphone icon with multi-layered design and glow effects

### 🔒 Privacy & Legal
- **Privacy Policy**: Comprehensive data protection information in both languages
- **Imprint**: Company and legal information with external links
- **Modal Popups**: Clean, accessible legal information display
- **External Links**: Direct links to official legal pages

### 🚀 Advanced Features
- **Real-time Language Switching**: Instant updates across all UI elements
- **Voice Language Detection**: Automatic language setting for speech recognition
- **Responsive Design**: Mobile-first approach with touch optimization
- **Performance Optimized**: Efficient animations and smooth scrolling

## 🚀 Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **AI Integration**: OpenAI GPT-3.5 API
- **Voice Recognition**: Web Speech API (SpeechRecognition)
- **Speech Synthesis**: Web Speech Synthesis API
- **Design**: Custom CSS with modern features (Grid, Flexbox, Animations, Backdrop-filter)
- **Fonts**: Google Fonts (Orbitron for headings, Roboto for body text)
- **Icons**: Custom SVG with glow effects and animations

## 📁 Project Structure

```
talking-robot-assistant/
├── index.html          # Main website file with complete functionality
├── images/             # Robot images and assets
│   ├── pic01.jpg      # Robot image 1
│   ├── pic02.jpg      # Robot image 2
│   ├── ...            # Additional robot images (26 total)
│   └── robotic_header.png  # Header image
├── README.md           # This comprehensive documentation
└── .gitignore          # Git ignore file (if using version control)
```

## 🛠️ Installation & Setup

### Prerequisites
- Modern web browser with Web Speech API support
- OpenAI API key for AI responses
- Web server with HTTPS support (required for voice features)

### Quick Start
1. **Clone or download** the project files
2. **Add your OpenAI API key** in the `askQuestionVoice` function
3. **Upload to your web server** with HTTPS enabled
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
// Speech recognition setup with language detection
if ('webkitSpeechRecognition' in window) {
    recognition = new webkitSpeechRecognition();
    recognition.lang = currentLanguage === 'en' ? 'en-US' : 'de-DE';
}
```

### Robot Image Rotation
```javascript
// Change robot image every 5 seconds with smooth transitions
setInterval(changeRobotImage, 5000);
```

### Complete Language System
```javascript
// Comprehensive translation object with all UI elements
const translations = {
    en: { /* Complete English translations */ },
    de: { /* Complete German translations */ }
};

// Apply all translations instantly
function applyTranslations(lang) {
    // Updates all UI elements with new language
}
```

### Modern Design Features
- **CSS Custom Properties**: Easy color scheme customization
- **Backdrop Filter**: Modern glass morphism effects
- **CSS Grid & Flexbox**: Responsive, flexible layouts
- **Keyframe Animations**: Smooth, professional animations

## 🎨 Customization

### Colors & Theme
Modify the CSS custom properties in `:root`:
```css
:root {
    --primary: #00d4ff;      /* Main accent color */
    --secondary: #ff6b9d;    /* Secondary accent */
    --accent: #7c3aed;       /* Additional accent */
    --bg-dark: #0a0a0f;      /* Background color */
    --bg-card: #1a1a2e;      /* Card background */
    --bg-glass: rgba(26, 26, 46, 0.8); /* Glass effect */
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

### Translations
Add new languages or modify existing ones in the `translations` object:
```javascript
const translations = {
    en: { /* English */ },
    de: { /* German */ },
    fr: { /* French - new language */ }
};
```

## 📱 Browser Compatibility

- **Chrome**: Full support (recommended)
- **Firefox**: Full support
- **Safari**: Full support
- **Edge**: Full support
- **Mobile Browsers**: Responsive design with touch optimization
- **HTTPS Required**: Voice features require secure connection

## 🔧 Troubleshooting

### Voice Recognition Not Working
- Ensure HTTPS is enabled (required for Web Speech API)
- Check browser permissions for microphone access
- Verify Web Speech API support in your browser
- Clear browser cache and permissions

### AI Responses Not Working
- Verify OpenAI API key is correct
- Check API quota and billing status
- Ensure proper CORS configuration
- Check browser console for error messages

### Design Issues
- Clear browser cache
- Verify CSS is loading properly
- Check for JavaScript errors in console
- Ensure modern browser support

### Language Switching Issues
- Verify all HTML elements have proper IDs
- Check translation object structure
- Ensure `applyTranslations()` function is working
- Clear browser cache

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

## 🔄 Recent Updates

### Version 2.0 (December 2024)
- **Complete Website Redesign**: Modern, futuristic robotic theme
- **Full Translation System**: Complete English and German localization
- **Custom Robotic Microphone**: Multi-layered SVG icon with glow effects
- **Enhanced UI/UX**: Glass morphism, animations, and responsive design
- **Improved Performance**: Optimized animations and smooth interactions
- **Professional Legal System**: Modal popups with external links

### Version 1.0 (Previous)
- Basic voice recognition functionality
- Simple language switching
- Basic robot image rotation

---

**Last Updated**: December 2024  
**Version**: 2.0  
**Status**: Production Ready  
**Features**: Complete, Professional, Multi-language 