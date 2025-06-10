# Voice to Invoice React App

A modern, responsive React web application that allows users to record their voice and convert spoken content into structured invoice PDFs.

## 🚀 Features

### 🔐 User Authentication

- Clean, responsive login/register interface
- Client-side form validation with real-time feedback
- Password visibility toggle for enhanced UX
- Mock authentication system with proper error handling
- Email format validation and password requirements

### 🎤 Voice Recording

- Browser-based voice recording using MediaDevices API
- Visual feedback during recording (animated microphone button)
- Microphone permission handling with user-friendly messages
- Real-time recording status indicators
- Cross-browser compatibility checks

### 📝 Voice-to-Text Conversion

- Mock transcription service that simulates real voice-to-text conversion
- Displays structured invoice content from voice input
- Processing animations and loading states
- Error handling for failed transcriptions

### 📄 Invoice PDF Generation

- Converts transcribed text into downloadable invoice files
- Mock PDF generation (downloads as .txt file for demo)
- Professional invoice formatting with structured layout
- Loading states during generation process

### 📱 Responsive Design

- Mobile-first responsive design using Tailwind CSS
- Chat-like interface inspired by modern AI assistants (Gemini/ChatGPT style)
- Optimized for all screen sizes (mobile, tablet, desktop)
- Modern UI with smooth animations and transitions

## 🛠️ Technology Stack

- **React 18** - Modern React with functional components and hooks
- **TypeScript** - Type safety and better developer experience
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first CSS framework for styling
- **Browser APIs** - MediaDevices API for voice recording

## 🏁 Getting Started

### Prerequisites

- Node.js (version 16 or higher)
- Modern web browser with microphone support
- npm or yarn package manager

### Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd voice-to-invoice-app
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. **🔒 Set up environment variables (IMPORTANT)**:

   ```bash
   # Copy environment templates
   cp .env.example .env
   cp backend/.env.example backend/.env

   # Edit the files with your actual credentials
   # See SECURITY_SETUP.md for detailed instructions
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Open your browser and navigate to `http://localhost:5173` (or the port shown in terminal)

### 🔐 Security Setup

**⚠️ IMPORTANT**: Before running the application, you must configure your environment variables securely.

📖 **Read the complete security guide**: [SECURITY_SETUP.md](./SECURITY_SETUP.md)

Quick checklist:

- [ ] Copy `.env.example` to `.env` and update values
- [ ] Copy `backend/.env.example` to `backend/.env` and update values
- [ ] Never commit `.env` files to version control
- [ ] Use strong, unique passwords and API keys

### Building for Production

\`\`\`bash
npm run build
\`\`\`

The built files will be in the \`dist\` directory.

## 📖 Usage Guide

### Authentication

1. Open the application
2. Enter any email address and a password (minimum 6 characters)
3. Use the eye icon to toggle password visibility
4. Click "Sign In" or "Sign Up" - both will work with the mock authentication
5. Toggle between login and signup using the link at the bottom

### Recording Voice

1. After logging in, click the microphone button in the main interface
2. Allow microphone access when prompted by your browser
3. The microphone button will turn red and animate while recording
4. Speak your invoice details clearly
5. Click the microphone button again to stop recording

### Generating Invoice

1. Wait for the voice transcription to complete (simulated 2-second delay)
2. Review the transcribed invoice content in the chat-like display
3. Click "Generate Invoice PDF" to download the invoice file
4. Use the "Clear" button to remove transcription and start over

## 📁 Project Structure

\`\`\`
src/
├── components/ # Reusable React components (ready for expansion)
├── pages/ # Main page components
│ ├── AuthPage.tsx # Authentication page with login/signup
│ └── MainAppPage.tsx # Main application interface
├── types/ # TypeScript type definitions
│ └── index.ts # Shared types and interfaces
├── utils/ # Utility functions
│ ├── auth.ts # Authentication utilities and mock services
│ └── voice.ts # Voice recording and processing utilities
├── App.tsx # Main app component with routing logic
├── main.tsx # Application entry point
└── index.css # Tailwind CSS imports
\`\`\`

## 🌐 Browser Compatibility

This application requires a modern browser with support for:

- MediaDevices API (for microphone access)
- MediaRecorder API (for audio recording)
- ES6+ features and modern JavaScript APIs

**Recommended browsers:**

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 80+

## 🔧 Mock Services

This application uses mock services for demonstration purposes:

- **Authentication**: Always succeeds with proper email/password validation
- **Voice Transcription**: Returns a predefined invoice template after 2-second delay
- **PDF Generation**: Downloads a text file instead of a PDF after 1.5-second delay

## 🎨 UI/UX Features

- **Modern Design**: Clean, professional interface with consistent styling
- **Loading States**: Visual feedback for all async operations
- **Error Handling**: User-friendly error messages for all failure scenarios
- **Accessibility**: Proper ARIA labels and keyboard navigation support
- **Responsive**: Works seamlessly on mobile, tablet, and desktop
- **Animations**: Smooth transitions and micro-interactions

## 🚀 Future Enhancements

- Integration with real speech-to-text services (Google Speech API, Azure Speech Services)
- Real PDF generation using libraries like jsPDF or PDFKit
- User account persistence with backend integration
- Invoice template customization and themes
- Multi-language support for voice recognition
- Voice command recognition for specific invoice fields
- Export to various formats (PDF, Excel, JSON)
- Invoice history and management
- Client database integration

## 💻 Development

### Available Scripts

- \`npm run dev\` - Start development server with hot reload
- \`npm run build\` - Build for production with optimization
- \`npm run preview\` - Preview production build locally
- \`npm run lint\` - Run ESLint for code quality checks

### Code Quality

The project follows best practices with:

- TypeScript for type safety and better IDE support
- ESLint for code linting and consistency
- Proper error handling and loading states
- Responsive design principles
- Component-based architecture
- Clean separation of concerns

### Development Tips

1. The app checks for microphone support on load
2. All async operations have proper loading states
3. Error boundaries handle unexpected failures
4. Mock delays simulate real-world API response times
5. Components are designed to be easily replaceable with real services

## 📄 License

This project is licensed under the MIT License.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (\`git checkout -b feature/amazing-feature\`)
3. Make your changes with proper TypeScript types
4. Add or update tests if applicable
5. Ensure responsive design works on all screen sizes
6. Submit a pull request with detailed description

For bug reports and feature requests, please create an issue on the repository.

## 📞 Support

If you encounter any issues:

1. Check browser console for error messages
2. Ensure microphone permissions are granted
3. Try refreshing the page
4. Use a supported browser (Chrome recommended)
5. Check if the development server is running on the correct port

## 🙏 Acknowledgments

- Inspired by modern AI chat interfaces (ChatGPT, Gemini)
- Built with React and TypeScript best practices
- Styled with Tailwind CSS for rapid development
- Uses modern browser APIs for optimal performance
