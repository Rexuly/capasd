# Captha Lua Key Redeem - Configuration Guide

## 🔧 Discord Configuration

### Where to Configure Discord Settings

#### 1. Environment Variables (Primary Method)
Create a `.env` file in your root directory with:

```bash
# Discord Bot Configuration
DISCORD_BOT_TOKEN=your_discord_bot_token_here
DISCORD_GUILD_ID=your_discord_server_id_here  
DISCORD_WEBHOOK_URL=your_discord_webhook_url_here
DISCORD_CHANNEL_ID=your_discord_channel_id_here

# System Settings
JWT_SECRET=your-super-secret-jwt-key-change-in-production
```

#### 2. Code Files for Discord Settings

**Bot Configuration:** `server/discord/bot.ts`
- Lines 8-13: Discord configuration interface
- Lines 15-30: Bot initialization
- Lines 51-75: Slash commands setup
- Lines 76-120: Key redemption handling

**Webhook Configuration:** `server/routes.ts`
- Lines 114-127: New key creation webhooks
- Lines 145-157: Key deletion webhooks
- Lines 180-192: Key renewal webhooks

**Discord Integration:** `server/index.ts`
- Lines 15-25: Bot initialization
- Environment variable reading

### 🤖 Setting Up Discord Bot

#### Step 1: Create Discord Application
1. Go to https://discord.com/developers/applications
2. Click "New Application" 
3. Name it "Captha Lua Key Redeem"
4. Go to "Bot" section → "Add Bot"
5. Copy the bot token → Add to `DISCORD_BOT_TOKEN`

#### Step 2: Get Server/Channel IDs
1. Enable Developer Mode in Discord Settings
2. Right-click your server → "Copy Server ID" → Add to `DISCORD_GUILD_ID`
3. Right-click target channel → "Copy Channel ID" → Add to `DISCORD_CHANNEL_ID`

#### Step 3: Create Webhook
1. Server Settings → Integrations → "Create Webhook"
2. Choose channel and copy webhook URL
3. Add URL to `DISCORD_WEBHOOK_URL`

#### Step 4: Bot Permissions
Add these permissions when inviting bot:
- Send Messages
- Use Slash Commands  
- Read Message History
- Embed Links

## ⚙️ System Features Status

### ✅ Fully Working Features
- **Admin Panel**: Login, logout, dashboard
- **Key Management**: Create, delete, renew keys
- **Password Change**: Secure admin password updates
- **Username Change**: Admin username modification  
- **Dark Theme**: Complete Discord-inspired styling
- **Key Redemption**: User key activation system
- **Hardware Binding**: Machine-specific key binding
- **Discord Notifications**: Webhook alerts for key events

### 🔧 Available Discord Commands (When Bot Configured)
- `/redeem [key]`: Redeem activation key via Discord
- `/status`: Check user's key redemption status

### 📊 Admin Dashboard Features
- **Statistics Cards**: Total, active, expired, unused keys
- **Key Table**: Complete key management interface  
- **Discord Logs**: Track Discord-related activities
- **Injection Code Display**: Shows Lua injection code
- **Real-time Updates**: Live status monitoring

## 🎨 Theme Customization

### Primary Colors (in `client/src/index.css`)
- **Primary Color**: `hsl(258 64% 64%)` (#785fd3)
- **Background**: Dark Discord theme
- **Error Color**: `hsl(0 84% 65%)` (Red for errors)

### Key UI Files
- `client/src/index.css`: Theme colors and styling
- `client/src/pages/admin-view.tsx`: Admin interface
- `client/src/pages/user-view.tsx`: User redemption interface  
- `client/src/pages/login.tsx`: Login page styling

## 🔐 Security Configuration

### Admin Credentials
- **Default**: admin/admin123
- **Change via**: Admin Panel → "Change Username/Password" buttons
- **Storage**: In-memory (MemStorage) or PostgreSQL

### JWT Configuration
- **Secret**: Set `JWT_SECRET` environment variable
- **Location**: `server/routes.ts` lines 20-30
- **Token Expiration**: 24 hours (configurable)

## 📝 Injection Code
The Lua injection code displayed in admin panel:
```lua
MachoIsolatedInject(MachoWebRequest("https://raw.githubusercontent.com/33qb643trgjiewog-903/532regdfs8923dfg/main/CapTha_protected.lua"))
```

## 🚀 Production Deployment
1. Set all environment variables
2. Change default admin credentials
3. Use strong JWT secret
4. Configure Discord bot properly
5. Monitor system logs

## 📞 Support
- Configuration files: `.env.example`, `DISCORD_SETUP.md`
- All features tested and fully functional
- Dark theme implemented throughout
- Security measures in place