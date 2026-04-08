Simon Lee (李仲軒) — Personal Website

Head of Product | Web3 & DeFi | Cross-Regional Teams (50+) | 17+ Years Experience
Live site → https://skinnerlee1225.github.io

📋 About This Site

A modern, dark-themed personal portfolio website built from resume data.
Supports bilingual switching (English ↔ 繁體中文) with a one-click toggle.
When browsing locally, an extra 🤖 AI 翻譯 button appears that connects to your local Ollama model for AI-powered translation.

🌐 Features

Feature	Description
🌐 Language Toggle	Switch between English and Traditional Chinese instantly
🤖 AI Translate (Local)	Calls your local Ollama model — only shows when browsing locally
📱 Responsive	Fully mobile-friendly layout
⚡ Zero Dependencies	Pure HTML + CSS + JS, no frameworks required
🚀 GitHub Pages Ready	Single index.html file, deploy in minutes
🤖 Local AI Translation Setup

The 🤖 AI 翻譯 button appears automatically when you open the site locally (file:// or localhost).
It calls your local Ollama server to perform AI-powered translation.

Step 1 — Install Ollama

# macOS
brew install ollama

# or download from https://ollama.ai
Step 2 — Pull a model

# Recommended: llama3 (good Chinese support)
ollama pull llama3

# Alternatives with strong Chinese support:
# ollama pull qwen2       # Alibaba's model, excellent Chinese
# ollama pull mistral
Step 3 — Start Ollama

ollama serve
# Ollama runs at http://localhost:11434
Step 4 — Open the site locally

# In the project folder:
open index.html
# or serve with Python:
python3 -m http.server 8080
# then visit http://localhost:8080
Step 5 — Use AI Translate

The 🤖 AI 翻譯 button will now appear in the navigation bar.
Click it to translate the page using your local model.

Note: To change the model, edit this line in index.html:

model: 'llama3',   // ← change to 'qwen2', 'mistral', etc.
🚀 Deploying to GitHub Pages

First time setup:

Go to github.com → New repository
Name it exactly: skinnerlee1225.github.io
Set to Public → Create repository
Upload index.html and README.md
Go to Settings → Pages → Source: main branch → Save
Your site will be live at https://skinnerlee1225.github.io within 1–2 minutes.

Update the site:

# Clone the repo
git clone https://github.com/skinnerlee1225/skinnerlee1225.github.io
cd skinnerlee1225.github.io

# Edit index.html, then push
git add index.html
git commit -m "Update content"
git push origin main
📁 File Structure

skinnerlee1225.github.io/
├── index.html        # Main website (all-in-one: HTML + CSS + JS)
└── README.md         # This file
✏️ Customization Guide

All content is in index.html. Look for these sections:

Section	What to edit
#hero	Name, title, stats, CTA buttons
#about	Bio paragraphs, personal info card
#competencies	5 core competency cards
#experience	Work history timeline (.tl-item)
#skills	Skill chips and tool tags
#projects	Project cards (.proj-card)
#education	Education and certifications
#contact	Contact links
Each section has both English and Chinese versions using data-lang="en" and data-lang="zh" attributes.

Example — editing bilingual text:

<h3 data-lang="en">Your English Title</h3>
<h3 data-lang="zh">您的中文標題</h3>
🛠 Tech Stack

HTML5 — semantic markup
CSS3 — custom properties, grid, flexbox, animations
Vanilla JavaScript — language toggle, Ollama API integration
Google Fonts — Inter + Space Grotesk
Ollama API — local AI model for dynamic translation (optional)
📄 License

Personal use only. Content belongs to Simon Lee (李仲軒).

Built with ❤️ · Hosted on GitHub Pages
