# NIP-05 Verification Service

Get your business verified on Nostr with a custom NIP-05 identifier.

## 🌐 Live Services

| Service | URL |
|---------|-----|
| Landing Page | https://hiftyco.github.io/OllieAI-NIP-05-VerificationAsService |
| Verification Checker | https://hiftyco.github.io/OllieAI-NIP-05-VerificationAsService/check.html |
| NIP-05 JSON (raw) | https://raw.githubusercontent.com/hiftyco/OllieAI-NIP-05-VerificationAsService/main/nostr.json |

## 🔧 Setup Cloudflare Pages (for .well-known support)

NIP-05 requires `/.well-known/nostr.json`. GitHub Pages doesn't serve dotfiles, so we use Cloudflare Pages:

1. Go to https://pages.cloudflare.com
2. Connect your GitHub repo: `hiftyco/OllieAI-NIP-05-VerificationAsService`
3. Set build command: leave empty
4. Set output directory: `/`
5. Enable **Preview deployments** for all branches
6. Custom domain: `nip05.hifty.co`

Cloudflare Pages serves dotfiles properly and auto-deploys when you push to GitHub!

## ✅ Verified Users

| Username | Domain |
|---------|--------|
| hifty | nip05.hifty.co |

## 💰 Pricing

- Basic Setup: 10,000 sats (you provide domain)
- Full Hosting: 50,000 sats (we host on nip05.hifty.co subdomain)
