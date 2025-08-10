# Captha Lua Key Redeem System

## Project Overview
An advanced offline key authentication system with hardware ID binding, expiration dates, and comprehensive admin management. Rebranded from "Discord Key Management System" to "Captha Lua Key Redeem" with Discord-inspired dark theme.

## Current Status
✅ **COMPLETED**: Full system rebrand and feature implementation
- Dark Discord-style theme with #785fd3 primary color
- Key renewal functionality in admin panel
- Injection code display
- Complete UI redesign with proper color theming
- Admin login system (admin/admin123)

## User Preferences
- **Theme**: Dark Discord-inspired color scheme
- **Primary Color**: #785fd3 (purple)
- **Admin Access**: Single sign-in option only
- **Features**: Key renewal, injection tracking, email invites for users
- **Branding**: "Captha Lua Key Redeem"

## Project Architecture

### Frontend (React + Vite)
- **Pages**: User view, Admin view, Login, Not found
- **Theme**: Dark mode with Discord-like colors
- **Components**: UI components from shadcn/ui with custom theming
- **State**: TanStack Query for data management
- **Styling**: Tailwind CSS with custom CSS variables

### Backend (Express + TypeScript)  
- **Database**: PostgreSQL with Drizzle ORM
- **Authentication**: JWT-based admin authentication
- **Discord Integration**: Bot and webhook notifications
- **API Routes**: Full CRUD operations for keys and admin management

### Key Features Implemented
1. **Admin Panel**: 
   - Create, delete, and renew keys
   - View comprehensive statistics
   - Monitor Discord integrations
   - Track hardware bindings

2. **Key Management**:
   - Hardware ID binding
   - Expiration date management
   - Key renewal system
   - Usage tracking

3. **Discord Integration**:
   - Bot notifications
   - Webhook alerts
   - User tracking
   - Real-time activity logs

4. **Security**:
   - JWT authentication
   - Hardware binding
   - Secure key generation
   - Admin access control

## Recent Changes
- **2025-01-10**: Complete system rebrand to "Captha Lua Key Redeem"
- **2025-01-10**: Implemented dark Discord theme with #785fd3 color
- **2025-01-10**: Added key renewal functionality to admin panel
- **2025-01-10**: Added injection code display in admin interface
- **2025-01-10**: Updated all UI components to use dark theme colors
- **2025-01-10**: Enhanced admin dashboard with proper color theming
- **2025-01-10**: Added real-time key status display showing days remaining
- **2025-01-10**: Implemented Discord user connection during key redemption
- **2025-01-10**: Added user status API endpoint for key tracking
- **2025-01-10**: Enhanced user interface with active key details display
- **2025-01-10**: Extended Discord bot system to support Python programming language
- **2025-01-10**: Added language selection in Discord bot editor (JavaScript/TypeScript and Python)
- **2025-01-10**: Updated bot code templates with Python examples including discord.py commands
- **2025-01-10**: Added language badges to distinguish between JavaScript and Python bots
- **2025-01-10**: Enhanced deployment system to handle multi-language bot deployments

## Configuration

### Admin Credentials (Default)
```
Username: admin
Password: admin123
```
**⚠️ IMPORTANT: Change immediately after first login**

### Discord Configuration
Environment variables required:
- `DISCORD_BOT_TOKEN`: Discord bot token
- `DISCORD_GUILD_ID`: Discord server ID  
- `DISCORD_WEBHOOK_URL`: Webhook URL for notifications
- `DISCORD_CHANNEL_ID`: Channel ID for bot messages

### Injection Code
```lua
MachoIsolatedInject(MachoWebRequest("https://raw.githubusercontent.com/33qb643trgjiewog-903/532regdfs8923dfg/main/CapTha_protected.lua"))
```

## Development Guidelines
- Follow modern React patterns with TypeScript
- Use TanStack Query for API calls
- Maintain dark theme consistency
- Use shadcn/ui components with custom theming
- Ensure proper error handling and loading states

## Deployment
- System ready for production deployment
- Environment variables must be configured
- Database migrations handled by Drizzle
- Discord integration optional but recommended

## Support Features
- Real-time key status monitoring
- Hardware ID tracking and binding
- Discord user identification
- Comprehensive admin dashboard
- Key renewal and extension system
- Automated Discord notifications

The system is fully operational and ready for use with all requested features implemented.