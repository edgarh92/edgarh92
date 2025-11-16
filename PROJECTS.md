# Projects Portfolio

A comprehensive overview of professional and personal projects showcasing technical expertise across media automation, AI research (prompt engineering, Langgraph, Ollama, ChromaDB), web development, and automation tools.

---

## 💼 Professional Projects @ LinkedIn

### 1. Licensed Content to Vantage Pipeline
**Status**: Active | **Tech Stack**: Python 3.12, MediaInfo, pydub-ng, pymediainfo

Automated validation and submission system for raw video files of licensed content to Vantage, bypassing the video editing team.

**Key Features**:
- **Media Validation**: Comprehensive video file validation with support for 1:1 aspect ratios (1080x1080 to 3840x3840)
- **Audio Processing**: Automatic mono-to-stereo conversion with backup functionality
- **File Handling**: Unified video file selection combining MP4 and MOV files
- **Type Safety**: Comprehensive type annotations and Optional handling throughout codebase
- **Interactive Selection**: File selection with support for individual files, ranges, and wildcard patterns
- **Truncated File Detection**: MediaInfo integration for detecting truncated files
- **User Experience**: Enhanced input handling with graceful Ctrl-C exit and extended course ID format support

**Technologies Used**:
- Python 3.12
- MediaInfo, pymediainfo for media analysis
- pydub-ng for audio processing
- colorlog for enhanced logging
- Type annotations and type safety improvements

**Repository**: `mwerner_LinkedIn/enp-emea-licensed-to-vantage` (Private)

**Notable Technical Achievements**:
- Implemented robust media validation pipeline
- Created backup system for audio conversions
- Enhanced type safety across entire codebase
- Improved Linux compatibility for folder operations

**Last Updated**: September 2024

---

### 3. Closed Caption Order Tool (GCP)
**Status**: Active | **Tech Stack**: Python, Google Cloud Platform

GCP-based closed caption ordering system for E&P EMEA region, streamlining the caption workflow process.

**Key Features**:
- Automated caption ordering workflow
- GCP integration for cloud operations
- EMEA region-specific optimizations

**Technologies Used**:
- Python
- Google Cloud Platform
- API integrations

**Repository**: `mwerner_LinkedIn/gcp-enp-emea-cc-order` (Private)

**Last Updated**: June 2024

---

### 4. Globus Thumbnail Distribution
**Status**: Active | **Tech Stack**: Python 3.12, Systemd, Watchdog

Hotfolder service for syncing graphics thumbnails to course projects. This service monitors configured directories for thumbnail files and processes them according to course ID, locale, and file type.

**Key Features**:
- **Automatic File Monitoring**: Polling-based hotfolder service with configurable intervals
- **Course ID and Filename Validation**: Validates filenames against patterns and courselist CSV
- **Multi-Locale Support**: Supports 7 locales (de_DE, en_US, es_ES, fr_FR, ja_JP, pt_BR, zh_CN)
- **Intelligent Routing**: Automatic routing to course folders, asset bank, and archive based on locale and file type
- **Remote Sync Support**: EMEAL locales (de_DE, es_ES, fr_FR, pt_BR) processed for remote sync with outgoing cache
- **Audio-Only File Handling**: Special handling for audio-only files with dedicated destinations
- **Structured Logging**: Comprehensive logging with correlation IDs for traceability
- **Retry Logic**: Exponential backoff retry mechanism for transient failures
- **Mount Availability Monitoring**: Health checks verify mount points before processing
- **Systemd Watchdog Integration**: Production-ready service health monitoring with automatic restart
- **Courselist Freshness Validation**: Warns when courselist CSV is stale (configurable threshold)

**Technologies Used**:
- Python 3.12
- Systemd service management
- Watchdog integration for health monitoring
- Environment-based configuration (Pydantic-style)
- Structured logging with rotation
- File system operations and path management

**Repository**: `lct-globus-thumbnail-distribution` (Private)

**Notable Technical Achievements**:
- Production-ready service with systemd integration
- Robust error handling with failed file isolation
- Health monitoring and mount availability checks
- Configurable via environment variables with sensible defaults
- Comprehensive logging for debugging and monitoring

**Last Updated**: January 2025

---

### 5. Cosmo Report Center Exporter
**Status**: Active | **Tech Stack**: Python

