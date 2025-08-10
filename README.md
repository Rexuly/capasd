# Discord Key Management System

A comprehensive key authentication system with Discord bot integration, hardware ID binding, expiration dates, and advanced admin management.

## Features

### 🔑 Key Management
- Cryptographically secure key generation
- Hardware ID binding for device-specific activation
- Key expiration and usage limits
- Multi-use key support with usage tracking
- Comprehensive key lifecycle management

### 🤖 Discord Integration
- Discord bot with slash commands (`/redeem`, `/status`)
- Real-time webhook notifications
- Discord user tracking and activity logs
- Direct key redemption through Discord

### 🛡️ Security & Authentication
- JWT-based admin authentication
- Bcrypt password hashing
- Hardware fingerprinting for key binding
- Session management with secure cookies

### 📊 Admin Dashboard
- Advanced admin panel with authentication
- Real-time statistics and analytics
- Discord activity monitoring
- Key creation and management tools
- User activity logging

## Quick Start

### Prerequisites
- Node.js 18 or later
- PostgreSQL database (or use in-memory storage)

### Installation

1. Clone the repository and install dependencies:
```bash
npm install
```

2. Set up environment variables:
```bash
cp .env.example .env
```

3. Configure your environment variables (see Configuration section below)

4. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5000`

## Configuration

### Required Environment Variables

```env
# Database (Optional - uses in-memory storage if not provided)
DATABASE_URL=postgresql://username:password@localhost:5432/keymanagement

# JWT Secret (Change in production)
JWT_SECRET=your-super-secret-jwt-key-change-in-production

# Discord Bot Configuration (Optional)
DISCORD_BOT_TOKEN=your_discord_bot_token
DISCORD_GUILD_ID=your_discord_server_id
DISCORD_WEBHOOK_URL=your_discord_webhook_url
```

### Discord Bot Setup

1. **Create a Discord Application:**
   - Go to https://discord.com/developers/applications
   - Click "New Application" and give it a name
   - Navigate to the "Bot" section and create a bot
   - Copy the bot token for `DISCORD_BOT_TOKEN`

2. **Set Bot Permissions:**
   - In the Bot section, enable the following permissions:
     - Send Messages
     - Use Slash Commands
     - Read Message History
   - Generate an OAuth2 URL with these permissions and add the bot to your server

3. **Create a Webhook (Optional):**
   - In your Discord server, go to Server Settings > Integrations > Webhooks
   - Create a new webhook and copy the URL for `DISCORD_WEBHOOK_URL`

4. **Get Guild ID:**
   - Enable Developer Mode in Discord (User Settings > Advanced > Developer Mode)
   - Right-click your server and select "Copy ID" for `DISCORD_GUILD_ID`

## Usage

### Admin Access

Default admin credentials:
- **Username:** `admin`
- **Password:** `admin123`

**⚠️ Important:** Change these credentials immediately after first login!

### Discord Commands

Once the bot is set up, users can interact with it using:

- `/redeem <key>` - Redeem an activation key
- `/status` - Check your key redemption status

### API Endpoints

The system provides RESTful API endpoints:

#### Public Endpoints
- `POST /api/redeem` - Redeem a key
- `GET /api/hardware-id` - Get hardware ID for current system

#### Admin Endpoints (Requires Authentication)
- `POST /api/login` - Admin login
- `GET /api/admin/keys` - List all keys
- `POST /api/admin/keys` - Create a new key
- `DELETE /api/admin/keys/:id` - Delete a key
- `GET /api/admin/stats` - Get system statistics
- `GET /api/admin/discord-logs` - Get Discord activity logs

## Development

### Project Structure

```
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Page components
│   │   └── lib/           # Utilities and configurations
├── server/                 # Express backend
│   ├── discord/           # Discord bot implementation
│   ├── middleware/        # Authentication middleware
│   └── lib/              # Server utilities
├── shared/                # Shared types and schemas
└── README.md
```

### Tech Stack

**Frontend:**
- React with TypeScript
- Vite for build tooling
- TanStack Query for data fetching
- Shadcn/ui components with Tailwind CSS
- Wouter for routing

**Backend:**
- Express.js with TypeScript
- Drizzle ORM with PostgreSQL
- Discord.js for bot functionality
- JWT for authentication
- Bcrypt for password hashing

### Building for Production

1. Build the application:
```bash
npm run build
```

2. Start the production server:
```bash
npm start
```

## Key Features in Detail

### Hardware ID Binding
Keys are bound to specific hardware configurations using a fingerprinting system that combines:
- System platform and architecture
- Hardware specifications
- Browser/client characteristics (for web usage)
- Discord user ID (for Discord redemptions)

### Discord Integration Benefits
- **Seamless User Experience:** Users can redeem keys directly in Discord
- **Real-time Notifications:** Admins get instant webhook notifications
- **Activity Tracking:** Complete audit trail of Discord interactions
- **User Management:** Track which Discord users have redeemed keys

### Security Features
- **JWT Authentication:** Secure admin access with token-based auth
- **Password Hashing:** Bcrypt with salt rounds for secure password storage
- **Hardware Validation:** Prevents key sharing across different devices
- **Session Management:** Secure session handling with HttpOnly cookies

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support and questions:
1. Check the documentation above
2. Review the Discord bot setup guide
3. Ensure all environment variables are properly configured
4. Check the console for any error messages

---

**Note:** This system is designed for legitimate software licensing and key management purposes. Ensure compliance with applicable laws and Discord's Terms of Service when deploying.