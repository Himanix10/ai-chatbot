# AI Chat Assistant

A modern, full-stack chatbot application built with React, TypeScript, and Express.js. Features intelligent AI responses powered by OpenAI's GPT-4o model with a clean, responsive design.

![Chat Interface](https://img.shields.io/badge/React-18-blue) ![TypeScript](https://img.shields.io/badge/TypeScript-5-blue) ![Express](https://img.shields.io/badge/Express.js-4-green) ![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o-orange)

## ✨ Features

- **Real-time Chat Interface** - Smooth messaging experience with typing indicators
- **AI-Powered Responses** - Intelligent conversations using OpenAI's latest GPT-4o model
- **Modern UI/UX** - Clean design with shadcn/ui components and Tailwind CSS
- **Message History** - Persistent conversation context throughout the session
- **Responsive Design** - Works seamlessly on desktop and mobile devices
- **Demo Mode** - Intelligent fallback responses when API quota is reached
- **Error Handling** - Robust error management and user feedback

## 🚀 Tech Stack

### Frontend
- **React 18** with TypeScript
- **Vite** for fast development and optimized builds
- **Tailwind CSS** for styling
- **shadcn/ui** for modern UI components
- **TanStack Query** for server state management
- **Wouter** for lightweight routing

### Backend
- **Node.js** with Express.js
- **TypeScript** for type safety
- **OpenAI API** integration
- **In-memory storage** for development
- **RESTful API** design

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ai-chat-assistant.git
   cd ai-chat-assistant
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   NODE_ENV=development
   ```

4. **Start the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:5000`

## 🔧 Configuration

### OpenAI API Key
Get your API key from [OpenAI Platform](https://platform.openai.com/api-keys):
1. Create an account at OpenAI
2. Navigate to API Keys section
3. Create a new API key
4. Add it to your `.env` file

### Demo Mode
When the OpenAI API is unavailable or quota is exceeded, the application automatically switches to demo mode with intelligent contextual responses.

## 🏗️ Project Structure

```
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/         # Page components
│   │   ├── hooks/         # Custom React hooks
│   │   └── lib/           # Utility functions
├── server/                # Backend Express application
│   ├── routes.ts          # API routes
│   ├── storage.ts         # Data storage layer
│   └── index.ts           # Server entry point
├── shared/                # Shared types and schemas
│   └── schema.ts          # Data models and validation
└── package.json           # Dependencies and scripts
```

## 🎯 Key Components

### Chat Interface
- **ChatHeader**: App branding with action buttons
- **ChatMessages**: Scrollable message history with role-based styling
- **ChatInput**: Auto-resizing input with quick action prompts
- **MessageBubble**: Styled message containers with timestamps

### API Endpoints
- `GET /api/messages/:sessionId` - Retrieve conversation history
- `POST /api/messages` - Send message and get AI response
- `DELETE /api/messages/:sessionId` - Clear chat history

## 🔄 Data Flow

1. User sends message through the chat input
2. Frontend validates and sends to backend API
3. Backend saves user message and requests AI response
4. OpenAI processes conversation history and generates response
5. Backend saves AI response and returns both messages
6. Frontend updates the UI with new messages

## 🚀 Deployment

### Development
```bash
npm run dev
```

### Production Build
```bash
npm run build
npm start
```

### Environment Variables
- `OPENAI_API_KEY`: Your OpenAI API key (required)
- `NODE_ENV`: Environment mode (development/production)

## 🎨 Customization

### Styling
- Modify `client/src/index.css` for global styles
- Update Tailwind configuration in `tailwind.config.ts`
- Customize component styles in individual component files

### AI Behavior
- Adjust system prompt in `server/routes.ts`
- Modify response parameters (temperature, max_tokens)
- Add custom demo responses for fallback mode

## 📝 Features in Detail

### Real-time Messaging
- Instant message sending and receiving
- Typing indicators while AI is responding
- Smooth scrolling to new messages
- Auto-resizing text input

### Error Handling
- Network error recovery
- API quota management
- User-friendly error messages
- Automatic fallback to demo mode

### Responsive Design
- Mobile-first approach
- Tablet and desktop optimizations
- Touch-friendly interface
- Accessible design patterns

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [OpenAI](https://openai.com/) for the GPT-4o API
- [shadcn/ui](https://ui.shadcn.com/) for the beautiful UI components
- [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS framework
- [React](https://reactjs.org/) and [TypeScript](https://www.typescriptlang.org/) for the robust development experience

## 📞 Support

If you have any questions or need help getting started, please open an issue or reach out!

---

**Built with ❤️ using modern web technologies**
