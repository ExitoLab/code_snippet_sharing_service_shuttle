# Context7 MCP Server Setup for Rust Documentation

This guide shows how to set up and use the Context7 MCP server to get Rust documentation directly in your Cursor editor.

## Setup

1. **Install Context7 MCP Server**:
   ```bash
   npm install -g @context7/mcp-server
   ```

2. **Get Context7 API Key**:
   - Visit [Context7](https://context7.io) and sign up
   - Get your API key from the dashboard

3. **Configure MCP Server**:
   The `.cursor/mcp.json` file has been created with the Context7 configuration. Update the API key:
   ```json
   {
     "mcpServers": {
       "context7": {
         "command": "npx",
         "args": ["@context7/mcp-server"],
         "env": {
           "CONTEXT7_API_KEY": "your-actual-api-key-here"
         }
       }
     }
   }
   ```

4. **Restart Cursor** to load the MCP server

## Usage Examples

Once configured, you can ask questions about Rust documentation directly in Cursor:

### Basic Rust Documentation Queries
- "How do I use Axum's State extractor?"
- "What are the best practices for error handling in Rust?"
- "How do I implement async functions in Rust?"
- "Show me examples of using serde for JSON serialization"

### Project-Specific Queries
- "How do I handle CORS in Axum?"
- "What's the best way to implement authentication in Rust web services?"
- "How do I use Shuttle for deployment?"
- "Show me examples of using tokio for async programming"

### Library-Specific Documentation
- "How do I use the uuid crate for generating IDs?"
- "What are the features of the chrono crate?"
- "How do I use nanoid for generating short IDs?"

## Benefits

- **Real-time Documentation**: Get up-to-date Rust documentation without leaving your editor
- **Context-Aware**: The AI understands your project structure and dependencies
- **Interactive Learning**: Ask follow-up questions and get detailed explanations
- **Code Examples**: Get practical examples tailored to your use case

## Troubleshooting

If the MCP server isn't working:

1. Check that the API key is correct
2. Ensure npm is installed and accessible
3. Restart Cursor completely
4. Check the Cursor logs for MCP server errors

## Your Current Dependencies

Based on your `Cargo.toml`, you're using:
- `axum` - Web framework
- `tokio` - Async runtime
- `shuttle-axum` - Deployment platform
- `serde` - Serialization
- `uuid` - UUID generation
- `chrono` - Date/time handling
- `nanoid` - Short ID generation

You can ask Context7 about any of these libraries and their integration patterns.