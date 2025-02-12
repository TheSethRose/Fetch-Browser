# Fetch Browser

[![smithery badge](https://smithery.ai/badge/@TheSethRose/fetch-browser)](https://smithery.ai/server/@TheSethRose/fetch-browser)

A powerful headless browser MCP server that enables AI agents to fetch web content and perform Google searches without requiring any API keys. Built with modern web standards and designed for seamless integration with AI platforms.

## Features

- **No API Keys Required**: Uses a sophisticated headless browser approach to fetch content directly
- **Smart Google Search**:
  - Extract structured results from Google searches
  - Support for both web and news results
  - Configurable number of results (1-100)
  - Full content fetching of search results
  - Automatic retry and error handling

- **Universal Content Fetching**:
  - Support for any webpage or API endpoint
  - Multiple output formats (HTML, JSON, Text, Markdown)
  - Automatic content type detection
  - Response size limits and timeout protection
  - Rate limiting protection

- **Format Conversion**:
  - Clean HTML to Markdown conversion
  - Pretty-printed JSON responses
  - Structured HTML output
  - Plain text with proper formatting

## Tools

### 1. Google Search Tool (`google_search`)
Executes Google searches and fetches full content of results:

```typescript
{
  query: "your search query",
  responseType: "markdown", // or "json", "html", "text"
  maxResults: 10,          // 1-100 results
  topic: "web"            // or "news"
}
```

### 2. URL Fetcher Tool (`fetch_url`)
Fetches content from any URL:

```typescript
{
  url: "https://example.com",
  responseType: "markdown", // or "json", "html", "text"
  timeout: 30000          // optional, in milliseconds
}
```

## Installation

### Via Smithery
```bash
# For Claude
npx -y @smithery/cli install @TheSethRose/fetch-browser --client claude

# For Cursor
npx -y @smithery/cli install @TheSethRose/fetch-browser --client cursor

# For TypeScript
npx -y @smithery/cli install @TheSethRose/fetch-browser --client typescript
```

### Manual Installation
```bash
# Clone the repository
git clone https://github.com/TheSethRose/fetch-browser.git
cd fetch-browser

# Install dependencies
npm install

# Build the project
npm run build

# Start the server
npm start
```

## Development

```bash
# Watch mode with auto-rebuild
npm run watch

# Run with inspector
npm run inspector

# Debug mode
npm run debug

# Debug with watch mode
npm run debug:watch
```

## Response Formats

### 1. Markdown Format
```markdown
## [Page Title](https://example.com)

Content converted to clean markdown with:
- Lists
- **Bold text**
- *Italic text*
- [Links](https://example.com)
```

### 2. JSON Format
```json
{
  "url": "https://example.com",
  "content": "Extracted content...",
  "error": null
}
```

### 3. HTML Format
```html
<div class="search-result">
  <h2><a href="https://example.com">Page Title</a></h2>
  <div class="content">
    Original HTML content
  </div>
</div>
```

### 4. Text Format
```text
### https://example.com

Plain text content with preserved formatting
==========
```

## Error Handling

- Automatic retries with exponential backoff
- Rate limiting protection
- Timeout handling
- Detailed error messages
- Individual result error tracking

## Security Features

- Response size limits
- Request timeouts
- Rate limiting protection
- No API keys or secrets required
- Proper error handling

## Credits

**Created by Seth Rose**:
- **Website**: [https://www.sethrose.dev](https://www.sethrose.dev)
- **𝕏 (Twitter)**: [https://x.com/TheSethRose](https://x.com/TheSethRose)
- **🦋 (Bluesky)**: [https://bsky.app/profile/sethrose.dev](https://bsky.app/profile/sethrose.dev)

## License

MIT License - See [LICENSE](LICENSE) for details
