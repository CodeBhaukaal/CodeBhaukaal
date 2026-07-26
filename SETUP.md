# Setup — GitHub Profile README

## ज़रूरी बात
यह README तभी आपकी profile पर दिखेगा जब repo का नाम **बिल्कुल आपके username जैसा** हो:
`CodeBhaukaal/CodeBhaukaal` (public + README.md root में)।

## Steps

1. GitHub पर नया **public** repo बनाएँ जिसका नाम हो: `CodeBhaukaal`
   (GitHub खुद बोलेगा: "You found a secret! CodeBhaukaal/CodeBhaukaal is a special repository ✨")

2. इस फोल्डर से push करें:

```bash
git init
git add .
git commit -m "feat: modern profile README with stats and graphs"
git branch -M main
git remote add origin https://github.com/CodeBhaukaal/CodeBhaukaal.git
git push -u origin main
```

3. **Snake animation चालू करने के लिए** (एक बार करना है):
   - repo → **Settings → Actions → General → Workflow permissions**
   - `Read and write permissions` select करें → Save
   - फिर repo → **Actions** tab → `Generate Contribution Snake` → **Run workflow**
   - 1 मिनट बाद `output` branch बन जाएगी और snake README में दिखने लगेगा।

## Private contributions भी count कराने हों?
Profile → Settings → Public profile → ✅ *Include private contributions on my profile*

## बदलने लायक चीज़ें (README.md में)
- **Line ~205 के आसपास**: LinkedIn / Discord / Telegram के `href="#"` को अपने असली link से बदल दें
- **Theme**: सब cards में `theme=tokyonight` है। पसंद न आए तो बदलें —
  `radical`, `dracula`, `catppuccin_mocha`, `gruvbox`, `merko`, `nightowl`
- **Banner colors**: `capsule-render` वाले URL में `color=0:0f2027,50:203a43,100:2c5364` बदलें
- **Featured projects**: pin cards में `repo=` की value बदलकर कोई और repo लगा सकते हैं

## अगर stats card "Maximum retries exceeded" दिखाए
`github-readme-stats` का public instance rate-limited है। ठीक करने के लिए अपना Vercel instance
deploy करें: https://github.com/anuraghazra/github-readme-stats#deploy-on-your-own-vercel-instance
फिर README में `github-readme-stats.vercel.app` को अपने domain से replace कर दें।
