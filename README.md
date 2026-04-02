# NIP-05 Verification Service

A fully automated NIP-05 verification service for Nostr.

## 🌐 Live Site

Access the landing page at: **https://nip05.hifty.co**

## 📋 Setup Instructions

### 1. GitHub Repository Setup

```bash
# Create a new GitHub repo called "nip05-verified" (or similar)
# Clone it locally and copy these files:

git clone https://github.com/YOUR_USERNAME/nip05-verified.git
cd nip05-verified

# Copy the contents of nip05_github/ into this repo:
cp -r /home/node/.openclaw/nip05_github/* .
cp -r /home/node/.openclaw/nip05_github/.* . 2>/dev/null

# Push to GitHub
git add .
git commit -m "Initial NIP-05 service setup"
git push
```

### 2. Enable GitHub Pages

1. Go to repo Settings → Pages
2. Source: Deploy from branch `main`
3. Folder: `/ (root)`
4. Click Save

Your site will be live at: `https://YOUR_USERNAME.github.io/nip05-verified`

Or custom domain: `https://nip05.YOURDOMAIN.com`

### 3. Configure GitHub Token

Add these secrets to your GitHub repo (Settings → Secrets):

- `GH_TOKEN` - Personal access token with `repo` scope

### 4. Set Up Local Environment

```bash
export GITHUB_TOKEN="your_github_token"
export GITHUB_REPO="your_username/nip05-verified"
export GITHUB_BRANCH="main"
```

## 🔄 How It Works

```
Client DMs on Nostr
        ↓
Generates NIP-05 record
        ↓
Client pays 10k-50k sats to paradigmtech21@coinos.io
        ↓
auto_nip05_payment_listener.py detects payment
        ↓
Adds to nostr.json + index.html
        ↓
Pushes to GitHub
        ↓
GitHub Pages serves updated nostr.json
        ↓
Client is VERIFIED! ✅
```

## ⚡ Commands

```bash
# Check status
python3 auto_nip05_payment_listener.py status

# Manually verify a client (after payment)
python3 auto_nip05_payment_listener.py verify <username> <pubkey>

# Check payments
python3 auto_nip05_payment_listener.py check
```

## 📁 File Structure

```
nip05-verified/
├── index.html          # Landing page
├── index.md            # GitHub Pages source
├── .well-known/
│   └── nostr.json      # NIP-05 records (served via Pages)
├── _includes/          # Jekyll includes
├── assets/             # CSS, JS, images
└── .github/
    └── workflows/
        └── update.yml   # GitHub Actions
```

## 💰 Pricing

| Service | Price |
|---------|-------|
| Basic Setup | 10,000 sats |
| Full Hosting | 50,000 sats |

## 🔒 Security

- Payment is verified BEFORE adding to nostr.json
- GitHub token required for automatic updates
- All client data stored locally in `nip05_clients/`

## 🤖 Automation

The `auto_nip05_payment_listener.py` script:
1. Runs via cron every 15 minutes
2. Checks NWC balance for incoming payments
3. When payment detected, auto-adds to verified
4. Pushes to GitHub and deploys

Add to crontab:
```bash
*/15 * * * * cd /home/node/.openclaw/workspace && python3 auto_nip05_payment_listener.py check >> logs/nip05.log 2>&1
```

## 📞 Contact

Nostr: `npub1a3lz855htm20sfcd0y2hp38e4h2akrqjj92spvruw8ge9yslrgws4x8vth`
Payment: `paradigmtech21@coinos.io`
