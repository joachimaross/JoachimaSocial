# Quemiai 🧠🔥

A NestJS-based backend platform for scalable AI-driven applications. Built with TypeScript, WebSockets, and modern cloud infrastructure.

## 🚀 Getting Started

### Prerequisites

- Node.js >= 18 < 21
- npm or yarn
- PostgreSQL (for database)
- Redis (optional, for caching)

### Installation

```bash
# Install dependencies
npm install

# Copy environment variables
cp .env.example .env

# Edit .env with your configuration
```

### Development

```bash
# Run in development mode with hot reload
npm run start:dev

# Run in debug mode
npm run start:debug

# Build the project
npm run build

# Run in production mode
npm run start:prod
```

## 🧪 Testing

```bash
# Run unit tests
npm run test

# Run tests in watch mode
npm run test:watch

# Run tests with coverage
npm run test:cov

# Run e2e tests
npm run test:e2e
```

**See [TESTING.md](TESTING.md) for comprehensive testing guide, coverage goals, and best practices.**

### Current Test Coverage

- **Overall Coverage:** ~42% (Target: 75%+)
- **Unit Tests:** 10 tests passing
- **Integration Tests:** Included
- **E2E Tests:** Available

### Coverage Goals

| Metric | Current | Target |
|--------|---------|--------|
| Statements | ~42% | 75% |
| Branches | ~20% | 65% |
| Functions | ~15% | 70% |
| Lines | ~41% | 75% |

## 🧹 Code Quality

```bash
# Run linter
npm run lint

# Format code with Prettier
npm run format
```

## 🏗️ Tech Stack

- **Framework:** NestJS
- **Language:** TypeScript
- **Real-time:** Socket.IO (WebSockets)
- **Testing:** Jest
- **Linting:** ESLint + Prettier
- **Logging:** Pino
- **Database:** PostgreSQL with Prisma ORM
- **Caching:** Redis
- **Cloud:** Google Cloud Platform, Firebase
- **Deployment:** Vercel-ready, Docker support

## 📁 Project Structure

```
src/
├── api/                # API route handlers
├── config/             # Configuration files (logger, redis, firebase, etc.)
├── modules/            # Feature modules
│   └── chat/           # Real-time chat module with WebSocket gateway
├── middleware/         # Custom middleware (error handling, validation)
├── services/           # Business logic services
├── gateways/           # WebSocket gateways
├── utils/              # Utility functions
├── app.module.ts       # Root application module
└── main.ts             # Application entry point
```

## 🔧 Environment Variables

See `.env.example` for all required environment variables:

- **PORT:** Server port (default: 4000)
- **DATABASE_URL:** PostgreSQL connection string
- **JWT_SECRET:** Secret for JWT token generation
- **REDIS_URL:** Redis connection URL (optional)
- **Google OAuth:** GOOGLE_CLIENT_ID, GOOGLE_CLIENT_SECRET
- **Apple OAuth:** APPLE_CLIENT_ID, APPLE_TEAM_ID, etc.
- **Firebase:** FIREBASE_PROJECT_ID, FIREBASE_CLIENT_EMAIL, etc.
- **Storage:** Cloud storage credentials

## 🌟 Features

- ✅ RESTful API architecture
- ✅ Real-time WebSocket communication (Chat module)
- ✅ JWT authentication
- ✅ OAuth integration (Google, Apple)
- ✅ Firebase integration
- ✅ Structured logging with Pino
- ✅ Global error handling
- ✅ Request validation
- ✅ **Rate limiting with @nestjs/throttler**
- ✅ **Sentry error tracking and performance monitoring**
- ✅ CORS configuration
- ✅ Swagger API documentation (configurable)
- ✅ Docker support
- ✅ CI/CD with GitHub Actions
- ✅ **Enhanced Vercel deployment with security headers**

## 🐳 Docker

Build and run with Docker:

```bash
# Build image
docker build -t quemiai .

# Run container
docker run -p 4000:4000 --env-file .env quemiai
```

## 🚀 Deployment

### Vercel (Recommended)

The project is configured for Vercel deployment with enhanced `vercel.json`.

**Key Features:**
- Automatic HTTPS and security headers
- Environment variable management
- Preview deployments for PRs
- Automatic scaling
- Built-in analytics

**Quick Deploy:**
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

**See [DEPLOYMENT.md](DEPLOYMENT.md) for:**
- Complete Vercel deployment checklist
- Sentry integration setup
- Rate limiting configuration
- Environment variables guide
- Troubleshooting and best practices

### Docker

Use the included `Dockerfile` for containerized deployment on any platform.

```bash
docker build -t quemiai .
docker run -p 4000:4000 --env-file .env quemiai
```

## 📋 Git Workflow

We follow a standard Git workflow:

- **main** - Production branch
- **dev** - Development/staging branch
- **feature/** - Feature branches
- **hotfix/** - Hotfix branches

See `CONTRIBUTING.md` for contribution guidelines.

## ✅ Roadmap

See our comprehensive [ROADMAP.md](ROADMAP.md) for detailed development phases and timelines.

### Completed
- [x] Base NestJS setup
- [x] Real-time chat with WebSockets
- [x] Authentication & OAuth
- [x] Logging & error handling
- [x] Docker & CI/CD setup


## 📝 License

UNLICENSED - Private project

## 🤝 Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## 📧 Support

For questions or issues, please open an issue in the GitHub repository.

---

**Built with ❤️ using NestJS**