Python tool for exporting reports from Cosmo report center, improving data accessibility and workflow efficiency.

**Key Features**:
- Report export automation
- Data extraction and formatting
- Integration with Cosmo report center

**Technologies Used**:
- Python
- Data processing libraries
- Report generation

**Repository**: `mwerner_LinkedIn/enp-emea-cosmo-report-center-exporter` (Private)

**Last Updated**: October 2024

---

### 6. Cronjob Lock Alert Service (GCP)
**Status**: Active | **Tech Stack**: Python, Google Cloud Platform, Microsoft Teams

Publishing Operations cronjob lock monitor with Teams webhook alerts using messaging stream to file.

**Key Features**:
- Cronjob lock monitoring
- Teams webhook integration for alerts
- Messaging stream to file
- Automated alerting system

**Technologies Used**:
- Python
- Google Cloud Platform
- Microsoft Teams API
- File-based messaging streams

**Repository**: `ehernand_LinkedIn/gcp-cron-lock-alert-service` (Private)

**Last Updated**: July 2024

---

### 7. Publishing Services API
**Status**: Active | **Tech Stack**: Python, FastAPI, Pydantic, SSL/TLS

Major refactoring and enhancement of publishing services API, migrating to modern configuration patterns and adding comprehensive features.

**Key Features**:
- **Configuration Refactoring**: Migrated from legacy api_secrets.py to environment-based configuration using Pydantic
- **SSL Certificate Management**: Comprehensive SSL certificate setup script with validation and extraction
- **Environment-Aware Configuration**: Factory pattern for development/production environments
- **FastAPI Enhancements**: SSL support and enhanced health/config endpoints
- **Email Configuration**: Refactored to use environment variables instead of JSON files
- **TOC/PTOC Endpoints**: Action-based filtering and improved functionality
- **PTOC Validation**: Enhanced validation service with path-based validation and business rule improvements (13,149+ additions)

**Technologies Used**:
- Python, FastAPI
- Pydantic for configuration management
- SSL/TLS certificate handling
- Environment-based configuration
- Dependency injection patterns

**Repository**: `linkedin-managed/pub-ops-publishing-services-api` (Private)

**Contributions**: 6 PRs, including major v1.3.0 release with 2,763 additions, 492 deletions

**Last Updated**: November 2024

---

### 8. Course Filename Validator
**Status**: Active | **Tech Stack**: Python, Validation, Pattern Matching

Enhanced validation system for course filename patterns with improved error messaging and stricter validation rules.

**Key Features**:
- **Stricter Pattern Validation**: Removed backward compatibility for legacy formats, enforcing clear separation between PERPETUAL and PERPETUAL_V2 patterns
- **Enhanced Validation Logic**: Improved locale regex (mixed-case support), robust multi-part descriptor detection, early failure for invalid course IDs
- **Improved Error Messaging**: Standardized error messages with consistent "Pattern:" prefix, better formatting and clarity
- **Version Management**: Version bumping and changelog management
- **Performance Optimizations**: Early failure mechanisms for better performance

**Technologies Used**:
- Python
- Regex pattern matching
- Validation frameworks
- Error handling and messaging

**Repository**: `linkedin-managed/pubops-course-filename-validator` (Private)

**Contributions**: 7 PRs, including major enhancement with 870 additions, 494 deletions

**Last Updated**: November 2024

---

### 9. Reingest Scripts
**Status**: Active | **Tech Stack**: Python, CLI, Modular Architecture

Refactored VIT WorkOrder Builder for better modularity and maintainability, improving code organization and test coverage.

**Key Features**:
- **Modular Restructuring**: Reduced complexity by restructuring main script into modular components
- **CLI Command Registration**: Improved CLI interface with command registration
- **Enhanced Logging**: Better logging setup and configuration
- **Test Coverage**: New test configurations and comprehensive unit tests for CLI commands
- **Maintainability**: Enhanced readability and maintainability through better code organization

**Technologies Used**:
- Python
- CLI frameworks
- Modular architecture patterns
- Unit testing frameworks

**Repository**: `linkedin-managed/pub-ops-reingest-scripts` (Private)

**Contributions**: 6 PRs, including major refactoring with 3,210 additions, 472 deletions

**Last Updated**: June 2024

---

### 10. Course Path Utilities
**Status**: Active | **Tech Stack**: Python, Path Management, Schema Validation

