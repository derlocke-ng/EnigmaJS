# EnigmaJS Changelog

## [2.0.0] - 2026-01-17 - Vue.js Migration

### 🚀 Major Rewrite

Complete migration from vanilla HTML/JS to Vue 3 with modern tooling.

### Architecture Changes

- **Vue 3 Composition API** - Modern reactive framework with `<script setup>`
- **Vite Build System** - Fast HMR development and optimized production builds
- **Pinia State Management** - Centralized store for app state
- **Component-Based Architecture** - Modular, reusable UI components
- **Composables** - `useEnigma` and `useQRScanner` for reusable logic

### New Features

#### Room Management

- ✨ **Public/Private Rooms** - Toggle room visibility with public room listing
- ✨ **Room Passwords** - Optional PIN protection for rooms
- ✨ **Configurable Room Size** - Set max users (2-256)
- ✨ **Host Migration** - Transfer host role to another user
- ✨ **Destroy Room** - Host can kick all users and close room
- ✨ **Auto-Promote** - Automatic host promotion when host leaves

#### Sharing & Connectivity

- ✨ **Share Link Button** - Copy room invite link to clipboard
- ✨ **QR Code Scanner** - Scan QR codes to join rooms (mobile-friendly)
- ✨ **10 Gun.js Relays** - Multiple public relays for better connectivity
- ✨ **Network Quality Indicator** - Real-time latency monitoring with signal bars
- ✨ **Keep-Alive** - Background ping to maintain connections on locked phones

#### User Experience

- ✨ **Browser Notifications** - Get notified of new messages when tab is inactive
- ✨ **Notification Sounds** - Audio alert for incoming messages
- ✨ **Message Timestamps** - See when each message was sent
- ✨ **User Colors** - Unique colors for each participant
- ✨ **User List Panel** - See all connected users with kick option for hosts
- ✨ **Auto-Scroll** - Smart scroll with "jump to bottom" button
- ✨ **Dark/Light Theme** - Toggle between themes

#### Error Handling

- ✨ **Error Toast Notifications** - User-friendly error messages
- ✨ **Connection Status** - Clear visual feedback for connection state
- ✨ **Better Error Messages** - Descriptive errors for connection failures

### Components Created

- `App.vue` - Main application container
- `AppHeader.vue` - Header with theme toggle and network indicator
- `UsernameSetup.vue` - Initial username entry
- `ModeSelector.vue` - Host/Join mode selection
- `ChatRoom.vue` - Main chat interface with settings panel
- `ChatMessages.vue` - Message list with auto-scroll
- `UserList.vue` - Connected users sidebar
- `StatusBadge.vue` - Connection status indicator
- `NetworkIndicator.vue` - Latency and signal quality
- `QRScanner.vue` - Camera-based QR code scanner
- `PublicRoomList.vue` - Browse and join public rooms
- `DebugPanel.vue` - Developer debugging tools

### Technical Improvements

- **HTTPS Development** - SSL enabled for camera/notification APIs
- **Modular Code** - EnigmaJS core extracted to reusable ES module
- **Reactive State** - All UI automatically updates on state changes
- **Clean Lifecycle** - Proper cleanup of Gun.js listeners and intervals
- **Error Boundaries** - Graceful error handling throughout

### Security

- 🔒 E2E encryption maintained (ECDH + AES-GCM)
- 🔒 No message persistence - ephemeral by design
- 🔒 Room passwords hashed before transmission
- 🔒 Cryptographically secure random for all keys

---

## [1.0.0] - Original Release

### Features

- Single-file HTML application (`index.html`)
- E2E encrypted P2P chat over Gun.js
- QR code room sharing
- Basic host/join functionality
- Dark mode support
- Verbose logging toggle
