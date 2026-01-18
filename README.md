# 🔐 EnigmaJS

**Ephemeral • End-to-End Encrypted • Decentralized Chat**

A private chat application where conversations disappear when the room closes. No servers store your messages. No accounts required.

---

## ✨ What Makes EnigmaJS Different

### 🔥 Truly Ephemeral

Messages exist **only during the active session**. When the host closes the room or everyone leaves, the conversation is gone forever. There's no chat history to leak, no database to breach, no logs to subpoena. The encryption keys are generated fresh for each room and discarded when the room ends.

### 🔐 End-to-End Encrypted

Every message is encrypted **before it leaves your device** using [Gun SEA](https://gun.eco/docs/SEA) (Security, Encryption, Authorization). Messages travel through relay servers as encrypted blobs - the relays cannot read them. Only participants who received the room's encryption key can decrypt the conversation.

### 🌐 Decentralized Architecture

EnigmaJS uses [Gun.js](https://gun.eco/), a decentralized database protocol. Messages sync through multiple public relay servers - if one goes down, others keep working. There's no single point of failure and no central authority controlling access.

### 👤 No Registration Required

No accounts. No emails. No phone numbers. No tracking. Just:

1. Create a room → Get a code
2. Share the code → Friends join
3. Chat → Messages stay between you
4. Leave → Everything disappears

---

## 🛡️ Honest Security Notes

**What we do:**

- Generate unique encryption keys per room using cryptographically secure randomness
- Encrypt all messages client-side before transmission
- Use ECDH key exchange (via Gun SEA) to securely share room keys with new joiners
- Store nothing persistently - all data lives in memory only

**What we don't do:**

- We don't protect against compromised devices (if someone's watching your screen, they see your messages)
- We don't guarantee message delivery (decentralized systems can have sync delays)
- We don't prevent screenshots or copy/paste
- We can't verify the identity of who you're talking to (share room codes through trusted channels)

**The relays:**
Gun.js relay servers see encrypted message blobs pass through. They cannot decrypt them. However, they could theoretically log metadata (timestamps, IP addresses, message sizes). For maximum privacy, you can [run your own Gun relay](https://gun.eco/docs/Installation) or use a VPN or run it over Tor.

---

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build
```

---

## 🔧 How It Works

1. **Host creates room** → Generates room ID + encryption key
2. **Host shares room ID** → Via QR code, copy/paste, or link
3. **Guest joins** → Sends join request with their public key
4. **Host approves** → Encrypts room key with guest's public key, sends welcome
5. **Secure channel established** → All messages encrypted with shared room key
6. **Room closes** → Keys discarded, messages become permanently unrecoverable

---

## 📝 License

MIT - Use it, modify it, host it yourself.

---

_Built with Vue 3, Vite, Gun.js, and a commitment to privacy._
