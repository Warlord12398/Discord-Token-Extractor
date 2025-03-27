# Discord-Token-Extractor
This script helps you retrieve your Discord token from the browser console by accessing internal application data using Discord's webpack modules.

# How to Extract Your Discord Token Using Browser Console
To use the Discord Token Extractor, follow these steps:

1. Open Discord in your Browser:

Go to https://discord.com and log into your account.



2. Open Developer Tools:

Press Ctrl + Shift + I (Windows/Linux) or Cmd + Option + I (Mac) to open the browser's Developer Tools.



3. Navigate to the Console:

Select the Console tab.



4. Paste the Code:

Copy and paste the following code into the console:

window.webpackChunkdiscord_app.push([
  [Math.random()],
  {},
  req => {
    for (let m of Object.values(req.c)) {
      if (m?.exports?.default?.getToken) {
        console.log(m.exports.default.getToken());
      }
    }
  }
]);

# Warning 
This script is made for educational purposes only. I am not responsible for any misuse or malicious activities performed using this code. Use it responsibly and within legal boundaries.
