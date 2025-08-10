# Discord Configuration Guide for Captha Lua Key Redeem

## Overview
Your Captha Lua Key Redeem system is now fully configured with Discord integration and dark theme. This guide provides all the setup information and login credentials.

## 🔐 Admin Login Credentials
```
Username: admin
Password: admin123
```

**⚠️ IMPORTANT: Change these credentials immediately after first login!**

## 🎨 Theme & Colors
- **Primary Color**: #785fd3 (Discord-like purple)
- **Theme**: Dark Discord-inspired theme
- **Color Scheme**: Dark backgrounds with purple accents

## 🤖 Discord Bot & Webhook Configuration

### Environment Variables
Add these to your `.env` file or environment variables:

```bash
# Discord Bot Configuration (Optional)
DISCORD_BOT_TOKEN=your_discord_bot_token_here
DISCORD_GUILD_ID=your_discord_server_id_here
DISCORD_WEBHOOK_URL=your_discord_webhook_url_here
DISCORD_CHANNEL_ID=your_discord_channel_id_here

# JWT Secret (Change in production)
JWT_SECRET=your-super-secret-jwt-key-change-in-production
```

### Getting Discord Bot Token
1. Go to https://discord.com/developers/applications
2. Create a new application
3. Go to the "Bot" section
4. Create a bot and copy the token
5. Add the token to `DISCORD_BOT_TOKEN`

### Getting Discord Guild (Server) ID
1. Enable Developer Mode in Discord settings
2. Right-click your server name
3. Select "Copy Server ID"
4. Add this ID to `DISCORD_GUILD_ID`

### Getting Discord Webhook URL
1. In your Discord server, go to Server Settings > Integrations
2. Create a new webhook
3. Copy the webhook URL
4. Add it to `DISCORD_WEBHOOK_URL`

### Getting Discord Channel ID
1. Enable Developer Mode in Discord settings
2. Right-click the channel where you want notifications
3. Select "Copy Channel ID"
4. Add this ID to `DISCORD_CHANNEL_ID`

## 🔑 Key Management Features

### Admin Panel Access
- Navigate to the admin panel using the "Admin Panel" button
- Login with the credentials above
- Access all key management features

### Key Renewal
- Click the sync (🔄) icon next to any key in the table
- Select a new expiration date
- Keys can be renewed multiple times

### Injection Code
The injection code for users is displayed in the admin panel:
```lua
MachoIsolatedInject(MachoWebRequest("https://raw.githubusercontent.com/33qb643trgjiewog-903/532regdfs8923dfg/main/CapTha_protected.lua"))
```

### Key Features
- **Create Keys**: Generate new activation keys with custom expiration dates
- **Renew Keys**: Extend expiration dates for existing keys
- **Hardware Binding**: Keys bind to specific hardware IDs
- **Discord Integration**: Track which Discord users redeemed keys
- **Real-time Stats**: Monitor key usage and status
- **Discord Notifications**: Get notified when keys are created, redeemed, or deleted

## 🔧 System Features
- Dark theme with Discord-like appearance
- Real-time key status tracking
- Hardware ID binding and monitoring
- Discord user tracking
- Comprehensive admin dashboard
- Key renewal system
- Injection code display

## 📊 Dashboard Statistics
The admin panel displays:
- Total Keys created
- Active Keys (redeemed and not expired)
- Expired Keys
- Unused Keys (not yet redeemed)
- Discord Users (keys redeemed via Discord)

## 🚨 Security Notes
1. **Change default admin credentials immediately**
2. **Use strong JWT secret in production**
3. **Keep Discord bot token secure**
4. **Regularly monitor key usage**
5. **Review hardware bindings for suspicious activity**

## ✅ Next Steps
1. Update admin credentials
2. Configure Discord bot and webhooks
3. Test key creation and renewal
4. Monitor system activity
5. Distribute injection code to users

Your Captha Lua Key Redeem system is now fully operational with all requested features!