Utilities for course path management and validation, fixing schema mappings and improving path handling.

**Key Features**:
- Course path management utilities
- Schema mapping fixes
- Path validation and handling
- Missing return statement fixes

**Technologies Used**:
- Python
- Path manipulation libraries
- Schema validation

**Repository**: `linkedin-managed/enp-course-path-utils` (Private)

**Contributions**: 4 PRs

**Last Updated**: November 2024

---

### 11. Caption Order Bot (GCP)
**Status**: Active | **Tech Stack**: Python, Google Cloud Platform, Automation

GCP-based bot for automated caption ordering workflow, fixing bugs and improving automation.

**Key Features**:
- Automated caption ordering
- Missing videos bug fixes
- Workflow automation improvements

**Technologies Used**:
- Python
- Google Cloud Platform
- Automation frameworks

**Repository**: `linkedin-managed/gcp-enp-caption-order-bot` (Private)

**Contributions**: 2 PRs (316+ additions, 89 deletions)

**Last Updated**: November 2024

---

### 12. Vantage Ingest Tool
**Status**: Active | **Tech Stack**: Perl, Automation, Media Processing

Enhanced Vantage ingest automation with ACL overrides and improved error handling.

**Key Features**:
- Vantage ingest automation
- ACL override functionality
- Improved error handling
- Media processing workflows

**Technologies Used**:
- Perl
- Automation scripts
- Media processing tools

**Repository**: `linkedin-managed/gcp-vantage-ingest-tool` (Private)

**Contributions**: 3 PRs

**Last Updated**: July 2024

---

## 🚀 Personal Projects

---

## 🤖 AI Research Projects

### 7. AI-Powered Screenshot Organizer (SaaS)
**Status**: Active | **Tech Stack**: Next.js, TypeScript, React, Tailwind CSS, AI Research Tools, Pinata/IPFS, Vercel

A production-ready SaaS application that automatically categorizes and analyzes screenshots using AI research tools. Features OCR for text extraction and decentralized storage on IPFS.

**Key Features**:
- Screenshot categorization using AI research tools (Work, Shopping, Entertainment, etc.)
- OCR for text extraction and searchability
- Decentralized storage via Pinata Files API (IPFS)
- Cross-device sync capability
- Drag-and-drop interface with real-time analysis
- Serverless deployment on Vercel

**Technologies Used**:
- Frontend: Next.js 14, React 18, TypeScript
- UI: Tailwind CSS, Radix UI, Framer Motion, shadcn/ui
- AI: AI research tools for OCR and classification
- Storage: Pinata Files API for IPFS
- Deployment: Vercel serverless functions

**Repository**: `ai-screenshot-organiser/`

---

### 8. Agentic System Research Project
**Status**: Active | **Tech Stack**: Python, FastAPI, Langgraph, Ollama, ChromaDB

Research project exploring agentic systems for multi-step reasoning and tool usage, using Langgraph for workflow orchestration and Ollama for local LLM inference.

**Key Features**:
- Multi-step reasoning and task breakdown using Langgraph
- Local LLM inference with Ollama
- ChromaDB for embeddings and vector storage
- Custom tools: code execution, web search, math operations
- CLI interface for experimentation
- FastAPI/Uvicorn server

**Technologies Used**:
- Python 3.10+, FastAPI, Uvicorn
- Langgraph for workflow orchestration
- Ollama for local LLM inference
- ChromaDB for embeddings and vector storage
- Custom tool integration framework

**Repository**: `llama-agentic-system/`

**Research Focus**:
- Exploring agentic workflows and tool integration
- Experimenting with local LLM inference
- Vector storage and embedding research
- Prompt engineering and optimization

---

### 9. Image Tagger with Vector Storage
**Status**: Active | **Tech Stack**: Python, ChromaDB, PIL

Image tagging system using vector storage for similarity search and embeddings.

**Key Features**:
- Image tagging with vector-based similarity search
- ChromaDB for embeddings and vector storage
- Web interface for image processing
- Batch processing capabilities

**Technologies Used**:
- Python
- ChromaDB for vector database and embeddings
- PIL for image processing
- Web interface (Flask/Streamlit)

**Repository**: `llama-vision-image-tagger/`

---

## 🎵 Media & Music Automation Projects

