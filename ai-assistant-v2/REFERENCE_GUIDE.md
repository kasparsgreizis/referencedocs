# AI Assistant V2 Reference Guide

## Project Overview
This document serves as a reference guide for the AI Assistant V2 project, which integrates ChatGPT capabilities with local file operations.

## Key Components

### 1. ChatGPT Integration
- API Endpoint: `/api/chat`
- Features:
  - Real-time chat with GPT-4 Turbo
  - Message history management
  - Error handling and rate limiting

### 2. File Operations
- API Endpoint: `/api/files`
- Supported Operations:
  - File creation
  - File reading
  - File deletion
  - Directory management

### 3. Security Features
- Environment variable protection
- Rate limiting implementation
- Error boundary handling
- Secure file operations

## Configuration

### Environment Variables
```env
OPENAI_API_KEY=your-api-key
NEXT_PUBLIC_APP_URL=http://localhost:3000
NODE_ENV=development
```

### API Configuration
- Base URL: `http://localhost:3000`
- Rate Limit: 10 requests per 60 seconds
- Supported Models: GPT-4 Turbo

## Development Setup

1. Clone the repository:
```bash
git clone https://github.com/kasparsgreizis/ai-assistent-v2.git
```

2. Install dependencies:
```bash
npm install
```

3. Configure environment:
```bash
cp .env.example .env
# Edit .env with your configuration
```

4. Start development server:
```bash
npm run dev
```

## API Reference

### Chat API
```typescript
POST /api/chat
{
  "messages": [
    {"role": "user", "content": "Your message"}
  ]
}
```

### File Operations API
```typescript
POST /api/files
{
  "action": "create|read|delete",
  "filePath": "path/to/file",
  "content": "file content" // for create action
}
```

## Related Documentation
- [API Documentation](API_DOCUMENTATION.md)
- [User Guide](USER_GUIDE.md)
- [Project Overview](PROJECT_OVERVIEW.md)
- [Getting Started](GETTING_STARTED.md)

## Contributing
Please refer to the main repository's contribution guidelines for information on how to contribute to this project.

## License
This project is licensed under the terms specified in the main repository.

## References
- [Reference Docs Repository](https://github.com/kasparsgreizis/referencedocs)
- [Main Project Repository](https://github.com/kasparsgreizis/ai-assistent-v2) 