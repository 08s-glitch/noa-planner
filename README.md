# My Planner ✨ — Netlify Deployment Guide

## What's in this folder

```
planner-deploy/
├── index.html                  ← The full app (mobile + desktop)
├── netlify.toml                ← Netlify config
└── netlify/
    └── functions/
        └── chat.js             ← Serverless function (handles AI securely)
```

## Deploy in 5 steps

### Step 1 — Go to Netlify
Open https://app.netlify.com and log in.

### Step 2 — Create a new site
Click **"Add new site"** → **"Deploy manually"**

### Step 3 — Drag and drop
Drag the entire `planner-deploy` folder onto the Netlify deploy area.
Wait about 30 seconds. Netlify will give you a URL like `random-name.netlify.app`.

### Step 4 — Add your Anthropic API key (makes AI work)
1. In your Netlify site dashboard, go to **Site settings** → **Environment variables**
2. Click **Add a variable**
3. Key: `ANTHROPIC_API_KEY`
4. Value: your Anthropic API key (starts with `sk-ant-...`)
5. Click **Save**
6. Go to **Deploys** → click **Trigger deploy** → **Deploy site**

### Step 5 — Give her the link
Share the `.netlify.app` URL with her. She can:
- Bookmark it on her phone (tap Share → Add to Home Screen for an app icon)
- Open it on any browser, any device
- Everything saves automatically to her browser

## Rename the site (optional)
In Netlify: **Site settings** → **Site details** → **Change site name**
e.g. `noa-planner.netlify.app`

## What works after deployment
✅ Full planner with monthly calendar + weekly schedule
✅ AI chat (type or voice) — reads her actual schedule
✅ Everything saves automatically (localStorage)
✅ Mobile layout (bottom tab nav, bottom sheet AI)
✅ Desktop layout (sidebar nav, floating AI panel)
✅ Responsive — auto-detects phone vs computer
✅ Jewish holidays pre-loaded
✅ Shabbat dinner blocked every Friday 7-7:45pm
✅ Battery bar that fills as she completes goals
✅ Confetti when she finishes everything

## Getting an Anthropic API key
If you don't have one yet:
1. Go to https://console.anthropic.com
2. Sign up / log in
3. Go to **API Keys** → **Create Key**
4. Copy the key and paste it into Netlify as shown in Step 4