### 10. YouTube to Spotify Archiver
**Status**: Active | **Tech Stack**: Python, Spotify API, YouTube API, OAuth2, yt-dlp

Automated tool for migrating playlists from YouTube to Spotify with high accuracy matching.

**Key Features**:
- Automated playlist migration (85-95% success rate)
- Fuzzy matching for song titles and artists
- OAuth2 authentication for secure API access
- JSON metadata export
- Dry-run mode for testing
- Comprehensive logging

**Technologies Used**:
- Python 3.8+
- Spotify API (spotipy)
- YouTube API (google-api-python-client)
- yt-dlp for video metadata
- thefuzz for fuzzy string matching
- OAuth2 for authentication

**Repository**: `Youtube-to-Spotify-Archiver/`

**Stats**: Successfully migrated 142 songs out of 150 from a test playlist (94.7% success rate)

---

### 11. Music Information Parser
**Status**: Active | **Tech Stack**: Python, Selenium, Playwright, BeautifulSoup

Web scraping tool for extracting music metadata from dynamic web pages across multiple platforms.

**Key Features**:
- Multi-platform support (Spotify, YouTube Music, Facebook, Instagram, etc.)
- Multiple extraction methods with confidence scoring
- Browser console JavaScript for instant extraction
- Selenium and Playwright support
- Pattern matching for various site structures

**Technologies Used**:
- Python, BeautifulSoup4, lxml
- Selenium 4.15+, Playwright
- Pattern matching and CSS selectors
- Confidence scoring algorithm

**Repository**: `music_parser/`

**Supported Platforms**:
- ✅ Spotify Web Player
- ✅ YouTube Music
- ✅ Apple Music Web
- ✅ SoundCloud
- ✅ Bandcamp
- ✅ Facebook/Instagram music posts

---

## 🌐 Browser Extensions & Web Tools

### 12. Reddit Enhancement Suite (Contributor)
**Status**: Active Contributor | **Tech Stack**: JavaScript, Chrome Extension API, Flow, Babel

Open-source browser extension with 1M+ users for enhancing Reddit browsing experience.

**Key Contributions**:
- Modular architecture development
- Cross-browser compatibility (Chrome, Firefox)
- i18n support implementation
- Code quality improvements (Flow, ESLint)
- Build system optimization

**Technologies Used**:
- JavaScript (ES6+), Flow type system
- Babel, Webpack, esbuild
- Chrome Extension API, Firefox WebExtensions API
- SCSS, PostCSS
- Nightwatch for E2E testing

**Repository**: `Reddit-Enhancement-Suite/`

---

### 13. YouTube Playlist Cleaner
**Status**: Active | **Tech Stack**: JavaScript, Chrome Extension API

Browser extension for managing and cleaning YouTube playlists with batch operations.

**Key Features**:
- Batch playlist operations
- User-friendly interface
- Efficient playlist management
- Clean and simple UI

**Technologies Used**:
- JavaScript
- Chrome Extension Manifest V3
- YouTube API integration

**Repository**: `YouTube-Playlist-Cleaner/`

---

### 14. YouTube Watch Later Deleter
**Status**: Active | **Tech Stack**: JavaScript, Chrome Extension API

Simple browser extension for managing YouTube Watch Later playlist.

**Key Features**:
- Quick deletion of watch later items
- Batch operations support
- Lightweight and fast

**Technologies Used**:
- JavaScript
- Chrome Extension API
- Content scripts and background workers

**Repository**: `youtube-watch-later-deleter/`

---

## 📊 Project Statistics & Impact

### Code Quality
- **Total Projects**: 20+ active projects (12+ professional + 8 personal)
- **Active Contributions**: 50+ pull requests across 19+ repositories
- **Major Refactorings**: Publishing Services API (13,149+ additions), Reingest Scripts (3,210+ additions), Course Filename Validator (870+ additions)
- **Languages**: Python, JavaScript/TypeScript, SQL, Bash
- **Frameworks**: Next.js, FastAPI, React, Chrome Extensions
- **APIs Integrated**: Spotify, YouTube, Brave Search, Wolfram Alpha, Pinata/IPFS

### Performance Metrics
- **Video Processing**: 60% HLS performance improvement
- **Media Workflows**: 80% QoE increase
- **Archiving Efficiency**: 70% process improvement
- **Playlist Migration**: 85-95% success rate

