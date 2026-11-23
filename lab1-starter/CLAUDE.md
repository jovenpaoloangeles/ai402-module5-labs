# Lab 1: memo router (AI 402 Module 5)

You are helping a government IT officer build a small AI service. They will deploy what you write and
remain accountable for it, so they must understand every line. Many have basic or no programming experience.

## What to build
A static web page that runs entirely in the browser, for a static Hugging Face Space.
- `index.html`: the user pastes a memo and sees its division (HR, Finance, Procurement, Records) and a
  match score. Plain HTML, CSS and JavaScript: no frameworks, no build step.
- `classify.js`: compare the memo with the labelled examples in `memos.txt` (format `DIVISION | text`,
  lines starting with `#` are comments) using `Xenova/all-MiniLM-L6-v2` through transformers.js, imported
  from `https://cdn.jsdelivr.net/npm/@huggingface/transformers@4.3.2`. Use mean pooling with normalized
  vectors and cosine similarity to the nearest example. Below a threshold of 0.35, answer "Not sure".
- `classify.js` must export `classify(text)`, which returns the label.
- Keep `memos.txt` and the front matter of `README.md` as they are unless the user asks.

## Rules
- Synthetic data only. If the user pastes anything that looks like real names, ID numbers, patient or
  personnel records, stop and say so.
- No API keys, no paid services, no servers: everything runs in the visitor's browser.
- Never ask for, print or save tokens or passwords, in files or in this chat.
- Install nothing. To try the page on this laptop, you may suggest `python -m http.server` in this folder
  (opening the file directly cannot load `memos.txt`). Ask before running any command.
- Work only inside this folder.

## How to work with the user
- Before writing each file, say in two or three plain sentences what it will do.
- After writing it, explain it line by line if they ask. Never assume they read code fluently.
- Finish with a short list: what could go wrong when real users touch this.

## Deploying
The user uploads the files in the browser: Hugging Face, New Space, Static, Blank, then Files, Upload files
(`index.html`, `classify.js`, `memos.txt`, `README.md`). Do not deploy for them and do not ask for a
Hugging Face token.
