# X Ads MCP Server (Twitter Ads)

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/x-ads)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect X Ads (formerly Twitter Ads) to AI assistants for real-time social advertising analytics.**

The X Ads MCP server enables Claude, ChatGPT, Cursor, and other AI assistants to analyze your X advertising campaigns. Track promoted tweets, monitor engagement, and get AI-powered recommendations.

![X Ads MCP Server](https://insightfulpipe.com/images/x-social-media-black-icon.svg)

## MCP Server URL

```
https://x-ads.insightfulmcp.com/
```

## What is X Ads MCP?

X Ads MCP is a **remote Model Context Protocol server** that connects your X Ads Manager to AI assistants. This real-time advertising integration allows you to:

- Query X ad performance using natural language
- Analyze promoted tweet engagement
- Track video views and website conversions
- Create async analytics jobs for large datasets
- Get AI recommendations for campaign optimization

## Installation

### Claude

1. Copy the MCP Server URL: `https://x-ads.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** on the connector to start authorization
6. Click **Authorize access** in the browser to complete the connection

### ChatGPT

1. Copy the MCP Server URL: `https://x-ads.insightfulmcp.com/`
2. Open ChatGPT Settings → **Connections**
3. Click **Add Connection** and paste the URL
4. Authorize with your InsightfulPipe account

### Claude Code

```bash
claude mcp add x-ads https://x-ads.insightfulmcp.com/
```

### Cursor

1. Open Cursor Settings → **MCP Servers**
2. Add new server with URL: `https://x-ads.insightfulmcp.com/`
3. Authorize the connection

## Available Actions

| Action | Description |
|--------|-------------|
| `get_account` | Get details for a specific ad account |
| `get_campaigns` | List all campaigns for an ad account |
| `get_campaign` | Get details for a specific campaign |
| `get_line_items` | List all line items for an ad account |
| `get_line_item` | Get details for a specific line item |
| `get_media_creatives` | List all media creatives for an ad account |
| `get_media_creative` | Get details for a specific media creative |
| `get_stats` | Retrieve synchronous analytics for an ad account |
| `get_active_entities` | Get active entities that had activity in a time range |
| `get_async_jobs` | Retrieve details for async analytics jobs |
| `create_async_job` | Create an async analytics job for longer time ranges |
| `cancel_async_job` | Cancel a processing async analytics job |

## Usage Examples

### Campaign Performance

```
"How are my X ad campaigns performing this week?"
```

### Tweet Analysis

```
"Which promoted tweets have the highest engagement rate?"
```

### Line Item Performance

```
"Show me stats for my top performing line items"
```

### Async Reports

```
"Create an async analytics job for the last 90 days"
```

### Creative Performance

```
"What creatives are driving the most conversions?"
```

## Supported Metrics

| Metric | Description |
|--------|-------------|
| Impressions | Total tweet views |
| Engagements | Likes, retweets, replies, clicks |
| Engagement Rate | Engagements / impressions |
| Link Clicks | Clicks to your website |
| Video Views | Video ad views |
| Follows | New follower gains |
| App Installs | Mobile app installations |
| Cost Per Engagement | Average CPE |

## Why X Ads MCP?

### For Brand Marketers
- **Real-time engagement** - Join conversations
- **Trending topics** - Capitalize on trends
- **Brand awareness** - Measure reach and sentiment

### For Performance Marketers
- **Conversion tracking** - Website and app actions
- **Async analytics** - Handle large data ranges
- **Line item optimization** - Granular performance data

### For Agencies
- **Multi-account management** - Handle client portfolios
- **Automated reporting** - Generate engagement reports
- **Competitive insights** - Share of voice analysis

## Security & Privacy

- **X Developer Platform** - Official API access
- **OAuth 2.0** - Secure X authentication
- **Read-only access** - Safe analytics queries
- **Data encryption** - Secure transmission

## Related MCP Servers

- [Facebook Ads MCP](https://insightfulpipe.com/mcp-servers/facebook-ads) - Social advertising
- [TikTok Ads MCP](https://insightfulpipe.com/mcp-servers/tiktok-ads) - Video advertising
- [LinkedIn Ads MCP](https://insightfulpipe.com/mcp-servers/linkedin-ads) - Professional social

## Resources

- [Documentation](https://insightfulpipe.com/docs/x-ads)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blogs)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **Email**: support@insightfulpipe.com

## License

MIT License - see [LICENSE](LICENSE) for details.
