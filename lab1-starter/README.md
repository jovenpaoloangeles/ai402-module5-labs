---
title: Memo Router
emoji: 📨
colorFrom: blue
colorTo: gray
sdk: static
app_file: index.html
short_description: AI 402 Lab 1, routes memos to divisions
pinned: false
---

# Memo router (AI 402 Module 5, Lab 1)

Paste a memo; the page names the division (HR, Finance, Procurement, Records) by comparing it with the
example memos in `memos.txt` using `all-MiniLM-L6-v2`, and says "Not sure" below a match score of 0.35.
All memos are synthetic. The model runs in your browser with transformers.js; this Space only serves files.

Files: `index.html` (the page), `classify.js` (the logic), `memos.txt` (the examples).
Change `memos.txt` or `THRESHOLD` to change behaviour.
