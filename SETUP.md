# Setup Instructions

To make this application works, you need to configure two things in `TaskReminder.html`.

## 1. Google Gemini API Key (For AI Features)
1.  Go to [Google AI Studio](https://aistudio.google.com/).
2.  Create a new API Key.
3.  Open `TaskReminder.html`.
4.  Find `const apiKey = "PASTE_YOUR_GEMINI_API_KEY_HERE";` and paste your key.

## 2. Firebase Configuration (For Database & Login)
1.  Go to [Firebase Console](https://console.firebase.google.com/).
2.  Create a new project.
3.  Add a Web App (`</>`).
4.  Copy the `firebaseConfig` object (it looks like a JSON object with `apiKey`, `authDomain`, etc.).
5.  Open `TaskReminder.html`.
6.  Find `const __firebase_config = JSON.stringify({...})` and replace the content with your config.

## Running the App
Simply double-click `TaskReminder.html` and it will open in your default browser.

*Note: If you encounter issues (like CORS errors), consider using a browser extension like "Web Server for Chrome" or just ignore them if the basic features work.*


