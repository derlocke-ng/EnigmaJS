# 🔐 EnigmaJS

**Secure peer-to-peer encrypted chat** - No servers, no data storage, complete privacy.

EnigmaJS is a web-based encrypted messaging app that connects users directly through a decentralized network. All messages are end-to-end encrypted, and nothing is stored anywhere - your conversations stay completely private.

## ✨ Key Features

- **🔒 End-to-End Encryption** - Messages are encrypted using Gun.js SEA cryptographic library
- **🌐 Peer-to-Peer** - Direct connections between users via Gun.js decentralized network
- **🚫 No Data Storage** - Nothing is saved on servers or your device
- **📱 QR Code Connect** - Quickly join rooms by scanning a QR code
- **🎨 Light & Dark Mode** - Switch between themes with one click
- **👥 Multi-User Rooms** - Chat with up to 10 users simultaneously
- **🎯 Simple Setup** - Just open the file in your browser and start chatting

## 🚀 Getting Started

### Opening the App

1. Download or clone this repository
2. Open `index.html` in any modern web browser (Chrome, Firefox, Safari, Edge)
3. That's it! No installation or setup required

### First Time Setup

1. **Enter Your Display Name** - Choose any name you want others to see
2. **Choose Your Mode** - Host a new chat room or join an existing one

## 🏠 Host Mode - Creating a Chat Room

1. Click **"Host Connection"** after entering your name
2. You'll see:
   - Your unique **Room ID** (e.g., FIRE-3K7-WXYZ)
   - A **QR code** for easy sharing
3. Share the Room ID or QR code with others
4. Wait for people to join - you'll see them appear in the user list
5. Start chatting once connected!

### Host Controls

As the host, you have special privileges:
- **Kick Users** - Remove disruptive users from the room
- **Promote Users** - Transfer host privileges to another user

## 📱 Join Mode - Joining a Chat Room

You have three ways to join:

### Option 1: Manual Entry
1. Click **"Join Connection"**
2. Paste the **Room ID** you received from the host
3. Click **"Connect"**

### Option 2: Scan QR Code with Camera
1. Click **"Scan with Camera"**
2. Point your camera at the host's QR code
3. You'll connect automatically when detected

### Option 3: Upload QR Code Image
1. Click **"Upload QR Image"**
2. Select a screenshot or photo of the QR code
3. Connect automatically if the QR code is recognized

## 💬 Using the Chat

- **Sending Messages** - Type in the message box and press Enter or click "Send"
- **Colored Messages** - Each user has a unique color for easy identification
- **User List** - See everyone in the room with their display names
- **Scroll Button** - Quickly jump to the latest messages

## 🔒 Security & Privacy

- **End-to-End Encryption** - All messages are encrypted before leaving your device
- **No Server Storage** - Messages only exist in active sessions, nothing is saved
- **Peer-to-Peer Network** - Direct connections via Gun.js decentralized relay network
- **Ephemeral Rooms** - Rooms disappear when everyone leaves
- **No Registration** - No accounts, emails, or personal data required

## 🐛 Troubleshooting

### Can't Connect?
- Check your internet connection
- Try refreshing the page
- Make sure you're using a modern browser
- Check if the Room ID is correct (no extra spaces)

### Camera Not Working?
- Grant camera permissions when prompted
- Try uploading a QR code image instead
- Check browser settings for camera access

### Messages Not Appearing?
- Verify you're connected (status shows "✅ Connected!")
- Check the debug logs (expand "Debug Info & Logs")
- Try refreshing and reconnecting

### QR Code Not Scanning?
- Ensure good lighting on the QR code
- Hold camera steady and at proper distance
- Try uploading a screenshot instead

## 🔧 Debug Mode

Need more details? Click **"Debug Info & Logs"** at the bottom to see:
- Connection status and role (Host/Client)
- Number of connected users
- Message count
- Detailed logs (enable "Verbose Logging" for more)

## 💡 Tips

- **Stable Connection** - Keep the browser tab open while chatting
- **Room Capacity** - Maximum 10 users per room
- **Privacy First** - Close the tab to destroy the conversation completely
- **Dark Mode** - Click the moon/sun icon in the top right corner

---

**Ready to chat?** Just open `index.html` and start your secure conversation! 🚀