### Technical Highlights
- Production-grade microservices architecture
- Cloud migration leadership (on-premises to AWS)
- AI research with Langgraph, Ollama, and ChromaDB
- Decentralized storage implementation (IPFS)
- Cross-platform browser extension development
- Professional media automation tools for enterprise use
- GCP-based automation and monitoring services
- Advanced media validation and processing pipelines

---

## 🔧 Technical Patterns & Practices

### Architecture Patterns
- **Microservices**: Modular, scalable service architecture
- **Serverless**: Vercel serverless functions, AWS Lambda
- **API-First**: RESTful APIs with FastAPI and Next.js API routes
- **Event-Driven**: Asynchronous processing for media workflows

### Development Practices
- **Type Safety**: TypeScript, Flow, Python type hints
- **Testing**: Unit tests, integration tests, E2E testing
- **CI/CD**: Automated builds and deployments
- **Code Quality**: ESLint, Prettier, Black, pre-commit hooks

### DevOps & Deployment
- **Cloud Platforms**: AWS, Azure, Vercel
- **Containerization**: Docker (where applicable)
- **Version Control**: Git with proper branching strategies
- **Monitoring**: Logging, performance metrics, error tracking

---

## 🚀 Future Projects & Ideas

### Planned Enhancements
- Enhanced prompt engineering and AI research tool integration
- Real-time collaboration features
- Mobile app versions of key tools
- Advanced analytics and reporting
- Integration with more platforms and services

### Learning Focus
- Advanced prompt engineering techniques
- Distributed systems architecture
- Performance optimization techniques
- Accessibility improvements
- Security best practices

---

## 📝 Project Organization

### Personal Projects
All personal projects are organized in the `/Users/ehernand/personal_projects/` directory:

```
personal_projects/
├── ai-screenshot-organiser/     # Next.js SaaS app
├── llama-agentic-system/        # AI agentic system
├── llama-vision-image-tagger/    # Image tagging tool
├── Youtube-to-Spotify-Archiver/ # Playlist migration tool
├── music_parser/                 # Music metadata extractor
├── Reddit-Enhancement-Suite/     # Browser extension (contributor)
├── YouTube-Playlist-Cleaner/     # Playlist management tool
└── youtube-watch-later-deleter/  # Watch later manager
```

### Professional Projects @ LinkedIn
Professional projects are hosted on LinkedIn's GitHub organization:

**Publishing Operations & Orchestration:**
```
linkedin-managed/
├── pub-ops-publishing-services-api (6 PRs, 13,149+ additions)
├── pubops-course-filename-validator (7 PRs, 870+ additions)
├── pub-ops-reingest-scripts (6 PRs, 3,210+ additions)
├── enp-course-path-utils (4 PRs)
├── pubops-sandbox (3 PRs)
└── gcp-vantage-ingest-tool (3 PRs)
```

**Caption & Media Services:**
```
linkedin-managed/
├── gcp-enp-caption-order-bot (2 PRs, 316+ additions)
└── gcp-enp-vantage-ingest-copy-service (3 PRs)
```

**EMEA Tools & Utilities:**
```
mwerner_LinkedIn/
├── enp-emea-licensed-to-vantage
├── gcp-enp-emea-cc-order
└── enp-emea-cosmo-report-center-exporter
```

**LinkedIn Learning Content Tools:**
```
lct-globus-thumbnail-distribution/
└── globus-thumbnail-distribution (Hotfolder service)
```

**Other Services:**
```
linkedin-managed/
├── gcp-gfx-genome (3 PRs, JavaScript)
├── gcp-create-course-toc (2 PRs)
├── gcp-edit-sagan (1 PR)
├── gcp-editing-auto-scheduler (2 PRs)
├── gcp-ppm-auto-scheduler (1 PR)
└── gcp-ppm-clickup-cosmo-sync (2 PRs)

ehernand_LinkedIn/
└── gcp-cron-lock-alert-service
```

---

## 🔗 Links & Resources

- **GitHub**: [edgarh92](https://github.com/edgarh92)
- **Twitter**: [@eggpression](https://twitter.com/eggpression)
- **LinkedIn**: [ehernandez0](https://linkedin.com/in/ehernandez0)
- **Email**: h.edgar714@gmail.com

---

*Last Updated: [Current Date]*

