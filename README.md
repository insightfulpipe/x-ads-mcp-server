# X Ads MCP Server (Twitter Ads) by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/x-ads)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect X Ads (formerly Twitter Ads) to AI assistants for real-time social advertising analytics.**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — The X Ads MCP server enables Claude, ChatGPT, Cursor, and other AI assistants to analyze your X advertising campaigns. Track promoted tweets, monitor engagement, and get AI-powered recommendations.

[![Explore All MCP Servers](https://img.shields.io/badge/Explore_All-MCP_Servers-blue?style=for-the-badge)](https://insightfulpipe.com/mcp-servers)

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

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://x-ads.insightfulmcp.com/`
3. Authorize with your InsightfulPipe account

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http x-ads https://x-ads.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "x-ads": {
      "url": "https://x-ads.insightfulmcp.com/"
    }
  }
}
```

Then authorize the connection when Cursor prompts you.

## Available Actions

80 actions: 53 read, 27 write.

### Read Actions (53)

<details>
<summary>Show all 53 read actions</summary>

| Action | Description |
|--------|-------------|
| `cancel_async_job` | Cancel a PROCESSING async analytics job |
| `create_async_job` | Create an async analytics job |
| `get_account` | Get details for a specific ad account |
| `get_account_history` | Retrieve a summary of changes made to a specific entity on the account |
| `get_account_media` | List account media assets associated with the current account |
| `get_account_media_item` | Get details for a specific account media object |
| `get_active_entities` | Get active entities (campaigns, line items, etc.) that had activity in a time range |
| `get_advertiser_business_categories` | Retrieve valid advertiser business categories for line items |
| `get_async_jobs` | Retrieve details for async analytics jobs |
| `get_authenticated_user_access` | Retrieve the permissions of the authenticated user for the current account |
| `get_campaign` | Get details for a specific campaign |
| `get_campaigns` | List all campaigns for an ad account |
| `get_card` | Get details for a specific card |
| `get_cards` | List cards associated with the current account |
| `get_content_categories` | Retrieve content categories for preroll video targeting |
| `get_features` | Retrieve features enabled for the current account |
| `get_funding_instrument` | Get details for a specific funding instrument |
| `get_funding_instruments` | List all funding instruments for an ad account |
| `get_iab_categories` | Retrieve IAB content categories |
| `get_line_item` | Get details for a specific line item |
| `get_line_items` | List all line items for an ad account |
| `get_media_creative` | Get details for a specific media creative |
| `get_media_creatives` | List all media creatives for an ad account |
| `get_media_library` | List media library objects associated with the current account |
| `get_media_library_item` | Get details for a specific media library object |
| `get_promotable_user` | Get details for a specific promotable user |
| `get_promotable_users` | List promotable users associated with the current account |
| `get_promoted_account` | Get details for a specific promoted account |
| `get_promoted_accounts` | List promoted accounts associated with line items under the current account |
| `get_promoted_tweet` | Get details for a specific promoted tweet |
| `get_promoted_tweets` | List promoted tweets associated with line items under the current account |
| `get_recommendations` | Retrieve campaign optimization recommendations for the account |
| `get_scheduled_promoted_tweet` | Get details for a specific scheduled promoted tweet |
| `get_scheduled_promoted_tweets` | List scheduled promoted tweets associated with the current account |
| `get_stats` | Retrieve synchronous analytics for an ad account |
| `get_targeting_app_store_categories` | Discover available app store category-based targeting criteria |
| `get_targeting_conversations` | Discover available conversation-based targeting criteria |
| `get_targeting_criteria` | List targeting criteria associated with line items under the current account |
| `get_targeting_criterion` | Get details for a specific targeting criterion |
| `get_targeting_devices` | Discover available device-based targeting criteria |
| `get_targeting_events` | Discover available event-based targeting criteria |
| `get_targeting_interests` | Discover available interest-based targeting criteria |
| `get_targeting_languages` | Discover available language targeting criteria |
| `get_targeting_locations` | Discover available location-based targeting criteria (countries, regions, cities, postal codes, metros) |
| `get_targeting_network_operators` | Discover available network operator (carrier) targeting criteria |
| `get_targeting_platform_versions` | Discover available mobile OS version-based targeting criteria |
| `get_targeting_platforms` | Discover available platform-based targeting criteria (iOS, Android, etc.) |
| `get_targeting_suggestions` | Get keyword or user targeting suggestions to complement your targeting selection |
| `get_targeting_tv_markets` | Discover available TV markets where TV shows can be targeted |
| `get_targeting_tv_shows` | Discover available TV show-based targeting criteria |
| `get_tax_settings` | Retrieve tax setting details for the current account |
| `get_tracking_tag` | Get details for a specific tracking tag |
| `get_tracking_tags` | List tracking tags associated with the current account |

</details>

### Write Actions (27)

<details>
<summary>Show all 27 write actions</summary>

| Action | Description |
|--------|-------------|
| `create_ad_tweet` | Create a promoted-only (nullcast) tweet for use in ad campaigns |
| `create_campaign` | Create a new campaign (created in PAUSED status for safety) |
| `create_card` | Create a card (website, app, or carousel) for use in tweets |
| `create_line_item` | Create a new line item (ad group) under a campaign (created in PAUSED status for safety) |
| `create_media_creative` | Create a media creative and associate it with a line item |
| `create_media_library_item` | Add a media asset to the account media library |
| `create_promoted_account` | Associate a user account with a line item as a promoted account |
| `create_promoted_tweet` | Associate tweets with a line item as promoted tweets |
| `create_scheduled_promoted_tweet` | Associate a scheduled tweet with a line item as a scheduled promoted tweet |
| `create_scheduled_tweet` | Create a scheduled tweet for future publishing |
| `create_targeting_criterion` | Create a targeting criterion for a line item |
| `create_tracking_tag` | Create a tracking tag for a line item |
| `delete_campaign` | Delete a campaign |
| `delete_card` | Delete a card |
| `delete_line_item` | Delete a line item |
| `delete_media_creative` | Delete a media creative |
| `delete_promoted_account` | Remove a promoted account association |
| `delete_promoted_tweet` | Remove a promoted tweet association |
| `delete_scheduled_promoted_tweet` | Remove a scheduled promoted tweet association |
| `delete_scheduled_tweet` | Delete a scheduled tweet |
| `delete_targeting_criterion` | Delete a targeting criterion |
| `delete_tracking_tag` | Delete a tracking tag |
| `update_campaign` | Update an existing campaign |
| `update_line_item` | Update an existing line item |
| `update_media_library_item` | Update a media library object's metadata |
| `update_tracking_tag` | Update an existing tracking tag |
| `upload_media` | Upload an image for use in ads |

</details>

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
- **Brand awareness** - Measure reach and engagement

### For Performance Marketers
- **Conversion tracking** - Website and app actions
- **Async analytics** - Handle large data ranges
- **Line item optimization** - Granular performance data

### For Agencies
- **Multi-account management** - Handle client portfolios
- **Automated reporting** - Generate engagement reports

## Security & Privacy

- **X Developer Platform** - Official API access
- **OAuth 2.0** - Secure X authentication
- **Data encryption** - Secure transmission

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers for marketing and analytics.

### Social Advertising MCP Servers
- [Facebook Ads MCP](https://insightfulpipe.com/mcp-servers/facebook-ads) - Social advertising
- [TikTok Ads MCP](https://insightfulpipe.com/mcp-servers/tiktok-ads) - Video advertising
- [LinkedIn Ads MCP](https://insightfulpipe.com/mcp-servers/linkedin-ads) - Professional social
- [Snapchat Ads MCP](https://insightfulpipe.com/mcp-servers/snapchat-ads) - Gen-Z advertising

### Search Advertising MCP Servers
- [Google Ads MCP](https://insightfulpipe.com/mcp-servers/google-ads) - Search advertising
- [Microsoft Ads MCP](https://insightfulpipe.com/mcp-servers/microsoft-ads) - Bing advertising

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs/connectors-x-ads)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
