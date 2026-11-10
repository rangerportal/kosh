KOSH MONEY BOOK v2 — cloud sync with Firebase + works offline

UPLOAD TO GITHUB
Replace the files in your repo with these (Add file -> Upload files -> Commit).
Then wait 1–2 minutes for GitHub Pages to rebuild.

ONE-TIME FIREBASE SETUP (console.firebase.google.com -> project kosh-9edf3)
1. Build -> Authentication -> Sign-in method -> enable "Email/Password".
2. Build -> Firestore Database -> Rules tab -> delete everything there,
   paste the contents of firestore.rules, click Publish.

HOW IT WORKS
- Sign up (needs internet): name, mobile, username, password.
- Sign in with username OR mobile number on any phone; your entries appear.
- Offline: after signing in once, the app opens and saves entries without internet.
  They sync automatically when you are back online ("Synced" badge at the top).
- Passwords are handled by Firebase Authentication (never stored in the database).
- Each user can only read their own entries (enforced by firestore.rules).
