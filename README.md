# ⚡ NIP-05 Verification Service

**Get a verified checkmark on Nostr. No coding. No DNS. Just 10,000 sats.**

---

## 🌐 Live Services

| Service | URL |
|---------|-----|
| **Landing Page** | https://hiftyco.github.io/OllieAI-NIP-05-VerificationAsService/ |
| **NIP-05 Endpoint** | https://hiftyco.github.io/.well-known/nostr.json |
| **Verification Checker** | https://hiftyco.github.io/OllieAI-NIP-05-VerificationAsService/check.html |

---

## ✅ How It Works

1. **DM on Nostr** with your desired username + npub
2. **Send 10,000 sats** to `paradigmtech21@coinos.io`
3. **We verify you instantly** - your checkmark appears! ✅

---

## 💰 Pricing

| Service | Price | Description |
|---------|-------|-------------|
| **Full Hosting** | 10,000 sats | We host your NIP-05. Example: `you@hiftyco.github.io` |
| **Custom Domain** | 50,000 sats | Your own subdomain. Example: `you@yourbrand.com` |

---

## 🎯 Why Get Verified?

- ✅ **Proves you're real** - No more "is this really you?"
- ✅ **Builds trust** - Clients know they're dealing with the real you
- ✅ **Instant setup** - No DNS, no coding, no headaches
- ✅ **Works everywhere** - Primal, Damus, Iris, all Nostr clients

---

## 🔍 Check Verification

Enter any username to verify their NIP-05 status:

https://hiftyco.github.io/OllieAI-NIP-05-VerificationAsService/

---

## ✅ Verified Users

Currently verified on this endpoint:

| Username | NIP-05 ID |
|----------|-----------|
| hiftyco | hiftyco@hiftyco.github.io |
| OllieAI | OllieAI@hiftyco.github.io |

---

## 🔧 For Developers

### Endpoints

- **NIP-05 JSON**: `https://hiftyco.github.io/.well-known/nostr.json`
- **Format**: Standard NIP-05 JSON with `names` object

### Adding Users (Automated)

```bash
python3 scripts/verify_user.py <username> <pubkey>
```

### Manual GitHub Update

1. Edit `nostr.json` in `hiftyco/.well-known` repo
2. Add username → pubkey mapping
3. GitHub Pages auto-deploys

---

## 📡 NIP-05 Specification

This service follows [NIP-05](https://github.com/nostr-protocol/nips/blob/master/05.md):

```json
{
  "names": {
    "username": "hex_pubkey"
  }
}
```

Hosted at: `https://hiftyco.github.io/.well-known/nostr.json`

---

## 💬 Contact

- **Nostr**: npub1a3lz855htm20sfcd0y2hp38e4h2akrqjj92spvruw8ge9yslrgws4x8vth
- **Payment**: paradigmtech21@coinos.io

---

## 📜 License

MIT - Use freely, modify as needed.

---

*Powered by Nostr • The decentralized social network*
