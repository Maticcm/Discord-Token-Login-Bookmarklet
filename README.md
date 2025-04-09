# 🔐 Discord Token Login Bookmarklet (Educational Use Only)

 ## ⚠️ Disclaimer:
 This project is for **educational and personal testing purposes only**.  
 It is not intended for misuse, unauthorized access, or any activity that violates Discord's Terms of Service.  
 **Do NOT use this with any token other than your own.**  
 Public distribution or use of this script for malicious purposes is strictly prohibited.
 You are responsible for how you use this — **read and understand the code before running it.**

## 📌 What is this?

A simple bookmarklet that allows you to log into the web version of Discord using your account token.  
It prompts you for a token and injects it into local storage, then reloads the page to log in.

---

## 🧠 How it Works

The script:
1. Prompts for a Discord token.
2. Injects the token into `localStorage`.
3. Reloads the page to trigger login.

---

## 🚀 How to Use

1. Copy the bookmarklet code.
2. Create a new bookmark in your browser.
3. Paste the code into the URL field of the bookmark.
4. Go to [https://discord.com/login](https://discord.com/login).
5. Click the bookmark.
6. When prompted, enter/paste your Discord token.
7. The page will reload and log you in.

---

## 📎 Bookmarklet Code

Paste this as the URL of a bookmark in your browser:

```js
javascript:(function(){let t=prompt("Enter your Discord token:");if(!t)return;function login(token){setInterval(()=>{document.body.appendChild(document.createElement('iframe')).contentWindow.localStorage.token=`"${token}"`},50);setTimeout(()=>{location.reload()},2500)}login(t);})();
